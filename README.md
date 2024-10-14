# Phonebook

# General Description

The Phone Book application is a simple Java Swing-based Graphical User Interface (GUI) that allows users to manage a list of contacts. The program enables users to add, delete, search, display, and sort contacts by name. It validates input data to ensure phone numbers consist only of digits and are 10 digits long. The application also prevents duplicate entries for contacts with the same name.

The main class is Phonebook GUI, which extends JFrame and serves as the primary GUI for interacting with the phone book.

## IDE Used: Eclipse



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

## Contributor: Jollene Joemba

## 3. Display contacts

Description:  Displays the list of all contacts in the phone book. If no contacts are available, it shows a message stating that there are no contacts.

## Contributor: Erastus Mukuve

## 4. Delete contacts

Description: Prompts the user to enter the name of a contact to delete. If a contact with the specified name is found, it is deleted. Otherwise, an error message is shown.

## Contributor: Stephan Ndabeni

## 5.Update contacts

Description: The primary purpose of the update Contact function is to find a contact by name in the phonebook and update their phone number with a new one provided by the user.

## Contributor: Heron Hamutenya

## 6.Sort contacts

Description: Sorts the contacts alphabetically by name (case-insensitive). If no contacts are available, a message is displayed.

## Contributor: Sophia Shinedima

# Pseudocode 

    FUNCTION addContact(name, phoneNumber):
        CREATE new Contact with name and phoneNumber
        ADD new Contact to contacts list

    FUNCTION displayContacts():
        IF contacts list is empty THEN
            PRINT "No contacts found."
        ELSE
            FOR each contact in contacts DO
                PRINT "Name: " + contact.name + ", Phone Number: " + contact.phoneNumber
            END FOR
        END IF

    FUNCTION binarySearch(name):
        SET start to 0
        SET end to size of contacts - 1
        WHILE start is less than or equal to end DO
            SET middle to start + (end - start) / 2
            SET contact to contacts[middle]
            SET comparison to contact.name compared to name
            IF comparison is less than 0 THEN
                SET start to middle + 1
            ELSE IF comparison is greater than 0 THEN
                SET end to middle - 1
            ELSE
                RETURN middle  // Found the contact
            END IF
        END WHILE
        RETURN -1  // Contact not found

    FUNCTION searchContact(name):
        CALL sortContacts()  // Ensure contacts are sorted
        SET index to result of binarySearch(name)
        IF index is not -1 THEN
            SET contact to contacts[index]
            PRINT "Found: Name: " + contact.name + ", Phone Number: " + contact.phoneNumber
        ELSE
            PRINT "Contact not found."
        END IF

    FUNCTION deleteContact(name):
        REMOVE contacts from the list where contact.name equals name

    FUNCTION updateContact(oldName, newName, newPhoneNumber):
        FOR each contact in contacts DO
            IF contact.name equals oldName THEN
                SET contact.name to newName
                SET contact.phoneNumber to newPhoneNumber
                BREAK the loop
            END IF
        END FOR

    FUNCTION sortContacts():
        SORT contacts list by contact.name

END CLASS

FUNCTION main():
    CREATE PhoneBook instance named phoneBook
    WHILE true DO
        PRINT menu options:
            "1. Add Contact"
            "2. Display Contacts"
            "3. Delete Contact"
            "4. Update Contact"
            "5. Sort Contacts"
            "6. Search Contact"
            "7. Exit"
        GET user choice

        IF ( choice ==1)
            PROMPT for name and phone number
            CALL phoneBook.addContact(name, phoneNumber)
        ELSE IF ( choice ==2)  THEN
            CALL phoneBook.displayContacts()
        ELSE IF ( choice ==3) THEN
            PROMPT for name of contact to delete
            CALL phoneBook.deleteContact(name)
        ELSE IF ( choice ==4) THEN
            PROMPT for current name, new name, and new phone number
            CALL phoneBook.updateContact(oldName, newName, newPhoneNumber)
        ELSE IF( choice ==5) THEN
            CALL phoneBook.sortContacts()
            PRINT "Contacts sorted."
        ELSE IF (choice ==6)  THEN
            PROMPT for name to search
            CALL phoneBook.searchContact(name)
        ELSE IF (choice ==7) THEN
            BREAK the loop
        END IF
    END WHILE

    CLOSE scanner
END FUNCTION


# Flowchart

![WhatsApp Image 2024-10-13 at 22 16 39_ee1f05a9](https://github.com/user-attachments/assets/e0e66e2a-e17c-4153-9984-bf3e4a79d647)


### Group Members

- 223077666 Ndabeni S.N.N
- 224047655 Tjihambuma A.K
- 224079921 Mukuve E.A
- 223040622 Jeomba J.V.V
- 224084909 Hamutenya H.H.F
- 224027832 Shinedima S.U.P
























