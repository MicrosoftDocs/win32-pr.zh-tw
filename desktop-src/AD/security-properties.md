---
title: 使用者安全性屬性
description: 除了命名使用者物件的屬性（例如 objectGUID、objectSid、cn、distinguishedName 等等）之外，還有其他安全性屬性用於登入、網路存取和存取控制。
ms.assetid: eeb16938-4380-4622-804f-6b2ff19aa68d
ms.tgt_platform: multiple
keywords:
- 安全性屬性，使用 AD
- 使用者安全性屬性 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51000aefdf9ec0f26406607bd781ac4d87b6106
ms.sourcegitcommit: 25bf66769c2087b1a87d6db5930b604cb57e0f98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/23/2020
ms.locfileid: "103933694"
---
# <a name="user-security-attributes"></a>使用者安全性屬性

除了命名使用者物件的屬性（例如 [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)、 [**objectSid**](/windows/desktop/ADSchema/a-objectsid)、 [**cn**](/windows/desktop/ADSchema/a-cn)、 [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)等等）之外，還有其他安全性屬性用於登入、網路存取和存取控制。 Windows 2000 安全性系統會使用這些屬性。 這些屬性可由 Active Directory 使用者和電腦] 嵌入式管理單元來查看和管理。

<dl> <dt>

<span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)
</dt> <dd>

[**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires)屬性會指定帳戶到期的時間。 此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。 TIMEQ 中定義 **的 \_ 永久** (值) 指出帳戶永遠不會過期。

</dd> <dt>

<span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)
</dt> <dd>

[**AltSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)屬性是多重值屬性，其中包含針對驗證目的，x.509 憑證或外部 Kerberos 使用者帳戶到這位使用者的對應。 各種安全性套件（包括公開金鑰驗證套件和 Kerberos）會在使用者出示替代形式的身分識別（例如憑證、UNIX Kerberos 票證等等）時，使用這項資料來驗證使用者。 根據對應的使用者帳戶建立 Windows 2000 權杖，讓他們可以存取系統資源。

針對 x.509 憑證，這些值應為 x.509v3 憑證中的簽發者和主體名稱（由外部公開憑證授權單位單位所簽發），該憑證會對應到用來尋找帳戶以進行驗證的使用者帳戶。 SSL (Schannel) 封裝使用下列語法： X509： <somecertinfotype> somecertinfo。 例如，下列值會以 dn " \<I\> c = us，o = InternetCA，CN = APublicCertificateAuthority"，以及 \<S\> Dn "c = Us，o = FABRIKAM，OU = SALES，CN = Jeff Smith" 的主體 dn ""，來指定簽發者 DN ""。


```C++
X509:<I>C=US,O=InternetCA,CN=APublicCertificateAuthority<S>C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith
```



請注意， \<S\> 支援 "" 或 " \<I> " 和 " \<S\> "。 \<I\>不支援「」。 應用程式不應該修改 " \<I\> " 或 "" 內的值， \<S\> 因為不支援部分 DN 比對。

若為外部 Kerberos 帳戶，值應為 Kerberos 帳戶名稱。 Kerberos 封裝會使用下列語法： "Kerberos： MITaccountname"。 例如，以下是 Fabrikam.com 帳戶的值：


```C++
Kerberos:Jeff.Smith@Fabrikam.com
```



</dd> <dt>

<span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)
</dt> <dd>

非複寫。 [**BadPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)屬性會指定使用者上次嘗試使用不正確的密碼登入帳戶的時間。 此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。 這個屬性會在網域中的每個網域控制站上分開維護。 值為零表示最後一個錯誤的密碼時間是未知的。 若要取得使用者在網域中的上次錯誤密碼時間的準確值，您必須查詢網域中的每個網域控制站，並使用最大的值。

</dd> <dt>

<span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)
</dt> <dd>

非複寫。 [**BadPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)屬性會指定使用者嘗試使用不正確的密碼登入帳戶的次數。 這個屬性會在網域中的每個網域控制站上分開維護。 值為0表示值不明。 若要取得使用者在網域中的錯誤密碼嘗試總數的精確值，必須查詢網域中的每個網域控制站，並使用值的總和。

</dd> <dt>

<span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**字碼頁**](/windows/desktop/ADSchema/a-codepage)
</dt> <dd>

代碼 [**頁屬性會**](/windows/desktop/ADSchema/a-codepage) 指定使用者所選擇語言的字碼頁。 Windows 2000 不會使用這個值。

