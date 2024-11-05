
INDEX

1.	If a total of 33 MHz of bandwidth is allocated to a particular FDD cellular telephone system which uses two 25 kHz simplex channels to provide full duplex voice and control channels, compute the number of channels available per cell if a system uses (a) 4-cell reuse, (b) 7-cell reuse (c) 12-cell reuse. If 1 MHz of the allocated spectrum is dedicated to control channels, determine an equitable distribution of control channels and voice channels in each cell for each of the three systems.

2.	If a signal to interference ratio of 15 dB is required for satisfactory forward channel performance of a cellular system, what is the frequency reuse factor and cluster size that should be used for maximum capacity if the path loss exponent is (a) n= 4 , (b) n = 3? Assume that there are 6 co-channels cells in the first tier and all of them are at the same distance from the mobile. Use suitable approximations.


3.	How many users can be supported for 0.5% blocking probability for the following number of trunked channels in a blocked calls cleared system? (a) 1, (b) 5, (c) 10, (d) 20, (e) 100. Assume each user generates 0.1 Erlangs of traffic.

4.	An urban area has a population of 2 million residents. Three competing trunked mobile networks (systems A, B, and C) provide cellular service in this area. System A has 394 cells with 19 channels each, system B has 98 cells with 57 channels each, and system C has 49 cells, each with 100 channels. Find the number of users that can be supported at 2% blocking if each user averages 2 calls per hour at an average call duration of 3 minutes. Assuming that all three trunked systems are operated at maximum capacity, compute the percentage market penetration of each cellular provider.


