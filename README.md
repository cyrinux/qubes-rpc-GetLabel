# Qubes RPC GetLabel
A Qubes RPC service to inform an AppVM what label it has for theming purposes. The label is written as an English color to the /etc/qubes/label file, which can be changed in the qubes-get-label file with the OUTPUT variable

# WARNING
This RPC passes information to dom0 from an AppVM! This RPC has NOT been rigorously tested and anyone with extremely high security needs should be wary of installing it in its current state.

## Suggested Installation Directories
qubes-get-label -> (AppVM) /usr/local/bin/qubes-get-label

qubes-send-label -> (dom0) /usr/local/bin/qubes-send-label

qubes.GetLabel -> (dom0) /etc/qubes-rpc/qubes.GetLabel

policy/qubes.GetLabel -> (dom0) /etc/qunes-rpc/policy/qubes.GetLabel

## Running
To run this RPC, issue the following command in your desired AppVM:

/usr/lib/qubes/qrexec-client-vm dom0 qubes.GetLabel /usr/local/bin/qubes-get-label