</dd> <dt>

<span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**countryCode**](/windows/desktop/ADSchema/a-countrycode)
</dt> <dd>

[**CountryCode**](/windows/desktop/ADSchema/a-countrycode)屬性會指定使用者語言的國家/地區代碼。 Windows 2000 不會使用這個值。

</dd> <dt>

<span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)
</dt> <dd>

[**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory)屬性會指定使用者的主目錄路徑。 字串可以是 null。

如果已設定 [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) 並指定磁碟機號， [**HOMEDIRECTORY**](/windows/desktop/ADSchema/a-homedirectory) 應該是 UNC 路徑。 路徑必須是表單 \\ \\ 伺服器 \\ 共用目錄的網路 UNC 路徑 \\ 。 這個值可以是 null 字串。

如果未設定 [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) ， [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) 應該是本機路徑，例如 C： \\ mylocaldir。

</dd> <dt>

<span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**homeDrive**](/windows/desktop/ADSchema/a-homedrive)
</dt> <dd>

[**HomeDrive**](/windows/desktop/ADSchema/a-homedrive)屬性會指定要對應 **homeDirectory** 所指定之 UNC 路徑的磁碟機號。 磁碟機號必須以下列格式指定：


```C++
<drive letter>:
```



其中 " \<drive letter\> " 是要對應之磁片磁碟機的字母。 例如：


```C++
Z:
```



如果未設定此屬性， [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) 應該是本機路徑，例如 C： \\ mylocaldir。

</dd> <dt>

<span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)
</dt> <dd>

非複寫。 [**LastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)屬性會指定上次發生登出的時間。 此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。 這個大型整數的最高部分對應至 [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)結構的 **dwHighDateTime** 成員，而低部分則對應至 **filetime** 結構的 **dwLowDateTime** 成員。 這個屬性會在網域中的每個網域控制站上分開維護。 值為零表示最後一次登出時間是未知的。 若要取得使用者在網域中上次登出的精確值，您必須查詢網域中的每個網域控制站，並使用最大的值。

</dd> <dt>

<span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)
</dt> <dd>

非複寫。 [**LastLogon**](/windows/desktop/ADSchema/a-lastlogon)屬性會指定上次登入的時間。 此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。 這個大型整數的最高部分對應至 [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)結構的 **dwHighDateTime** 成員，而低部分則對應至 **filetime** 結構的 **dwLowDateTime** 成員。 這個屬性會在網域中的每個網域控制站上分開維護。 值為零表示最後一個登入時間未知。 若要取得使用者在網域中最後一次登入的精確值，您必須查詢網域中的每個網域控制站，並使用最大的值。

</dd> <dt>

<span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)
</dt> <dd>

[**LmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)屬性是區域網路管理員中使用者的密碼歷程記錄， (LM)  (OWF) 的單向格式。 LM OWF 是用於與 LAN Manager 2.x 用戶端、Windows 95 和 Windows 98 的相容性。 這個屬性僅供作業系統使用。 請注意，您無法從密碼的 OWF 形式衍生純文字密碼。

</dd> <dt>

<span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**logonCount**](/windows/desktop/ADSchema/a-logoncount)
</dt> <dd>

非複寫。 [**LogonCount**](/windows/desktop/ADSchema/a-logoncount)屬性會計算使用者嘗試登入此帳戶的成功時間數目。 這個屬性會在網域中的每個網域控制站上進行維護。 值為0表示值不明。 若要取得使用者在網域中成功登入嘗試總數的精確值，必須查詢網域中的每個網域控制站，並使用值的總和。

</dd> <dt>

<span id="mail"></span><span id="MAIL"></span>[**郵件**](/windows/desktop/ADSchema/a-mail)
</dt> <dd>

[**Mail**](/windows/desktop/ADSchema/a-mail)屬性是單一值屬性，其中包含使用者的 SMTP 位址，例如 " jeff@Fabrikam.com "。

</dd> <dt>

<span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)
</dt> <dd>

[**MaxStorage**](/windows/desktop/ADSchema/a-maxstorage)屬性會指定使用者可使用的硬碟空間數量上限。 使用在 Lmaccess 中定義的「 **使用者 \_ MAXSTORAGE \_ 無限制** (，) 值來使用所有可用的磁碟空間。

</dd> <dt>

