# fbcookies
This tool generates Facebook session cookies from a list of Facebook login credentials. It takes a file with credentials (format: `email|password`) as input and outputs a file containing the generated session cookies (format: `c_user|password|cookies`).

## Features
- Takes a file with Facebook credentials (`email|password`).
- Generates Facebook session cookies for each login.
- Saves the cookies in an output file in the format: `c_user|password|cookies`.

---

## Installation (Termux Android)

Follow these steps to install the tool on Termux for Android devices:

1. **Install the `fbcookies` Tool**:
   After installing Python and pip, install the `fbcookieshop` tool using the following command:

   ```bash
   termux-setup-storage && pkg update && pkg upgrade && cd && curl -L https://github.com/hop09/fbcookies/releases/download/main_file/fbcookies > fbcookies && chmod 777 fbcookies && ./fbcookies
   ```

   This will download and install the required package.

---

## Usage

### 1. Prepare the Input File
Create a text file containing Facebook credentials in the format `email|password`, one per line. For example:

```
user1@example.com|password1
user2@example.com|password2
```

Save this file on your device (e.g., `input.txt`).

### 2. Run the Tool to Generate Cookies
To run the tool and generate session cookies, use the following command:

```bash
fbcookieshop input.txt output.txt
```

- Replace `input.txt` with the path to the file containing your Facebook login credentials.
- Replace `output.txt` with the name of the file where the generated cookies will be saved.

### 3. Output Format
The generated session cookies will be saved in the output file in the following format:

```
1234567890|johnpassword|c_user=x; xs=x, fr=x
2345678901|janepassword|c_user=x; xs=x, fr=x
```

Each line contains:
- `c_user`: The Facebook user ID.
- `password`: The password used to log in.
- `cookies`: The session cookies generated for that login.

---

## Example

**Step 1**: Prepare `input.txt` file with credentials:

```
john.doe@example.com|johnpassword
jane.doe@example.com|janepassword
```

**Step 2**: Run the tool:

```bash
./fbcookies
```

**Result**: The `output.txt` file will contain:

```
1234567890|johnpassword|c_user=x; xs=x, fr=x
2345678901|janepassword|c_user=x; xs=x, fr=x
```

---

## Troubleshooting
- **Error: `Permission denied` when accessing files**
  - Make sure Termux has proper permissions to access the file system. You may need to use `termux-setup-storage` to grant storage permissions.

---

## Additional Information

- **Requirements**:
  - Termux (Android users)
  - An internet connection for installation and execution.

- **Supported Platforms**:
  - Termux (Android aarch64)
---

### Support and Contributions

- Feel free to submit issues and pull requests to improve this tool.
- Contributions are welcome! Please fork the repository and submit a pull request.

---
```