5.	A certain city has an area of 1,300 square miles and is covered by a cellular system using a 7-cell reuse pattern. Each cell has a radius of 4 miles and the city is allocated 40 MHz of spectrum with a full duplex channel bandwidth of 60 kHz. Assume a GOS of 2% for an Erlang B system is specified. If the offered traffic per user is 0.03 Erlangs, compute (a) the number of cells in the service area, (b) the number of channels per cell, (c) traffic intensity of each cell, (d) the maximum carried traffic; (e) the total number of users that can be served for 2% GOS, (f') the number of mobiles per channel, and (g) the theoretical maximum number of users that could be served at one time by the system.

6.	If a transmitter produces 50 watts of power, express the transmit power in units of (a) dBm, and (b) dBW. If 50 watts is applied to a unity gain antenna with a 900 MHz carrier frequency, find the received power in dBm at a free space distance of 100 m from the antenna, what is P (10 km)? Assume unity gain for the receiver antenna.


7.	Determine the path loss of a 900MHz cellular system in a large city from a base station with the height of 100m and mobile station installed in a vehicle with antenna height of 2m. The distance between mobile and base station is 4Km.

8.	 Determine the path loss between base station (BS) and mobile station (MS) of a 1.8GHz PCS system operating in a high-rise urban area. The MS is located in a perpendicular street to the location of the BS. The distances of the BS and MS to the corner of the street are 20 and 30 meters, respectively. The base station height is 20m.


9.	 A mobile is located 5 km away from a base station and uses a vertical λ /4 monopole antenna with a gain of 2.55 dB to receive cellular 3 radio signals. The E-field at 1 km from the transmitter is measured to be V/rn. The carrier frequency used for this system is 900 MHz. (a) Find the length and the gain of the receiving antenna. (b) Find the received power at the mobile using the 2-ray ground reflection model assuming the height of the transmitting antenna is 50 m and the receiving antenna is 1.5m above ground.

10.	A hexagonal cell within a 4-cell system has a radius of 1.387 km. A total of 60 channels are used within the entire system. If the load per user is 0.029 Erlangs, and λ= call/hour, compute the following for an Erlang C system that has a 5% probability of a delayed call: (a) How many users per square kilometer will this system support? (b) What is the probability that a delayed call will have to wait for more than 10s? (c) What is the probability that a call will be delayed for more than 10seconds? 
Problem-1: If a total of 33 MHz of bandwidth is allocated to a particular FDD cellular telephone system which uses two 25 kHz simplex channels to provide full duplex voice and control channels, compute the number of channels available per cell if a system uses (a) 4-cell reuse, (b) 7-cell reuse (c) 12-cell reuse. If 1 MHz of the allocated spectrum is dedicated to control channels, determine an equitable distribution of control channels and voice channels in each cell for each of the three systems.

Solution:
Have given,
Total bandwidth	= 33 MHz,
= 33,000 kHz
Channel bandwidth	= 25 kHz x 2 simplex channels
= 50 kHz / duplex channel
Total available channels	= Total Bandwidth / Channel Bandwidth
= 33,000 / 50
= 660 channels
If 1 MHz of the allocated spectrum is dedicated to control channels,
i.e. Control channel bandwidth	= 1000 kHz
The number of available control channel	= Control channel bandwidth / Channel bandwidth
= 1000 / 50
= 20 channels
(a)
Have given,
Cluster size, N = 4

Total number of channels available per cell  = Total available channels / N
= 660/4
≈165 channels.
∴ Equitable distribution of,
Voice Channel	= (Total available channels - The number of available control channel) / N
= (660 – 20) / 4
≈ 160 channels
Control Channel = Total number of channels available per cell – Voice Channel
= 165 – 160
= 5 channels

      (b)
Have given,
Cluster size, N = 7

Total number of channels available per cell = Total available channels / N
= 660/7
≈94 channels.
∴ Equitable distribution of,
Voice Channel	= (Total available channels - The number of available control channel) / N
= (660 – 20) / 7
≈ 91 channels
Control Channel = Total number of channels available per cell – Voice Channel
= 94 – 91
= 3 channels

       (c)
Have given,
Cluster size, N = 12

Total number of channels available per cell = Total available channels / N
= 660/12
≈ 55 channels.
∴ Equitable distribution of,
Voice Channel	= (Total available channels - The number of available control channel) / N
= (660 – 20) / 12
≈ 53 channels
Control Channel = Total number of channels available per cell – Voice Channel
= 55 – 53
= 2 channels

Source Code (Python):

import numpy as np

# Clear all variables and close all figures (not needed in Python)

# User input for cluster sizes
cluster_sizes = list(map(int, input("Enter Cluster Sizes with [ ] around Them (e.g., 4 7 12): ").split()))

bw = 33000  # Total Bandwidth in kHz
sim_ch_bw = 25  # Simplex channel bandwidth in kHz
dup_ch_bw = 2 * sim_ch_bw  # Duplex channel bandwidth in kHz
t_ch = bw / dup_ch_bw  # Total available channels
cc_bw = 1000  # Control channel bandwidth
t_cc = cc_bw / dup_ch_bw  # Number of available control channels

# Loop over each cluster size
for N in cluster_sizes:
    # Calculate the desired results for each system use
    ch_per_cell = round(t_ch / N)  # Channels available per cell
    vc = round((t_ch - t_cc) / N)  # Voice channels
    cc = ch_per_cell - vc  # Control channels

    # Print the results
    print(f"For Cluster size N = {N}")
    print("-------------------------")
    print(f"Total number of channels available per cell: {ch_per_cell} channels")
    print(f"Voice Channels: {vc} channels")
    print(f"Control Channels: {cc} channels")
    print("\n")







Input:
Enter Cluster Sizes with [ ] around them: [4 7 12].

Output:
For Cluster size N = 4
Total number of channels available per cell : 165 channels Voice Cannel	: 160 channels
Control Cannel	: 5 channels

For Cluster size N = 7
Total number of channels available per cell : 94 channels Voice Cannel	: 91 channels
Control Cannel	: 3 channels

For Cluster size N = 12
Total number of channels available per cell : 55 channels Voice Cannel	: 53 channels
Control Cannel	: 2 channels

 
Problem-2: If a signal to interference ratio of 15 dB is required for satisfactory forward channel performance of a cellular system, what is the frequency reuse factor and cluster size that should be used for maximum capacity if the path loss exponent is (a) n= 4 , (b) n = 3? Assume that there are 6 co-channels cells in the first tier and all of them are at the same distance from the mobile. Use suitable approximations. 

Solution:
Have given,
Minimum Required Signal-to-Noise interference ratio, S/I = 15 dB, The number of Co-channel interfering cells, io	= 6
We Know,
Number of cell reuse, N = i2 + i*j + j2	(i)
First, let us consider a 7-cell reuse pattern, N = 7	For i=1, j=2 Also,
 



Where,
 
The Frequency Reuse Factor, Q = D/R
= √(3𝑁)	(ii)
= 4.583.

D = Distance between centers of the nearest Co-channel cells. R = Radius of the cell.
 

(a)
Have given,
Path Loss exponent, n	= 4
Frequency Reuse Factor, Q = 4.583.
We know,
Signal-to-Noise interference ratio, S/R = 10 log (Qn / i0 )
= 10 log ((4.583)4 / 6)
= 18.66 dB.
Since this is greater than the minimum required S/I (18.66 > 15), N = 7 can be used.

(b)
Have given,
Path Loss exponent, n = 3
We know,
Signal-to-Noise interference ratio, S/R   = 10 log(Qn / i0 )	(iii)
= 10 log ((4.583)3 / 6)
= 12.05 dB.
 
Since this is less than the minimum required S/I (12.05 < 15), we need to use a larger N.
Using equation (i), the next possible value of N = 12;	For i = j = 2. The corresponding co-channel ratio is given by equation (ii) as Frequency Reuse Factor, Q = 6.
Using equation (iii) the signal-to-interference ratio, S/I = 15.56 dB.
Since, this is greater than the minimum required S/I (15.56 > 15), N = 12 can be used.

Source Code (Python):

import numpy as np

# User input for path loss exponent
pl_exponent = list(map(int, input("Enter Path Loss exponent with [ ] around Them (e.g., 4 3): ").split()))

r_si = 15  # Minimum Required S/I in dB
i0 = 6     # The number of Co-channel interfering cells

for n in pl_exponent:
    N = 7  # Cluster size

    # Calculate the results
    Q = np.sqrt(3 * N)  # Frequency reuse factor
    si = 10 * np.log10((Q**n) / i0)  # Signal to interference ratio in dB

    # If the first condition is not satisfied
    if si < r_si:
        i = 2
        j = 2
        N = (i * i) + (i * j) + (j * j)
        Q = np.sqrt(3 * N)
        si = 10 * np.log10((Q**n) / i0)

    # Print the results
    print(f"For Path Loss Exponent, n = {n}")
    print("---------------------------")
    print(f"Signal-to-Noise interference Ratio S/I: {si:.3f} dB > {r_si} dB")
    print(f"Hence, Cluster size N: {N}")
    print(f"Frequency Reuse Factor Q: {Q:.3f}\n\n")

Input:
Enter Path Loss exponent with [ ] around them: [4 3].

Output:
For Path Loss Exponent, n = 4
Signal-to-Noise interference Ratio, S/ I: 18.663 dB > 15 dB Hence, Cluster size, N	7
Frequency Reuse Factor, Q	:	4.583
For Path Loss Exponent, n = 3
Signal-to-Noise interference Ratio, S/I : 15.563 dB > 15 dB Hence, Cluster size, N	12
Frequency Reuse Factor, Q	:	6.000
 
Problem-3: How many users can be supported for 0.5% blocking probability for the following number of trunked channels in a blocked calls cleared system? (a) 1, (b) 5, (c) 10, (d) 20, (e) 100. Assume each user generates 0.1 Erlangs of traffic.

Solution:
Have given,
Blocking Probability, PB  = 0.5%, Traffic Intensity, Au =0.1 Erlangs
We Know,
For Erlangs B, Grade of Service, GOS = PB = 0.005
And, Total number of user, U = A / Au	(i)
 
Where, Also,
   

A = Offered Traffic Intensity.

Table 3.1: Capacity of an Erlang B System.
 

 
From Table 3.1, we can find the total capacity in Erlangs for the 0.5% GOS for different numbers of channels.

(a)
Have given,
Trunked channels, C = 1  From table 3.1, 
For C = 1 we obtain, A = 0005
From equation (i), we have-
Total number of user, U = A / Au
= 0.05 users.
But, actually one user could be supported on one channel. So, U = 1.
 
(b)
Have given,
Trunked channels, C = 5
From table 3.1, For C = 5  we obtain, A = 1.13 Erlang.
From equation (i), we have-
Total number of user, U = A / Au
≈ 11 users.
(c)
Have given,
Trunked channels, C = 10
From table 3.1, For C = 10 we obtain, A = 3.96 Erlang From equation (i), we have-
Total number of user, U = A / Au
≈ 39 users.
(d)
Have given,
Trunked channels, C = 20
From table 3.1, For C = 20 we obtain, A = 11.10 Erlang From equation (i), we have-
Total number of user, U = A / Au
≈ 110 users.
(e)
Have given,
Trunked channels, C = 100
From table 3.1, For C = 100 we obtain, A = 80.9 Erlang.
From equation (i), we have-
Total number of user, U = A / Au
≈ 809 users.



Source Code (Python):

import numpy as np

# Given parameters
GOS = 0.5 / 100  # Blocking probability (0.5%)
Au = 0.1         # Traffic intensity per user (in Erlangs)

# From Erlang B chart - Offered Traffic Intensity, A
A = np.array([0.005, 1.13, 3.96, 11.1, 80.9])  # Offered traffic intensities for different channels

# Trunked Channels
C = np.array([1, 5, 10, 20, 100])  # Number of trunked channels

# Total number of users calculation
U = np.round(A / Au).astype(int)  # Total number of users (rounded to nearest integer)

# Print the results
print(f"Grade of Service, GOS = {GOS:.3f}")
print("Trunked Channels, C:")
print(C)
print("From table 3.1, we obtain Offered Traffic Intensity, A for all Channels, C:")
print(A)
print("Total number of users, U:")
print("---------------------------")
print(U)


Input:
Trunked Channels, C = [1 5 10 20 100];

Output:
Grade of Service, GOS =	0.005	
Trunked Channels,		C:	1	5	10	20	100
Offered Traffic Intensity,		A:	0.0050	1.1300	3.9600	11.1000	80.9000
Total number of user,		U:	0	11	40	111	809


 
Problem-4: An urban area has a population of 2 million residents. Three competing trunked mobile networks (systems A, B, and C) provide cellular service in this area. System A has 394 cells with 19 channels each, system B has 98 cells with 57 channels each, and system C has 49 cells, each with 100 channels. Find the number of users that can be supported at 2% blocking if each user averages 2 calls per hour at an average call duration of 3 minutes. Assuming that all three trunked systems are operated at maximum capacity, compute the percentage market penetration of each cellular provider.

Solution:
Have given,
Blocking Probability, PB	= 2%, The average number of call requests per unit time 𝜆	= 2.
The average duration of a call, H	= 3/60 seconds There are 2 million residents in the given urban area = 2000000
We Know,
For Erlangs B, Grade of Service, GOS = PB = 0.02
And, Traffic Intensity,    Au = 𝜆H = 0.1 Erlangs

 

Where, Also,
 
Also, Total number of user, U = A / Au	(i)

A = Offered Traffic Intensity.

Table 4.1: Capacity of an Erlang B System.
 

 
 
From Table 4.1, we can find the total capacity in Erlangs for the 2% GOS for different numbers of channels.
For System-A
Have given,
Number of channels per cell used in the system,	C = 19
From table 4.1, For C = 19 and GOS = 0.02 we obtain, A = 12 Erlangs From equation (i), we have-
Total number of user, U = A / Au
= 120 users.
Since there are 394 cells, the total number of' subscribers that can be supported by System A
is equal to 120 x 394 = 47280.
Since, the percentage market penetration = 47280/2000000 = 2.36%

For System-B
Have given,
Number of channels per cell used in the system,	C = 57
From table 4.1, For C = 57 and GOS = 0.02 we obtain, A = 45 Erlangs From equation (i), we have-
Total number of user, U = A / Au
= 450 users.
Since there are 98 cells, the total number of' subscribers that can be supported by System B
is equal to 450 x 98 = 44,100.
Since, the percentage market penetration = 44100/2000000 = 2.205%

For System-C
Have given,
Number of channels per cell used in the system,	C = 100
From table 4.1, For C = 100 and GOS = 0.02 we obtain, A = 88 Erlangs From equation (i), we have-
Total number of user, U = A / Au
= 880 users.
Since there are 49 cells, the total number of' subscribers that can be supported by System C
is equal to 880 x 49 = 43,120.
Since, the percentage market penetration = 43,120/2000000 = 2.156%
Therefore, total number of cellular subscribers that can be supported by these three systems are (47280 + 44100 + 43120) = 134500 users.
The market penetration of the three systems combined is equal to 134500/2000000 = 6.725

Source Code (Python):

# Constants
blocking_probability = 2 / 100  # GOS
population = 2000000
Au = (2 / 60) * 3  # Traffic intensity per user

print('For system A:')
print('--------------')
C1 = 19  # Number of channels per cell
A1 = 12  # Total traffic intensity from Erlang B chart, GOS=0.02, C=19
U1 = A1 / Au  # Total number of users
Aa = U1 * 394  # Total Number of Subscribers
percentage_A = (Aa / population) * 100
print(f'Total number of users for system A: {int(Aa)}')
print(f'Percentage market penetration for System A: {percentage_A:.3f}%\n')

# System B
print('\nFor system B:')
print('--------------')
C2 = 57  # Number of channels per cell
A2 = 45  # Total traffic intensity from Erlang B chart, GOS=0.02, C=57
U2 = A2 / Au  # Total number of users
Bb = U2 * 98  # Total Number of Subscribers
percentage_B = (Bb / population) * 100
print(f'Total number of users for system B: {int(Bb)}')
print(f'Percentage market penetration for System B: {percentage_B:.3f}%\n')

# System C
print('\nFor system C:')
print('--------------')
C3 = 100  # Number of channels per cell
A3 = 88   # Total traffic intensity from Erlang B chart, GOS=0.02, C=100
U3 = A3 / Au  # Total number of users
Cc = U3 * 49  # Total Number of Subscribers
percentage_C = (Cc / population) * 100
print(f'Total number of users for system C: {int(Cc)}')
print(f'Percentage market penetration for System C: {percentage_C:.3f}%\n')

# Total for all systems
print('\nFor all three systems:')
print('--------------------')
T = Aa + Bb + Cc  # Total Subscribers
percentage_T = (T / population) * 100
print(f'Total number of users of all three systems: {int(T)}')
print(f'Percentage market penetration for all three Systems: {percentage_T:.3f}%')
Output:
For system A:
--------------
Total number of users for system A: 47280
Percentage market penetration for System A: 2.364%

For system B:
--------------
Total number of users for system B: 44100
Percentage market penetration for System B: 2.205%

For system C:
--------------
Total number of users for system C: 43120
Percentage market penetration for System C: 2.156%

For all three systems:
--------------------
Total number of users of all three systems: 134500
Percentage market penetration for all three Systems: 6.725%
 
Problem-5: A certain city has an area of 1,300 square miles and is covered by a cellular system using a 7-cell reuse pattern. Each cell has a radius of 4 miles and the city is allocated 40 MHz of spectrum with a full duplex channel bandwidth of 60 kHz. Assume a GOS of 2% for an Erlang B system is specified. If the offered traffic per user is 0.03 Erlangs, compute (a) the number of cells in the service area, (b) the number of channels per cell, (c) traffic intensity of each cell, (d) the maximum carried traffic; (e) the total number of users that can be served for 2% GOS, (f') the number of mobiles per channel, and (g) the theoretical maximum number of users that could be served at one time by the system.

Solution:
(a)
Have given,
Total coverage area = 1300 miles Cell radius = 4 miles
We know,
The area of a cell (hexagon) can be shown to be 2.5981R2 Thus each cell covers 2.5981 × (4)2 = 41.57 sq km.
Hence, the total number of cells, Nc = 1300/41.57 = 31 cells

(b)
Have given,
Allocated spectrum	= 40, 000,000 Hz
Channel width	= 60,000 Hz
Frequency reuse factor, N	= 7 cells
We know,
The total number of channels per cell, C = Allocated spectrum / (Channel width × N)
= 40, 000,000 / (60,000 × 7)
= 95 channels/cell
(c)
Have given,
From (b) No, C = 95 And, GOS	= 0.02

From the table 4.1 (Erlang B chart) For C = 95 and GOS = 0.02, we have- Traffic intensity per cell, A = 84 Erlangs/cell

(d)
Have given,
From (a), Number of cells	= 31 cells
From (c), Traffic intensity per cell = 84 Erlangs/cell
We Know,
Maximum carried traffic = Number of cells × Traffic intensity per cell
= 31 × 84
= 2604 Erlangs.
(e)
Have given,
Traffic per user, Au	= 0.03 Erlangs From (d), Total traffic, A	= 2604 Erlangs.
We Know,
Total number of users, U = A / Au
= 2604 / 0.03 = 86,800 users.

(f)
Have given,
Allocated spectrum	= 40, 000,000 Hz
Channel width	= 60,000 Hz From (e), Number of users, U	= 86,800 users.
We Know,
Number of channels	= Allocated Spectrum / Channel Width
= 40, 000,000/60,000
≈ 666
Number of mobiles per channel = Number of users/Number of channels
= 86,800 / 666
≈ 130 mobiles/channel
(g)
Have given,
From (b) No, C	= 95 channels/cell From (a), the total number of cells, Nc= 31 cells.
From (e) Total number of users, U	= 86,800 users.
We Know,
The theoretical maximum number of served mobiles is the number of available channels in the system (all channels occupied)
= C × Nc
= 95  × 31 = 2945 users,


	Which is (2945/86,800) × 100 = 3.4% of the customer base.


Source Code (Python):

import numpy as np
from math import floor  # Importing the floor function from the math module

# Question (a)
total_city_coverage_area = 1300  # Total city coverage area in km^2
radius = 4  # Radius in km
a = (2.591 * radius**2)  # Area covered by each cell in km^2
Nc = round(total_city_coverage_area / a)  # Total number of cells, Nc
print(f'(a) Total number of cells, Nc: {Nc} cells\n')

# Question (b)
allocated_spectrum = 40000  # Allocated spectrum in kHz (40 MHz)
channel_width = 60  # Full duplex channel BW in kHz
N = 7  # Frequency reuse factor
C = round(allocated_spectrum / (channel_width * N))  # Total number of channels per cell
print(f'(b) The total number of channels per cell, C: {C} channels/cell\n')

# Question (c)
A = 84  # Traffic intensity per cell (C=95, GOS=0.02 from Erlang B chart)
print(f'(c) Traffic intensity per cell, A: {A} Erlangs/cell\n')

# Question (d)
max_c_t = floor(Nc * A)  # Maximum carried traffic
print(f'(d) Maximum carried traffic: {max_c_t} Erlangs\n')

# Question (e)
Au = 0.03  # Traffic per user
U = round(max_c_t / Au)  # Total number of users
print(f'(e) Total number of users, U: {U} users\n')

# Question (f)
no_of_channel = floor(allocated_spectrum / channel_width)  # Total number of channels available
no_of_m_p_c = floor(U / no_of_channel)  # Number of mobiles per channel
print(f'(f) Number of mobiles per channel: {no_of_m_p_c} mobiles/channel\n')

# Question (g)
g = C * Nc  # Theoretical maximum number of users that could be served
print(f'(g) Theoretical maximum number of users that could be served: {g} users\n')


Output:

(a) Total number of cells, Nc: 31 cells

(b) The total number of channels per cell, C: 95 channels/cell

(c) Traffic intensity per cell, A: 84 Erlangs/cell

(d) Maximum carried traffic: 2604 Erlangs

(e) Total number of users, U: 86800 users

(f) Number of mobiles per channel: 130 mobiles/channel

(g) Theoretical maximum number of users that could be served: 2945 users
 
Problem-6: If a transmitter produces 50 watts of power, express the transmit power in units of (a) dBm, and (b) dBW. If 50 watts is applied to a unity gain antenna with a 900 MHz carrier frequency, find the received power in dBm at a free space distance of 100 m from the antenna, what is P (10 km)? Assume unity gain for the receiver antenna.

Solution:
Have given,
Transmitter power, Pt = 50 W Carrier frequency, fc    = 900 MHz
(a)
We know,
Transmitter power, Pt(dBm) = 10 log[Pt(mW)/(1mW)]
= 10 log [50 x 103]
= 47.0 dBm
(b)
We know,
Transmitter power, Pt(dBW) = 10 log[Pt(W)/(1W)]
= 10 log [50]
= 17.0 dBW
(c)
If 50 watts is applied to a unity gain antenna with a 900 MHz carrier frequency, Have given,
Transmitter Gain, Gt	= 1
Receiver Gain, Gr	= 1
Wave length λ	= c / f = 1 /3 m The T-R separation distance, d	= 100m
The system loss factor, L	= 1
We know,
The received power, Pr	= (Pt × Gt × Gr × λ2) / (4π2 × d2 × L)
= (50 × 1 × 1 × (1/3)2) / ((4π)2 × 1002 × 1)
= 3.5 × 10-3 mW
Received power, Pr(dBm)	= 10 log[Pr(mW)]
= 10 log[Pr(3.5 × 10-3)]
= -24.5 dBm

(d)
Have given,
do	= 10 km = 10000 m
We Know,
The received power at 10 km can be expressed in terms of dBm, we have
∴ Pr(10 km)	= Pr(100) + 20 log[d / do]
= Pr(100) + 20 log[100 / 10000]
= -24.5 – 40
= -64.5 dBm





Source Code (Python):

import numpy as np

# Given parameters
pt = 50  # Transmitted power in Watts
fc = 900  # Carrier frequency in MHz
gt = 1  # Transmitter antenna gain
gr = 1  # Receiver antenna gain
d = 100  # Free space distance in meters
L = 1  # Loss factor (assuming unity)
c = 3 * 10**8  # Speed of light in m/s

# Wavelength calculation
lambda_ = c / (fc * 10**6)  # lambda = c/f

# Question (a)
tr_dBm = np.ceil(10 * np.log10(pt * 1000))  # Convert from Watts to dBm
print(f'(a) Transmitter power, Pt in dBm: {int(tr_dBm)} dBm\n')

# Question (b)
tr_dBW = np.ceil(10 * np.log10(pt))  # Convert from Watts to dBW
print(f'(b) Transmitter power, Pt in dBW: {int(tr_dBW)} dBW\n')

# Question (c)
# Received power calculation at d = 100 meters
c_received = (pt * gt * gr * (lambda_ ** 2)) / ((4 * np.pi) ** 2 * d ** 2 * L) * 1000  # Received power in mW
Pr = 10 * np.log10(c_received)  # Convert to dBm
print(f'(c) Received power, Pr in dBm: {Pr:.2f} dBm\n')

# Question (d)
# Received power calculation at d = 10,000 meters (10 km)
d_10km = 10000  # Distance in meters
Pr_at_10km = (pt * gt * gr * (lambda_ ** 2)) / ((4 * np.pi) ** 2 * d_10km ** 2 * L) * 1000  # Received power in mW at 10km
Pr_at_10km_dBm = 10 * np.log10(Pr_at_10km)  # Convert to dBm
print(f'(d) Received power, Pr at 10km in dBm: {Pr_at_10km_dBm:.2f} dBm\n')

Output:
(a) Transmitter power, Pt in dBm: 47 dBm

(b) Transmitter power, Pt in dBW: 17 dBW

(c) Received power, Pr in dBm: -24.54 dBm

(d) Received power, Pr at 10km in dBm: -64.54 dBm


 
Problem-7: Determine the path loss of a 900MHz cellular system in a large city from a base station with the height of 100m and mobile station installed in a vehicle with antenna height of 2m. The distance between mobile and base station is 4Km.

Solution:
Have given,
The frequency, fc = 900 MHz (150 MHz to 1500MHz) 
The effective transmitter (base station) antenna height, the       = 100m
The effective transmitter (mobile) antenna height, hre = 2m T-R separation distance, d = 4 km
Now, The correction factor for effective movile antenna height,
a(hre) = 3.2 (log 11.75 hre)2 – 4.97 dB for fc ≥ 300 MHz From Okumura-Hata Model we know,
The path loss in urban areas is given by

= 69.55 + 26.16 × 2.954 – 13.82 × 2 – 1.045 + (44.9 – 13.1) × 0.6
= 137.3 dB


Source Code (Python):

import numpy as np

# Given parameters
hte = 100  # Effective transmitter (base station) antenna height in meters
hre = 2    # Effective receiver (mobile) antenna height in meters
fc = 900   # Frequency in MHz
d = 4      # T-R separation distance in kilometers

# Correction factor using the Okumura-Hata model
a_hre = (3.2 * (np.log10(11.75 * hre)) ** 2) - 4.97

# Path Loss in urban areas
Lp = 69.55 + (26.16 * np.log10(fc)) - (13.82 * np.log10(hte)) - a_hre + ((44.9 - 6.55 * np.log10(hte)) * np.log10(d))

# Output the path loss
print(f'The path loss in urban areas, Lp = {Lp:.2f} dB')

Output:
The path loss in urban areas, Lp = 137.29 dB.
 
Problem-8: Determine the path loss between base station (BS) and mobile station (MS) of a 1.8GHz PCS system operating in a high-rise urban area. The MS is located in a perpendicular street to the location of the BS. The distances of the BS and MS to the corner of the street are 20 and 30 meters, respectively. The base station height is 20m.

Solution:
Have given,
The frequency, fc = 1.8 GHz (0.9 to 2 GHz) 
The effective transmitter (base station) antenna height, hb = 20m
T-R separation distance,  d = √(202 + 302) = 0.036 km From Okumura-Hata Model we know,
The path loss in a high-rise urban areas with Perpendicular Street to the location of the Base Station is given by-
= 135.41 + 12.49 × log (1.8) – 4.99 × log 20 + [46.84 – 2.34 log20] × log 0.036
= 68.91 dB

Source Code (Python):

import numpy as np

# Given parameters
fc = 1.8  # Frequency in GHz
hb = 20   # Effective transmitter (base station) antenna height in meters
d = (np.sqrt(20**2 + 30**2)) / 1000  # T-R separation distance in kilometers

# Path Loss in high-rise urban areas
Lp = 135.41 + (12.49 * np.log10(fc)) - (4.99 * np.log10(hb)) + ((46.84 - 2.34 * np.log10(hb)) * np.log10(d))

# Output the path loss
print(f'The path loss in high-rise urban areas, Lp = {Lp:.2f} dB')

Output:
The path loss in a high-rise urban areas, Lp = 68.91 dB
 
Problem-9: A mobile is located 5 km away from a base station and uses a vertical λ /4 monopole antenna with a gain of 2.55 dB to receive cellular 3 radio signals. The E-field at 1 km from the transmitter is measured to be V/m. The carrier frequency used for this system is 900 MHz.
a)	Find the length and the gain of the receiving antenna.
b)	Find the received power at the mobile using the 2-ray ground reflection model assuming the height of the transmitting antenna is 50 m and the receiving antenna is 1.5m above ground.