<span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**memberOf**](/windows/desktop/ADSchema/a-memberof)
</dt> <dd>

[**MemberOf**](/windows/desktop/ADSchema/a-memberof)屬性是多重值的屬性，其中包含使用者是直接成員的群組，但主要群組除外，其由 [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)所代表。 群組成員資格相依于從中抓取此屬性 (DC) 的網域控制站：

-   在包含使用者之網域的 DC 中，使用者的 [**memberOf**](/windows/desktop/ADSchema/a-memberof) 是針對該網域中群組的成員資格完成的。不過， **memberOf** 不包含使用者在網域本機的成員資格以及其他網域中的全域群組。
-   在 GC 伺服器上，使用者的 [**memberOf**](/windows/desktop/ADSchema/a-memberof) 是針對所有通用群組成員資格完成的。

如果 DC 的這兩個條件都成立，則這兩組資料都會包含在 [**memberOf**](/windows/desktop/ADSchema/a-memberof)中。

請注意，這個屬性會列出成員屬性中包含使用者的群組，而不包含嵌套前置項的遞迴清單。 例如，如果 user O 是群組 C 的成員，而群組 B 是嵌套在群組 A 中，使用者 O 的 [**memberOf**](/windows/desktop/ADSchema/a-memberof) 屬性會列出群組 C 和群組 b，但不會列出群組 a。

這個屬性不會儲存，而是計算的後置連結屬性。

</dd> <dt>

<span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)
</dt> <dd>

[**NtPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)屬性是使用者的密碼歷程記錄，以 Windows NT 的單向格式 (OWF) 。 Windows 2000 使用 Windows NT OWF。 這個屬性僅供作業系統使用。 請注意，您無法從密碼的 OWF 形式衍生純文字密碼。

</dd> <dt>

<span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox)
</dt> <dd>

[**OtherMailbox**](/windows/desktop/ADSchema/a-othermailbox)屬性是多重值屬性，其中包含表單中其他的其他郵寄地址，例如 "CCMAIL： JeffSmith"。

</dd> <dt>

<span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods)
</dt> <dd>

密碼到期日不是使用者物件上的屬性。 它是以使用者的 [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) 與使用者網域 [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) 的總和為基礎的計算值。 若要取得密碼到期日，請取得 [**IADsUser. PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods) 屬性。 您無法為使用者修改此屬性;請改為設定 [**IADsDomain MaxPasswordAge**](/windows/desktop/ADSI/iadsdomain-property-methods) 屬性，以變更網域的設定。

</dd> <dt>

<span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)
</dt> <dd>

[**PrimaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)屬性是單一值屬性，其中包含做為物件之主要群組的群組 [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) 。 物件的主要群組未包含在 [**memberOf**](/windows/desktop/ADSchema/a-memberof) 屬性中。 例如，根據預設，使用者物件的主要群組是 Domain Users 群組的 **primaryGroupToken** ，但是 domain users 群組不是 user 物件的 **memberOf** 屬性的一部分。

</dd> <dt>

<span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**profilePath**](/windows/desktop/ADSchema/a-profilepath)
</dt> <dd>

[**ProfilePath**](/windows/desktop/ADSchema/a-profilepath)屬性會指定使用者設定檔的路徑。 這個值可以是 null 字串、區域絕對路徑或 UNC 路徑。

</dd> <dt>

<span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)
</dt> <dd>

[**PwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)屬性會指定上次變更密碼的時間。 此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。

系統會使用此屬性的值和包含使用者物件之網域的 [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) 屬性，來計算密碼到期日。 也就是使用者網域的使用者和 **maxPwdAge** 的 [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)總和。

這個屬性會控制使用者下次登入時是否必須變更密碼。 如果 [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) 為零（預設值），則使用者必須在下次登入時變更密碼。 值-1 表示使用者不需要在下次登入時變更密碼。 系統會在使用者設定密碼之後，將此值設定為-1。

</dd> <dt>

<span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)
</dt> <dd>

[**SAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)屬性會指定代表帳戶類型的整數。 這是在建立物件時由作業系統設定。

</dd> <dt>

<span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)
</dt> <dd>

[**ScriptPath**](/windows/desktop/ADSchema/a-scriptpath)屬性會指定使用者的登入腳本、.cmd、.exe 或 .bat 檔案的路徑。 字串可以是 null。

</dd> <dt>

<span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)
</dt> <dd>

