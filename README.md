# Reflex
# Reflex App API Documentation

## Introduction
Welcome to the API documentation for Reflex, your trusted emergency service app. Reflex provides a seamless experience for accessing emergency services quickly and efficiently. This API allows developers to integrate Reflex functionalities into their applications to ensure users' safety during emergencies.

## Base URL
`https://api.reflexapp.com`

## Authentication
Reflex supports two authentication methods:
- Google Sign-In: Users can sign up or log in using their Google account.
- Phone Number Authentication: Users can sign up or log in using their name and phone number.

## Endpoints
### Sign-Up/Onboarding
- `POST /api/signup/google`: Sign up with Google account.
- `POST /api/signup/phone`: Sign up with name and phone number.
- `POST /api/password/recovery`: Recover forgotten password or unlock account.

### Emergency Service Selection
- `GET /api/emergency/helplines`: Get quick helplines for emergencies.
- `GET /api/emergency/services`: Get available emergency services.
- `POST /api/user/services`: Add or remove emergency services from the user's homepage.

### Geolocation Services
- `GET /api/user/location`: Get the user's current location.
- `GET /api/emergency/outposts`: Get the nearest emergency service outposts.

### Direct Contact
- `POST /api/emergency/call`: Place an instant emergency call.
- `POST /api/emergency/provider-call`: Directly contact a chosen emergency service provider.

### Optional Customization
- `POST /api/user/emergency-contacts`: Add emergency contacts.
- `POST /api/user/preferences`: Set preferences for specific emergency contacts.

### Information Resources
- `GET /api/emergency/info`: Get offline access to relevant emergency information.
- `GET /api/emergency/contacts`: Get offline access to relevant emergency contacts.

## Request Parameters
- For sign-up endpoints: Name, email (for Google sign-up), phone number.
- For password recovery: Email or phone number.

## Response Format
Responses are returned in JSON format and include relevant information based on the endpoint called.

## Status Codes
- `200 OK`: Successful request.
- `201 Created`: Resource successfully created.
- `400 Bad Request`: Invalid request parameters.
- `401 Unauthorized`: Authentication failed.
- `404 Not Found`: Resource not found.
- `500 Internal Server Error`: Server encountered an unexpected condition.

## Sample Request (Sign-Up with Google)
```http
POST /api/signup/google HTTP/1.1
Host: api.reflexapp.com
Content-Type: application/json

{
  "google_token": "<user_google_token>"
}
```
## Sample Response (Sign-Up with Google)
{
  "user_id": "123456789",
  "name": "John",
  "email": "john@example.com"
}

Conclusion
Reflex API empowers developers to integrate essential emergency service functionalities into their applications, ensuring users like John have access to swift assistance during critical situations. For further assistance or inquiries, please contact our support team at support@reflexapp.com.
