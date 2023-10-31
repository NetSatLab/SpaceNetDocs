==============
FAQ
==============



#. How many people have access to the lab machine?

    * Currently, the lab machine is operated by two research groups:

        #. Space Domain Awareness (SDA)
        #. Space Mega-Constellation Network (SpaceNet)

    * When using the lab machine, please acknowledge that another research group requires the **lab machine to be left on at all times.**


#. Where are the main SpaceNet simulator files?

    * To configure the simulation set-up, the file is `starlink_config.yml` under:
      `constellation-simulator-main/controller/starlink_config.yml`
    
    * To run a simulation, the file is `main_mn.py` under: 
      `constellation-simulator-main/controller/main_mn.py`

    * To generate pre-configured routing tables, the file is `satnet_topology_updates.py` under:
      `constellation-simulator-main/utils/satnet_topology_updates.py`

    * To obtain the most recent TLE sets from the Starlink constellation (these are pulled from http://www.celestrak.org/), the file is `get_tles.sh` under:
      `constellation-simulator-main/utils/get_tles.sh`
 
    * To define the ground-to-satellite routing (association) criteria, the file is `mobility_utils.py` under:
      `constellation-simulator-main/mobility/mobility_utils.py`


#. How do I run a simulation?

    * In order to run a successful simulation, you must have already executed a successful run from `satnet_topology_updates.py` as its output files are necessary
      input to `main_mn.py`. If not, please run `satnet_topology_updates.py` first by using the command:

      `sudo python3 satnet_topology_updates.py`

      Please wait for the process to finish. Depending on the simulation settings in `starlink_config.yml`, it may take a few minutes to several hours.

      Once that is complete, you may execute the main simulation using the command below. Please be sure to run the simulation script in its directory to avoid code dependency errors.

      `sudo python3 main_mn.py`