[**UnicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)屬性是使用者密碼。

若要設定使用者密碼，請使用 [**IADsUser**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) 方法，如果您的腳本或應用程式可讓使用者變更自己的密碼，或 [**IADsUser SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) 方法（如果您的腳本或應用程式允許系統管理員重設密碼）。

Windows NT 單向格式的使用者密碼 (OWF) 。 Windows 2000 使用 Windows NT OWF。 這個屬性僅供作業系統使用。 請注意，您無法從密碼的 OWF 形式衍生純文字密碼。

</dd> <dt>

<span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)
</dt> <dd>

[**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)屬性會指定旗標，以控制使用者的密碼、鎖定、停用/啟用、腳本和主目錄行為。 這個屬性也包含一個旗標，指出物件的帳戶類型。 使用者物件通常會 \_ 設定 UF 一般 \_ 帳戶。

下列旗標定義于 Lmaccess 中。



| 旗標                     | 描述                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UF \_ 腳本               | 執行的登入腳本。 必須為 LAN Manager 2.0 或 Windows NT 設定此值。                                                                             |
| UF \_ ACCOUNTDISABLE       | 使用者帳戶已停用。                                                                                                                                    |
| \_需要 UF HOMEDIR \_    | 需要主目錄。 在 Windows NT 和 Windows 2000 中，會忽略此值。                                                                            |
| UF \_ PASSWD \_ NOTREQD      | 不需要密碼。                                                                                                                                         |
| 無法 \_ 變更 UF 密碼 \_ \_ | 使用者無法變更密碼。                                                                                                                             |
| UF \_ 鎖定              | 帳戶目前已鎖定。 您可以清除此值以解除鎖定先前鎖定的帳戶。 此值不能用來鎖定先前鎖定的帳戶。 |
| UF 不會讓 \_ \_ \_ PASSWD 過期 | 代表密碼，此密碼永遠不會在帳戶上到期。                                                                                               |



 

下列旗標描述帳戶類型。 只能設定一個值。 您無法變更帳戶類型。



| 旗標                            | 描述                                                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UF \_ 一般 \_ 帳戶             | 這是代表一般使用者的預設帳戶類型。                                                                                                                                                                                  |
| UF \_ 暫存 \_ 重複 \_ 帳戶    | 這是主要帳戶位於另一個網域的使用者帳戶。 此帳戶可讓使用者存取此網域，但不提供任何信任此網域的網域。 使用者管理員會將此帳戶類型稱為本機使用者帳戶。 |
| UF \_ 工作站 \_ 信任 \_ 帳戶 | 這是 Windows NT 工作站/Windows 2000 Professional 或 Windows NT Server/Windows 2000 伺服器（此網域的成員）的電腦帳戶。                                                                                     |
| UF \_ 伺服器 \_ 信任 \_ 帳戶      | 這是屬於此網域成員 Windows NT 備份網域控制站的電腦帳戶。                                                                                                                                           |
| 每個 UF \_ 域 \_ 信任 \_ 帳戶 | 這是允許信任其他網域的 Windows NT 網域的帳戶。                                                                                                                                                            |



 

</dd> <dt>

<span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**userCertificate**](/windows/desktop/ADSchema/a-usercertificate)
</dt> <dd>

[**UserCertificate**](/windows/desktop/ADSchema/a-usercertificate)屬性是多重值屬性，其中包含發給使用者的 DER 編碼 X509v3 憑證。 請注意，此屬性包含由 Microsoft 憑證服務發給此使用者的公開金鑰憑證。

</dd> <dt>

<span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)
</dt> <dd>

[**UserSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)屬性會指定使用者的 [共用文件] 資料夾的 UNC 路徑。 路徑必須是表單 \\ \\ 伺服器 \\ 共用目錄的網路 UNC 路徑 \\ 。 這個值可以是 null 字串。

</dd> <dt>

<span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)
</dt> <dd>

[**UserWorkstations**](/windows/desktop/ADSchema/a-userworkstations)屬性是單一值屬性，其中包含使用者可以登入之工作站的 NetBIOS 名稱。 每個 NetBIOS 名稱會以逗號分隔。

如果未設定任何值，則表示沒有任何限制。 若要停用此帳戶的所有工作站登入，請 \_ 在 [ [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) ] 屬性中，將 [ACCOUNTDISABLE]) 中定義的 [UF] 值設定 (。

</dd> </dl>

 

 
