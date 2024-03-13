import random
import string

def generate_code(length=10):
    characters = string.ascii_uppercase + string.ascii_lowercase + string.digits
    code = ''.join(random.choice(characters) for _ in range(length))
    return code

def generate_spotify_codes(num_codes):
    codes = [generate_code() for _ in range(num_codes)]
    return codes

# Generate Spotify codes
num_codes = 5
spotify_codes = generate_spotify_codes(num_codes)
print("Generated Spotify Codes:")
for code in spotify_codes:
    print(code)
