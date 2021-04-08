---
description: 列出驗證 Api 中使用的函數。
ms.assetid: 946ab34a-f52a-4720-8516-cdcae2883d9b
title: 驗證函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3634996aa7217e88dab81dd65e5f61cbd8c015a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693511"
---
# <a name="authentication-functions"></a>驗證函式

驗證函式會根據使用方式分類，如下所示：

-   [SSPI 函數](#sspi-functions)
    -   [封裝管理](#package-management)
    -   [認證管理](#credential-management)
    -   [內容管理](#context-management)
    -   [訊息支援](#message-support)
-   [由 SSP/Ap 所執行的函式](#functions-implemented-by-sspaps)
-   [使用者模式 SSP/Ap 所執行的函式](#functions-implemented-by-user-mode-sspaps)
-   [由 SSP/Ap 呼叫的 LSA 函數](#lsa-functions-called-by-sspaps)
-   [使用者模式 SSP/Ap 所呼叫的 LSA 函數](#lsa-functions-called-by-user-mode-sspaps)
-   [GINA 匯出函數](#gina-export-functions)
-   [登入使用者功能](#logon-user-functions)
-   [Winlogon 支援函式](#winlogon-support-functions)
-   [網路提供者函式](#network-provider-functions)
    -   [網路提供者所執行的函式](#functions-implemented-by-network-providers)
    -   [支援函式](#winlogon-support-functions)
    -   [連接通知函數](#connection-notification-functions)
-   [LSA 登入功能](#lsa-logon-functions)
-   [由驗證封裝所執行的函式](#functions-implemented-by-authentication-packages)
-   [由驗證套件呼叫的 LSA 函數](#lsa-functions-called-by-authentication-packages)
-   [子驗證函式](#subauthentication-functions)
-   [認證管理功能](#credentials-management-functions)
    -   [認證管理 UI 函數](#credentials-management-ui-functions)
    -   [低層級認證管理功能](#low-level-credentials-management-functions)
    -   [認證管理通知函式](#credential-management-notification-functions)
-   [智慧卡功能](#smart-card-functions)
-   [SASL 函數](#sasl-functions)
-   [其他函式](#other-functions)

## <a name="sspi-functions"></a>SSPI 函數

安全性支援提供者介面 (SSPI) 函式屬於下列主要類別。

-   [套件管理](#package-management)

    列出可用 [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 和選取封裝的函式。

-   [認證管理](#credential-management)

    建立和處理 [*主體*](/windows/desktop/SecGloss/p-gly)[*認證*](/windows/desktop/SecGloss/c-gly)之控制碼的函式。

-   [內容管理](#context-management)

    使用認證控制碼來建立 [*安全性內容*](/windows/desktop/SecGloss/s-gly)的函式。

-   [訊息支援](#message-support)

    使用安全性內容的函式，以確保訊息在透過安全連線交換期間的訊息 [*完整性*](/windows/desktop/SecGloss/i-gly) 和 [*隱私權*](/windows/desktop/SecGloss/p-gly) 。 您可以透過訊息簽署和簽章驗證來實現完整性。 透過訊息加密和解密來達成隱私權。

### <a name="package-management"></a>封裝管理

SSPI 封裝管理功能會起始 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)、列舉可用的套件，以及查詢安全性封裝的屬性。 下列 SSPI 函數提供安全性封裝的管理服務。



| 函式                                                       | 描述                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) | 列出可用的安全性套件和其功能。<br/>                                                                                                                                                                                                                                                                   |
| [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea)         | 抓取 (SSP) 分派資料表之安全性支援提供者的指標。<br/>                                                                                                                                                                                                                                                    |
| [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa)   | 抓取指定 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)的相關資訊。 這項資訊包含驗證 [*資訊、認證和內容*](/windows/desktop/SecGloss/c-gly)的大小界限。<br/> |



 

### <a name="credential-management"></a>認證管理

SSPI 認證管理函式提供 [*認證*](/windows/desktop/SecGloss/c-gly) 控制碼、不透明安全性物件的參考，以存取主體。 安全性物件不透明，因為應用程式只能存取控制碼，而不是結構的實際內容。

認證內容內容的所有參考都是透過物件的控制碼，而 [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 會將該控制碼的存取權取值為，以存取認證的詳細資訊。 認證控制碼是介於 {0x00000000，0x00000000} 和 {0xFFFFFFFF，0xFFFFFFFE} 之間的64位值。

應用程式會使用認證控制碼搭配 [內容管理](#context-management) 功能來建立 [*安全性內容*](/windows/desktop/SecGloss/s-gly)。

認證管理函式也會釋放認證控制碼和查詢 [*認證的*](/windows/desktop/SecGloss/c-gly)[*屬性*](/windows/desktop/SecGloss/a-gly)。 目前，與認證相關聯的名稱是唯一可查詢的屬性。

下列函式會搭配認證管理使用。



| 函式                                                                         | 描述                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireCredentialsHandle (一般)**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) | 取得指定主體之預先存在認證的控制碼。<br/>                                                                                                                                                             |
| [**ExportSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-exportsecuritycontext)                           | 將安全性內容匯出至內容緩衝區。<br/>                                                                                                                                                                                      |
| [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle)                           | 釋放認證控制碼和相關聯的資源。<br/>                                                                                                                                                                                 |
| [**ImportSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-importsecuritycontexta)                           | 使用 [**ExportSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-exportsecuritycontext) 將匯出的安全性內容匯入至目前的進程。<br/>                                                                                                          |
| [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa)                 | 抓取 [*認證*](/windows/desktop/SecGloss/c-gly)的 [*屬性*](/windows/desktop/SecGloss/a-gly)，例如與認證相關聯的名稱。<br/> |



 

### <a name="context-management"></a>內容管理

SSPI 內容管理功能會建立和使用 [*安全性*](/windows/desktop/SecGloss/s-gly)內容。

在通訊連結中，用戶端和伺服器會合作建立共用的安全性內容。 用戶端和伺服器都使用安全性內容與 [訊息支援](#message-support) 函式，以確保連接期間的訊息 [*完整性*](/windows/desktop/SecGloss/i-gly) 和 [*隱私權*](/windows/desktop/SecGloss/p-gly) 。

安全性內容是不透明的安全性物件。 應用程式無法使用安全性內容中的資訊。 內容管理函式會建立並使用內容控制碼，而安全性封裝會對內容控制碼進行取值，以存取其安全性內容。

內容控制碼是介於 {0x00000000，0x00000000} 和 {0xFFFFFFFF，0xFFFFFFFE} 之間的64位值。

下列函式會搭配內容管理使用。



| 函式                                                                           | 描述                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)         | 由伺服器用來根據從用戶端接收到的不透明訊息來建立 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 。<br/>                                                                                                                                                                                                      |
| [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken)                                     | 將補充安全性訊息套用至現有的安全性內容。<br/>                                                                                                                                                                                                                                                                                                                |
| [**CompleteAuthToken**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken)                                     | 完成驗證權杖。 此函式是由通訊協定（例如 DCE）所使用，這些通訊協定需要在傳輸應用程式更新某些訊息參數之後修改安全性資訊。<br/>                                                                                                                                                                                   |
| [**DeleteSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext)                             | 釋出安全性內容和相關聯的資源。<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**FreeCoNtextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer)                                     | 釋出安全性封裝所配置的記憶體緩衝區。<br/>                                                                                                                                                                                                                                                                                                                                  |
| [**ImpersonateSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext)                   | 模擬安全性內容，以用戶端的形式出現在系統中。<br/>                                                                                                                                                                                                                                                                                                                |
| [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) | 用戶端用來藉由產生要傳遞至伺服器的不透明訊息來起始安全性內容。<br/>                                                                                                                                                                                                                                                                               |
| [**QueryCoNtextAttributes (一般)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa)       | 可讓傳輸應用程式查詢安全性 [*內容*](/windows/desktop/SecGloss/c-gly)的特定 [*屬性*](/windows/desktop/SecGloss/a-gly)之 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)。<br/>                                                         |
| [**QuerySecurityCoNtextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken)                     | 取得用戶端 [*安全性內容*](/windows/desktop/SecGloss/s-gly)的 [*存取權杖*](/windows/desktop/SecGloss/a-gly)，並直接使用。<br/>                                                                                                                                                |
| [**SetCoNtextAttributes**](/windows/desktop/api/Sspi/nf-sspi-setcontextattributesa)                               | 可讓傳輸應用程式設定 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)的安全性 [*內容*](/windows/desktop/SecGloss/c-gly)的 [*屬性*](/windows/desktop/SecGloss/a-gly)。 只有 Schannel 安全性套件支援此函式。<br/> |
| [**RevertSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-revertsecuritycontext)                             | 允許 [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 中斷呼叫端的模擬，並還原其本身的 [*安全性內容*](/windows/desktop/SecGloss/s-gly)。<br/>                                                                                                      |



 

### <a name="message-support"></a>訊息支援

SSPI 訊息支援函式可讓應用程式傳輸和接收防篡改的訊息，以及加密和解密訊息。 這些函式適用于一或多個包含訊息的緩衝區，以及 [內容管理](#context-management)功能所建立的 [*安全性內容*](/windows/desktop/SecGloss/s-gly)。 函數的行為會根據連接、 [*資料包*](/windows/desktop/SecGloss/d-gly)或串流內容是否正在使用而有所不同。 如需這些差異的說明，請參閱 [SSPI 內容語義](sspi-context-semantics.md)。

下列函數提供訊息的安全性支援。



| 函式                                                     | 描述                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DecryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) | 使用 [*安全性內容*](/windows/desktop/SecGloss/s-gly)中的 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly)，將加密的訊息解密。<br/> |
| [**EncryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) | 使用安全性內容中的工作階段金鑰來加密訊息。<br/>                                                                                                                                                                      |
| [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)                       | 產生訊息的密碼編譯總和檢查碼，也包含排序資訊以防止訊息遺失或插入。<br/>                                                                                                         |
| [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)                   | 使用 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函式來驗證傳送者所簽署之訊息的簽章。<br/>                                                                                                  |



 

## <a name="functions-implemented-by-sspaps"></a>由 SSP/Ap 所執行的函式

下列函式是由 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly)驗證套件中包含的 [安全性套件](#sspi-functions)所執行 / [](/windows/desktop/SecGloss/a-gly) (SSP/ap) 。

在下表中，第一組函式是由 Windows XP SSP/AP 安全性套件所執行。 第二組函式只由 SSP/AP 安全性封裝執行。

[*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 使用 SSP/AP 的 [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn)函式所提供的 SECPKG 函式 [**\_ \_ 資料表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table)結構來存取這些函數。

下列函式是由所有驗證套件所執行。



| 函式                                                           | 描述                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LsaApCallPackage**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_call_package)                       | 由 [*本機安全機構*](/windows/desktop/SecGloss/l-gly) 呼叫 (lsa) 當具有 lsa 信任連線的登入應用程式呼叫 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) 函式並指定驗證封裝的識別碼時。<br/> |
| [**LsaApCallPackagePassthrough**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_call_package_passthrough) | 傳送至 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) 函數之傳遞登入要求的分派函式。<br/>                                                                                                                                                                                                            |
| [**LsaApCallPackageUntrusted**](/previous-versions/windows/desktop/legacy/aa378218(v=vs.85))     | 當具有不受信任的 LSA 連接的應用程式呼叫 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)函式並指定驗證封裝的識別碼時，由 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 。<br/>   |
| [**LsaApInitializePackage**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_initialize_package)           | 由 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) 呼叫一次 (LSA 在系統初始化期間) ，以提供驗證封裝本身的初始化機會。<br/>                                                                                                       |
| [**LsaApLogonTerminated**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_terminated)               | 用來在登入會話終止時通知驗證套件。 當最後一個參考登入會話的權杖被刪除時，登入會話就會終止。<br/>                                                                                                                                                                                          |
| [**LsaApLogonUser**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user)                           | 驗證使用者的登入認證。<br/>                                                                                                                                                                                                                                                                                                                   |
| [**LsaApLogonUserEx**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex)                       | 驗證使用者的登入認證。<br/>                                                                                                                                                                                                                                                                                                                   |
| [**LsaApLogonUserEx2**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex2)                     | 用來驗證使用者初始登入的使用者登入嘗試。 為使用者建立新的登入會話，並傳回使用者的驗證資訊。<br/>                                                                                                                                                                                |



 

下列額外的函式是由 SSP/AP 安全性套件所執行。



| 函式                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SpAcceptCredentials**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptcredentialsfn)                   | 由「[*本地安全機構*](/windows/desktop/SecGloss/l-gly)」（ (LSA) ）呼叫，以傳遞 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)針對已驗證 [*安全性主體*](/windows/desktop/SecGloss/s-gly)儲存的任何 [*認證*](/windows/desktop/SecGloss/c-gly)。<br/> |
| [**SpAcceptLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn)             | 用來建立伺服器和用戶端共用之 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 的伺服器分派函數。<br/>                                                                                                                                                                                                                                                                                                                  |
| [**SpAcquireCredentialsHandle**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacquirecredentialshandlefn)     | 呼叫以取得主體 [*認證*](/windows/desktop/SecGloss/c-gly)的控制碼。<br/>                                                                                                                                                                                                                                                                                                                                                              |
| [**SpAddCredentials**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spaddcredentialsfn)                         | 用來新增 [*安全性主體*](/windows/desktop/SecGloss/s-gly)的 [*認證*](/windows/desktop/SecGloss/c-gly)。<br/>                                                                                                                                                                                                                                                                              |
| [**SpApplyControlToken**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spapplycontroltokenfn)                   | 將控制項標記套用至 [*安全性內容*](/windows/desktop/SecGloss/s-gly)。 [*本地安全機構*](/windows/desktop/SecGloss/l-gly)目前未呼叫此函數 (LSA) 。<br/>                                                                                                                                                                              |
| [**SpDeleteCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-kspdeletecontextfn)                           | 刪除 [*安全性內容*](/windows/desktop/SecGloss/s-gly)。<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**SpDeleteCredentials**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spdeletecredentialsfn)                   | 從 [*安全性套件*](/windows/desktop/SecGloss/s-gly)的 [*主要*](/windows/desktop/SecGloss/p-gly)或 [*補充*](/windows/desktop/SecGloss/s-gly)認證清單中刪除 [*認證*](/windows/desktop/SecGloss/c-gly)。<br/>                                               |
| [**SpFreeCredentialsHandle**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spfreecredentialshandlefn)           | 釋放呼叫 [**SpAcquireCredentialsHandle**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacquirecredentialshandlefn)函式所取得的 [*認證*](/windows/desktop/SecGloss/c-gly)。<br/>                                                                                                                                                                                                                                                                                                 |
| [**SpGetCredentials**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spgetcredentialsfn)                         | 擷取使用者認證。                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**SpGetExtendedInformation**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn)         | 提供 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)的延伸資訊。<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**SpGetInfo**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spgetinfofn)                                       | 提供 [*安全性套件*](/windows/desktop/SecGloss/s-gly)的一般資訊，例如其名稱和功能。<br/>                                                                                                                                                                                                                                                                                                                |
| [**SpGetUserInfo**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spgetuserinfofn)                               | 抓取登入 [*會話*](/windows/desktop/SecGloss/s-gly)的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| [**SPInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn)                                 | [*本地安全機構*](/windows/desktop/SecGloss/l-gly)會呼叫一次 (LSA) 來提供 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)和一般安全性資訊，以及支援函式的分派資料表。<br/>                                                                                                                                          |
| [**SpInitLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn)                 | 用來在伺服器和用戶端之間建立 [*安全性內容*](/windows/desktop/SecGloss/c-gly) 的用戶端分派函數。<br/>                                                                                                                                                                                                                                                                                                                               |
| [**SpQueryCoNtextAttributes**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spquerycontextattributesfn)         | 捕獲 [*安全性內容*](/windows/desktop/SecGloss/s-gly)的屬性。<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**SpQueryCredentialsAttributes**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spquerycredentialsattributesfn) | 抓取 [*認證*](/windows/desktop/SecGloss/c-gly)的屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**SpSaveCredentials**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spsavecredentialsfn)                       | 將 [*補充認證*](/windows/desktop/SecGloss/s-gly) 儲存至使用者物件。<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**SpSetExtendedInformation**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn)         | 設定 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)的延伸資訊。<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**SpShutdown**](/previous-versions/windows/desktop/legacy/aa380183(v=vs.85))                                     | 在卸載 SSP/AP 之前，執行任何所需的清除。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**SslCrackCertificate**](/windows/desktop/api/Schannel/nf-schannel-sslcrackcertificate)                   | 傳回 [**X509Certificate**](/windows/desktop/api/Schannel/ns-schannel-x509certificate) 結構，其中包含指定之憑證 [*BLOB*](/windows/desktop/SecGloss/b-gly)中包含的資訊。<br/>                                                                                                                                                                                                                                                                                                  |
| [**SslEmptyCache**](/windows/desktop/api/Schannel/nf-schannel-sslemptycachea)                               | 從 Schannel 快取中移除指定的字串。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**SslFreeCertificate**](/windows/desktop/api/Schannel/nf-schannel-sslfreecertificate)                     | 釋放先前呼叫 [**SslCrackCertificate**](/windows/desktop/api/Schannel/nf-schannel-sslcrackcertificate) 函式所配置的憑證。<br/>                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="functions-implemented-by-user-mode-sspaps"></a>使用者模式 SSP/Ap 所執行的函式

下列函式是由 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) / [*驗證套件*](/windows/desktop/SecGloss/a-gly)所執行， (可以載入用戶端/伺服器應用程式的 SSP/ap) 。

SSP/AP 表示它會在 [**SpInitLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn)和 [**SpAcceptLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn)函式的 *MappedCoNtext* 參數中傳回 **TRUE** ，以執行使用者模式函數。 **SpInitLsaModeCoNtext** 函數是由傳輸層級應用程式的用戶端所使用，而 **SpAcceptLsaModeCoNtext** 則是由伺服器端使用。

將 SSP/AP 載入至用戶端進程或伺服器進程是由安全性提供者 DLL （Security.dll 或 Secur32.dll 所處理。 安全性提供者 DLL 會藉由找出 SSP/AP 所執行之 [**SpUserModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spusermodeinitializefn) 函式的位址並加以呼叫，來載入 SSP/ap。 此函式會傳回一組表格，其中包含每個 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)中所執行之使用者模式函數的指標。

將 SSP/AP 載入至用戶端或伺服器進程之後， (LSA) 的「 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) 」會將 [**SpInitLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) 或 [**SpAcceptLsaModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn)) 所傳回的安全性內容 (資訊，以及任何其他與內容相關的資料複製到處理程式，並呼叫安全性封裝的 [**SpInitUserModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitusermodecontextfn) 函式。

用戶端/伺服器應用程式會藉由呼叫 (SSPI) 函式的 [安全性支援提供者介面](sspi.md) 來存取使用者模式功能。 SSPI 函式是由安全性提供者 DLL 使用封裝提供的 [**SECPKG \_ 使用者 \_ \_**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_user_function_table) 函式資料表所對應。



| 函式                                                           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SpCompleteAuthToken**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spcompleteauthtokenfn)                 | 完成驗證權杖。 <br/> 實行 SSPI [**CompleteAuthToken**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) 函式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**SpDeleteCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-kspdeletecontextfn)                         | 刪除 [*安全性內容*](/windows/desktop/SecGloss/s-gly)。<br/> 實行 SSPI [**DeleteSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) 函式。<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| [**SpExportSecurityCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spexportsecuritycontextfn)         | 將安全性內容匯出至另一個進程。<br/> 實行 SSPI [**ExportSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-exportsecuritycontext) 函式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**SpFormatCredentials**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spformatcredentialsfn)                 | 格式化要儲存在使用者物件中的 [*認證*](/windows/desktop/SecGloss/c-gly) 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SpGetCoNtextToken**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spgetcontexttokenfn)                     | 取得要模擬的權杖。<br/> 由 SSPI [**ImpersonateSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) 函式使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**SpImportSecurityCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spimportsecuritycontextfn)         | 從另一個進程匯入安全性內容。<br/> 實行 SSPI [**ImportSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-importsecuritycontexta) 函式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**SpInitUserModeCoNtext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitusermodecontextfn)             | 從封裝的 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 模式內容建立使用者模式 [*安全性內容*](/windows/desktop/SecGloss/s-gly)。<br/>                                                                                                                                                                                                                                                                                                 |
| [**SpInstanceInit**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinstanceinitfn)                           | 初始化 SSP/AP 中的使用者模式安全性封裝。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**SpMakeSignature**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-kspmakesignaturefn)                         | [*根據指定*](/windows/desktop/SecGloss/d-gly)的訊息和 [*安全性內容*](/windows/desktop/SecGloss/s-gly)產生簽章。<br/> 實行 SSPI [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函式。<br/>                                                                                                                                                                                                                                                    |
| [**SpMarshallSupplementalCreds**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spmarshallsupplementalcredsfn) | 將來自公用格式的 [*補充認證*](/windows/desktop/SecGloss/s-gly) 轉換成適合本機程序呼叫的格式。<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| [**SpQueryCoNtextAttributes**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spquerycontextattributesfn)       | 捕獲 [*安全性內容*](/windows/desktop/SecGloss/s-gly)的屬性。<br/> 將 SSPI [**QueryCoNtextAttributes (一般)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) 函式。<br/>                                                                                                                                                                                                                                                                                                                             |
| [**SpSealMessage**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spsealmessagefn)                             | 加密在用戶端與伺服器之間交換的訊息。<br/> 將 SSPI [**EncryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) 函式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SpUnsealMessage**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spunsealmessagefn)                         | 解密先前使用 [**SpSealMessage**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spsealmessagefn) 函式加密的訊息。<br/> 將 SSPI [**DecryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) 函式。<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**SpUserModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spusermodeinitializefn)               | 當 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) / [*驗證套件*](/windows/desktop/SecGloss/a-gly) (SSP/AP) DLL 載入至用戶端/伺服器應用程式的進程空間時呼叫。 此函式會針對 SSP/AP DLL 中的每個 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)，提供 [**SECPKG \_ 使用者 \_ 函數 \_ 資料表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_user_function_table)資料表。<br/> |
| [**SpVerifySignature**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-kspverifysignaturefn)                     | 根據簽章來確認收到的訊息是否正確 [*。*](/windows/desktop/SecGloss/d-gly)<br/> 實行 SSPI [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函式。<br/>                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="lsa-functions-called-by-sspaps"></a>由 SSP/Ap 呼叫的 LSA 函數

[*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 為 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly)驗證套件中部署的 [*安全性套件*](/windows/desktop/SecGloss/s-gly)提供下列功能 / [](/windows/desktop/SecGloss/a-gly) (SSP/ap) 。 這些函式可在 [**lsa SECPKG 函式 \_ \_ \_ 資料表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) 結構中使用，而當 SSP/AP 載入至 LSA 的進程空間時，可以呼叫這些函數。 下列功能可供所有 Ap 使用。



| 函式                                             | 描述                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddCredential**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_add_credential)               | 新增使用者 [*認證*](/windows/desktop/SecGloss/c-gly)。<br/>                         |
| [**AllocateClientBuffer**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer) | 在封裝用戶端的位址空間中配置記憶體。<br/>                                                         |
| [**AllocateLsaHeap**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap)           | 在堆積上配置記憶體。 傳遞回 LSA 的部分資訊應使用此函式進行配置。<br/> |
| [**CopyFromClientBuffer**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_copy_from_client_buffer) | 從用戶端進程的位址空間，將資訊複製到目前進程中的緩衝區。<br/>                    |
| [**CopyToClientBuffer**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_copy_to_client_buffer)     | 從目前進程中的緩衝區將資訊複製到用戶端進程的位址空間。<br/>                         |
| [**CreateLogonSession**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_create_logon_session)     | 建立登入會話。<br/>                                                                                                |
| [**DeleteCredential**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_delete_credential)         | 刪除使用者認證。<br/>                                                                                              |
| [**DeleteLogonSession**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_delete_logon_session)     | 刪除 LSA 登入會話。<br/>                                                                                          |
| [**FreeClientBuffer**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_free_client_buffer)         | 釋出套件用戶端位址空間中的記憶體。<br/>                                                             |
| [**FreeLsaHeap**](/windows/win32/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap)                   | 解除配置先前由 [**AllocateLsaHeap**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap)配置的堆積記憶體。<br/>                            |
| [**GetCredentials**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_get_credentials)             | 捕獲與登入會話相關聯的認證。<br/>                                                                 |



 

