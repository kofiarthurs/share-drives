<h1>Share Drives</h1>
<h2>Description</h2>
I will be creating share drives on Active Directory and mapping them to Jess (regular user).
</br>
In Server Manager we go to File and Storage Services and click on shares. We right click and selct New Share.
</br>
</br>
<img src="https://imgur.com/0qufYzo.png" height="80%" width="80%"/>

We are choosing SMB Share – Quick.
</br>

<img src="https://imgur.com/Xr1zHbj.png" height="80%" width="80%"/>

We name the share, gallery.
</br>

<img src="https://imgur.com/1IEAWYM.png" height="80%" width="80%"/>
<img src="https://imgur.com/BcLOFh9.png" height="80%" width="80%"/>

We are going to give users in the HR security group access to the share. We select the Gallery Properties and the security tab and select Advanced.
</br>

<img src="https://imgur.com/Diyo58K.png" height="80%" width="80%"/>

In Advanced Security Settings for Gallery, we disable inheritance and convert them into explicit permissions. This allows us to modify who has access to the share.
</br>

<img src="https://imgur.com/FqZhVfM.png" height="80%" width="80%"/>

We remove User (EA\Users) which is default OU in Active Directory that houses many groups. WE only want HR security group to access and the administrators.
</br>

<img src="https://imgur.com/sTakVuY.png" height="80%" width="80%"/>

We add HR by selecting Add, then Select a principal. We make sure the Modify permission is selected. The other permissions were already selected. 
</br>

<img src="https://imgur.com/M1PmRfF.png" height="80%" width="80%"/>
<img src="https://imgur.com/8giIClB.png" height="80%" width="80%"/>

We will use Jess’s account because she is already part of the HR security group.
</br>

<img src="https://imgur.com/HlNplVl.png" height="80%" width="80%"/>

We will search for the drive.
</br>

<img src="https://imgur.com/fOy0ZFL.png" height="80%" width="80%"/>

To map the drive, we will right click on Network.
</br>

<img src="https://imgur.com/kn3q9QQ.png" height="80%" width="80%"/>

We put in the path and make sure “Reconnect at sign-in” in selected, so that Jess's access is permanent.
</br>

<img src="https://imgur.com/ft9K2sM.png" height="80%" width="80%"/>

Success
</br>

<img src="https://imgur.com/VP9ECXv.png" height="80%" width="80%"/>

<h2>Using Active Directory to Map a Drive</h2>

You go to AD Users and Computers, select the users properties, Profile, type in the share path and apply.
</br>

<img src="https://imgur.com/slqO0bf.png" height="80%" width="80%"/>
<img src="https://imgur.com/E6xU2p3.png" height="80%" width="80%"/>


<h2>Viewing Jess's share on The Command Line</h2>
We type net use
</br>
</br>

<img src="https://imgur.com/BQnM6EF.png" height="80%" width="80%"/>

<h2>Viewing Jess's share on REmote Registry</h2>
We select File, Connect Netork Registry then add Desktop-2, which is the name on Jess's pc.
</br>
</br>

<img src="https://imgur.com/STBkdyO.png" height="80%" width="80%"/>

