# Process_Docs : For Windows Defender Onboarding with verification steps.
# Steps to onboard windows server 2016 to windows defender portal.

1. Enable windows defender feature
2. Ensure latest Servicing stack update and Cumulative Update is installed on the server.
3. Ensure that the server is restarted and the windows defender service is running : **this verification step that the defender feature is installed properly.**
 2a. If windows defender service is not starting that "Disable Anti-spyware Reg key" as following:
    HKLM\Software\Policies\Microsoft\Windows Defender\
     Key Name : DisableAntiSpyware vlaue to be 0 ( change the key value to zero)
4. Once the windows defender service is running than install KB4052623.( The latest platform update)
   4.a : Platform update will reflect under c:\program Data\Microsoft\windows defender\platform with latest date7&time stamp.
5. Now, try to run the .msi agemt for windows defender unified agent or try to install it using SCCM as MDE agent from client settings
6. Run the on-boardimng script on the server by either of the option like local script, GPO or SCCM (.onboarding script)
