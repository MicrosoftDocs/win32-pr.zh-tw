---
title: WinRM 中的多重躍點支援
description: Windows遠端系統管理 (WinRM) 支援跨多部遠端電腦委派使用者認證。
ms.assetid: 0e6c8966-bb05-4dfb-b154-300fa76e8d9c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76be3054fc9c0d624c206cf5a26d7788e763dfc81f1b2069f6abff8736be2388
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121758"
---
# <a name="multi-hop-support-in-winrm"></a>WinRM 中的多重躍點支援

Windows遠端系統管理 (WinRM) 支援跨多部遠端電腦委派使用者認證。 多重躍點支援功能現在可使用 (CredSSP) 的認證安全性服務提供者進行驗證。 CredSSP 可讓應用程式將使用者的認證從用戶端電腦委派至目標伺服器。

CredSSP 驗證適用于無法使用 Kerberos 委派的環境。 已新增 CredSSP 的支援，可讓使用者連線到遠端伺服器，而且能夠存取第二躍點的電腦，例如檔案共用。

如需 CredSSP 的詳細資訊，請參閱 [KB 951608](https://support.microsoft.com/kb/951608)。

> [!Note]  
> WinRM 用戶端和伺服器將僅支援使用明確認證的 CredSSP 驗證。

 

## <a name="multi-hop-support-configuration-setup-and-details"></a>多重躍點支援設定和詳細資料

有多個機制可設定 WinRM 設定。 在下列程式中，會使用 [ **winrm** 公用程式] 和 [群組原則編輯器] (**gpedit.msc**) 。 您也可以使用 Windows PowerShell，針對 WinRM 啟用 CredSSP。 如需詳細的設定資訊和使用範例，請參閱[WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true)、 [WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)和[Disable WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) Windows PowerShell Cmdlet。

您必須在用戶端設定和遠端電腦上的服務設定中啟用 CredSSP 委派。 此外，使用 CredSSP 需要在伺服器上設定 HTTP [*或 HTTPS 接聽*](windows-remote-management-glossary.md) 程式。

**若要使用適用于 WinRM 的 CredSSP 驗證設定多重躍點支援**

1.  您必須在用戶端設定中啟用 CredSSP。 您可以手動或透過群組原則設定來啟用此旗標。 預設值是 **False**。 [**允許 CredSSP 驗證** 原則] 位於下列路徑： [電腦設定系統 \\ 管理範本] \\ Windows 元件 \\ Windows 遠端管理 (winrm) \\ winrm 用戶端。

    下列命令示範如何使用 winrm 公用程式在 WinRM 用戶端上啟用 CredSSP：

    **winrm set winrm/config/client/auth @ {CredSSP = "true"}**

2.  您必須在 WinRM 服務設定中啟用 CredSSP。 您可以手動或透過群組原則設定來啟用此旗標。 預設值是 **False**。 [**允許 CredSSP 驗證**] 原則位於下列路徑： [電腦設定系統 \\ 管理範本] \\ Windows 元件 \\ Windows 遠端管理 (winrm) \\ winrm 服務。

    下列命令示範如何使用 winrm 公用程式在 WinRM 服務上啟用 CredSSP：

    **winrm set winrm/config/service/auth @ {CredSSP = "true"}**

3.  必須在 WinRM 用戶端上啟用 [允許委派新認證 (**AllowFreshCredentials** ]) 原則設定，以及必須將具有 WSMAN 首碼 (SPN) 的服務主體名稱新增至原則。 SPN 代表可以委派使用者認證的目的電腦。 SPN 可以設定為一或多部電腦。 下表包含 Spn 的有效格式範例。

    

    | SPN                                       | 描述                                                                         |
    |-------------------------------------------|-------------------------------------------------------------------------------------|
    | WSMAN/myComputer<br/>  | 在 myComputer.myDomain.com 上執行的 WinRM 伺服器。<br/>                         |
    | WSMAN/ \* . myDomain.com<br/>          | 所有在 myDomain.com 中執行的 WinRM 伺服器。<br/>                               |
    | WSMAN/ \* . fabrikam.myDomain.com<br/> | 所有在 fabrikam.myDomain.com 中的電腦上執行的 WinRM 伺服器。<br/> |

    

     

    如需設定群組原則的詳細資訊，請參閱[Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。

    如需 **AllowFreshCredentials** 原則的詳細資訊，請參閱群組原則編輯器提供的原則描述和 [KB 951608](https://support.microsoft.com/kb/951608)。 **AllowFreshCredentials** 原則位於下列路徑： \\ 系統管理範本 \\ 系統認證委派的電腦配置 \\ 。

4.  [*必須在*](windows-remote-management-glossary.md)伺服器上設定 HTTPS 或 HTTP 接聽程式。 用於設定 HTTPS 接聽程式的憑證指紋也用來設定 WinRM 服務設定下的 [CertificateThumbprint *]* 設定。

    下列命令示範如何使用 winrm 公用程式來 [*設定 HTTPS 接聽*](windows-remote-management-glossary.md)程式：

    **winrm quickconfig-傳輸： HTTPs**

如果用戶端與伺服器之間無法進行 Kerberos 驗證，則使用者必須針對多重躍點支援設定下列其中一項設定：

-   為了提高安全性，使用者應該將 **CertificateThumbprint** 屬性新增至 WinRM 服務設定。 如果 WinRM 服務設定了 **CertificateThumbprint** 屬性，服務就會嘗試在本機電腦存放區中找出對應的憑證，並使用此憑證進行 CredSSP 驗證。 如果 WinRM 服務使用本機電腦存放區中的憑證來驗證服務器，則必須允許 Network Service 帳戶存取憑證的私密金鑰。

    > [!Note]  
    > 如果未設定服務設定，則 WinRM 伺服器會使用在記憶體中建立的自我簽署憑證來加密傳送至用戶端的訊息。 不過，此憑證不會用來進行驗證。

     

-   如果 Kerberos 驗證和憑證指紋皆無法使用，則使用者可以啟用 NTLM 驗證。 如果使用 NTLM 驗證，則必須啟用 [僅限 NTLM 伺服器驗證的全新認證] (**AllowFreshCredentialsWhenNTLMOnly**) 原則，而且必須將具有 WSMAN 首碼的 SPN 新增至原則。 這項設定比 Kerberos 驗證和憑證指紋的安全性低，因為認證會傳送到未經驗證的伺服器。

    如需 **AllowFreshCredentialsWhenNTLMOnly** 原則的詳細資訊，請參閱群組原則編輯器提供的原則描述和 [KB 951608](https://support.microsoft.com/kb/951608)。 **AllowFreshCredentialsWhenNTLMOnly** 原則位於下列路徑： \\ 系統管理範本 \\ 系統認證委派的電腦配置 \\ 。

## <a name="using-credssp-authentication-with-explicit-credentials"></a>使用具有明確認證的 CredSSP 驗證

使用者可以透過 HTTP 和 HTTPS 指定明確的認證。 下列命令示範如何使用 winrm 公用程式搭配透過 HTTPS 的明確認證來執行遠端操作：

**winrm 操作-遠端： https://myMachine -驗證： CredSSP-username： myUsername-password： myPassword**

 

