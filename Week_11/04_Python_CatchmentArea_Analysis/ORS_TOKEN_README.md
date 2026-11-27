# Note: For this exercise you will need a token from OpenRouteService.

## Link to [OpenRouteService](https://openrouteservice.org)

### Why do you need a OpenRouteService token?
This token is a key that allows you to request the OpenRouteService server.

### Steps to Obtain a Token:
1. Create an account on [OpenRouteService](https://openrouteservice.org).
2. Log in and go to **Dashboard** -> **Dev Dashboard** -> **Tokens**.
3. Create a token.
4. Use one of these options in the notebook:
   - Save the token in `ors_token.txt` in this folder.
   - Set the `ORS_TOKEN` or `ORS_API_KEY` environment variable before starting Jupyter.
   - If neither is configured, enter the token at the notebook's hidden prompt.

The hidden prompt does not display the token or write it to a file. OpenRouteService still requires a valid token; the prompt only avoids the missing-file error.