Solution:
Have given,
Frequency of operation, f = 900 MHz
Gain of antenna, G = 1.8 = 2.55 dB
(a)
We Know,
Wave length,


And, Gain of antenna, G = 2.55 dB.

(b)
Have given,
T-R separation distance, d	= 5 km
E-field at a distance of 1 km, Eo	= 10-3 V/m
Transmitter distance do	= 1km
Transmitting antenna height, ht	= 50m
Receiving antenna height, hr	= 1.5m
Wave length, λ	= 0.333
We Know,

 
Here, Effective Aperture
= 0.016 m2
Now, the received power at a distance d can be obtained using
= ((113.1 × 10-6)2 × 0.016)/337
= 5.4 × 10-13 W
= -122.68 dbW
= -92.68 dBm

Source Code (Python):

import numpy as np

# Given parameters
f = 900  # Frequency in MHz
g = 2.55  # Gain of antenna in dB

# Question (a)
gain = 10 ** (g / 10)  # Linear gain
lemda = (3 * 10**8) / (f * 10**6)  # Wavelength in meters
L = lemda / 4  # Antenna Length

print('For (a)')
print('---------')
print(f'Length of the antenna: {L:.3f} m')
print(f'Gain of the antenna: {gain:.1f} = {g:.2f} dB\n')

