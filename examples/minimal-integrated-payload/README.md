# SUIT minimal example with integrated payload

This example mirrors the `minimal` example, but uses SUITs integrated payload
functionality with Dress-Up's `integrated-payload` feature.

## Usage

Run the example with:

```console
cargo run -- suit.cbor public.pem
```

## Details

The application requires the suit manifest and the public key supplied as files
via the application arguments.

### Keypair

The public key must be a PEM-encoded plain ecdsa public key.
A keypair can be generated with openssl:

```console
openssl ecparam -name secp256k1 -genkey -noout -out private.pem
openssl ec -in private.pem -pubout -out public.pem
```

## Generating the SUIT Manifest

The [suit-tool] from ARM can be used to generate the keys and suit manifest.


[suit-tool]: https://gitlab.arm.com/research/ietf-suit/suit-tool
