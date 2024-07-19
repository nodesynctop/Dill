# Dill

![dillxyz](https://github.com/user-attachments/assets/0c34bde0-8717-40e4-a970-3847e762092a)

Twitter: https://x.com/dill_xyz_

Discord: https://discord.com/invite/dill

Explorer: https://andes.dill.xyz/

Guide Docs: https://past-chokeberry-e85.notion.site/andes-doc-a23a9f71a85a4be9a6737e54d2674060

## 1. Server preparation
```
sudo apt update && apt upgrade -y
sudo apt install wget curl make clang net-tools pkg-config libssl-dev build-essential jq lz4 gcc unzip snapd -y
```
## 2. Install Node

### 2.1 Download & Extract the package
```
cd $HOME && curl -O https://dill-release.s3.ap-southeast-1.amazonaws.com/linux/dill.tar.gz && \
tar -xzvf dill.tar.gz && cd dill
```
### 2.2 Generate Validator Keys
```
./dill_validators_gen new-mnemonic --num_validators=1 --chain=andes --folder=./
```

`sample output`

```
ubuntu@ip-xxxx:~/dill$ ./dill_validators_gen new-mnemonic --num_validators=1 --chain=andes --folder=./

***Using the tool on an offline and secure device is highly recommended to keep your mnemonic safe.***

Please choose your language ['1. العربية', '2. ελληνικά', '3. English', '4. Français', '5. Bahasa melayu', '6. Italiano', '7. 日本語', '8. 한국어', '9. Português do Brasil', '10. român', '11. Türkçe', '12. 简体中文']:  [English]: 3
Please choose the language of the mnemonic word list ['1. 简体中文', '2. 繁體中文', '3. čeština', '4. English', '5. Italiano', '6. 한국어', '7. Português', '8. Español']:  [english]: 4
Create a password that secures your validator keystore(s). You will need to re-enter this to decrypt them when you setup your Dill validators.:
Repeat your keystore password for confirmation:
The amount of DILL token to be deposited(2500 by default). [2500]:
This is your mnemonic (seed phrase). Write it down and store it safely. It is the ONLY way to retrieve your deposit.


Creating your keys.
Creating your keystores:	  [####################################]  1/1
Verifying your keystores:	  [####################################]  1/1
Verifying your deposits:	  [####################################]  1/1

Success!
Your keys can be found at: ./validator_keys


Press any key.
ubuntu@ip-xxxx:~/dill$
```
This will generate the validator keys and save them in  ./validator_keys directory 

```
ls -ltr ./validator_keys
```

