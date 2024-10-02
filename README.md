# C-Line to OSCAM Converter

This project provides a simple web interface to convert C-Line codes to OSCAM server format. The interface allows users to input C-Line codes and configure various parameters, then generates the corresponding OSCAM server configuration.

## Features

- Input C-Line codes and convert them to OSCAM server format.
- Configure parameters such as protocol, inactivity timeout, group, CCC version, and more.
- Generated output is displayed in a text area.
- Save the generated configuration to a file.

## Getting Started

### Usage

1. Open the `index.html` file in your web browser.
2. Configure the parameters as needed.
3. Enter your C-Line codes in the input text area.
4. The generated OSCAM server configuration will appear in the output text area.
5. Click the "Save" button to download the configuration as a file.

### Example
This input:
```plaintext
C: a1.domain.xyz 12300 username password
C: a2.domain.xyz 12301 username password
```
Will generate this output:
```
# Generated at 2024-10-02 07:23:35
[reader]
label             = a1.domain.xyz
protocol          = cccam 
device            = a1.domain.xyz,12300
user              = username 
password          = password 
inactivitytimeout = 30
group             = 1
cccversion        = 2.0.11
ccckeepalive      = 1
disablecrccws     = 1
keepalive         = 1
connectoninit     = 1
reconnecttimeout  = 10

[reader]
label             = a2.domain.xyz
protocol          = cccam 
device            = a2.domain.xyz,12301
user              = username 
password          = password 
inactivitytimeout = 30
group             = 1
cccversion        = 2.0.11
ccckeepalive      = 1
disablecrccws     = 1
keepalive         = 1
connectoninit     = 1
reconnecttimeout  = 10
```

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

