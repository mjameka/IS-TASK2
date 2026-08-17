#include <iostream>
#include <str
ing>
#include <cstdlib>
#include <ctime>

using namespace std;

// Function 1: Decimal to Binary
string decimalToBinary(int decimal)
{
    if (decimal == 0)
        return "0";

    string binary = "";

    while (decimal > 0)
    {
        binary = char('0' + (decimal % 2)) + binary;
        decimal = decimal / 2;
    }

    return binary;
}

// Function 2: Binary to Decimal
int binaryToDecimal(string binary)
{
    int decimal = 0;

    for (char digit : binary)
    {
        decimal = decimal * 2 + (digit - '0');
    }

    return decimal;
}

// Function 3: Decimal to Hexadecimal
string decimalToHexadecimal(int decimal)
{
    if (decimal == 0)
        return "0";

    string hexadecimal = "";
    string hexDigits = "0123456789ABCDEF";

    while (decimal > 0)
    {
        int remainder = decimal % 16;
        hexadecimal = hexDigits[remainder] + hexadecimal;
        decimal = decimal / 16;
    }

    return hexadecimal;
}

// Function 4: Hexadecimal to Decimal
int hexadecimalToDecimal(string hexadecimal)
{
    int decimal = 0;

    for (char digit : hexadecimal)
    {
        int value;

        if (digit >= '0' && digit <= '9')
        {
            value = digit - '0';
        }
        else if (digit >= 'A' && digit <= 'F')
        {
            value = digit - 'A' + 10;
        }
        else if (digit >= 'a' && digit <= 'f')
        {
            value = digit - 'a' + 10;
        }
        else
        {
            return -1;
        }

        decimal = decimal * 16 + value;
    }

    return decimal;
}

// Main menu
int main()
{
    int choice;

    srand(time(0));

    do
    {
        cout << "\n====================================\n";
        cout << "       NUMBER CONVERTER MENU\n";
        cout << "====================================\n";
        cout << "1. Convert Decimal to Binary\n";
        cout << "2. Convert Binary to Decimal\n";
        cout << "3. Convert Decimal to Hexadecimal\n";
        cout << "4. Convert Hexadecimal to Decimal\n";
        cout << "5. Demo - Random Number to Binary\n";
        cout << "6. Exit\n";
        cout << "====================================\n";
        cout << "Enter your choice: ";
        cin >> choice;

        switch (choice)
        {
            case 1:
            {
                int decimal;

                cout << "Enter a decimal number: ";
                cin >> decimal;

                if (decimal < 0)
                {
                    cout << "Please enter a positive number.\n";
                }
                else
                {
                    cout << "Binary: " << decimalToBinary(decimal) << endl;
                }

                break;
            }

            case 2:
            {
                string binary;

                cout << "Enter a binary number: ";
                cin >> binary;

                bool valid = true;

                for (char digit : binary)
                {
                    if (digit != '0' && digit != '1')
                    {
                        valid = false;
                        break;
                    }
                }

                if (valid)
                {
                    cout << "Decimal: " << binaryToDecimal(binary) << endl;
                }
                else
                {
                    cout << "Invalid binary number. Use only 0 and 1.\n";
                }

                break;
            }

            case 3:
            {
                int decimal;

                cout << "Enter a decimal number: ";
                cin >> decimal;

                if (decimal < 0)
                {
                    cout << "Please enter a positive number.\n";
                }
                else
                {
                    cout << "Hexadecimal: "
                         << decimalToHexadecimal(decimal) << endl;
                }

                break;
            }

            case 4:
            {
                string hexadecimal;

                cout << "Enter a hexadecimal number: ";
                cin >> hexadecimal;

                int result = hexadecimalToDecimal(hexadecimal);

                if (result == -1)
                {
                    cout << "Invalid hexadecimal number.\n";
                }
                else
                {
                    cout << "Decimal: " << result << endl;
                }

                break;
            }

            case 5:
            {
                int randomNumber = rand() % 100;

                cout << "Random decimal number: "
                     << randomNumber << endl;

                cout << "Binary equivalent: "
                     << decimalToBinary(randomNumber) << endl;

                break;
            }

            case 6:
                cout << "Thank you for using the Number Converter.\n";
                break;

            default:
                cout << "Invalid choice. Please select an option from 1 to 6.\n";
        }

    } while (choice != 6);

    return 0;
}
