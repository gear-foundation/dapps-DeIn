# DeIn

## Connect your dapp to the Decentrilized Internet

To connect your program to the Decentrilized Internet on Gear it's necessary to have variable of type `Option<DnsMeta>` that will contain metadata of DNS record.

```rust
pub struct DnsMeta {
    pub name: String,
    pub link: String,
    pub description: String,
}
```

One more thing that you need to do is to include the following enum variants

1. in handle_input type

- `GetDnsMeta` - it has to be the first variant of the enum
- `SetDnsMeta(DnsMeta)` - it is needed to setup the dns record

2. in handle_output type

- `DnsMeta(Option<DnsMeta>)` - it also has to be the first variant of the enum

After your program will be uploaded on chain you need to build your frontend to a single html file and upload it to IPFS.

1. Download and install IPFS Desktop - https://github.com/ipfs/ipfs-desktop
2. Upload your built web app using 'Files' tab
3. Get file link by pressing option dots button on file and choose 'Share link'

The next step is to send Metadata to your program using `SetDnsMeta` enum variant. Where you need to set name, link (that is link to html file on IPFS) and description.

To register your dapp in Dns you need to send message to Dns program. You can do it through idea.gear-tech.io find dns program and send message `Register` with the id of your program.

Here is the id of dns program: `0xdd6ebf2548f5f26317f9139e519cdefd7f95479b07dfdd26dab73b9a3c9f3396`

## Open and use dapp

Firstly you need to download dns.html file from releases and open in your browser.
If you have register your dapp in dns program you will see it in the list of available dapps. Just click open and your interface will be opened in the new tab.
