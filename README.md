# goit-node-cli

This project is a command-line application that allows users to manage a list of contacts. Users can perform various actions such as listing all contacts, adding a new contact, getting a contact by ID, and removing a contact. The application is built using `Node.js` and utilizes the `commander package` for command-line interface (CLI) interaction.

## Installation

To install the necessary dependencies, run the following command:

```bash
npm install
```

## Usage

The application supports the following commands:

- `node index.js -a list`: Lists all contacts.
- `node index.js -a get -i <contactId>`: Gets a contact by ID.
- `node index.js -a add -n <name> -e <email> -p <phone>`: Adds a new contact.
- `node index.js -a remove -i <contactId>`: Removes a contact by ID.

To execute a command, run node `index.js` followed by the desired action and any additional options.

## Examples:

### List all contacts:

```bash
node index.js -a list
┌─────────┬─────────────────────────┬─────────────────┬─────────────────────────────────────────────────┬──────────────────┐
│ (index) │           id            │      name       │                      email                      │      phone       │
├─────────┼─────────────────────────┼─────────────────┼─────────────────────────────────────────────────┼──────────────────┤
│    0    │ 'AeHIrLTr6JkxGE6SN-0Rw' │ 'Allen Raymond' │           'nulla.ante@vestibul.co.uk'           │ '(992) 914-3792' │
│    1    │ 'qdggE76Jtbfd9eWJHrssH' │  'Chaim Lewis'  │              'dui.in@egetlacus.ca'              │ '(294) 840-6685' │
│    2    │ 'drsAJ4SHPYqZeG-83QTVW' │ 'Kennedy Lane'  │         'mattis.Cras@nonenimMauris.net'         │ '(542) 451-7038' │
│    3    │ 'vza2RIzNGIwutCVCs4mCL' │  'Wylie Pope'   │               'est@utquamvel.net'               │ '(692) 802-2949' │
│    4    │ '05olLMgyVQdWRwgKfg5J6' │ 'Cyrus Jackson' │            'nibh@semsempererat.com'             │ '(501) 472-5218' │
│    5    │ '1DEXoP8AuCGYc1YgoQ6hw' │ 'Abbot Franks'  │            'scelerisque@magnis.org'             │ '(186) 568-3720' │
│    6    │ 'Z5sbDlS7pCzNsnAHLtDJd' │ 'Reuben Henry'  │           'pharetra.ut@dictum.co.uk'            │ '(715) 598-5792' │
│    7    │ 'C9sjBfCo4UJCWjzBnOtxl' │ 'Simon Morton'  │           'dui.Fusce.diam@Donec.com'            │ '(233) 738-2360' │
│    8    │ 'e6ywwRe4jcqxXfCZOj_1e' │ 'Thomas Lucas'  │                 'nec@Nulla.com'                 │ '(704) 398-7993' │
│    9    │ 'rsKkOQUi80UsgVPCcLZZW' │  'Alec Howard'  │ 'Donec.elementum@scelerisquescelerisquedui.net' │ '(748) 206-2688' │
└─────────┴─────────────────────────┴─────────────────┴─────────────────────────────────────────────────┴──────────────────┘
```

### Get a contact by ID:

```bash
node index.js -a get -i 05olLMgyVQdWRwgKfg5J6
{
  id: '05olLMgyVQdWRwgKfg5J6',
  name: 'Cyrus Jackson',
  email: 'nibh@semsempererat.com',
  phone: '(501) 472-5218'
}
```

### Add a new contact:

```bash
node index.js -a add -n Mango -e mango@gmail.com -p 322-22-22
{
  id: 'hNE9JTUkoBqmBS0qWB20A',
  name: 'Mango',
  email: 'mango@gmail.com',
  phone: '322-22-22'
}
```

### Remove a contact by ID:

```bash
node index.js -a remove -i qdggE76Jtbfd9eWJHrssH
{
  id: 'qdggE76Jtbfd9eWJHrssH',
  name: 'Chaim Lewis',
  email: 'dui.in@egetlacus.ca',
  phone: '(294) 840-6685'
}
```

## File Structure

- `index.js`: Main entry point of the application.
- `contacts.js`: Module containing functions to perform operations on contacts.
- `db/`: Directory containing `contacts.json` to store contacts.

## Requirements

- Node.js
- npm

## Dependencies

- `commander`: For creating command-line interfaces.
- `nanoid`: For generating unique IDs.
