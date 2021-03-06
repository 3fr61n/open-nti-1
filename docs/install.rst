How to install or upgrade
=========================

Requirements
------------

.. _docker: http://docs.docker.com/engine/installation/ubuntulinux/
.. _docker-compose: https://docs.docker.com/compose/install/
.. _Mac: https://docs.docker.com/engine/installation/mac/
.. _Windows: https://docs.docker.com/engine/installation/windows/
.. _DockerCloud: https://hub.docker.com/r/juniper/open-nti/

The requirements is to have docker and docker-compose installed on your Linux server/machine.
Instructions to install are available below
 - docker_
 - docker-compose_

It's also available for:
 - Mac_
 - Windows_

How to Install/Start
--------------------

OpenNTI is available on DockerCloud_ and this project provide scripts to easily download/start/stop it.

.. code-block:: text

  git clone https://github.com/Juniper/open-nti.git
  cd open-nti
  make start

.. NOTE::
  On Ubuntu, you'll have to add "sudo" before the last command

By default it will start 3 containers and it's working in **non-persistent mode**, once you stop it all data are gone.
It's possible to start the main container in **persistent mode** to save the database outside the container, b
y using the startup script ``make start-persistent``.
`Persistent mode on Mac OS requires at least v1.12`

How to update
-------------

It's recommended to upgrade the project periodically, both the files from github.com and the containers from Docker Hub.
You can update easily with

.. code-block:: text

  make update