# Question (b)
print('For (b)')
print('---------')
d = 5000  # T-R separation distance in meters
E0 = 10**-3  # Electric-field in V/m
d0 = 1000  # Transmitter distance in meters
ht = 50  # Transmitting antenna height in meters
hr = 1.5  # Receiving antenna height in meters

# Electric Field
Er_d = (2 * E0 * d0 * 2 * np.pi * ht * hr) / (lemda * d**2)  # Electric Field
Ae = (gain * lemda**2) / (4 * np.pi)  # Effective Aperture
Pr_d = (Er_d**2 / (120 * np.pi)) * Ae  # Received power at a distance d
Pr_dB = 10 * np.log10(Pr_d)  # Received power in dBW

# Output results
print(f'Electric Field, Er(d): {Er_d:.9f} V/m')
print(f'Effective Aperture, Ae: {Ae:.3f} m^2')
print(f'Received power at 5 km distance Er(5 km): {Pr_dB:.3f} dBW')
 
Input:
f = 900;	% Frequency in MHz
g = 2.55;	% Gain of antenna in dB

d = 5000;	% T-R separation distance
E0 = 10^-3;	% Electric-field
d0 = 1000;	% Transmitter distance
ht = 50;	% Transmitting antenna height, ht (m)
hr = 1.5;	% Receiving antenna height, hr (m)

