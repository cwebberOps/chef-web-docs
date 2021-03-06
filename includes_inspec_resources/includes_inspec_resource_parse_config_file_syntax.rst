.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

A ``parse_config_file`` InSpec audit resource block declares the location of the configuration file to be tested, and then which settings in that file are to be tested.

.. code-block:: ruby

   describe parse_config_file('/path/to/file', { data_config_option: value } ) do
     its('setting') { should eq 1 }
   end

or:

.. code-block:: ruby

   options = {
     assignment_re: /^\s*([^:]*?)\s*:\s*(.*?)\s*$/,
     multiple_values: true
   }

   describe parse_config_file('path/to/file', options) do
     its('setting') { should eq 1 }
   end

where each test

* Must declare the location of the configuration file to be tested
* Must declare one (or more) settings to be tested
* May run a command to ``stdout``, and then run the test against that output
* May use options to define how configuration data is to be parsed
