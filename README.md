# test-3gpp-hampi

- <https://github.com/ystero-dev/hampi>

## Install tools

```sh
cargo install asn1-compiler
# download the docx

git clone https://github.com/Its-Just-Nans/3gpp_asn1
cp *.docx 3gpp_asn1
```

## Extract types

```sh
python 3gpp_asn1/decode_as1n.py
```

## Generate rust code from types

```sh

hampi-rs-asn1c  --codec  uper --derive serialize --derive deserialize --module toto.rs -- output.asn1
```