Output:
For (a)
Length of the antenna, L	: 0.083 m
Gain of the antenna, G	: 1.8 =   2.55dB

For (b)
Electric Field, Er(d)	: 0.000113098 v/m
Effective Aperture, Ae	: 0.016 m^2 Received power at 5 km distance Er(5 km)	: -122.679 dbW
 
Problem-10: A hexagonal cell within a 4-cell system has a radius of 1.387 km. A total of 60 channels are used within the entire system. If the load per user is 0.029 Erlangs, and λ= call/hour, compute the following for an Erlang C system that has a 5% probability of a delayed call-

a)	How many users per square kilometer will this system support?
b)	What is the probability that a delayed call will have to wait for more than 10s?
c)	What is the probability that a call will be delayed for more than 10 seconds?

Solution:
Have given,
Cell radius, R = 1.387 km
Area covered per cell is 2.598 x (1.387)2  ≈ 5 sq k 
 Number of cells per cluster,n = 4
Total number of channels, N =60 
Therefore, number of channels per cell = 60 / 4 = 15 channels. From Erlang C chart, for 5% probability of delay with C = 15, Traffic intensity, A = 9.0 Erlangs.
(a)
Have given,
Traffic per user, Au = 0.029 Erlangs.
We know,
The number of users, U = A / Au = 9.0/0.029 = 310 users
The number of users per square km	= 310 users /5 sq km
= 62 users /sq km

