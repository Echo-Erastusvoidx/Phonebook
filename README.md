# Phonebook

# General Description

The Phone Book application is a simple Java Swing-based Graphical User Interface (GUI) that allows users to manage a list of contacts. The program enables users to add, delete, search, display, and sort contacts by name. It validates input data to ensure phone numbers consist only of digits and are 10 digits long. The application also prevents duplicate entries for contacts with the same name.

The main class is Phonebook GUI, which extends JFrame and serves as the primary GUI for interacting with the phone book.

# Modules

### import java.util.ArrayList;

•	Description: This module imports the array List class from the java.util package. array List is a resizable array implementation of the List interface. It allows you to dynamically add, remove, and access elements.

### import java.util.Collections;

•	Description: This module imports the Collections class from the java.util package. Collections provides static methods for sorting, searching, and modifying collections.

### import java.util.Comparator;

•	Description: This module imports the Comparator interface from the java.util package. Comparator is used to define custom ordering for objects. It allows you to create custom sorting logic.

### import java.util.Scanner;

•	Description: This module imports the Scanner class from the java.util package. Scanner is used to read input from various sources, such as user input from the console.

# Contact Class

Description: Represents a single contact in the phone book, consisting of a name and a phone number.

## Attributes:

String name: The name of the contact.
String phone Number: The contact's phone number.

## Constructor:

Contact(String name, String phone Number): Initializes a contact with the provided name and phone number.

# Phonebook GUI Class

Description: This is the main class that creates the GUI for the phone book. It extends JFrame and handles user interactions such as adding, displaying, deleting, sorting, and searching contacts.

## Attributes:

Array List<Contact> contacts: Stores the list of contacts.
JText Area display Area: Displays the list of contacts or search results.
JText Field name Field, phone Field: Text fields for inputting the contact's name and phone number.

## Constructor:

Phonebook GUI(): Sets up the graphical interface, including buttons and text fields for user interaction.

# Functions

## 1.Insertion
Description: Adds a new contact to the phone book. It validates the contact's name and phone number, checks for duplicates, and displays a message indicating whether the contact was successfully added or if errors occurred.
## Contributor: Alishia Tjihambuma

## 2. Search contacts
Description: Prompts the user to enter a name to search for. If the contact is found, it is displayed. If not, an appropriate message is shown.

## Search Code
<img src="![WhatsApp Image 2024-10-13 at 19 54 59_65f3d19e](https://github.com/user-attachments/assets/dd7ab77b-f398-40f5-a15b-3e747292567c)">






