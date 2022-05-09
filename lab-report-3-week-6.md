# Week 6 Lab Report

## Streamlining ssh Configuration

Below you can see my config file:
![Config file](config.png)

You can write to your config file from the terminal with the following command (replacing `text` with your information):
```
$ echo "text" > config
```

I am now able to login only using the alias I indicated (`ieng6`):
![No username login](no_username.png)

As well as that you can use other commands such as `scp` to tranfer a file without indicating the full server adress:

![No username scp](scp_ieng6.png)

## Setup Github Access from ieng6

I have first generated new public/private key pair on the server. Both of those files were saved in the `.ssh` directory on the server:

![Public/private key pair files](keys.png)

I have also uploaded the public key to github:

![Key added to github](github_key.png)

Here you can see me running the git commands from the server, pushing the changes to Github:

![Git commands](git_commands.png)

You can see the commit [here](https://github.com/matveyvilkin/new_repo/commit/ffa353fc30c05cd9867199e00b0cc46748703abb).

## Copy whole directories with `scp -r`

You can copy a whole directory to a remote server using `scr -r`:
![scp -r](scp_r.png)

Once I copied the directory with the code I run the tests for the code on the server:
![tests on ieng6](tests.png)

You can also run all these commands together combining them using `;` like below:
![Combined commands](combined_commands.png)