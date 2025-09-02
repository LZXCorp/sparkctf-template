# SparkCTF 2.0 - Challenge Template

This is the Official SparkCTF 2.0 Challenge Template Repository. This repository defines the submission guidelines to the main SparkCTF 2.0 Challenges Repository. 

## Flag Format

The format of the flag prefix is `SPARK`.

> [!tip]
> **Flag Example:** `SPARK{1_aM_a_aw3s0m3_F1Ag}`

If the flag is unobtainable in the requireed format, you are required to state the flag format within the challenge description.

> [!tip]
> **Flag Format Description**
>
> **Flag Format:** \
> Type in the interchange name (first word only) and include a 'interchange' at the end, and replace spacings with '_'. \
> `SPARK{bedok_interchange}`

## `README.md`

Make use of the provided [`README.md`](./README.md) template for your challenge description. Remove any of the optional headings; Hints, Files, Services and Flags.

Mistakes made within the optional headers will be automatically corrected. These include services, provided files and flag format. \
If a mistake can't be corrected during parsing, the script will show an error and the issue that occured.

## `dist` and `soln`

The `dist` folder contains the files that the participants will be provided with as part of the challenge. Users will be able to download these files from the CTF website.

The `soln` folder consists of your `writeup.md` that specifies a step-by-step process of how your challenge is solved. You may also include other supporting images/PoC scripts that are used to solve your challenge.

## `service`

The `service` folder is where you define containers as part of your challenge. These services could include, but not limited to, websites, network binaries and SSH access to a server.

Any resources that your Dockerfile requires should all be defined within the `service` folder.

> [!warning]
> You **MUST** include the `EXPOSE` directive within your Dockerfile, specifying the internal container port to expose outwards for the participants to connect to.

> [!tip]
> You can define multiple services by separating them into their own distinct directory.
>
> ```
> service/
> ├─ fakeuser/
> │  └─ Dockerfile
> └─ webserv/
>    └─ Dockerfile
> ```

## Template File Tree
```
challenge-name/
├─ dist/        (optional)
│  └─ <files provided to participants>
├─ service/     (optional)
│  ├─ Dockerfile
│  └─ <artifact files for building Docker container>
├─ soln/
│  └─ writeup.md
└─ README.md
```

## Example File Tree
```tree
sparkconsole1/
├─ dist/
│  ├─ Dockerfile
│  └─ sc-redact.c
├─ service/
│  ├─ docker-compose.yaml
│  ├─ Dockerfile
│  ├─ flag.txt
│  └─ sparkconsole.c
├─ soln/
│  ├─ soln.py
│  └─ writeup.md
└─ README.md
```
