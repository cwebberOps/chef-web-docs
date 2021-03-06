.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The syntax for using the |resource machine_execute| resource in a recipe is as follows:

.. code-block:: ruby

   machine_execute 'name' do
     attribute 'value' # see properties section below
     ...
     action :action # see actions section below
   end

where 

* ``machine_execute`` tells the |chef client| to use the ``Chef::Provider::MachineExecute`` provider during the |chef client| run
* ``name`` is the name of the resource block; when the ``command`` property is not specified as part of a recipe, ``name`` is also the command to be run
* ``attribute`` is zero (or more) of the properties that are available for this resource
* ``:action`` identifies which steps the |chef client| will take to bring the node into the desired state
