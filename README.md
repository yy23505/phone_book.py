Overview and Purpose
This phone book application provides a simple and efficient tool to manage a list of contacts. Users can add, delete, sort, and search for contacts using various criteria. The application illustrates basic data structure and Python algorithmic principles in a real-world setting, making it a useful tool for personal and professional use.

Target Audience
Users who need to manage contacts
Businesses
Anyone who wants to store and retrieve contact information easily

## Installation
Using Jupyter Notebook to write and run python scripts, will need to download the latest version of Anaconda from the Anaconda download page https://www.anaconda.com/download. Once downloaded, 'Jupyter Notebook' can be launched  by selecting the tab in the Home section in Anaconda Navigator.

# phone_book.py
When creating a new Phonebook object, it will have an empty dictionary called contacts that will store the phonebook's contacts.

# Phonebook class
class Phonebook:
    def __init__(self):
        self.contacts = {}
        
`class Phonebook`: This line defines the `phonebook` class.

`def __init__(self)`: This line defines a special method in Python called the constructor. The __init__ method is called when a new `Phonebook` object is created.

`self.contacts = {}`: This line initialises an empty dictionary called contacts within the Phonebook object, which will store phonebook contacts.

Creating a Phonebook
To create a new phonebook, instantiate the Phonebook class:
phonebook = Phonebook()

Adding a Contact
To add a new contact to the phonebook, use the add_contact method:
def add_contact(self, name, phone_number):
        self.contacts[name] = phone_number

Deleting a Contact
To delete a contact from the phonebook, use the delete_contact method:
    def delete_contact(self, name):
        if name in self.contacts:
            del self.contacts[name]
        else:
            print("Contact not found")

Sorting Contacts
To sort the contacts in the phonebook by name, use the sort_contacts method:def sort_contacts(self):
        sorted_contacts = sorted(self.contacts.items())
        return sorted_contacts

Searching for a Contact
To search for a contact by name, use the search_contact method:
def search_contact(self, name):
        if name in self.contacts:
            return self.contacts[name]
        else:
            return "Contact not found"

Displaying All Contacts
To display all contacts in the phonebook, use the display_contacts method:
def display_contacts(self):
        for name, phone_number in self.contacts.items():
            print(f"{name}: {phone_number}")
