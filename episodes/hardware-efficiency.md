---
title: Hardware Efficiency
teaching: 20
exercises: 0
---

::::::::::::::::::::::::::::::::::::::: objectives

- Understand what is meant by "embodied carbon" in the context of HPC systems.
- Learn how embodied carbon efficiency can be bettered by extending the lifespan of HPC systems and improving performance of applications on HPC systems.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- What is embodied carbon on HPC systems?
- How can embodied carbon efficiency be improved on HPC systems?
- What can I do to improve the embodied carbon efficiency during my use of HPC systems?

::::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction

The hardware that makes up the HPC systems you are using is an important element to consider when looking to be a greener user of HPC. Indeed, for HPC systems located where carbon intensity of electricity generation is low, the hardware may be the dominant component of emissions associated with HPC system use.

You will see how embodied carbon is a hidden cost when it comes to hardware and the different measures you can take to reduce the impact that the creation, destruction, and running of this hardware involves. More specifically, extending hardware lifetime and improving the efficiency of your hardware use are the main ways of reducing this impact.

## Key concepts

### Embodied carbon

The manufacturing of the device you are using to participate in this workshop produced carbon and disposing of it at the end of its life may release more. Embodied (or embedded) carbon is the amount of carbon emissions due to the creation and disposal of a device.

When calculating the total carbon emissions for HPC services, both the carbon emissions associated with running the system as well as the embodied carbon of the system must be accounted for.

![Bar chart illustrating embodied carbon from various end-user devices](./fig/17_embodioed_carbon.png "Bar chart illustrating embodied carbon from various end-user devices")

Embodied carbon varies significantly between different hardware. For some devices, the carbon emitted during manufacturing is much higher than that emitted during usage, as illustrated by a [study](https://www.ifi.uzh.ch/dam/jcr:fa4e956e-7a53-4038-98a5-00e09e2f4303/Study_Digitalization_Climate_Protection_Summary_Oct2017.pdf) from University of Zurich. As a result, the embodied carbon cost can sometimes be much higher than the carbon cost of the electricity powering it.

By thinking in terms of embodied carbon, any device, even one not consuming electricity, is responsible for the release of carbon over its lifetime.

### Amortisation

A way to account for embodied carbon is to amortise the carbon over the expected lifespan of a device. For example, suppose it took 4000&nbsp;kgCO<sub>2</sub>e to build an HPC system, and we expect it to last four years. Amortisation means that we can say the HPC system emits 1000&nbsp;kgCO<sub>2</sub>e/year in embodied carbon alone.

![Diagram illustrating amortisation](./fig/18_amortization.png "Diagram illustrating amortisation")

Rather than years, we typically amortise the embodied emissions over the total amount of resource available on the HPC system over its lifetime. For example, if the resource use of an HPC system is measured in GPUh then we would amortise the embodied emissions over the total GPUh available on the service over its whole lifetime (to give an emissions rate in kgCO<sub>2</sub>e/GPUh).

## How to improve hardware efficiency

By taking into account the embodied carbon, it is clear that by the time we come to install an HPC system, it has already emitted a large amount of carbon. Computers also have a limited lifespan, which means they are eventually unable to handle modern workloads, or they suffer failures and need to be replaced. In these terms, hardware consumption is a proxy for carbon, and since our goal is to be carbon efficient, we must also be hardware efficient.

There are two main approaches to improving hardware carbon efficiency:

- **Extending the lifespan** of the hardware - which reduces the carbon emission rate per unit of resource due to amortisation.
- **Increasing the utilisation and performance** of the hardware - getting more useful work out of the hardware per unit of resource.

### Extending the lifespan of hardware

In the example we saw previously, if we can add just one more year to the lifespan of our HPC system, then the amortised carbon emissions rate drops from 1000&nbsp;kgCO<sub>2</sub>e/year to 800&nbsp;kgCO<sub>2</sub>e/year.

![Diagram illustrating amortisation](./fig/19_lifespan.png "Diagram illustrating amortisation")

HPC systems have historically had lifetimes of around 5-7 years at which point they are replaced by newer systems that provide improved performance and functionality and that are typically more energy efficient. However, extending the lifetime of HPC systems may lead to improved carbon efficiency through the amortisation of embodied carbon, and using older HPC systems for our research may actually lead to a more carbon efficient use of HPC. 

### Increasing utilisation and performance

As well as increasing the lifespan to improve the embodied carbon efficiency, we can also work to make sure we get the most out of the HPC hardware during its lifetime.

At a service/system level this often corresponds to maximising the usage of the service - it's better to have 100% utilisation than 20% utilisation because of the cost of embodied carbon (and also because of the fact that even idle components in HPC systems consume some electricity).

For individual users and groups, improving the carbon efficiency with respect to embodied carbon typically corresponds to increasing the performance of their use of the HPC system so they get more output per unit of time. Of course, increasing the performance of your use may lead to higher power draw and higher electricity use which increases the emissions from the use of electricity. This means that you need to know what the balance between embodied emissions and emissions from electricity use are for the HPC system you are using to make useful choices about improving your carbon efficiency. There are three potential scenarios to maximise carbon efficiency:

- **Embodied carbon dominates -** run as high performance as possible irrespective of electricity use
- **Embodied carbon and carbon from electricity use are evenly balanced -** you need to find a balance of performance and energy efficiency
- **Carbon from electricity use dominates -** run in as energy efficient a manner as possible

We will look at a specific example of this balance in a later episode of this workshop.

:::::::::::::::::::::::::::::::::::::::: callout

## Carbon efficiency can be complex - flexibility is key

Understanding the most carbon efficient way to make use of HPC systems (and the most carbon efficient way to operate them, including choosing their lifetime) can be complex as it depends on many factors. These can include the embodied carbon of the hardware, the lifetime of the system, the carbon intensity of the electricity supply and how that changes over the service lifetime, and the efficiency of the workload you are running on the type of hardware provided by the system. However, one key aspect of being able to use HPC in a carbon efficient way is for your workflow to have the flexibility to run on different system types efficiently.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: keypoints

- Embodied carbon of an HPC system is the amount of carbon pollution emitted during the creation and disposal of the HPC system.
- When calculating your total carbon pollution, you must consider both that which is emitted when running on the HPC system as well as the embodied carbon associated with its creation and disposal.
- Extending the lifetime of an HPC system has the effect of amortising the carbon emitted so that its embodied CO<sub>2</sub>e/year is reduced.
- Increasing utilisation and performance also improve the embodied carbon efficiency from HPC system use.

::::::::::::::::::::::::::::::::::::::::::::::::::


