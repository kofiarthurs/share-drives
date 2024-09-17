<h1>Share Drives</h1>
<h2>Description</h2>
I will be creating share drives on Active Directory and mapping them to Jess (regular user).
</br>
In Server Manager we go to File and Storage Services and click on shares. We right click and selct New Share.

We are choosing SMB Share – Quick.

We name the share, gallery.

We are going to give users in the HR security group access to the share. We select the Gallery Properties and the security tab and select Advanced.

In Advanced Security Settings for Gallery, we disable inheritance and convert them into explicit permissions. This allows us to modify who has access to the share.

We remove User (EA\Users) which is default OU in Active Directory that houses many groups. WE only want HR security group to access and the administrators.

We add HR by selecting Add, then Select a principal. We make sure the Modify permission is selected. The other permissions were already selected. 

We will use Jess’s account because she is already part of the HR security group.

We will search for the drive.

To map the drive, we will right click on Network.

We put in the path and make sure “Reconnect at sign-in” in selected, so that Jess's access is permanent.

Success

<h2>Using Active Directory to Map a Drive</h2>

You go to AD Users and Computers, select the users properties, Profile, type in the share path and apply.

<h2>Viewing Jess's share on The Command Line</h2>
We type net use

<h2>Viewing Jess's share on REmote Registry</h2>
We select File, Connect Netork Registry then add Desktop-2, which is the name on Jess's pc.
