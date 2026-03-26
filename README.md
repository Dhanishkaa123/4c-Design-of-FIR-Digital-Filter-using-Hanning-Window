# FIR-FILTER-DESIGN
# EXP 4 c: Design-of-FIR-Digital-Filter-using-Hanning-Window

# AIM 1:  To perform Design-of-LOWPASS FIR-Digital-Filter-using-Hanning-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
    // FIR HPF using Hamming Window

     clc;
    clear;
    close;

    // Input values
    M = input("Enter the Odd Filter Length = ");
    Wc = input("Enter the Digital Cut off frequency = ");

    alpha = (M-1)/2;     // Center value

    // Ideal High Pass Filter impulse response
    for n = 1:M
    if (n == alpha + 1) then
        hd(n) = 1 - Wc/%pi;
    else
        hd(n) = -sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
    end
 

     // Hamming Window
    for n = 1:M
    W(n) = 0.54 - 0.46*cos((2*%pi*(n-1))/(M-1));
    end

     // Windowed filter coefficients
     h = hd .* W;

    disp("Filter Coefficients are");
    disp(h);

    // Frequency response
     [hz, fr] = frmag(h,256);

       // Magnitude plot
    subplot(2,1,1)
      plot(2*fr, hz)
    xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude")
    title("Frequency Response of FIR HPF using Hamming Window")

     // Magnitude in dB
     hz_dB = 20*log10(hz);

      subplot(2,1,2)
            plot(2*fr, hz_dB)
         xlabel("Normalized Digital Frequency W")
          ylabel("Magnitude in dB")
        title("Frequency Response of FIR HPF using Hamming Window")


# OUTPUT: 
<img width="975" height="577" alt="image" src="https://github.com/user-attachments/assets/088f5f9c-7fdf-480c-9c7c-6cb42fd2dc99" />


# RESULT: 

Thus design of low pass FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
  // FIR HPF using Hamming Window

     clc;
    clear;
    close;

    // Input values
    M = input("Enter the Odd Filter Length = ");
    Wc = input("Enter the Digital Cut off frequency = ");

    alpha = (M-1)/2;     // Center value

    // Ideal High Pass Filter impulse response
    for n = 1:M
    if (n == alpha + 1) then
        hd(n) = 1 - Wc/%pi;
    else
        hd(n) = -sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
    end
 

     // Hamming Window
    for n = 1:M
    W(n) = 0.54 - 0.46*cos((2*%pi*(n-1))/(M-1));
    end

     // Windowed filter coefficients
     h = hd .* W;

    disp("Filter Coefficients are");
    disp(h);

    // Frequency response
     [hz, fr] = frmag(h,256);

       // Magnitude plot
    subplot(2,1,1)
      plot(2*fr, hz)
    xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude")
    title("Frequency Response of FIR HPF using Hamming Window")

     // Magnitude in dB
     hz_dB = 20*log10(hz);

      subplot(2,1,2)
            plot(2*fr, hz_dB)
         xlabel("Normalized Digital Frequency W")
          ylabel("Magnitude in dB")
        title("Frequency Response of FIR HPF using Hamming Window")


# OUTPUT: 
<img width="975" height="577" alt="image" src="https://github.com/user-attachments/assets/a23d35cb-5a73-4440-ae57-53995f9cdc51" />


# RESULT: 
Thus design of HIGH pass FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
 // FIR HPF using Hamming Window

     clc;
    clear;
    close;

    // Input values
    M = input("Enter the Odd Filter Length = ");
    Wc = input("Enter the Digital Cut off frequency = ");

    alpha = (M-1)/2;     // Center value

    // Ideal High Pass Filter impulse response
    for n = 1:M
    if (n == alpha + 1) then
        hd(n) = 1 - Wc/%pi;
    else
        hd(n) = -sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
    end
 

     // Hamming Window
    for n = 1:M
    W(n) = 0.54 - 0.46*cos((2*%pi*(n-1))/(M-1));
    end

     // Windowed filter coefficients
     h = hd .* W;

    disp("Filter Coefficients are");
    disp(h);

    // Frequency response
     [hz, fr] = frmag(h,256);

       // Magnitude plot
    subplot(2,1,1)
      plot(2*fr, hz)
    xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude")
    title("Frequency Response of FIR HPF using Hamming Window")

     // Magnitude in dB
     hz_dB = 20*log10(hz);

      subplot(2,1,2)
            plot(2*fr, hz_dB)
         xlabel("Normalized Digital Frequency W")
          ylabel("Magnitude in dB")
        title("Frequency Response of FIR HPF using Hamming Window")

# OUTPUT: 
<img width="975" height="577" alt="image" src="https://github.com/user-attachments/assets/08826a8a-1d63-475b-9dee-51dbd691abec" />


# RESULT: 
Thus design of BAND pass FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
 // FIR HPF using Hamming Window

     clc;
    clear;
    close;

    // Input values
    M = input("Enter the Odd Filter Length = ");
    Wc = input("Enter the Digital Cut off frequency = ");

    alpha = (M-1)/2;     // Center value

    // Ideal High Pass Filter impulse response
    for n = 1:M
    if (n == alpha + 1) then
        hd(n) = 1 - Wc/%pi;
    else
        hd(n) = -sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
    end
 

     // Hamming Window
    for n = 1:M
    W(n) = 0.54 - 0.46*cos((2*%pi*(n-1))/(M-1));
    end

     // Windowed filter coefficients
     h = hd .* W;

    disp("Filter Coefficients are");
    disp(h);

    // Frequency response
     [hz, fr] = frmag(h,256);

       // Magnitude plot
    subplot(2,1,1)
      plot(2*fr, hz)
    xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude")
    title("Frequency Response of FIR HPF using Hamming Window")

     // Magnitude in dB
     hz_dB = 20*log10(hz);

      subplot(2,1,2)
            plot(2*fr, hz_dB)
         xlabel("Normalized Digital Frequency W")
          ylabel("Magnitude in dB")
        title("Frequency Response of FIR HPF using Hamming Window")

# OUTPUT: 
<img width="975" height="577" alt="image" src="https://github.com/user-attachments/assets/23efb9fe-7fae-4dfd-a2e5-33c0fc701892" />


# RESULT: 
Thus design of BAND STOP FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.
