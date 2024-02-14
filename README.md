# test-3gpp-hampi

- <https://github.com/ystero-dev/hampi>

## 1.Install tools

```sh
cargo install asn1-compiler
# download the docx

git clone https://github.com/Its-Just-Nans/3gpp_asn1
cp *.docx 3gpp_asn1
```

## 2.Extract asn1

```sh
python 3gpp_asn1/decode_as1n.py
```

## 3.Generate rust types from asn1

```sh

hampi-rs-asn1c  --codec  uper --derive serialize --derive deserialize --module code.rs -- output.asn1
```

## 4. Test to load

The rust file uses the types in code.rs

```sh
cargo run
```
