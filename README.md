# My-first-project
has_lower = False
has_upper = False
has_digit = False
has_symbol = False

for c in password:
    if c.islower():
        has_lower = True
    elif c.isupper():
        has_upper = True
    elif c.isdigit():
        has_digit = True
    elif c in string.punctuation:
        has_symbol = True

if has_lower:
    strength += 1
if has_upper:
    strength += 1
if has_digit:
    strength += 1
if has_symbol:
    strength += 1
if len(password) >= 12:
    strength += 1

if strength <= 2:
    return "Weak"
elif strength <= 4:
    return "Medium"
else:
    return "Strong"
