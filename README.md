# flight-monitor
After many years of opening the FlightRadar24 app on my phone every time a plane would fly overhead I decided there had to be a lazier way.  What if I could build a display device that would monitor for aircraft flying over my location and let me know what type of plane it was and where it was going.  I was inspired by a post I found on reddit where someone made a display of a flight flying nearby and I set about trying to make my own.  

I started by looking for sources of data that I could access through an API.  As it turns out, this is much harder to find than I thought.  There are plenty of free sources for flight information but the information tends to be:
- Partial Information - it might have a aircraft type code and flight number but not the airline and 
- Definitely not the origin and destination information of the flight and
- Rate limited in how many API calls you can make

The project on reddit which inspired me was using data from hexdb.io which is a great free API to get good information on the aircraft but it's route information can be quite out of date and inaccurate.  As I worked on this project I would see planes flying over my house in Chicago and hexdb.io would report they were flying from San Francisco to Los Angeles (not likely).

Then I stumbled upon the ADSB community on reddit and did some more digging.  ADS-B stands for Automatic Dependent Surveillance-Broadcast, a technology that uses aircraft avionics, GPS, and ground infrastructure to provide surveillance information to air traffic control (ATC) and other aircraft. ADS-B is more precise than radar.

All planes (essentially) are broadcasting ADS-B radio signals and anyone can tune in to these signals with an antenna and some radio signal processing.

I purchased a radio antenna and signal processor from flightaware.com and I hooked it up to a raspberry pi to run software called piAware.  By setting this up I could sign up for an account on FlightAware and feed the data to this company who uses it for commercial purposes.  What I get in return is some extra calls to their very robust API library.  If I make too many calls I get charged but if I keep it under a certain number per month it remains free.

Here is the flow

### Sections Explained

1. **Title**: `# LED Display Project` - This is the name of your project. Use `#` for the largest header.

2. **Introduction**: A quick summary of what the project does.

3. **Badges** (optional): Badges give status about the build, license, or other important information. You can find badges at [shields.io](https://shields.io/).

4. **Table of Contents**: Helps users navigate a long `README`. Use links like `[Installation](#installation)` to link to sections within your document.

5. **Installation**: Instructions on how to set up the project. Include commands for cloning the repository, installing dependencies, and setting up any hardware.

6. **Usage**: Provide code examples or usage instructions so users can run the software. This can include commands to execute scripts, explanations of parameters, and more.

7. **Features**: A list of features that the project offers.

8. **Contributing**: Instructions on how others can contribute. Include details about forking the repository, creating branches, making pull requests, and testing.

9. **License**: Information about how the project is licensed. Typically, include a link to the `LICENSE` file in your repository.

10. **Contact**: Provide your contact information or a link to your GitHub profile so people can reach you with questions.

### Formatting Tips
- **Headings**: Use `#` through `######` for headings of different levels.
- **Bold Text**: Use `**text**` for bold text.
- **Italic Text**: Use `*text*` for italics.
- **Code Blocks**: Use triple backticks (```) for code blocks.
- **Inline Code**: Use single backticks (`) for inline code, like `git clone`.
- **Links**: `[Text](URL)` format for hyperlinks.
- **Lists**: Use `-` or `*` for bullet points and numbers for ordered lists.

### Example for Your Project
For your LED display project, customize the sections according to your specific requirements. For instance, in the "Installation" section, you could include detailed instructions about setting up the hardware or any specific library for the display.

Let me know if you need more help with any part of the `README` or have specific content you'd like to add!
