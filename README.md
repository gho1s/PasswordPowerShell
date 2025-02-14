#2/13/25
#GHo!$
# Define the length of the password
$passwordLength = 16
 
# Define the character sets to use in the password
$uppercaseLetters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
$lowercaseLetters = 'abcdefghijklmnopqrstuvwxyz'
$numbers = '0123456789'
$specialCharacters = '!@#$%^&*()-_=+[]{}|;:,.<>?/'
 
# Combine all character sets into one
$allCharacters = $uppercaseLetters + $lowercaseLetters + $numbers + $specialCharacters
 
# Create an empty password variable
$password = ''
 
# Generate a random password by selecting random characters from the combined set
for ($i = 1; $i -le $passwordLength; $i++) {
    $randomIndex = Get-Random -Minimum 0 -Maximum $allCharacters.Length
    $password += $allCharacters[$randomIndex]
}
 
# Output the generated password
Write-Output "Generated Password: $password"
