def is_valid_email(email):
    
    if not isinstance(email, str):
        return False

    // Check for the presence of exactly one '@' symbol
    if email.count('@') != 1:
        return False

    local_part, domain = email.split('@', 1)

    // Check local part and domain
    if not local_part or not domain:
        return False

    // Check for domain part having a dot and valid characters
    if '.' not in domain:
        return False

    domain_parts = domain.split('.')
    
    // Domain should have at least two parts: e.g., 'example.com'
    if len(domain_parts) < 2:
        return False

    // Local part and domain should not be empty
    if any(not part for part in domain_parts):
        return False

    // Check for valid characters in local part
    valid_chars_local = set("abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789._%+-")
    if any(char not in valid_chars_local for char in local_part):
        return False

    // Check for valid characters in domain part
    valid_chars_domain = set("abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789.-")
    if any(char not in valid_chars_domain for char in domain):
        return False

    // Check for no consecutive dots in local part and domain part
    if '..' in local_part or '..' in domain:
        return False

    return True

def main():
    
    // Prompt user for an email address
    email = input("Enter an email address to validate: ").strip()
    
    // Validate the email address
    is_valid = is_valid_email(email)
    
    // Print the result
    if is_valid:
        print("The email address is valid.")
    else:
        print("The email address is invalid.")

// Run the main function if the script is executed directly
if __name__ == "__main__":
    main()