(b)
Have given,
Wave length, 𝜆	= 1 call/hour
Holding time, H	= Au / 𝜆
= 0.029 hour
= 104.4 seconds.
Time, t	= 10s

We know,
The conditional probability that a delayed call will have to wait for more than t seconds is Pr[delay > t | delay] = exp(-(C-A)t/H)
= exp (-(15-9)10/104.4)
= 56.29 %
(c)
Have given,
The probability of delayed call, Pr[delay > 0] = 5 % = 0.05
We know,
Probability that a call is delayed more than 10 seconds,
Pr[delay > 10] = Pr[delay > 0] × Pr[delay > t | delay]
= 0.05 × 0.5629
= 2.81 %


 

Source Code (Python):

import numpy as np

# Given parameters
R = 1.387  # Cell Radius
n = 4  # Number of cells
N = 60  # Total number of channels
area = round(2.5981 * R**2)  # Area covered per cell
C = N / 4  # Number of channels per cell
A = 9  # Traffic intensity at c=15, GOS=0.05, Au=0.029 from Erlang C chart

# Question (a)
Au = 0.029  # Traffic per user
U = np.floor(A / Au)  # Number of users
U_per = round(U / area)  # Number of users per square km
print(f'(a) Number of users per square km: {U_per} users/sq km\n')

# Question (b)
lemda = 1  # lambda = 1 hour
H = (Au / lemda) * 3600  # Holding Time hour to second
Prb = np.exp(-((C - A) * 10) / H)  # t=10s, C=15, A=9, H
print(f'(b) The probability that a delayed call will have to wait: {Prb * 100:.2f}%\n')

# Question (c)
Prc = 0.05 * Prb * 100  # 5% probability of delayed call
print(f'(c) The probability that a call will be delayed: {Prc:.2f}%\n')


Output:
(a)	Number of users per square km	: 62 users/sq km
(b)	The probability that a delayed call will have to wait	: 56.29%
(c)	The probability that a call will be delayed	: 2.81%
