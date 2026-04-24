# Validation of ECN in ns-3 

This repository contains the files to validate the implementation of ECN in ns-3.

## Steps to generate ns-3 plot
* Clone the ns-3-dev repository: `https://gitlab.com/nsnam/ns-3-dev`
* Installation steps are described here: `https://www.nsnam.org/wiki/Installation#Ubuntu.2FDebian.2FMint`
* Copy `tcp-ecn-example-with-aqm.cc` or `tcp-ecn-example-without-aqm.cc` from the `ns-3 scripts` directory provided in this repository and paste it in `ns-3-dev/scratch`
* Copy `Plot Scripts` directory from the `ns-3 scripts` directory provided in this repository and paste it in the ns-3 root directory (i.e., in parallel to `src` or `scratch`)
* Run `tcp-ecn-example-with-aqm.cc` using the following command:
```shell
./ns3 build
./ns3 run scratch/tcp-ecn-example-with-aqm
```
* Run `tcp-ecn-example-without-aqm.cc` using the following command:
```shell
./ns3 build
./ns3 run scratch/tcp-ecn-example-without-aqm
```
* The results will be stored in a new directory called `ecn-results`
* Plot the graphs using the `.dat` files and `gnuplot`

* The results will be stored in the same directory where you run the `gnuplot` command.

## Acknowledgments
This work was a joint effort by the following students at National Institute of Technology Karnataka, Surathkal, India:
* ns-3 scripts were developed by Aarti Nandagiri and Vivek Jain
* NeST scripts were developed by Sushma Meena and Aditya Chaudhary
