
This project contains the source files to reproduce the results of experiments on the Simpop Local model.

Page project website : http://iscpif.github.io/simpoplocal-epb/

Licence
-------

This software is licenced under the GNU Affero GPLv3 software licence. 

Usage (simulation)
------------------

To compile and run this project you need sbt 0.12 (http://www.scala-sbt.org/).

Go to the fitness directory.

`cd fitness`

To execute a single run: 

`sbt run`

To build the OpenMOLE plugin:

`sbt osgi-bundle`

Get the plugin in your target directory, for instance:

`target/scala-2.11/exploration-profiles_2.11-1.0.0.jar`

We use OpenMoLE to describe and launch our experimentation.

> OpenMOLE (Open MOdeL Experiment) is a workflow engine designed to leverage the computing power of parallel execution environments for naturally parallel processes. A process is told naturally parallel if the same computation runs many times for a set of different inputs. OpenMOLE workflows are suitable for many types of naturally parallel processes such as model experiment, image processing, text analysis… It is distributed under the AGPLv3 free software license.

Description of OpenMoLE installation is described on www.openmole.org website.

You can find multiple other great tutorials and examples of other applications on same website.

To launch OpenMoLE in console mode and load the exploration jar : 

`openmole -c -p /path/to/exploration_2.11.jar`

Then you can use the workflow available in the openmole directory (it is compatible with OpenMOLE 1.0). This workflow is configured to run on the biomed VO of the grid EGI, however switching the execution environment in OpenMoLE is easy so you can use this workflow on you own multi-core machine, cluster or grid virtual organisation (you can find examples of workflows in the tutorial section on the openmole website).

