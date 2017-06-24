# Spigot Plugin Archetype

This is an archetype for creating a Spigot Plugin. These plugins can be used to create Minecraft Mods.

1. `mvn clean install`
2. `mvn release:prepare -Prelease`
3. `git push`
  * (I was unable to make maven-release-plugin to correctly format the git url, so i've added `<pushChanges>false</pushChanges>` in plugin)
4. `mvn release:perform -Prelease`

settings.xml:

    <settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
    		  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    		  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
    					  https://maven.apache.org/xsd/settings-1.0.0.xsd">  
    	<servers>
    		<server>
    			<id>github</id>
    			<username>mihai-vasilache</username>
    			<password>XXXXXXXXX</password>
    		</server>
    		<server>
    			<id>ossrh</id>
    			<username>mihai-vasilache</username>
    			<password>XXXXXXXXX</password>
    		</server>
    		<server>
    			<id>ossrh</id>
    			<username>mihai-vasilache</username>
    			<password>XXXXXXXXX</password>
    		</server>
    	</servers>
    	<profiles>
    		<profile>
    			<id>release</id>
    			<properties>
    				<gpg.keyname>11111111</gpg.keyname>
    				<gpg.passphrase>XXXXXXXXX</gpg.passphrase>
    				<gpg.defaultKeyring>false</gpg.defaultKeyring>
    				<gpg.useagent>true</gpg.useagent>
    				<gpg.lockMode>never</gpg.lockMode>
    				<gpg.homedir>c:\Users\mihai\AppData\Roaming\gnupg</gpg.homedir>
    				<gpg.publicKeyring>c:\Users\mihai\AppData\Roaming\gnupg\pubring.gpg</gpg.publicKeyring>
    				<gpg.secretKeyring>c:\Users\mihai\AppData\Roaming\gnupg\secring.gpg</gpg.secretKeyring>
    			</properties>
    		</profile>
    	</profiles>
    </settings>