下列函式適用于 SSP/Ap。



| 函式                                                 | 描述                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateSharedMemory**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_allocate_shared_memory)     | 配置共用記憶體的區段。<br/>                                                                                                                                                                                                                                                                                                                   |
| [**AuditAccountLogon**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_audit_account_logon)           | 建立嘗試登入的審核記錄。<br/>                                                                                                                                                                                                                                                                                                             |
| [**AuditLogon**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_audit_logon)                         | 建立登入會話的審核記錄。<br/>                                                                                                                                                                                                                                                                                                             |
| [**CallPackage**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_call_package)                       | 呼叫封裝。<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**CallPackageEx**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_call_packageex)                   | 呼叫另一個套件。<br/>                                                                                                                                                                                                                                                                                                                                  |
| [**CallPackagePassthrough**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_call_package_passthrough) | 呼叫另一個安全性封裝。<br/>                                                                                                                                                                                                                                                                                                                |
| [**CancelNotification**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_cancel_notification)         | 取消特殊事件的通知。<br/>                                                                                                                                                                                                                                                                                                                |
| [**ClientCallback**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_client_callback)                 | 允許安全性封裝在用戶端進程中叫用函數。<br/> 如需 [**ClientCallback**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_client_callback) 函式原型，請參閱 ClientCallback 函式 [*原型*](/previous-versions/windows/desktop/legacy/aa374759(v=vs.85))。<br/>                                                                                                              |
| [**CloseSamUser**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_close_sam_user)                     | 關閉安全性帳戶管理員資料庫專案的控制碼。<br/>                                                                                                                                                                                                                                                                                          |
| [**ConvertAuthDataToToken**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_convert_auth_data_to_token) | 將授權資料轉換為使用者權杖。<br/>                                                                                                                                                                                                                                                                                                            |
| [**CrackSingleName**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_crack_single_name)               | 將名稱從一種格式轉換成另一種格式。<br/>                                                                                                                                                                                                                                                                                                             |
| [**CreateSharedMemory**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_create_shared_memory)         | 建立用戶端與 SSP/AP 之間共用的記憶體區段。<br/>                                                                                                                                                                                                                                                                                      |
| [**CreateThread**](/windows/win32/api/ntsecpkg/nc-ntsecpkg-lsa_create_thread)                     | 建立新的執行緒。<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**CreateToken**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_create_token)                       | 建立權杖。<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**DeleteSharedMemory**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_delete_shared_memory)         | 刪除共用記憶體的區段。<br/>                                                                                                                                                                                                                                                                                                                     |
| [**DuplicateHandle**](/windows/win32/api/ntsecpkg/nc-ntsecpkg-lsa_duplicate_handle)               | 複製控制碼。<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**FreeReturnBuffer**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_free_lsa_heap)             | 釋放 LSA 所配置的緩衝區。<br/>                                                                                                                                                                                                                                                                                                                    |
| [**FreeSharedMemory**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_free_shared_memory)             | 釋出共用記憶體的區段。<br/>                                                                                                                                                                                                                                                                                                                       |
| [**GetAuthDataForUser**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_get_auth_data_for_user)         | 捕獲使用者帳戶的授權資料。<br/>                                                                                                                                                                                                                                                                                                        |
| [**GetCallInfo**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_get_call_info)                       | 抓取最近函式呼叫的相關資訊。<br/>                                                                                                                                                                                                                                                                                              |
| [**GetClientInfo**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_get_client_info)                   | 抓取有關安全性封裝之使用者進程的資訊。<br/>                                                                                                                                                                                                                                                                                        |
| [**GetUserAuthData**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_get_user_auth_data)               | 傳回使用者的授權資料。<br/>                                                                                                                                                                                                                                                                                                              |
| **GetUserCredentials**                                   | 尚未實作。                                                                                                                                                                                                                                                                                                                                               |
| [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85))           | 由 [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 呼叫以模擬封裝使用者。<br/>                                                                                                                                                                                                          |
| [**MapBuffer**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_map_buffer)                           | 將 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)結構對應到 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) / [*驗證套件*](/windows/desktop/SecGloss/a-gly)的位址空間 (SSP/AP) 。<br/>              |
| [**OpenSamUser**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_open_sam_user)                       | 在 (SAM) 資料庫的 [*安全性帳戶管理員*](/windows/desktop/SecGloss/s-gly) 中，抓取使用者帳戶的控制碼。<br/>                                                                                                                                                               |
| [**RegisterNotification**](/windows/win32/api/ntsecpkg/nc-ntsecpkg-lsa_register_notification)     | 提供 [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 通知的機制。 通知可能會在固定間隔、事件物件已收到信號，或在特定系統事件期間發生。<br/>                                                                                          |
| **SaveSupplementalCredentials**                          | 已過時。 請勿使用。<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**UnloadPackage**](/previous-versions/windows/desktop/legacy/aa380520(v=vs.85))                   |  (SSP/AP) 卸載 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) / [*驗證套件*](/windows/desktop/SecGloss/a-gly)。<br/>                                                                                 |
| [**UpdateCredentials**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_update_primary_credentials)           | 提供一種機制，讓一個 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)通知其他套件，登入 [*會話*](/windows/desktop/SecGloss/s-gly)的 [*認證*](/windows/desktop/SecGloss/c-gly)已變更。<br/> |



 

