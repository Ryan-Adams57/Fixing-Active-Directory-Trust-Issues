# Fixing-Active-Directory-Trust-Issues

Fixing Active Directory Trust Relationship Issues: 3 Quick Methods.

If you get the error "𝘛𝘩𝘦 𝘵𝘳𝘶𝘴𝘵 𝘳𝘦𝘭𝘢𝘵𝘪𝘰𝘯𝘴𝘩𝘪𝘱 𝘣𝘦𝘵𝘸𝘦𝘦𝘯 𝘵𝘩𝘪𝘴 𝘸𝘰𝘳𝘬𝘴𝘵𝘢𝘵𝘪𝘰𝘯 𝘢𝘯𝘥 𝘵𝘩𝘦 𝘱𝘳𝘪𝘮𝘢𝘳𝘺 𝘥𝘰𝘮𝘢𝘪𝘯 𝘧𝘢𝘪𝘭𝘦𝘥" it’s often due to the computer losing sync with Active Directory (like when a password update is missed between the Domain Controller and a computer).

And in this post I'll give you 3 quick ways to Fix this issue: 

𝗠𝗲𝘁𝗵𝗼𝗱 𝟭: 𝗥𝗲𝗽𝗮𝗶𝗿 𝗧𝗿𝘂𝘀𝘁 𝘄𝗶𝘁𝗵 𝗣𝗼𝘄𝗲𝗿𝗦𝗵𝗲𝗹𝗹 (𝗦𝗶𝗺𝗽𝗹𝗲 & 𝗙𝗮𝘀𝘁).

𝟭️ > 𝗟𝗼𝗴 𝗶𝗻 𝗮𝘀 𝗮 Local Admin.
𝟮️ > 𝗥𝘂𝗻: Test-ComputerSecureChannel -Repair -Credential DomainName\Administrator
𝟯️ > 𝗥𝗲𝘀𝘁𝗮𝗿𝘁 𝗮𝗻𝗱 𝗶𝘁 𝘀𝗵𝗼𝘂𝗹𝗱 𝗿𝗲𝗰𝗼𝗻𝗻𝗲𝗰𝘁.

𝗠𝗲𝘁𝗵𝗼𝗱 𝟮: 𝗥𝗲𝘀𝗲𝘁 𝗖𝗼𝗺𝗽𝘂𝘁𝗲𝗿 𝗣𝗮𝘀𝘀𝘄𝗼𝗿𝗱 𝘄𝗶𝘁𝗵 𝗣𝗼𝘄𝗲𝗿𝗦𝗵𝗲𝗹𝗹.
𝟭️ > 𝗟𝗼𝗴 𝗶𝗻 𝗮𝘀 𝗮 Local Admin.
𝟮️ > 𝗥𝘂𝗻: Reset-ComputerMachinePassword -Server DomainServer -Credential DomainName\Administrator
𝟯️ > 𝗥𝗲𝘀𝘁𝗮𝗿𝘁 𝗮𝗻𝗱 𝗶𝘁 𝘀𝗵𝗼𝘂𝗹𝗱 𝗿𝗲𝗰𝗼𝗻𝗻𝗲𝗰𝘁.

𝗠𝗲𝘁𝗵𝗼𝗱 𝟯: 𝗗𝗶𝘀-𝗷𝗼𝗶𝗻 𝗮𝗻𝗱 𝗥𝗲-𝗷𝗼𝗶𝗻 𝗗𝗼𝗺𝗮𝗶𝗻 𝗨𝘀𝗶𝗻𝗴 𝗱𝘀-𝗷𝗼𝗶𝗻.
𝟭️ > 𝗟𝗼𝗴 𝗶𝗻 𝗮𝘀 𝗮 Local Admin.
𝟮️ > 𝗗𝗶𝘀𝗷𝗼𝗶𝗻 𝗳𝗿𝗼𝗺 𝘁𝗵𝗲 𝗱𝗼𝗺𝗮𝗶𝗻: dsjoin /leave
𝟯️ > 𝗥𝗲𝘀𝘁𝗮𝗿𝘁 𝘁𝗵𝗲𝗻 𝗿𝗲𝗷𝗼𝗶𝗻 𝘁𝗵𝗲 𝗱𝗼𝗺𝗮𝗶𝗻: dsjoin /domain DomainName /userD DomainAdminUser /passwordD *
𝟰️ > 𝗥𝗲𝘀𝘁𝗮𝗿𝘁 𝗮𝗴𝗮𝗶𝗻, 𝗮𝗻𝗱 𝘁𝗵𝗲 𝗿𝗲𝗹𝗮𝘁𝗶𝗼𝗻𝘀𝗵𝗶𝗽 𝘀𝗵𝗼𝘂𝗹𝗱 𝗯𝗲 𝗿𝗲𝘀𝘁𝗼𝗿𝗲𝗱.
