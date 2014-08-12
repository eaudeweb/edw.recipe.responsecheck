Example of usage
================
A simple buildout.cfg::

  [buildout]
  parts = checker

  [checker]
  recipe = edw.recipe.responsecheck
  start-port = 8000
  end-port = 9000
  step = 2
  backends = backend1 ... backend2
  path = ${buildout:directory}/bin

Recipe options
--------------
Explanation::

  start-port = Port to start the check.
  end-port   = Port to end the check.
  step       = The numeric value that the count is increased by each loop.
  backends   = List of backend names separated by space character.
  path       = Path to a folder where the bash script will be saved.

Note: All options must be specified.

