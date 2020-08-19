---
layout: default
title: Getting Started
parent: Tutorials
nav_order: 4
---


# Getting Started

---


### Declaring Variables

    set price to 50000
    
### Filter
    
    set imgs to images where containing car 
    set imgs to images where containing car and house_price of images > price
    
    
### Loop and condition

    foreach img in imgs:
        if house_price of img > price:
            print location, house_price of img
            
### Use packages

    use package math
    
    print math.mean( house_price of imgs )
    
    
### Detect objects

    set persons to imgs.detect(person) 
    set smiles to imgs.detect(smile) 
    
### Visualizations

    draw a histogram with properties { 
        x_axis = stats of persons
    }
    
    draw a scatter plot with properties { 
        x_axis = stats of persons, 
        y_axis = stats of smiles
    }
    
    
### Relationship

    print smiles.linear( persons )
    
    # output:
    # smiles = 0.7 * persons
    
    
### Train a model to detect new object

    # todo 