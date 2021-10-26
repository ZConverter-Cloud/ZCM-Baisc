
OCI Migration (Legacy)
============
>**ZConverter Cloud Migration Membership**
>
> **How to use ZConverter Cloud Migration**
>
> **Target VM generation**
>
> **Migration from Source VM to Target VM**

## ZConverter Cloud Migration Membership

   1. **Access https://www.z-cloud.net/ through a web browser.**

![z-cloud_login_page](https://objectstorage.ap-seoul-1.oraclecloud.com/p/LhU0LzQbizV37i_Ah3_n_DVaxLPp4epIQZovdSk1_sghBB47-5PXpMt80YWtk43-/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/login_page.png)

   2. **Click "Register a new membership" and proceed with membership registration.**
     ![join](https://objectstorage.ap-seoul-1.oraclecloud.com/p/NatEsknqsOQqPH9nglJ0uABApihcG6_5E2aVDkt9t_xStvMMhGw_BKWQUXwT8pq0/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/join.png)



## How to use ZConverter Cloud Migration

   1. **Click the target platform you want to migrate from "Cloud Migration" in the left menu.**
      ![menu](https://objectstorage.ap-seoul-1.oraclecloud.com/p/CHGAlT2dO8q16xdLNFDJRvpptYfait1ugwQUhlAdVheKbArRU7eHpfsohD5OEbYG/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/menu.png)

	2. **Register on the source server.**
	      
		* **ZConverter Cloud Source Agent installation.**
		* **You must register a source or target server for a migration operation, or install a zconverter cloud agent on the server for communication between the source or target server and the zconverter management server.**
		* **Download the Source Agent installation file corresponding to the source server's OS (Windows or Linux) from the "Download Agent" panel.**
![menu](https://objectstorage.ap-seoul-1.oraclecloud.com/p/2ru3qRxwo94pc5zujqUPYyDvpOUgOZWvpf6Xcz8w9gfEWBMSXkhh_Dql9I2NlLG4/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/download_source_agent.png)
			1. **Windows Server**
				* **Remote access to the source server and copy the downloaded agent installation file to the source server.**
![mst_win](https://objectstorage.ap-seoul-1.oraclecloud.com/p/63ewreDnVMyRDm03Rjre5HX_DrZP3lcXB0yv9Lc1wXJBkF7dokLe69DBhZ7Cs8LQ/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/mst_win.png)
				* **After running the installation file, select the installation language and click OK.**
![select_lengage](https://objectstorage.ap-seoul-1.oraclecloud.com/p/TjYpw21MRlt7VUFYW655Xb57_HggeLiqjjHgk_9wzHDxoVzZMxx-P-o9dmnjs76c/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/select_lengage.png)
				* **Click "next"**
![click_next](https://objectstorage.ap-seoul-1.oraclecloud.com/p/WGKkhFYNMkxTAQMTN_kcvivx2cmON7u0f3cm0elXkwb4rTP_2yKOAA35l8UcR3p3/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/click_next.png)
				* **Click "I Agree"**
![click_agree](https://objectstorage.ap-seoul-1.oraclecloud.com/p/UDTluFeglMYoKM78iL1E5JzqoqOX67h31FE1aJbeREwdKnrmP88avVaOU5hvJATv/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/click_agree.png)
				* **Click "Install"**
![click_install](https://objectstorage.ap-seoul-1.oraclecloud.com/p/SUk2-nR39rj4uqDs1q1KTecKmqYpAxhUqRjzO0BpiFUaT3KOgFa9mhatI6KDqzjt/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/click_install.png)
				* **When the settings window appears, enter or select the following information.**
					* **Connect option : Choose "Public ZConverter SaaS(http://www.z-cloud.net)"**
					* **Agent mode : "Source"**
					* **User Information : Enter the account information you are currently accessing.**
![setting](https://objectstorage.ap-seoul-1.oraclecloud.com/p/zxO07rutYuR56QWQ8eHtdb9u0xxvmSrcvsQuLMyu4F8sxW9kR0DwfTavJ7DBryEm/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/source_agent_setting.png)
		2. **Linux Server**
			* **SSH access to the source server, and copy the downloaded agent installation file to the /tmp directory of the source server.**
			* **Proceed with the installation through the following command.**
			![setting](https://objectstorage.ap-seoul-1.oraclecloud.com/p/kBabefUOUWB-1-37BD8DLOyfsdWAzFJySXatCiUrATZ-P7DtmV8UFeQT_wCDeyW0/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/linux_cmd.png)
			```script
			cd /tmp
			tar zxvf ZConverter_CloudSourceClient_Setup_RedHat_x86_V3.0_Build_3005.tar.gz
			cd zconverter_install_source
			```
			* **./install.sh command to proceed with the installation.**
			* **This is where the agent is to be installed. If you want to install it on a different path, enter that path. The default installation route is /ZConverteragent.**
![setting](https://objectstorage.ap-seoul-1.oraclecloud.com/p/EytFlCV9h7GRnGm8hTE9QUqt0x_uprcnRdyZJm9HOpmfyCpmQCO5ccupStEP3L1r/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/lin_install.sh.png)
			* **This is the type selection of ZConverter Cloud Migration.  
If you use Public ZCM, choose Item 1, and if you use Private ZCM, select Item 2 and enter the IP of that ZCM.**
			![setting](https://objectstorage.ap-seoul-1.oraclecloud.com/p/kLlZurifHbdyPkIn6U4RcntGT73gvRp-Yktoq3Sz3uyqKwIa-YgxaKC08-9Fr-dA/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/lin_cmd_set1.png)
			* **This is the part where you enter the account of ZCM that you are currently using.**
			![setting](https://objectstorage.ap-seoul-1.oraclecloud.com/p/GEBtU_EfhtMLlERYKJhFpINZZdMCpjY8mHAPoT4InC_oV43ZlbtN1ZmrSaiCcJBG/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/lin_cmd_set2.png)
			* **When the installation is complete as shown in the following screen, close the connection with the server and return to the z-cloud.net web portal.**
			![setting](https://objectstorage.ap-seoul-1.oraclecloud.com/p/MLxy9PhxFvrzbUu-UCid5ftWwxGlBVF7uYMGSzbgY17WIksezWGPsK5HhQGrXtVB/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/lin_cmd_set3.png)
			![setting](https://objectstorage.ap-seoul-1.oraclecloud.com/p/VdIfvxWm2dohvowgVnXYjj2rYgTmV0QhnZyd71niWzidjT2HOdT16UUmI0kZS9Jo/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/lin_cmd_set4.png)
3. **Register a source server.**
	* **Click the "Load a server list" button to bring the server where the source agent is installed to the list.**
	![setting](https://objectstorage.ap-seoul-1.oraclecloud.com/p/9jf4PvdBAU2imi9Tu8vkpbAW0qX-Egzt4bhJUmZenXP3lC1lcg6kYWR3xKu83W3f/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/register_a_source_server.png)
	* **Please check the connection status between the source server's agent and the ZConverter Cloud Management server through the leftmost icon in the server list. If the connection is disconnected, it is displayed as a red icon, and if the migration proceeds to this state, it may cause an error.**
![setting](https://objectstorage.ap-seoul-1.oraclecloud.com/p/JWDgwMLRRsNRyiDVO6KxGxzC_oQ_s8FBs4rTQ6PVEKyQvrJRRTM8cGI1An_KPCbc/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/source_server_error.png)
	
	* **Click on the server to migrate, and select a source server imaging method in the "Create or select a source image" panel.**
		* **"Create a new image" option: Select if you create and migrate a new image of the server.**
		* **"Use an listing image" option: Select if you are migrating an existing server image.**
		![setting](https://objectstorage.ap-seoul-1.oraclecloud.com/p/qPzwMWjml-Na0JSx6ni0FvHmHCUsx8OFDOzq5X3580gvm9NOptmCH4pjTVHIO-ED/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/register_a_source_server1.png)
		* **Check the disk to be migrated.**
		* **In the "Option" panel, select the type and path of the source image storage. 
		(The source image storage is used to store the image of the source server.)**
			* **"Basic" type: Local type storage that is created within the source server and stores images.**
				* We recommend creating a repository on a disk other than the disk to be migrated (when migrating Windows) or creating a repository in the root directory (when migrating Linux).
			* **"Advanced" type: Storage on a remote server. You can select a storage or other network storage within the target server.**
				* Select the "Target Repository" menu if you want to create a repository within the target server to store the source image.
		* **Click "next".**
		![setting](https://objectstorage.ap-seoul-1.oraclecloud.com/p/APAMJ8dSi-KlBXtBShDqWu_3fe-kypxGGQzXPLEXkO5DcLhI4FV5BwXdg0UaIAG8/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/register_a_source_server2.png)


## Target VM generation

   1. **Log in to the Oracle Cloud site and access the user portal.**

      ![Login](https://objectstorage.ap-seoul-1.oraclecloud.com/p/gXC1gD0QT92Z5YLpepd8Mj_nN-g8mggX_0whcHla5vqN3Fzx_z_os0IfJAlVWHpA/n/idffti7li8cs/b/github_image_bucket/o/login/login3.png)  

   2. **Enter the Instance menu.**

      ![Enter_instance_menu](https://objectstorage.ap-seoul-1.oraclecloud.com/p/JFNMFhEX7pbuuHxYM2ftE8t8KIMVq4oG4hPPlIyBVa0HrPSlx0xdlhQCHOySbV-U/n/idffti7li8cs/b/github_image_bucket/o/legacy/menu(instance).png)  

   3. **Click Create instance button**
      ![create_instance_button](https://objectstorage.ap-seoul-1.oraclecloud.com/p/aDnXftAn-Va7bZBH4g_DQer1K8m5lQXiEFzqtOZ_CLeGs158lBA0LoGfFWlR_hOZ/n/idffti7li8cs/b/github_image_bucket/o/legacy/create_instance.png)

   4. **Please choose the OS and shape you want to create.**

      ![Api-Key](https://objectstorage.ap-seoul-1.oraclecloud.com/p/scvVRsLUJSk5Lqr89y3O3Lf0GS7cE1L1GEklhz_NahEAZceWloUOc50RD5ocQRl4/n/idffti7li8cs/b/github_image_bucket/o/legacy/choice_os_and_shape.png)

   5. **If the selected OS is Linux series, the ssh key must also be registered.**
     ![use_ssh_key](https://objectstorage.ap-seoul-1.oraclecloud.com/p/PUIoPJqSZyHkKuQxXsCvjPZFMxtTkVfKVRHGpZft2copkVuoifLZ3kvN5MkvIVZN/n/idffti7li8cs/b/github_image_bucket/o/legacy/use_ssh_key.png)

   6. **Enter the Block Volumes menu.**

      ![block-menu](https://objectstorage.ap-seoul-1.oraclecloud.com/p/y1i7aKXyU3qmybxP_V761HYjuJfy0Cjns7fGul0v94NlR-WIc5gFWvNc-kgo1cNQ/n/idffti7li8cs/b/github_image_bucket/o/legacy/block_volume(menu).png)

   7. **Click Create Block Volume button**
     ![create_block_volume](https://objectstorage.ap-seoul-1.oraclecloud.com/p/P0m3zbndsGxNPGyCT3MIutT37rxWxQhqVdq7w1vCJqDiUsPu28cTLn-NcMMxE0dN/n/idffti7li8cs/b/github_image_bucket/o/legacy/block_volume_create.png)
   
   8. **Create blocks according to the options you need.**
     ![block_option](https://objectstorage.ap-seoul-1.oraclecloud.com/p/DY6pGKsCkzhIitE1cEz67fwHdM5ANp3mZ4w8MzwDOP4VFBGgIRtfCZqZvjIvGhNk/n/idffti7li8cs/b/github_image_bucket/o/legacy/block_volume_create_option.png)
   
   9. **Go back to the instance window and click the name of the instance you created.**

![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/eSNqkwbxXCC_fLsL0RMvydF7zh9bgqOr--QsbRM5b4ZoYXW_43a9xQ1UUp8O91hE/n/idffti7li8cs/b/github_image_bucket/o/legacy/attach_block.png)

   10. **In the lower left resource, click Attach block volume in the Attached block volumes column.**

![attach_block_volume](https://objectstorage.ap-seoul-1.oraclecloud.com/p/K-9mIAD1_Urm3S7TJ2KYi5SXJdVL_I82Z18kcJZVRlw9jY3nH5GFXvVR4JOIEFa6/n/idffti7li8cs/b/github_image_bucket/o/legacy/attach_block1.png)

   11. **Connect pre-generated blocks. In the case of Linux series of OS, the device path must be set. 
(left photo: Linux, right photo: windows)**
     ![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/PuoUS2H3KtZS_fsQ90JvBIETZLn5YpM2fmmRGz5G3uY03W2nWryNwPqBUmJ0OQJ_/n/idffti7li8cs/b/github_image_bucket/o/legacy/attach_block_linux_and_winows.png)

12.  **Register on the target server.**
		1.  **ZConverter Cloud Target Agent installation**
			- Download the Target Agent installation file corresponding to the target server's OS (Windows or Linux) from the "Download Agent" panel at the top of the page.
![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/UPSyu1t_NQFtgunLxyTU8fJPMoc5gfkJ7l_XRp9Bd6nelzPqqw9jddawKE8MS8sx/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_agent_install.png)
				A.  **Windows Server**
				- The target agent installation procedure is the same as for source agent installation.
				- After remote access to the target instance, copy the downloaded agent installation file to the target instance. The subsequent installation procedure proceeds the same as the second process of "How to use ZConverter Cloud Migration."
			
				B.  **Linux Server**
				- SSH access to the target server and copy the downloaded agent installation file to the /tmp directory of the target server.
				- Proceed with the installation through the following command.
				![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/rLVPyFec0OhJU1A97JJoHkYqdyeQNJ9JTui6sF7PCc9hqbDyyxAnKgZlSLQTBoS_/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_agent_install_lin1.png)
				```script
				cd /tmp
				tar zxvf ZConverter\_CloudTargetClient\_Setup\_RedHat\_x86\_V3.0\_Build\_3005.tar.gz
				#(The file name may be different. Please enter the exact file name of the downloaded agent installation file.)
				cd zconverter\_install\_target
				```
				- Enter the ./install.sh command to proceed with the installation.
				- This is where the agent is to be installed. If you want to install it on a different path, enter that path. The default installation route is /ZConverteragent.
				![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/oOMpwxMGBJ7SLToUWbRrkiKsvCQOwwZpWyiuCO8FHY_btxlurdpY2K9kctw3BhAV/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_agent_install_lin2.png)
				- This is the type selection of ZConverter Cloud Migration. If you use Public ZCM, choose Item 1, and if you use Private ZCM, select Item 2 and enter the IP of that ZCM.
				![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/4vLnZ-tubyDSvmnozySGe8JZEl4VBnWvue_DCRy93_Y2mBqDX_nitFvOb21r3uX0/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_agent_install_lin3.png)
				- This is the part where you enter the account of the ZCM you are currently using.
				![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/_gz0Ld0GtjDXf3MQ9I_f0fleBEzIbIEg3D5opshTnf_7rk9URGgIInOlj3XZyqWw/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_agent_install_lin4.png)
				- When the installation is complete as shown in the following screen, terminate access to the server and return to the z-cloud.net web portal.
				![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/bmzFiP8LFl1XLdbyeVtMpQIyO6wDEhNlwyJdefQ4i2VdBeCKTCzriOeSazWVN0ZM/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_agent_install_lin5.png)
				![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/0JXQBcCuGIfaHJb3L_Js2h2sKvtI1-l1c8KQKPpRsStCV5x4-Zt0z5I30DR6KToe/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_agent_install_lin6.png)
1.  **Register on the target server.**
	- Click the "Load a server list" button to retrieve the server on which the target agent is installed.
	![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/VCHwQAFsC3i0IHlanRBSVjHMdruHF37NpEXh99FAPhDD8KaBvHoX0YtgsW8EyOOD/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_server_register_1.png)
	- Please check the connection status between the source server's agent and the ZConverter Cloud Management server through the leftmost icon in the server list. When the connection is disconnected, it is displayed as a red icon, and if you proceed with the migration to this state, it may cause an error.
	![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/eh8bo0mG1yjUk2FX7MrcsxtLAsPBIRGmbUcC1tGUWNp4NdSDiOrJZeSvarRz7zoH/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_server_register_2.png)
- Click the migration target server in the target server list to retrieve disk information.
- Map the migration target disk of the source server to the "Mapping to the source server" item of the same disk drive as the migration target disk of the source server.
![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/A06h5twPkqx3ZggJOpctMnQShL5I04X4Rm_iPVYGRmgShtSTslK2x0LDPdkCoVS4/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_server_register_3.png)
- In the "Target Repository" panel, select the type and path of the image repository.

  

	- "Basic" Type : Select this option when the source image repository is set to the "Basic" type or "Advanced" type "Target Repository" menu.
		※ The target repository must be created on a drive other than the drive mapped to the source server (**Windows** migration), or on the /ZConverter/ZConverter path (**Linux** migration).
	- "Advanced" type: Select this option if the source image store is set to "Advanced" type of network store (please select the same network store selected as the source image store).
![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/08og3enrrGn2li2l_e-Yd2ps4W7XbrHkGOZAYv7aVTDW17hNIMkHaXLhqS-RLzAO/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_server_register_4.png)
  
- In the "Replication Option" panel, set the target server IP and port to which the source image is to be transmitted.
	- Target IP : Select the authorized IP of the target server 
	  (if not on the list, please press the "Add IP" button to add it).
	- Replication Port : Sets the port number to connect when sending the image (default: 50005).
- Set other migration options in the "Other Option" panel.
	- Hypervisor : Select the virtual device driver type for the cloud instance.
	- Kernel update : Check if you want to update the kernel version of the server. 
(When you migrate Linux)
	- Encryption (AES256) : Select if you want to apply data encryption during migration.
	- After job script : Register the script file to be executed after migration is completed.
(Only .cmd or .sh files can be registered.)
- Click "next".
![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/2YFY04QRpFRF7XPB9IUV7gHMt8LxgK99nTj6C5f8nADdOov615QgDk3eH4UrPtZ0/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_server_register_5.png)
- Press the "OK" button to start the migration.
![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/GTI7Xj0YHloo73Yv4XecZlC_2odllP3xbVMkuNgPFNkxBqAHqSDHxXU6BP5eX2kl/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_server_register_6.png)
- When the migration operation starts, it automatically goes to the "Monitoring Job" page.
![attach_block](https://objectstorage.ap-seoul-1.oraclecloud.com/p/SxUVI6xixpevYwRDMnAHYuud2M9ijGanr0WOTR6srS87ZsS5L9WCFvV8QF4kiZiF/n/idffti7li8cs/b/github_image_bucket/o/z-cloud/target_server_register_7.png)
