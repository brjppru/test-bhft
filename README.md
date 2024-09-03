
# hi

Q: Roman Bogdanov design quile можно прочитать как принято? или тут масс-набор бассейн, на сколько владение ansible совпадет с компанией?

A: Daria [2024-08-26 15:37] "можно ли заранее прочитать, как принято" –такого нет. скорее проверяем уровень владения инструментом

it's ok. then I will use the most vanilla ansible possible without external modules.

Goal: Write an Ansible role and playbook to prepare the server for operation
Task: Prepare the OS using Ansible

A: I have a virtual machine with ubuntu given as a test bench. in this case I will ignore the uefi/bios boot and test choices, since it actually has grub2 installed, let it figure it out.

>     Rename the active network interface to "net0". Display information about the renamed interface during the playbook.

ubuntu + netplan, ok see

see network_configuration.yml

>    -Disabling C-state for all available CPUs.
>    -Switching CPU operation from power-saving mode to more productive mode.

I have a virtual machine with ubuntu given as a test bench. 

In general, choosing goneover, or switching to C0 processor mode will lead to interesting results on a virtual machine. i still don't understand why we need to change C0 or switch goneover (the choice of which, by the way, is very limited). 

I am not smarter than engineers from intel and amd, as well as people who wrote the hypervisor, the impact on the cpu processing pipeline of linux commands is definitely worth measuring in this case. but I wrote a test in asible file.

see cpu_configuration.yml

>    -Implement the procedure of encrypting the second disk in the system (where there is no root partition) (partition name should be specified in the inventory).
>    -Implement a procedure to encrypt the partition that is present on the disk next to the root partition.

upd2:

Рома, привет, Нужно переделать с использованием luks

ok

see encrypt_disks_rroot.yml
see encrypt_disks.yml

> the rest of the script logic is set in main.yaml

see main.yml

final login to 

IP: 54.93.95.126
user: ubuntu

all stuff in /home/ubuntu/brj

p.s. I'd like to know the answer to the question that Daria couldn't answer - is it exactly a network engineer job?

wbr R.

