.. _playapp:

#####################
Play(Scala)
#####################



Megam is an open-standards, cloud-based platform for building, managing and running apps of all types (web, mobile, big data). Capabilities include apps, mobile, application monitoring, as well as capabilities from ecosystem partners and open source, all through an as-a-service model in the cloud.

If you haven't registered already, you'll need to do so at the megam home page. Just click **Sign up** for free to get set up.

Now, read further to get a clear walk through on ``how to deploy a play application`` with a single click on Megam PaaS.

Start by signing into Megam which takes you to the main dashboard. User logging in for the first time, belongs to a default organization. Read about :ref:`organization <orgs>`


Starter Packs
==============

Megam Browser based UI is designed to provide minimal-yet-effective navigation for user's ease and reduces unnecessary complexities. Read about :ref:`Browser based UI <nilavu_overview>`.

Once ``Create App`` is clicked from the :ref:`Browser base UI <nilavu_overview>`, the page loads to ``MarketPlace``.

The marketplace contains all the applications, addons and services neatly segregated.

|starter packs|

Clicking ``Create App`` lets you choose different kinds of Runtimes (like Java or Ruby..), Services (such as PostgreSQL or Riak) and Starer packs which are essentially pre-configured application templates that are great ways to get started.

Select the ``play icon``, which opens a panel that displays more information about what it does:

**Play Web Starter Pack**

When an app is launched in Megam the following steps are performed automatically for you by an operation invoker.  The steps are hidden and abstracted from the user.

- Install play
- Install Riak
- Uses the built-in application template for ``scala`` and configure in the cloud.
- Deploys and starts the play application.

|megam basiccombo playapp|

Lets look at the popup *Deploy Dialog Box* in detail.

Deploy Dialog box
------------------

|playweb starter|

Easy 5 step deployment of a play Application:

1. Click ``play``, this opens up a dialog with "Play + Riak" logo.

2. Pick your application name. A random name is filled by default.

3. Pick a cloud where you want to launch.  If you don't have a setting, then Read about :ref:`Cloud settings <cloud_settings>`
   Megam supports all major IaaS providers. Before launching in a particular IaaS provider, there are certain setup needed as described in the :ref:`Cloud settings <cloud_settings>`.

4. This launch has a built-in configuration.

5. Click **Create App** with all pride.

Voila! your application is running like a charm!

The source code used for this launch is

.. code::

  git clone https://githib/com/megamsys/megam_gateway.git

The App Overview page show the application performance, and ability to bind services.

Now that you have launched a pre-configured Play app, you'll be raring to launch your own.

Deploying Your Play App
========================

Now you have a Play app, which you want to deploy in Megam. Sure, first lets test it locally.


Running Locally
----------------


Basic Prerequisites
^^^^^^^^^^^^^^^^^^^

To get started with Play, you will need to prepare a few things:

sbt:
    SBT is a scala build tool.

.. code::

     $sudo apt-get install scala
     $sudo apt-get install sbt

play:

    Play Framework needs to be installed.
    Download the latest play binary package and extract the archive. For convenience, you should add the framework installation directory
    to your system PATH. If you’re on UNIX, make sure that the play script is runnable (otherwise simply do a chmod +x play). That’s all.

    Download Link : ``https://www.playframework.com/download``


An editor for Scala:
    IntelliJ and Eclipse are the most popular choices and work on all platforms, though there are others.

Git:
    This is a version-control system that we will use to download and manage our play projects.

.. code::

    $sudo apt-get update
    $sudo apt-get install git

A terminal:
    on OSX you have Terminal.app already installed, in Linux you have Terminal, and on Windows you have PowerShell.

Your favorite web browser:
    Chrome and Firefox are the most popular.


Now, clone the sample github project and test it locally.

.. code::

      $ git clone https://github.com/megamsys/megam_gateway.git
      $ cd megam_gateway
      $ sbt
      $ run


Verify and test your app running on localhost:9000


Deploying in Megam
-----------------------

Now we know the application is in a working state, let us deploy it in Megam. Megam will launch the application with same steps as explained in ``Deploy Dialog box`` except that you have to click "BYOC in Marketplace"

BYOC(Bring Your Own Code):
   Megam supports plethora of SCMs, select one. Enter the ``URL of your source code``

Voila! your application is running like a charm!

The ``App Overview page`` show the application performance, and ability to bind services.

Now that you have launched your app, you might want to launch a service (database) and bind it to the app. Read about :ref:`Binding a service <deployaservice>`







.. |playweb starter| image:: /images/playwebstarter_launch.png



.. |starter packs| image:: /images/starter_packs.png

.. |megam basiccombo playapp| image:: /images/megam_basiccombo_play.png
