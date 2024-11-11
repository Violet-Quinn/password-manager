# Password Manager

This is a **Password Manager** built using Python’s `tkinter` library. The app allows you to securely manage your passwords, generate strong passwords, and store them in a local JSON file. It offers a user-friendly interface to save, search, and manage passwords for various websites and services.

### Features

- **Password Generation**: Automatically generates a random, strong password using letters, numbers, and symbols.
- **Password Storage**: Saves passwords securely in a local JSON file, along with associated website and email information.
- **Search Functionality**: Search for saved passwords by entering the website name and retrieve the associated email and password.
- **Clipboard Copying**: The generated password is automatically copied to your clipboard for easy use.
- **Field Validation**: Ensures no fields (website, email, password) are left empty before saving the data.

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/password-manager.git
   cd password-manager
   ```

2. **Install Dependencies**:

   - The project uses `tkinter`, `Pillow`, and `pyperclip`.
   - `tkinter` comes pre-installed with Python, so no additional installation is needed.
   - Install `Pillow` and `pyperclip` by running:
     ```bash
     pip install pillow pyperclip
     ```

3. **Download the Logo Image**:
   - Place your desired logo image in the same directory as the code. The image will be displayed as the app's logo.

### Usage

Run the application by executing:

```bash
python password_manager.py
```

### How to Use the Password Manager

1. **Generate a Password**:
   - Click the "Generate Password" button to create a random password.
   - The password will be copied to your clipboard automatically for easy pasting.

2. **Save a Password**:
   - Enter the website, email/username, and password in the appropriate fields.
   - Click "Add" to save the password. If any fields are empty, an alert will prompt you to fill in the missing information.

3. **Search for a Password**:
   - Enter the website name and click "Search" to retrieve the saved password for that website.

4. **Reset Fields**:
   - After saving or searching, the input fields will be cleared automatically to allow you to add a new entry.

### File Storage

Passwords are stored in a file named `saved_pass.json` in the following format:

```json
{
    "example.com": {
        "email": "user@example.com",
        "password": "generatedPassword123"
    }
}
```

### Code Overview

- **Constants**: Defines character sets (letters, numbers, symbols) used for generating passwords.
- **Functions**:
  - `generate_password()`: Generates a random password, copies it to the clipboard, and inserts it into the password field.
  - `save_password()`: Validates the fields, saves the password details in `saved_pass.json`, and clears the input fields.
  - `find_password()`: Searches for a password in the `saved_pass.json` file by website name.
  
### UI Setup

- The application uses `tkinter` to create a simple GUI with labels, entry fields, buttons, and a logo image.
  
### Contributing

Feel free to contribute by opening issues, creating pull requests, or forking the repository. Improvements are always welcome!
