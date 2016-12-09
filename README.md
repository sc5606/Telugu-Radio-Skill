# Telugu-Radio-Skill
Amazon skill to play Indian Telugu Radio Stations

This is my first Alexa Skill and the first code to upload in GitHub. So, pardon me if I am not following standards.

I only modifed the index.js script from the main GitHub code "skill-sample-nodejs-audio-player" and replaced the contents of "audioAssets.js" with Telugu Radio Stations.

### Important:
There are couple of things that you need to do for this code to work on your device:
* constatns.js --> As the commented line says App-ID value should be the one from AWS Development under Skill Information.
    Please note that replacing with ARN value from Lambda will not work.
* I had lot of trouble with table not being created in DynamoDB. Some mentioned that by testing directly on the device itself will create the table but for some reason I was not sucessfull and had to create manually. 

#### Creating table manually in DynamoDB:
##### Table Name: LongFormAudioSample
##### Primary Key: userId

Once created, enable Streaming by selecting the table and selecting "Manage Stream"

As I mentioned earlier that this is my first Skill and I am still trying to get full hands on utterances and other stuff to see  how exactly this little interesting toy works.

For now, with this code, I can ask Alexa 
```
Alexa open MySkill-NameHere
```
and then I can ask Alexa to 
```
Alexa play next
```
or 
```
Alexa play previous
```
to play different radio stations.

##### Limitations:
As per [AudioPlayer Interface Reference](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/custom-audioplayer-interface-reference), the URL must be with https. It took a while to find Telugu radio stations with pls format and comptabile with https. So, please do share any other links if you come across.

### Step by Step Instructions:

Please follow the step by step instructions from this source: (This is where I got the code and edited for my purpose)
https://github.com/alexa/skill-sample-nodejs-audio-player

###### Big Thanks to @inhumantsar from GitHub who helped me to pass thru the table creation.
