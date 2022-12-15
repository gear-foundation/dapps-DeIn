# DNS

Dns program enable to register your program and its interface as DNS record.
The program stores program ids and meta info of theirs interfaces (name, description and link).

## Register

To register your dapp you have to send message to DNS program with the following payload:

```json
{
  "Register": "you program id"
}
```

Or you can use `idea.gear-tech.io` to do it.

## Get dns records

You can read state of the Dns program to get all records or filtered ones (by name, id, pattern).