## <a name="lsa-functions-called-by-user-mode-sspaps"></a>使用者模式 SSP/Ap 所呼叫的 LSA 函數

[*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) [](/windows/desktop/SecGloss/s-gly) / [*驗證封裝*](/windows/desktop/SecGloss/a-gly) (SSP/AP) 在使用者模式進程中執行的安全性封裝，可以使用 [**SECPKG \_ DLL \_**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_dll_functions)函式資料表中的指標來存取下列函式。



| 函式                                     | PSDK 狀態                                                                                                                                                                                        |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85))         | 為傳回到 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 的緩衝區配置記憶體。<br/> |
| [**FreeHeap**](/previous-versions/windows/desktop/legacy/aa375418(v=vs.85))                 | 釋放先前使用 [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85))配置的記憶體。<br/>                                                                                               |
| [**RegisterCallback**](/previous-versions/windows/desktop/legacy/aa379372(v=vs.85)) | 註冊使用者模式回呼函數。<br/>                                                                                                                                                 |



 

## <a name="gina-export-functions"></a>GINA 匯出函數

[*GINA*](/windows/desktop/SecGloss/g-gly) DLL 必須匯出下列函數。

> [!Note]  
> 在 Windows Vista 中會忽略 GINA Dll。

 



| 函式                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WlxActivateUserShell**](/windows/desktop/api/Winwlx/nf-winwlx-wlxactivateusershell)                     | 啟用使用者 shell 程式。<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**WlxDisplayLockedNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice)                 | 允許 GINA 顯示鎖定的相關資訊，例如鎖定工作站的人員以及鎖定的時間。<br/>                                                                                                                                                                                                                                                                    |
| [**WlxDisplaySASNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaysasnotice)                       | 當沒有使用者登入時， [*Winlogon*](/windows/desktop/SecGloss/w-gly)會呼叫此函式。<br/>                                                                                                                                                                                                                                                            |
| [**WlxDisplayStatusMessage**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaystatusmessage)               | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 會在 GINA DLL 應顯示訊息時呼叫此函式。<br/>                                                                                                                                                                                                                                           |
| [**WlxGetConsoleSwitchCredentials**](/windows/desktop/api/Winwlx/nf-winwlx-wlxgetconsoleswitchcredentials) | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 會呼叫此函式來讀取目前登入的使用者認證，以明確地將其傳送至目標會話。<br/>                                                                                                                                                                                |
| [**WlxGetStatusMessage**](/windows/desktop/api/Winwlx/nf-winwlx-wlxgetstatusmessage)                       | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 會呼叫此函式，以取得 GINA DLL 所顯示的狀態訊息。<br/>                                                                                                                                                                                                                            |
| [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize)                                   | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 會針對電腦上的每個視窗站呼叫此函式一次。 目前，作業系統支援每個工作站一個視窗工作站。<br/>                                                                                                                                                    |
| [**WlxIsLockOk**](/windows/desktop/api/Winwlx/nf-winwlx-wlxislockok)                                       | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 在嘗試鎖定工作站之前，會呼叫此函式。<br/>                                                                                                                                                                                                                                            |
| [**WlxIsLogoffOk**](/windows/desktop/api/Winwlx/nf-winwlx-wlxislogoffok)                                   | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 會在使用者起始登出作業時呼叫此函式。<br/>                                                                                                                                                                                                                                           |
| [**WlxLoggedOnSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas)                                 | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 會在使用者登入時收到 [*安全的注意順序*](/windows/desktop/SecGloss/s-gly) ， (SAS) 事件，而且工作站未鎖定。<br/>                                                           |
| [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)                               | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 在沒有使用者登入時，收到 (SAS) 事件的 [*安全注意順序*](/windows/desktop/SecGloss/s-gly) 時，就會呼叫此函式。<br/>                                                                                              |
| [**WlxLogoff**](/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff)                                           | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 會呼叫此函式來通知 GINA 此工作站上的登出操作，讓 GINA 能夠執行任何可能需要的登出作業。<br/>                                                                                                                                                |
| [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate)                                     | [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate)函式必須由取代 [*GINA*](/windows/desktop/SecGloss/g-gly) DLL 來執行。 這是 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 對 GINA DLL 進行的第一個呼叫。 **WlxNegotiate** 可讓 GINA 確認它是否支援已安裝的 Winlogon 版本。<br/> |
| [**WlxNetworkProviderLoad**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnetworkproviderload)                 | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 會呼叫此函式來收集有效的驗證和識別資訊。<br/>                                                                                                                                                                                                                       |
| [**WlxRemoveStatusMessage**](/windows/desktop/api/Winwlx/nf-winwlx-wlxremovestatusmessage)                 | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 會呼叫此函式，告知 GINA DLL 停止顯示狀態訊息。<br/>                                                                                                                                                                                                                           |
| [**WlxScreenSaverNotify**](/windows/desktop/api/Winwlx/nf-winwlx-wlxscreensavernotify)                     | [*Winlogon*](/windows/desktop/SecGloss/w-gly) 會在啟用螢幕保護裝置之前立即呼叫此函式，讓 GINA 能夠與螢幕保護裝置程式互動。<br/>                                                                                                                                                                          |
| [**WlxShutdown**](/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown)                                       | [*Winlogon*](/windows/desktop/SecGloss/w-gly)會在關機之前呼叫這個函式，讓 GINA 能夠執行任何關機工作，例如從 [*讀取器*](/windows/desktop/SecGloss/r-gly)中退出 [*智慧卡*](/windows/desktop/SecGloss/s-gly)。<br/>                          |
| [**WlxStartApplication**](/windows/desktop/api/Winwlx/nf-winwlx-wlxstartapplication)                       | 當系統需要在使用者的 [*內容*](/windows/desktop/SecGloss/c-gly)中啟動應用程式時， [*Winlogon*](/windows/desktop/SecGloss/w-gly)會呼叫此函式。<br/>                                                                                                                                        |
| [**WlxWkstaLockedSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas)                           | 當 [*Winlogon*](/windows/desktop/SecGloss/w-gly)收到 (SAS) 的 [*安全注意順序*](/windows/desktop/SecGloss/s-gly)，而且工作站已被鎖定時，就會呼叫此函式。<br/>                                                                                                 |



 

