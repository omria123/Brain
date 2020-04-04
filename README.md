![build status](https://travis-ci.org/BrainProjectTau/Brain.svg?branch=master)
![coverage](https://codecov.io/gh/BrainProjectTau/Brain/master/graph/badge.svg)
## Installation

1. Clone the repository and enter it:

    ```sh
    $ git clone git@github.com:BrainProjectTau/Brain.git
    ...
    $ cd Brain/
    ```

2. Run the installation script and activate the virtual environment:

    ```sh
    $ ./scripts/install.sh
    ...
    $ source .env/bin/activate
    [Brain] $ # you're good to go!
    ```

3. To check that everything is working as expected, run the tests:


    ```sh
    $ pytest tests/
    ...
    ```

## Usage

The `Brain` packages provides the following classes:
    
- `Area`

    This class represents an Area in the brain.

    ```pycon
    >>> from Brain import Area
    >>> area = Area(beta = 0.1, n = 10 ** 7, k = 10 ** 4)
    ```

- `Assembly`
    
    This class represents an Assembly in the brain.
    
- `Connectome`
    
    Represent the graph of connections between areas and stimuli of the brain.
    
    ```pycon
    >>> from Brain import Connectome, Area
    >>> connectome = Connectome()
    >>> area = Area(beta = 0.1, n = 10 ** 7, k = 10 ** 4)
    >>> connectome.add_area(area)
    ```

- `Brain`

    This class represents a simulated brain, with it's connectome which holds the areas, stimuli, and all the synapse weights.

    ```pycon
    >>> from Brain import Brain, Connectome, Area
    >>> connectome = Connectome()
    >>> area = Area(beta = 0.1, n = 10 ** 7, k = 10 ** 4)
    >>> connectome.add_area(area)
    >>> brain = Brain(connectome)
    ```
