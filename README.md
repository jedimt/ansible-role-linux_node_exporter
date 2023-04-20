Ansible Role: Linux Node Exporter
=========

Install the Prometheus Linux node exporter.

Requirements
------------

None.

Role Variables
--------------

    # Download location for the prometheus node_exporter tarball file
    linux_node_exporter_tarball: 'https://github.com/prometheus/node_exporter/releases/download/v1.5.0/node_exporter-1.5.0.linux-amd64.tar.gz'


Dependencies
------------

None.

Example Playbook
----------------

    # ===========================================================================
    # Linux Prometheus exporter
    # ===========================================================================

    - name: Install and configure Linux prometheus exporter
      hosts: mongo

      vars_files:
        # Ansible vault with all required passwords
        - "../../credentials.yml"

      roles:
        - { role: jedimt.linux_node_exporter,
            # Download location for the prometheus node_exporter tarball file
            linux_node_exporter_tarball: 'https://github.com/prometheus/node_exporter/releases/download/v1.5.0/node_exporter-1.5.0.linux-amd64.tar.gz'
        }

License
-------

MIT

Author Information
------------------

Aaron Patten
aaronpatten@gmail.com