## <a name="logon-user-functions"></a>登入使用者功能

下列函數提供登入使用者的能力。



| 函式                                 | 描述                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LogonUser**](/windows/desktop/api/Winbase/nf-winbase-logonusera)           | 嘗試將使用者登入本機電腦。<br/>                                                                                                                                                                                                                                                                                                |
| [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)       | 嘗試將使用者登入本機電腦。 此函式是安全機制函式 [**的延伸**](/windows/desktop/api/Winbase/nf-winbase-logonusera) 版本，可抓取已登入使用者的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) 的相關資訊 (SID) 、設定檔和配額限制。<br/>         |
| [**LogonUserExExW**](logonuserexexw.md) | [**LogonUserExExW**](logonuserexexw.md)函式會嘗試將使用者登入本機電腦。 此函式未在公用標頭中宣告，且沒有相關聯的匯入程式庫。 您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Advapi32.dll。<br/> |



 

## <a name="winlogon-support-functions"></a>Winlogon 支援函式

[*GINA*](/windows/desktop/SecGloss/g-gly) Dll 可以呼叫下列 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 支援函式。

> [!Note]  
> 在 Windows Vista 中會忽略 GINA Dll。

 



| 函式                                                                     | 由 GINA 呼叫                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WlxAssignShellProtection**](/windows/win32/api/winwlx/nc-winwlx-pwlx_assign_shell_protection)                 | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫，以將保護指派給新登入之使用者的 shell 程式。<br/>                                                                                                                                                                                                                                                                    |
| [**WlxChangePasswordNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_change_password_notify)                   | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫，以指出它已變更密碼。<br/>                                                                                                                                                                                                                                                                                                  |
| [**WlxChangePasswordNotifyEx**](/windows/win32/api/winwlx/nc-winwlx-pwlx_change_password_notify_ex)               | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫，以告知特定的網路提供者 (或所有網路提供者) 密碼已變更。<br/>                                                                                                                                                                                                                                             |
| [**WlxCloseUserDesktop**](/windows/win32/api/winwlx/nc-winwlx-pwlx_close_user_desktop)                           | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫以關閉替代使用者桌面，並在關閉桌面之後進行清除。<br/>                                                                                                                                                                                                                                                            |
| [**WlxCreateUserDesktop**](/windows/win32/api/winwlx/nc-winwlx-pwlx_create_user_desktop)                         | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫，為使用者建立替代的應用程式桌面。<br/>                                                                                                                                                                                                                                                                                  |
| [**WlxDialogBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                                         | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫，以從對話方塊範本建立強制回應對話方塊。<br/>                                                                                                                                                                                                                                                                            |
| [**WlxDialogBoxIndirect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)                         | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫，可從記憶體中的對話方塊範本建立強制回應對話方塊。<br/>                                                                                                                                                                                                                                                                      |
| [**WlxDialogBoxIndirectParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param)               | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫以初始化對話方塊控制項，然後從記憶體中的對話方塊範本建立強制回應對話方塊。<br/>                                                                                                                                                                                                                              |
| [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                               | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫以初始化對話方塊控制項，然後從對話方塊範本資源建立強制回應對話方塊。<br/>                                                                                                                                                                                                                               |
| [**WlxDisconnect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | 如果已啟用終端機服務，則由取代 GINA DLL 呼叫。 [*GINA*](/windows/desktop/SecGloss/g-gly) 會呼叫此函式，以中斷與終端機服務網路會話的連線。<br/>                                                                                                                                                                                                     |
| [**WlxGetOption**](/windows/win32/api/winwlx/nc-winwlx-pwlx_get_option)                                         | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫以取出選項的目前值。<br/>                                                                                                                                                                                                                                                                                             |
| [**WlxGetSourceDesktop**](/windows/win32/api/winwlx/nc-winwlx-pwlx_get_source_desktop)                           | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫，以判斷在 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 切換至 winlogon 桌面之前，目前的桌面名稱和控制碼。<br/>                                                                                                                                                    |
| [**WlxMessageBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                                       | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫以建立、顯示及操作訊息方塊。<br/>                                                                                                                                                                                                                                                                                          |
| [**WlxQueryClientCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | 如果已啟用終端機服務，則由取代 GINA DLL 呼叫。 GINA 會呼叫此函式，以抓取未使用網際網路連接器授權之遠端終端機機服務用戶端的認證。<br/>                                                                                                                                                                                                     |
| [**WlxQueryConsoleSwitchCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_consoleswitch_credentials) | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫，以讀取從暫時會話的 winlogon 傳送至目的地會話之 winlogon 的認證。<br/>                                                                                                                                                                                                              |
| [**WlxQueryInetConnectorCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | 如果已啟用終端機服務，則由取代 GINA DLL 呼叫。 [*GINA*](/windows/desktop/SecGloss/g-gly) 會呼叫此函式，以判斷終端機伺服器是否使用網際網路連接器授權和取得 [*認證*](/windows/desktop/SecGloss/c-gly) 資訊。<br/>                                                             |
| [**WlxQueryTerminalServicesData**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫，以在使用者登入之後取得終端機服務使用者設定資訊。<br/>                                                                                                                                                                                                                                                |
| [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify)                                         | 由 [*GINA*](/windows/desktop/SecGloss/g-gly)呼叫，以將安全的 [*注意順序*](/windows/desktop/SecGloss/s-gly)告知 [*Winlogon*](/windows/desktop/SecGloss/w-gly) (SAS) 事件。<br/>                                                                                                    |
| [**WlxSetCoNtextPointer**](/windows/win32/api/winwlx/nc-winwlx-pwlx_set_context_pointer)                         | 由 [*GINA*](/windows/desktop/SecGloss/g-gly)呼叫，以指定由 [*Winlogon*](/windows/desktop/SecGloss/w-gly)傳遞的 [*內容*](/windows/desktop/SecGloss/c-gly)指標，做為 GINA 函式所有未來呼叫的第一個參數。<br/>                                                                                       |
| [**WlxSetOption**](/windows/win32/api/winwlx/nc-winwlx-pwlx_set_option)                                         | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫以設定選項的值。<br/>                                                                                                                                                                                                                                                                                                          |
| [**WlxSetReturnDesktop**](/windows/win32/api/winwlx/nc-winwlx-pwlx_set_return_desktop)                           | 由 [*GINA*](/windows/desktop/SecGloss/g-gly)呼叫，以指定當目前的 [*安全注意順序*](/windows/desktop/SecGloss/s-gly) (SAS) 事件處理函式完成時， [*Winlogon*](/windows/desktop/SecGloss/w-gly)將切換至的替代應用程式桌面。<br/> |
| [**WlxSetTimeout**](/windows/win32/api/winwlx/nc-winwlx-pwlx_set_timeout)                                       | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫以變更與對話方塊相關聯的超時時間。 預設的超時時間是兩分鐘。<br/>                                                                                                                                                                                                                                               |
| [**WlxSwitchDesktopToUser**](/windows/win32/api/winwlx/nc-winwlx-pwlx_switch_desktop_to_user)                     | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫以切換至應用程式桌面。<br/>                                                                                                                                                                                                                                                                                                   |
| [**WlxSwitchDesktopToWinlogon**](/windows/win32/api/winwlx/nc-winwlx-pwlx_switch_desktop_to_winlogon)             | 允許 [*GINA*](/windows/desktop/SecGloss/g-gly) DLL 切換至 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 桌面。<br/>                                                                                                                                                                                                                                  |
| [**WlxUseCtrlAltDel**](/windows/win32/api/winwlx/nc-winwlx-pwlx_use_ctrl_alt_del)                                 | 由 [*GINA*](/windows/desktop/SecGloss/g-gly) 呼叫，以告知 [*WINLOGON*](/windows/desktop/SecGloss/w-gly) 使用標準 CTRL + ALT + DEL 按鍵組合，以安全的方式 (SAS) 的 [*順序*](/windows/desktop/SecGloss/s-gly) 。<br/>                                                           |
| [**WlxWin31Migrate**](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | 如果已啟用終端機服務，則由取代 GINA DLL 呼叫。 [*GINA*](/windows/desktop/SecGloss/g-gly) 會呼叫此函式來完成終端機服務用戶端的設定。<br/>                                                                                                                                                                                                      |



 

## <a name="network-provider-functions"></a>網路提供者函式

下列主題提供網路提供者功能的參考資訊。



| 主題                                      | 描述                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 網路提供者所執行的函式 | 詳細說明可由網路提供者執行的函數。<br/>                                                                                                                                                                                                                          |
| 支援函式                          | 詳述作業系統所執行的函式，而且可以由網路提供者呼叫。<br/>                                                                                                                                                                                   |
| 連接通知函數          | 詳細說明當網路資源已連線或中斷連線時，需要從 [*多個提供者路由器*](/windows/desktop/SecGloss/m-gly) 接收通知的應用程式所執行的功能 (MPR) 。<br/> |



 

### <a name="functions-implemented-by-network-providers"></a>網路提供者所執行的函式

下列函式可由網路提供者來執行。 網路提供者必須支援的唯一功能是 [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps)。



| 函式                                                         | 描述                                                                                                                                                                                                           |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | 將本機裝置連接到網路資源。<br/>                                                                                                                                                             |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | 將本機裝置連接到網路資源。<br/>                                                                                                                                                             |
| [**NPCancelConnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | 中斷網路連接。<br/>                                                                                                                                                                          |
| [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                               | 關閉列舉。<br/>                                                                                                                                                                                     |
| [**NPDeviceMode**](/windows/desktop/api/Npapi/nf-npapi-npdevicemode)                             | 指定裝置的父視窗。 此視窗擁有源自裝置的任何對話方塊。<br/>                                                                                                 |
| [**NPDirectoryNotify**](/windows/desktop/api/Npapi/nf-npapi-npdirectorynotify)                   | 通知網路提供者有某些目錄作業。<br/>                                                                                                                                             |
| [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                         | 根據 [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)所傳回的控制碼來執行列舉。<br/>                                                                                                                    |
| [**NPFormatNetworkName**](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname)               | 以提供者特定的格式來格式化網路名稱，以在控制項中顯示。<br/>                                                                                                                             |
| [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps)                                   | 傳回網路上支援哪些服務的相關資訊。<br/>                                                                                                                                     |
| [**NPGetConnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | 擷取連線的相關資訊。<br/>                                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | 抓取網路連接的相關資訊（即使目前已中斷連線）。<br/>                                                                                                                    |
| [**NPGetConnectionPerformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | 傳回用來存取網路資源之連接的預期效能相關資訊。 要求只能針對目前已連線的網路資源。<br/>                          |
| [**NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype)                 | 決定網路目錄的類型。<br/>                                                                                                                                                                |
| [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)                   | 抓取要加入至網路資源之屬性對話方塊的按鈕名稱。<br/>                                                                                                                     |
| [**NPGetResourceInformation**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation)     | 將透過 WNet API 存取的網路資源部分，與透過資源類型專屬的 Api 存取的部分分開。<br/>                                                                  |
| [**NPGetResourceParent**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)               | 抓取流覽階層中指定之網路資源的父系。<br/>                                                                                                                              |
| [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | 捕獲網路資源的通用名稱。 [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)函式可以採用 UNC 格式或較舊的遠端名稱格式來取得此通用名稱。<br/>      |
| [**NPGetUser**](/windows/desktop/api/Npapi/nf-npapi-npgetuser)                                   | 抓取目前預設使用者名稱的值，或是用來建立網路連接的使用者名稱。<br/>                                                                                              |
| [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                                 | 開啟網路資源或現有連接的列舉。 必須呼叫 [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum) 函式，才能取得列舉的有效控制碼。<br/>                               |
| [**NPPropertyDialog**](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)                     | 當使用者按一下使用 [**NPPropertyDialog**](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog) 函式加入的按鈕時呼叫。 **NPPropertyDialog** 函式只會針對檔案和目錄網路屬性進行呼叫。<br/> |
| [**NPSearchDialog**](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)                         | 除了在 [ **連接** ] 對話方塊中顯示的階層式視圖之外，還可讓網路廠商提供自己的流覽和搜尋形式。<br/>                                                          |



 

### <a name="support-functions"></a>支援函式

下列函式是由作業系統所執行，而且可以由網路提供者呼叫。



| 函式                                     | 描述                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) | 設定延伸錯誤資訊。 網路提供者應該呼叫此函式，而不是 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror)。<br/> |



 

### <a name="connection-notification-functions"></a>連接通知函數

當網路資源已連線或中斷連線時，應用程式會執行下列功能，這些應用程式需要接收來自 [*多個提供者路由器*](/windows/desktop/SecGloss/m-gly) 的通知 (MPR) 。 如需有關如何撰寫接收這類通知的應用程式的詳細資訊，請參閱 [接收連接通知](receiving-connection-notifications.md)。



| 函式                                           | 描述                                                                                                                                                                                                                   |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify)       | 在每個加入連接作業之前和之後呼叫 ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona)、 [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)和 [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) 。<br/> |
| [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) | 在每個取消連接作業之前和之後呼叫 ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) 或 [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)) 。<br/>                                       |



 

## <a name="lsa-logon-functions"></a>LSA 登入功能

下列 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 驗證函式會驗證和登入使用者，並提供登入會話資訊。



| 函式                                                                   | 描述                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)       | 從驗證套件要求封裝特定的服務。<br/>                                                                                                                                                                        |
| [**LsaConnectUntrusted**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaconnectuntrusted)                         | 建立與 LSA 不受信任的連接。<br/>                                                                                                                                                                                            |
| [**LsaDeregisterLogonProcess**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaderegisterlogonprocess)             | 中斷與 LSA 的連線，並釋放配置給呼叫端內容的資源。<br/>                                                                                                                                                            |
| [**LsaEnumerateLogonSessions**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratelogonsessions)             | 針對現有的登入會話， (Luid) 抓取 [*本機唯一識別碼*](/windows/desktop/SecGloss/l-gly) 。<br/>                                                              |
| [**LsaFreeReturnBuffer**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsafreereturnbuffer)                         | 釋出針對傳回給呼叫者的緩衝區所配置的記憶體。<br/>                                                                                                                                                                                  |
| [**LsaGetLogonSessionData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsagetlogonsessiondata)                   | 抓取指定之登入會話的相關資訊。<br/>                                                                                                                                                                                     |
| [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser)                                       | 針對預存認證驗證使用者登入資料。 如果成功，它會建立新的登入會話，並傳回使用者權杖。<br/>                                                                                                          |
| [**LsaLookupAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupauthenticationpackage)   | 取得驗證套件的唯一識別碼。<br/>                                                                                                                                                                                |
| [**LsaQueryDomainInformationPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerydomaininformationpolicy) | 從 [**Policy**](/windows/desktop/SecMgmt/policy-object) 物件中取出網域資訊。<br/>                                                                                                                                                         |
| [**LsaQueryForestTrustInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaqueryforesttrustinformation)   | 抓取指定之「 [*本地安全機構*](/windows/desktop/SecGloss/l-gly)」 [**TrustedDomain**](/windows/desktop/SecMgmt/trusteddomain-object) 物件的樹系信任資訊。<br/> |
| [**LsaRegisterLogonProcess**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterlogonprocess)                 | 建立與 LSA 伺服器的連接，並確認呼叫端是否為登入應用程式。<br/>                                                                                                                                            |
| [**LsaSetDomainInformationPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasetdomaininformationpolicy)     | 將網域資訊設定為 [**原則**](/windows/desktop/SecMgmt/policy-object) 物件。<br/>                                                                                                                                                                |
| [**LsaSetForestTrustInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasetforesttrustinformation)       | 為指定的「 [*本地安全機構*](/windows/desktop/SecGloss/l-gly)」 [**TrustedDomain**](/windows/desktop/SecMgmt/trusteddomain-object) 物件設定樹系信任資訊。<br/>    |



 

## <a name="functions-implemented-by-authentication-packages"></a>由驗證封裝所執行的函式

自訂驗證套件必須執行這些函式，這些函式是由 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 所呼叫。 這些函式是由 Microsoft 所 \_ 提供的 MSV1 0 和 Kerberos 驗證套件所執行。



| 函式                                                           | 描述                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LsaApCallPackage**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_call_package)                       | 當使用信任連接的應用程式在對 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) 的呼叫中指定了驗證套件的識別碼時呼叫。<br/> 此函式提供登入應用程式直接與驗證套件進行通訊的方法。<br/>                         |
| [**LsaApCallPackagePassthrough**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_call_package_passthrough) | 在傳遞登入要求的 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) 呼叫中指定驗證套件的識別碼時呼叫。<br/>                                                                                                                                                                  |
| [**LsaApCallPackageUntrusted**](/previous-versions/windows/desktop/legacy/aa378218(v=vs.85))     | 當應用程式使用未受信任的連接時，在對 [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) 的呼叫中指定了驗證套件的識別碼時呼叫。 這個函式是用來與沒有 SeTcbPrivilege 許可權的進程進行通訊。<br/>                                             |
| [**LsaApInitializePackage**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_initialize_package)           | 在系統初始化期間呼叫，以允許驗證封裝執行初始化工作。<br/>                                                                                                                                                                                                                                                   |
| [**LsaApLogonTerminated**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_terminated)               | 當登入會話結束時呼叫，以允許驗證套件釋放為登入會話配置的任何資源。<br/>                                                                                                                                                                                                                                |
| [**LsaApLogonUser**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user)                           | 在 [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser)的呼叫中指定驗證封裝時呼叫。 此函數會驗證 [*安全性主體的*](/windows/desktop/SecGloss/s-gly) 登入資料。<br/>                                                                                           |
| [**LsaApLogonUserEx**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex)                       | 與 [**LsaApLogonUser**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user) 相同，不同之處在于它會傳回用於進行審核的工作站名稱。<br/> 驗證套件可以執行 [**LsaApLogonUser**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user)、 [**LsaApLogonUserEx**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex)或 [**LsaApLogonUserEx2**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex2)。 它不需要全部執行。<br/> |
| [**LsaApLogonUserEx2**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex2)                     | 與 [**LsaApLogonUserEx**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex) 相同，不同之處在于它會傳回安全性主體的主要和補充認證。 驗證套件可以執行 [**LsaApLogonUser**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user)、 **LsaApLogonUserEx** 或 [**LsaApLogonUserEx2**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex2)。 它不需要全部執行。<br/>          |



 

## <a name="lsa-functions-called-by-authentication-packages"></a>由驗證套件呼叫的 LSA 函數

您可以從自訂驗證套件呼叫下列 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 函數。 當 LSA 呼叫 [**LsaApInitializePackage**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_ap_initialize_package) 來初始化封裝時，它會傳遞支援函數的資料表。



| 函式                                             | 描述                                                                                                                   |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**AddCredential**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_add_credential)               | 將認證新增至登入會話。<br/>                                                                               |
| [**AllocateClientBuffer**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer) | 配置用戶端位址空間中的緩衝區。<br/>                                                                  |
| [**AllocateLsaHeap**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap)           | 配置必須從驗證封裝傳回至 LSA 的緩衝區。<br/>                                |
| [**CopyFromClientBuffer**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_copy_from_client_buffer) | 將用戶端位址空間中緩衝區的內容複寫到本機緩衝區。<br/>                                 |
| [**CopyToClientBuffer**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_copy_to_client_buffer)     | 將本機緩衝區的內容複寫到用戶端的位址空間。<br/>                                             |
| [**CreateLogonSession**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_create_logon_session)     | 由驗證套件用來建立登入會話。<br/>                                                         |
| [**DeleteCredential**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_delete_credential)         | 刪除現有的認證。<br/>                                                                                    |
| [**DeleteLogonSession**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_delete_logon_session)     | 清除在判斷使用者的驗證資訊是否合法時，所建立的任何登入會話。<br/>  |
| [**FreeClientBuffer**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_free_client_buffer)         | 釋放先前使用 [**AllocateClientBuffer**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_allocate_client_buffer) 函數配置的用戶端緩衝區。<br/> |
| [**FreeLsaHeap**](/windows/win32/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap)                   | 釋放先前使用 [**AllocateLsaHeap**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_allocate_lsa_heap) 函數配置的緩衝區。<br/>               |
| [**GetCredentials**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_get_credentials)             | 抓取 [**AddCredential**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-lsa_add_credential)先前快取的認證。<br/>                                 |



 

## <a name="subauthentication-functions"></a>子驗證函式

您可以透過 Microsoft 提供的驗證套件呼叫下列子驗證函式，以提供其他使用者建立的登入驗證。



| 函式                                                                  | 描述                                                                           |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Msv1 \_ 0SubAuthenticationFilter**](/windows/desktop/api/Subauth/nf-subauth-msv1_0subauthenticationfilter)   | 執行網域控制站專用的使用者登入驗證。<br/> |
| [**Msv1 \_ 0SubAuthenticationRoutine**](/windows/desktop/api/Subauth/nf-subauth-msv1_0subauthenticationroutine) | 執行用戶端/伺服器特定的驗證。<br/>                            |



 

## <a name="credentials-management-functions"></a>認證管理功能

下列主題提供認證管理功能的參考資訊。



| 主題                                        | 描述                                                                                                                                |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| 認證管理 UI 函數          | 用於認證管理 UI 的詳細資料函數。<br/>                                                                           |
| 低層級認證管理功能   | 用於低層級認證管理的詳細資料功能。<br/>                                                                    |
| 認證管理通知函式 | 詳細說明認證管理員所執行的函式，以便在驗證資訊變更時接收通知。<br/> |



 

### <a name="credentials-management-ui-functions"></a>認證管理 UI 函數

以下是認證管理 UI 函數。



| 函式                                                                       | 描述                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CredUICmdLinePromptForCredentials**](/windows/desktop/api/WinCred/nf-wincred-creduicmdlinepromptforcredentialsa) | 提示輸入，並接受使用者在命令列程式中工作的使用者認證資訊。<br/>                                                                                                   |
| [**CredUIConfirmCredentials**](/windows/desktop/api/WinCred/nf-wincred-creduiconfirmcredentialsa)                   | 確認 [**CredUIPromptForCredentials**](/windows/desktop/api/WinCred/nf-wincred-creduipromptforcredentialsa) 或 [**CredUICmdLinePromptForCredentials**](/windows/desktop/api/WinCred/nf-wincred-creduicmdlinepromptforcredentialsa)傳回的認證有效性。<br/> |
| [**CredUIParseUserName**](/windows/desktop/api/WinCred/nf-wincred-creduiparseusernamea)                             | 從完整的使用者名稱中解壓縮網域和使用者帳戶名稱。<br/>                                                                                                                          |
| [**CredUIPromptForCredentials**](/windows/desktop/api/WinCred/nf-wincred-creduipromptforcredentialsa)               | 顯示接受使用者認證資訊的對話方塊。<br/>                                                                                                                              |
| [**CredUIPromptForWindowsCredentials**](/windows/desktop/api/WinCred/nf-wincred-creduipromptforwindowscredentialsa) | 建立並顯示可設定的對話方塊，可讓使用者使用安裝在本機電腦上的任何認證提供者來提供認證資訊。<br/>                                 |
| [**CredUIReadSSOCredW**](/windows/desktop/api/WinCred/nf-wincred-creduireadssocredw)                               | 抓取單一登入認證的使用者名稱。<br/>                                                                                                                                              |
| [**CredUIStoreSSOCredW**](/windows/desktop/api/WinCred/nf-wincred-creduistoressocredw)                             | 儲存單一登入認證。<br/>                                                                                                                                                                   |



 

### <a name="low-level-credentials-management-functions"></a>低層級認證管理功能

以下是低層級的認證管理功能。



| 函式                                                                 | 描述                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CredDelete**](/windows/desktop/api/WinCred/nf-wincred-creddeletea)                                         | 從使用者的認證集刪除認證。<br/>                                                                                                                                                                            |
| [**CredEnumerate**](/windows/desktop/api/WinCred/nf-wincred-credenumeratea)                                   | 列出使用者認證集中的認證。<br/>                                                                                                                                                                             |
| [**CredFindBestCredential**](/windows/desktop/api/WinCred/nf-wincred-credfindbestcredentiala)                 | 搜尋 [認證管理](credentials-management.md) (CredMan) 資料庫，尋找與目前登入會話相關聯，且最符合指定目標資源的一般認證集。<br/> |
| [**CredFree**](/windows/desktop/api/WinCred/nf-wincred-credfree)                                             | 釋放用於任何認證管理功能所傳回之緩衝區的記憶體。<br/>                                                                                                                                    |
| [**CredGetSessionTypes**](/windows/desktop/api/WinCred/nf-wincred-credgetsessiontypes)                       | 取得目前登入會話所支援的最大持續性。<br/>                                                                                                                                                      |
| [**CredGetTargetInfo**](/windows/desktop/api/WinCred/nf-wincred-credgettargetinfoa)                           | 取得命名資源的所有已知目標名稱資訊。<br/>                                                                                                                                                              |
| [**CredIsMarshaledCredential**](/windows/desktop/api/WinCred/nf-wincred-credismarshaledcredentiala)           | 判斷指定的使用者名稱字串是否為先前由 [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala)封送處理的封送認證。<br/>                                                                     |
| [**CredIsProtected**](/windows/desktop/api/WinCred/nf-wincred-credisprotecteda)                               | 指定指定的認證是否由先前對 [**CredProtect**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) 函式的呼叫進行加密。<br/>                                                                                              |
| [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala)                   | 將認證轉換成文字字串。<br/>                                                                                                                                                                                    |
| [**CredPackAuthenticationBuffer**](/windows/desktop/api/WinCred/nf-wincred-credpackauthenticationbuffera)     | 將字串使用者名稱和密碼轉換成驗證緩衝區。<br/>                                                                                                                                                       |
| [**CredProtect**](/windows/desktop/api/WinCred/nf-wincred-credprotecta)                                       | 加密指定的認證，如此一來，只有目前的安全性內容才能將其解密。<br/>                                                                                                                                |
| [**CredRead**](/windows/desktop/api/WinCred/nf-wincred-credreada)                                             | 從使用者的認證集讀取認證。<br/>                                                                                                                                                                              |
| [**CredReadDomainCredentials**](/windows/desktop/api/WinCred/nf-wincred-credreaddomaincredentialsa)           | 從使用者的認證集讀取網域認證。<br/>                                                                                                                                                                    |
| [**CredRename**](/windows/desktop/api/WinCred/nf-wincred-credrenamea)                                         | 從使用者的認證集重新命名認證。<br/>                                                                                                                                                                            |
| [**CredUnmarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala)               | 將封送處理的認證字串轉換回其 nonmarshaled 形式。<br/>                                                                                                                                                      |
| [**CredUnPackAuthenticationBuffer**](/windows/desktop/api/WinCred/nf-wincred-credunpackauthenticationbuffera) | 將呼叫 [**CredUIPromptForWindowsCredentials**](/windows/desktop/api/WinCred/nf-wincred-creduipromptforwindowscredentialsa) 函式所傳回的驗證緩衝區轉換成字串使用者名稱和密碼。<br/>                                     |
| [**CredUnprotect**](/windows/desktop/api/WinCred/nf-wincred-credunprotecta)                                   | 解密先前使用 [**CredProtect**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) 函式加密的認證。<br/>                                                                                                                 |
| [**CredWrite**](/windows/desktop/api/WinCred/nf-wincred-credwritea)                                           | 建立新的認證，或在使用者的認證集內修改現有的認證。<br/>                                                                                                                                         |
| [**CredWriteDomainCredentials**](/windows/desktop/api/WinCred/nf-wincred-credwritedomaincredentialsa)         | 將網域認證寫入至使用者的認證集。<br/>                                                                                                                                                                         |



 

### <a name="credential-management-notification-functions"></a>認證管理通知函式

認證管理員會執行下列函式，以在驗證資訊變更時接收通知。



| 函式                                                 | 描述                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)                   | MPR 會呼叫此函式，以通知認證管理員已發生登入事件，允許認證管理員傳回登入腳本。<br/> |
| [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) | MPR 會呼叫這個函式，以通知認證管理員密碼變更事件。<br/>                                                                |



 

