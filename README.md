# Lab 8
[Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo) this repo and clone it to your machine to get started!

## Team Members
- Ty Benjamin Majam

## Lab Question Answers

Question 1: What is the phone number dialed in sample3.py?

Answer: 5055034455

Question 2: Describe your algorithm. Explain what each of these functions do: get_peak_frqs(), get_max_frq(), and get_number_from_frq().

Answer: My algorithm begins by taking a slice of the audio sample and performing a fast fourier transform (fft) on it to convert it to the frequency domain. Then, using get_peak_frqs() function, my program is able to locate where the upper and lower frequency peaks are. This function works by splitting the FFT array in half, and finding the location of the highest amplitude within the respectively separated arrays using the get_max_frq() function. Get_max_frq() is a linear search function that traverses through the FFT array, which is provided as a parameter, and compares each value's amplitude to the next; storing the next value's amplitude and frequency as the maximum if it is greater than the previously compared values.

After this initial step has been taken, the program finds the value of the number that corresponds to the locations found from get_peak_frqs(). It uses the function get_number_from_frq() using the values returned from get_peak_frqs(); the function finds the values from the LOWER_FRQS and HIGHER_FRQS that are closest to the passed values by using minimum absolute distance between the sample and given values. Finally, this function will return the number corresponding to the low and high frequencies which was outlined by the dictionary defined at the beginning of the program. 

