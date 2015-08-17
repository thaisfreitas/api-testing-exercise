# Setting up Vagrant

If you don't have vagrant yet, you can start downloading it from [here](http://www.vagrantup.com/downloads).

Download Vagrant 1.6.5 box by running the command:

`vagrant init hashicorp/precise32`

On your project directory, you should be able to run `vagrant up` successfully.
If so, you are ready to start working on your vagrant machine.

Start running `vagrant ssh`.

Once it's done, you can run: 

`cd /vagrant/` & `npm install`

And finally you should be able to start your app by running:

`node .`

Check if your app is running on `http://localhost:4567`

# The Application

The project is generated by [LoopBack](http://loopback.io).

Loopback creates the basic structure of your API by simply running the command `slc loopback`.
After that, you already have the config files and directory structure.

Here’s a brief description of what each part of the structure means:

### Client: 

That is where the files for your API consumer should be located. In our case, it’s not going to be used right now.

### Server: 

This folder contains all the files needed to setup your API - since its authentication, host configuration, until which datasource you’re going to use (database memory, mongodb etc)

By running the command: `slc loopback:model`, Loopback creates your API models. 

It corresponds to the `common/models` directory we have in our repo. Under this folder, you have the config files of each one of your models. 

In our case, our model is called Flight. If you look into the model folder, you will find a `.js` and a `.json` file. If you want to implement Javascript calls for your API model, you should place its code on the `.js` file.
In case you’d like to set how the model is implemented, you can change the properties located on the `.json` file.

