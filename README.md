# nagios-plugin-systemd-service

Nagios plugin to check the status of a systemd service.

## Authors

Mohamed El Morabity <melmorabity -(at)- fedoraproject.org>

## Usage

    check_systemd_service.sh <service name>

## Examples

    $ ./check_systemd_service.sh sshd
    OK: service sshd is running

    $ sudo systemctl stop sshd
    $ ./check_systemd_service.sh sshd
    ERROR: service sshd is not running

    $ ./check_systemd_service.sh foo
    ERROR: service foo doesn't exist
