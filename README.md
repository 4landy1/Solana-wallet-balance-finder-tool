# Solana Wallet Balance Finder Tool: Locate Your Solana Funds

Need a tool to find the balance of your Solana wallet? **SolanaChecker** is your comprehensive solution, providing several functionalities to help you manage and examine your Solana wallets. It's designed to simplify interactions with the Solana blockchain, and offers robust balance checking capabilities, among other features.

<p align="left">
    <img src="/images/entity.webp" />
</p>

## Key Program Features

1.  **Solana Balance Checker:** Check the current Solana balance on a specified address. Quickly and easily track your funds.

<p align="left">
    <img src="/images/copy.webp" />
</p>

2.  **Token Security Analysis:** Evaluate the security of tokens.

<p align="left">
    <img src="/images/light.webp" />
</p>

3.  **Address Tracking:** Get real-time notifications about activity on specified addresses through a Telegram bot.

4.  **Wallet Data from Mnemonic:** Extract private key, address, and balance from your mnemonic.

<p align="left">
    <img src="/images/utility.webp" />
</p>

5.  **Solana Wallet Generator:** Create new Solana wallets.

<p align="left">
    <img src="/images/piece.webp" />
</p>

6.  **Brute-Force Balance Finder:** Generate seed phrases and check for existing balances. Finds active wallets (for research), with Telegram notification support.

<p align="left">
    <img src="/images/middle.webp" />
</p>

## Telegram Notification Setup

To receive notifications in Telegram, provide your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) in the 'telegram-settings.txt' file.

## Getting Started

Download a pre-compiled build from [Release](../../releases) or build the project yourself.

## Building the Project: Instructions

This project is written in C++ and depends on several libraries. We recommend using **vcpkg** for an easy installation:

### Installing Dependencies with vcpkg:

1.  If you do not already have **vcpkg**, clone the repository and install it by following the instructions on the [official page](https://github.com/microsoft/vcpkg).
2.  Add **vcpkg** to your system PATH environment variable.
3.  Run the following commands to install the dependencies:

    -   Install **OpenSSL**:

    ```bash
    vcpkg install openssl
    ```

    -   Install **nlohmann-json**:

    ```bash
    vcpkg install nlohmann-json
    ```

    -   Install **Crypto++**:

    ```bash
    vcpkg install cryptopp
    ```

    -   Install **libsodium**:

    ```bash
    vcpkg install libsodium
    ```

4.  Build the project after installing the dependencies.

### Building with Visual Studio:

1.  Open the project solution in Visual Studio.
2.  Ensure **vcpkg** is correctly integrated with your environment (see [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio)).
3.  Click **Build** -> **Build Solution**.
4.  The executable will be located in the `bin` folder.

### Building with Another C++ Compiler:

1.  Ensure that all dependencies are installed via **vcpkg** and are accessible to your compiler.
2.  Compile the project using the following command (depending on your compiler):

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line Usage

1.  **-s / -search**: Start a brute-force search for wallets with a balance.
2.  **-t / -track (ADDRESS)**: Track a specific address. The program will monitor activity on the specified address.
3.  **-g / -gen (NUMBER)**: Generate the specified number of Solana wallets. Use `<NUMBER>` to specify the quantity.
4.  **-m / -mnemonic (MNEMONIC)**: View wallet details. Replace `<MNEMONIC>` with your seed phrase.
5.  **-b / -balance (ADDRESS)**: View the balance of a specified address in the Solana network.

## Important Notes

-   This program is intended for research, not illegal activities.
-   Crypto investments have risks. Be sure to secure your data and wallets.

## License

This project is licensed under the [MIT License](/LICENSE). You are free to use, modify, and distribute the code according to the license.