## <a name="smart-card-functions"></a>智慧卡功能

智慧卡 SDK 提供下列功能。



| 函式                                                                             | 描述                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea)                                           | 取代為 [**SCardUIDlgSelectCard**](/windows/desktop/api/Winscard/nf-winscard-scarduidlgselectcarda)，它會顯示智慧卡 **選取卡片** 對話方塊。<br/>                                                                               |
| [**SCardAccessStartedEvent**](/windows/desktop/api/Winscard/nf-winscard-scardaccessstartedevent)                           | 當智慧卡資源管理員的開頭收到信號時，取得事件控制碼。                                                                                                                                 |
| [**SCardAddReaderToGroup**](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)                               | 將 [*讀者*](/windows/desktop/SecGloss/r-gly) 新增至讀者群組。                                                                                                                       |
| [**SCardAudit**](/windows/desktop/api/Winscard/nf-winscard-scardaudit)                                                     | 將事件訊息寫入 Windows 應用程式記錄檔 Microsoft-Windows-智慧卡-Audit/Authentication。                                                                                                               |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction)                               | 啟動 [*交易*](/windows/desktop/SecGloss/t-gly)。                                                                                                                        |
| [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                                                   | 終止 [*內容*](/windows/desktop/SecGloss/c-gly)內所有未完成的動作。                                                                                                 |
| **SCardCancelTransaction**                                                           | 保留供未來使用。                                                                                                                                                                                             |
| [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                                                 | 建立呼叫應用程式與智慧卡之間的連接。                                                                                                                                           |
| [**SCardControl**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)                                                 | 在呼叫 [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) 之後，取得讀取器的直接控制。                                                                                                                              |
| [**SCardDisconnect**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)                                           | 結束通話應用程式與智慧卡之間的連接。                                                                                                                                            |
| [**SCardEndTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)                                   | 完成 [*交易*](/windows/desktop/SecGloss/t-gly)。                                                                                                                     |
| [**SCardEstablishCoNtext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)                               | 建立 [*resource manager 內容*](/windows/desktop/SecGloss/r-gly) 以存取智慧卡資料庫。                                      |
| [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)                                   | 從 [*智慧卡子系統*](/windows/desktop/SecGloss/s-gly)移除先前定義的智慧卡。                                                     |
| [**SCardForgetReader**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                                       | 從智慧卡子系統移除先前定義的讀取器。                                                                                                                                                   |
| [**SCardForgetReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)                             | 從智慧卡子系統移除先前定義的讀者群組。                                                                                                                                             |
| [**SCardFreeMemory**](/windows/desktop/api/Winscard/nf-winscard-scardfreememory)                                           | 釋放資源管理員所配置的記憶體。                                                                                                                                                                       |
| [**SCardGetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib)                                             | 從指定的 [*讀取器*](/windows/desktop/SecGloss/r-gly)、驅動程式或 [*智慧卡*](/windows/desktop/SecGloss/s-gly)取得目前讀取器的屬性。 |
| [**SCardGetCardTypeProviderName**](/windows/desktop/api/Winscard/nf-winscard-scardgetcardtypeprovidernamea)                 | 取得提供者名稱，指定卡片名稱和提供者類型。                                                                                                                                                          |
| [**SCardGetDeviceTypeId**](/windows/desktop/api/Winscard/nf-winscard-scardgetdevicetypeida)                                 | 針對指定的讀取器名稱取得卡片讀取器的裝置類型識別碼。 這項功能不會影響讀取器的狀態。                                                                                 |
| [**SCardGetProviderId**](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)                                     | 取得智慧卡 [*主要服務提供者*](/windows/desktop/SecGloss/p-gly) 的識別碼 (GUID) 。                                       |
| [**SCardGetReaderDeviceInstanceId**](/windows/win32/api/winscard/nf-winscard-scardgetreaderdeviceinstanceida)             | 針對指定的讀取器名稱取得卡片讀取器的裝置實例識別碼。 這項功能不會影響讀取器的狀態。                                                                             |
| [**SCardGetReaderIcon**](/windows/win32/api/winscard/nf-winscard-scardgetreadericona)                                     | 取得指定讀者名稱之智慧卡讀卡機的圖示。                                                                                                                                                     |
| [**SCardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea)                                 | 封鎖執行，直到讀取器的狀態變更為止。                                                                                                                                                                |
| [**SCardGetTransmitCount**](/windows/desktop/api/Winscard/nf-winscard-scardgettransmitcount)                               | 抓取自插入指定卡片讀取器之後已完成的傳輸作業數目。                                                                                                        |
| [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)                             | 引進 [*智慧卡*](/windows/desktop/SecGloss/s-gly) 子系統的新智慧卡。                                                                                       |
| [**SCardIntroduceReader**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)                                 | 為智慧卡子系統引進了新的讀取器。                                                                                                                                                                 |
| [**SCardIntroduceReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)                       | 引進新的讀取器群組至智慧卡子系統。                                                                                                                                                           |
| [**SCardIsValidCoNtext**](/windows/desktop/api/Winscard/nf-winscard-scardisvalidcontext)                                   | 驗證智慧卡內容控制碼。                                                                                                                                                                                |
| [**SCardListCards**](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)                                             | 提供已引入子系統的智慧卡清單。                                                                                                                                                  |
| [**SCardListInterfaces**](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)                                   | 提供指定之智慧卡所提供的介面清單。                                                                                                                                                        |
| [**SCardListReaderGroups**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa)                               | 提供已引入子系統的讀者群組清單。                                                                                                                                                |
| [**SCardListReaders**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)                                         | 提供已引入子系統的讀取器清單。                                                                                                                                                      |
| [**SCardListReadersWithDeviceInstanceId**](/windows/win32/api/winscard/nf-winscard-scardlistreaderswithdeviceinstanceida) | 取得已提供裝置實例識別碼的讀取器清單。 這項功能不會影響讀取器的狀態。                                                                                     |
| [**SCardLocateCards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)                                         | 尋找符合指定 [*ATR 字串*](/windows/desktop/SecGloss/a-gly)的卡片。                                                                                               |
| [**SCardLocateCardsByATR**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsbyatra)                               | 尋找符合指定 [*ATR 字串*](/windows/desktop/SecGloss/a-gly)的卡片。                                                                                               |
| [**SCardReadCache**](/windows/desktop/api/Winscard/nf-winscard-scardreadcachea)                                             | 從 [智慧卡 Resource Manager](smart-card-resource-manager.md)所維護的全域快取中，抓取名稱/值組的值部分。                                                             |
| [**SCardReconnect**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)                                             | 重新建立從呼叫應用程式到智慧卡的現有連接。                                                                                                                                 |
| [**SCardReleaseCoNtext**](/windows/desktop/api/Winscard/nf-winscard-scardreleasecontext)                                   | 關閉已建立的 [*資源管理員內容*](/windows/desktop/SecGloss/r-gly)。                                                                    |
| [**SCardReleaseStartedEvent**](/windows/desktop/api/Winscard/nf-winscard-scardreleasestartedevent)                         | 使用 [**SCardAccessStartedEvent**](/windows/desktop/api/Winscard/nf-winscard-scardaccessstartedevent) 函式，遞減所取得之控制碼的參考計數。                                                                               |
| [**SCardRemoveReaderFromGroup**](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa)                     | 從現有的讀取器群組移除讀取器。                                                                                                                                                                      |
| [**SCardSetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib)                                             | 設定指定的讀取器屬性。                                                                                                                                                                                       |
| [**SCardSetCardTypeProviderName**](/windows/desktop/api/Winscard/nf-winscard-scardsetcardtypeprovidernamea)                 | 設定卡片名稱和提供者類型的提供者名稱。                                                                                                                                                            |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                                                   | 取得讀取器的目前 [*狀態*](/windows/desktop/SecGloss/s-gly) 。                                                                                                                      |
| [**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                                               | 將服務要求傳送至智慧卡。                                                                                                                                                                             |
| [**SCardUIDlgSelectCard**](/windows/desktop/api/Winscard/nf-winscard-scarduidlgselectcarda)                                 | 顯示智慧卡 **選取卡片** 對話方塊。                                                                                                                                                                  |
| [**SCardWriteCache**](/windows/desktop/api/Winscard/nf-winscard-scardwritecachea)                                           | 將智慧卡的名稱/值組寫入 [智慧卡 Resource Manager](smart-card-resource-manager.md)所維護的全域快取。                                                                     |



 

## <a name="sasl-functions"></a>SASL 函數

簡單驗證及安全性階層 (SASL) 提供下列功能。



| 函式                                                              | Description                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SaslAcceptSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-saslacceptsecuritycontext)         | 包裝對 SSPI AcceptSecurityCoNtext 的標準呼叫 [**(一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式，並包含建立 SASL 伺服器 cookie 的功能。              |
| [**SaslEnumerateProfiles**](/windows/desktop/api/Sspi/nf-sspi-saslenumerateprofilesa)                 | 列出提供 SASL 介面的封裝。                                                                                                                                |
| [**SaslGetCoNtextOption**](/windows/desktop/api/Sspi/nf-sspi-saslgetcontextoption)                   | 抓取指定的 SASL 內容之指定的屬性。                                                                                                                  |
| [**SaslGetProfilePackage**](/windows/desktop/api/Sspi/nf-sspi-saslgetprofilepackagea)                 | 傳回指定封裝的封裝資訊。                                                                                                                       |
| [**SaslIdentifyPackage**](/windows/desktop/api/Sspi/nf-sspi-saslidentifypackagea)                     | 傳回符合指定之 SASL 協商緩衝區的協商前置詞。                                                                                                 |
| [**SaslInitializeSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-saslinitializesecuritycontexta) | 將標準呼叫包裝給 SSPI [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函式，並處理來自伺服器的 SASL 伺服器 cookie。 |
| [**SaslSetCoNtextOption**](/windows/desktop/api/Sspi/nf-sspi-saslsetcontextoption)                   | 為指定的 SASL 內容設定指定之屬性的值。                                                                                                         |



 

## <a name="other-functions"></a>其他函數

以下是用於驗證的其他函數。



| 函式                                                                   | 描述                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddSecurityPackage**](/windows/desktop/api/Sspi/nf-sspi-addsecuritypackagea)                           | 將 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) 新增至 [Microsoft Negotiate](microsoft-negotiate.md)所支援的提供者清單。<br/>                                                                                                                              |
| [**ChangeAccountPassword**](/windows/desktop/api/Sspi/nf-sspi-changeaccountpassworda)                     | 使用指定的 [安全性支援提供者](sspi.md)，變更 Windows 網域帳戶的密碼。<br/>                                                                                                                                                                                                                                         |
| [**CredMarshalTargetInfo**](/windows/desktop/api/NTSecPkg/nf-ntsecpkg-credmarshaltargetinfo)                     | 將指定的目標序列化為位元組值陣列。<br/>                                                                                                                                                                                                                                                                                           |
| [**DeleteSecurityPackage**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritypackagea)                     | 從 [Microsoft Negotiate](microsoft-negotiate.md)支援的提供者清單中刪除 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly)。<br/>                                                                                                                         |
| [**LsaManageSidNameMapping**](/previous-versions/windows/desktop/legacy/jj902653(v=vs.85))                 | 從向 LSA 查閱服務註冊的對應集中，加入或移除 SID/名稱對應。<br/>                                                                                                                                                                                                                                                          |
| [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy)                                     | 在本機或遠端系統上開啟 [**原則**](/windows/desktop/SecMgmt/policy-object) 物件的控制碼。<br/>                                                                                                                                                                                                                                                          |
| [**LsaQueryInformationPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy)             | 捕獲 [**原則**](/windows/desktop/SecMgmt/policy-object) 物件的相關資訊。<br/>                                                                                                                                                                                                                                                                              |
| [**LsaSetInformationPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasetinformationpolicy)                 | 修改 [**原則**](/windows/desktop/SecMgmt/policy-object) 物件中的資訊。<br/>                                                                                                                                                                                                                                                                                  |
| [**NPFMXEditPerm**](/windows/desktop/api/Npapi/nf-npapi-npfmxeditperm)                                     | 可讓網路廠商提供自己的許可權編輯器對話方塊。<br/>                                                                                                                                                                                                                                                                             |
| [**NPFMXGetPermCaps**](/windows/desktop/api/Npapi/nf-npapi-npfmxgetpermcaps)                               | 抓取許可權編輯器的功能。 傳回值是位元遮罩，表示要啟用 [檔案管理員] 中的 [ **安全性** ] 功能表項目。<br/>                                                                                                                                                                               |
| [**NPFMXGetPermHelp**](/windows/desktop/api/Npapi/nf-npapi-npfmxgetpermhelp)                               | 當選取了 [檔案管理員] 之 [ **安全性** ] 功能表中的功能表項目，並按下 F1 時，會抓取 [許可權編輯器] 對話方塊的說明檔和說明內容。<br/>                                                                                                                                                                                 |
| [**SpGetCredUICoNtextFn**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spgetcreduicontextfn)                       | 從認證提供者抓取內容資訊。<br/>                                                                                                                                                                                                                                                                                               |
| [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn)                         | 針對 SSP/AP DLL 中每個 [*安全性套件*](/windows/desktop/SecGloss/s-gly) 所執行的函式，提供 LSA 指標。<br/>                                                                                                                                                               |
| [**SpQueryMetaDataFn**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spquerymetadatafn)                             | 取得 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) 在初始化 [*安全性內容*](/windows/desktop/SecGloss/c-gly)時 (SSP) 的中繼資料。<br/>                                                                                      |
| [**SpUpdateCredentialsFn**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spupdatecredentialsfn)                     | 更新與指定內容相關聯的認證。<br/>                                                                                                                                                                                                                                                                                          |
| [**SspiCompareAuthIdentities**](/windows/desktop/api/Sspi/nf-sspi-sspicompareauthidentities)             | 比較兩個指定的認證。<br/>                                                                                                                                                                                                                                                                                                                 |
| [**SspiCopyAuthIdentity**](/windows/desktop/api/Sspi/nf-sspi-sspicopyauthidentity)                       | 建立指定的不透明認證結構的複本。<br/>                                                                                                                                                                                                                                                                                            |
| [**SspiDecryptAuthIdentity**](/windows/desktop/api/Sspi/nf-sspi-sspidecryptauthidentity)                 | 解密指定的加密認證。<br/>                                                                                                                                                                                                                                                                                                            |
| [**SspiEncodeAuthIdentityAsStrings**](/windows/desktop/api/Sspi/nf-sspi-sspiencodeauthidentityasstrings) | 將指定的驗證識別編碼為三個字串。<br/>                                                                                                                                                                                                                                                                                         |
| [**SspiEncodeStringsAsAuthIdentity**](/windows/desktop/api/Sspi/nf-sspi-sspiencodestringsasauthidentity) | 將三個認證字串的集合編碼為驗證身分識別結構。<br/>                                                                                                                                                                                                                                                                      |
| [**SspiEncryptAuthIdentity**](/windows/desktop/api/Sspi/nf-sspi-sspiencryptauthidentity)                 | 加密指定的身分識別結構。<br/>                                                                                                                                                                                                                                                                                                              |
| [**SspiExcludePackage**](/windows/desktop/api/Sspi/nf-sspi-sspiexcludepackage)                           | 建立新的識別結構，此結構是為了將指定的 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) 排除 (SSP) 而修改的指定識別結構的複本。<br/>                                                                                              |
| [**SspiFreeAuthIdentity**](/windows/desktop/api/Sspi/nf-sspi-sspifreeauthidentity)                       | 釋出配置給指定之身分識別結構的記憶體。<br/>                                                                                                                                                                                                                                                                                        |
| [**SspiGetCredUICoNtext**](/windows/desktop/api/Sspi/nf-sspi-sspigetcreduicontext)                       | 從認證提供者抓取內容資訊。<br/>                                                                                                                                                                                                                                                                                               |
| [**SspiGetTargetHostName**](/windows/desktop/api/Sspi/nf-sspi-sspigettargethostname)                     | 取得與指定之目標相關聯的主機名稱。<br/>                                                                                                                                                                                                                                                                                                |
| [**SspiIsAuthIdentityEncrypted**](/windows/desktop/api/Sspi/nf-sspi-sspiisauthidentityencrypted)         | 指出指定的身分識別結構是否已加密。<br/>                                                                                                                                                                                                                                                                                        |
| [**SspiIsPromptingNeeded**](/windows/desktop/api/Sspi/nf-sspi-sspiispromptingneeded)                     | 指出呼叫 [**InitializeSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 或 [**AcceptSecurityCoNtext**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式之後傳回的錯誤，是否需要對 [**SspiPromptForCredentials**](/windows/desktop/api/Sspi/nf-sspi-sspipromptforcredentialsa) 函式進行額外的呼叫。<br/>                      |
| [**SspiLocalFree**](/windows/desktop/api/Sspi/nf-sspi-sspilocalfree)                                     | 釋出與指定緩衝區相關聯的記憶體。<br/>                                                                                                                                                                                                                                                                                                  |
| [**SspiMarshalAuthIdentity**](/windows/desktop/api/Sspi/nf-sspi-sspimarshalauthidentity)                 | 將指定的識別結構序列化為位元組陣列。<br/>                                                                                                                                                                                                                                                                                          |
| [**SspiPrepareForCredRead**](/windows/desktop/api/Sspi/nf-sspi-sspiprepareforcredread)                   | 從指定的身分識別結構產生目標名稱和認證類型。<br/>                                                                                                                                                                                                                                                                      |
| [**SspiPrepareForCredWrite**](/windows/desktop/api/Sspi/nf-sspi-sspiprepareforcredwrite)                 | 從可在 [**CredWrite**](/windows/desktop/api/WinCred/nf-wincred-credwritea) 函式的呼叫中傳遞做為參數值的身分識別結構產生值。<br/>                                                                                                                                                                                                    |
| [**SspiPromptForCredentials**](/windows/desktop/api/Sspi/nf-sspi-sspipromptforcredentialsa)               | 允許 (SSPI) 應用程式的 [*安全性支援提供者介面*](/windows/desktop/SecGloss/s-gly) 提示使用者輸入認證。<br/>                                                                                                                           |
| [**SspiUnmarshalAuthIdentity**](/windows/desktop/api/Sspi/nf-sspi-sspiunmarshalauthidentity)             | 將指定的位元組值陣列還原序列化為識別結構。<br/>                                                                                                                                                                                                                                                                             |
| [**SspiUnmarshalCredUICoNtext**](/windows/desktop/api/Sspi/nf-sspi-sspiunmarshalcreduicontext)           | 在前一次呼叫 [**ICredentialProvider：： SetSerialization**](/windows/win32/api/credentialprovider/nf-credentialprovider-icredentialprovider-setserialization) 方法期間，還原序列化認證提供者所取得的認證資訊。<br/>                                                                                                                                                    |
| [**SspiUpdateCredentials**](/windows/desktop/api/Sspi/nf-sspi-sspiupdatecredentials)                     | 更新與指定內容相關聯的認證。<br/>                                                                                                                                                                                                                                                                                          |
| [**SspiValidateAuthIdentity**](/windows/desktop/api/Sspi/nf-sspi-sspivalidateauthidentity)               | 指出指定的識別結構是否有效。<br/>                                                                                                                                                                                                                                                                                            |
| [**SspiZeroAuthIdentity**](/windows/desktop/api/Sspi/nf-sspi-sspizeroauthidentity)                       | 以零填滿與指定之身分識別結構相關聯的記憶體區塊。<br/>                                                                                                                                                                                                                                                                  |
| [**WlxQueryTsLogonCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ts_logon_credentials)           | 在啟用終端機服務的情況下，由取代 [*GINA*](/windows/desktop/SecGloss/g-gly) DLL 呼叫以取得 [*認證*](/windows/desktop/SecGloss/c-gly) 資訊。 GINA DLL 接著可以使用這項資訊來自動填入登入方塊，並嘗試將使用者登入。<br/> |



 

 

