
The so called *conventional approach* is a well established and widely used metric to estimate the energy consumption. It follows an average allocation methodology, more specifically network electricity is allocated using an average energy per data volume metric $kWh/GB$.

The conventional approach uses average [Transmission Network Energy](energy/Transmission%20Network%20Energy.md) intensity for estimation of the energy consumption.
For the estimation, it relies on an allocation approach that maps energy consumption of shared networks of services within the network.

In [Streaming](streaming/Streaming.md), the transmission network energy consumption is allocated based on the transmitted data volume for one hour of streaming.
The energy consumption of data centres and user devices is allocated based on the viewing duration.

The energy that is consumed by the network is shared among the various users and services. To divide the network energy consumption among the services and users, an allocation approach is employed.
For this, the transmission network energy consumption is calculated based on the data volume transmitted through the network by a streaming service.

### Intended Use Case

The intended use cases for the conventional approach are to create foot-prints for video streaming service providers and to generate a network/system level carbon footprint estimation.

### Strengths

One of the major strengths of the conventional approach is that it is well understood and widely used in the industry.
It accounts fro all energy consumption across the network and is a straightforward approach for accounting and allocation.

### Limitations

The conventional approach is only representative for a particular network and period of time.
This approach is sensitive to network characteristics such as network equipment efficiency, quantity of network users and the data traffic.
Another limitation is that it is not suitable for estimating the marginal carbon impact if a change in level of service is happening, e.g. change in video quality. This is due to the reliance on average transmission intensities, and is therefore not capable of reflecting on the dynamics of network transmission equipment when network load changes.