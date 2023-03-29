# Example IPC 2023 Learning Tracks submission

This repository contains the code for _Progressive Generalized Planner_, 
a minor refactored version of the framework published
in _"Scaling-up generalized planning as heuristic search with landmarks"_ (SoCS 2022).
For 2023, it serves as a baseline and an example for how to create learner and planner
submissions.

## Install Apptainer

See also https://apptainer.org/docs/admin/main/installation.html#install-ubuntu-packages

    sudo apt update
    sudo apt install -y software-properties-common
    sudo add-apt-repository -y ppa:apptainer/ppa
    sudo apt update
    sudo apt install -y apptainer

## Build and run learning image

    apptainer build learn.img Apptainer.pgp.learn
    ./learn.img dck.prog domains/gripper/domain.pddl domains/gripper/p-2-0.pddl domains/gripper/p-3-0.pddl domains/gripper/p-4-0.pddl domains/gripper/p-5-0.pddl ...

## Build and run planning image

    apptainer build plan.img Apptainer.pgp.plan
    ./plan.img dck.prog domains/gripper/domain.pddl domains/gripper/p-10-0.pddl plan.10
