---
title: 遠端連線的驗證
description: Windows遠端系統管理可支援數種標準的驗證方法和訊息加密，以維護電腦間通訊的安全性。
ms.assetid: 97a13b07-ae7a-4d2f-8841-77a22c91b204
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0622f3d80e923f7d910740c71ee99f0e9a0bc446cea259b292e2d645e3b5a973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858871"
---
# <a name="authentication-for-remote-connections"></a>遠端連線的驗證

Windows遠端系統管理可支援數種標準的驗證方法和訊息加密，以維護電腦間通訊的安全性。

## <a name="default-group-access"></a>預設群組存取

在安裝期間，WinRM 會建立本地 **組 \_ \_ WinRMRemoteWMIUsers**。 WinRM 接著會限制遠端存取不屬於本機系統管理群組或 **WinRMRemoteWMIUsers \_ \_** 群組成員的任何使用者。 您可以在命令提示字元中輸入 **net localgroup WinRMRemoteWMIUsers \_ \_ /add <domain> \\ <username>** ，將本機使用者、網域使用者或網域群組新增至 **WinRMRemoteWMIUsers \_ \_** 。 （選擇性）您可以使用群組原則將使用者新增至群組。

## <a name="default-authentication-settings"></a>預設驗證設定

預設認證（使用者名稱和密碼）是執行腳本之登入使用者帳戶的認證。

**若要變更為遠端電腦上的另一個帳戶**

1.  在 [**ConnectionOptions**](connectionoptions.md) 或 [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) 物件中指定認證，並將其提供給 [**CreateSession**](wsman-createsession.md) 呼叫。
2.  在 [**CreateSession**](wsman-createsession.md)呼叫的 *旗標* 參數中設定 **WSManFlagCredUserNamePassword** 。

以下清單包含在預設認證下執行腳本或應用程式時所發生的情況：

-   當用戶端位於網域中，而遠端目的地字串不是下列其中一項時， [*Kerberos*](windows-remote-management-glossary.md)是驗證的預設方法： localhost、127.0.0.1 或 \[ ：： 1 \] 。
-   當用戶端不在網域中，但遠端目的地字串為下列其中一項時， [*Negotiate*](windows-remote-management-glossary.md)即為預設方法： localhost、127.0.0.1 或 \[ ：： 1 \] 。

如果您以 [**ConnectionOptions**](connectionoptions.md) 物件提供明確的認證，Negotiate 即為預設方法。 「協商驗證」會根據電腦是否位於網域或工作組，判斷進行中的驗證方法是否為 Kerberos 或 NTLM。 如果使用本機帳戶連接到遠端目的電腦，則帳戶的前面應該會加上電腦名稱稱。 例如，myComputer \\ myUsername。

如果您指定 Negotiate、摘要式或基本驗證，但無法提供 [**ConnectionOptions**](connectionoptions.md) 物件，則您會收到錯誤，指出需要明確的認證。 如果 HTTPS 不是傳輸，則必須在信任的主機電腦清單中設定目標遠端電腦。

如需有關在預設設定中啟用之驗證類型的詳細資訊，請參閱[Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。

## <a name="basic-authentication"></a>基本驗證

若要在 [**CreateSession**](wsman-createsession.md)的呼叫中明確建立 [*基本*](windows-remote-management-glossary.md)身份驗證，請在 *flags* 參數中設定 **WSManFlagUseBasic** 和 **WSManFlagCredUserNamePassword** 旗標。 在 WinRM 用戶端和 WinRM 伺服器的預設設定中，已停用基本驗證。

## <a name="digest-authentication"></a>摘要式驗證

若要在 [**CreateSession**](wsman-createsession.md)的呼叫中明確建立 [*摘要式*](windows-remote-management-glossary.md)驗證，請在 Flags 參數中設定 **WSManFlagUseDigest** 旗 *標*。 不支援摘要。 它無法針對 WinRM 伺服器元件進行設定。

## <a name="negotiate-authentication"></a>協商驗證

若要明確建立 [*Negotiate*](windows-remote-management-glossary.md)驗證（也稱為 Windows 整合式驗證），請在 [**CreateSession**](wsman-createsession.md)的呼叫中，設定 flags 參數中的 **WSManFlagUseNegotiate** 旗 *標*。

[ (UAC) 的使用者帳戶控制 ](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) 會影響 WinRM 服務的存取權。 在工作組中使用「協商驗證」時，只有內建的系統管理員帳戶可以存取該服務。 若要允許 Administrators 群組中的所有帳戶存取服務，請設定下列登錄值：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **原則** \\ **系統** \\ **LocalAccountTokenFilterPolicy** = 1

## <a name="kerberos-authentication"></a>Kerberos 驗證

若要在 [**CreateSession**](wsman-createsession.md)的呼叫中明確建立 [*Kerberos*](windows-remote-management-glossary.md)驗證，請在 Flags 參數中設定 **WSManFlagUseKerberos** 旗 *標*。 用戶端和伺服器電腦都必須加入網域。 如果您使用 Kerberos 作為驗證方法，則不能在 [**CreateSession**](wsman-createsession.md) 或 [**IWSMan：： CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)的呼叫中使用 IP 位址。

## <a name="client-certificate-based-authentication"></a>以用戶端憑證為基礎的驗證

若要在 [**CreateSession**](wsman-createsession.md)的呼叫中建立用戶端憑證型驗證，請在 flags 參數中設定 **WSManFlagUseClientCertificate** 旗 *標* 。

您必須先使用 Winrm 命令列工具，在用戶端和服務上啟用憑證驗證。 如需詳細資訊，請參閱 [啟用驗證選項](#enabling-or-disabling-authentication-options)。 您也必須在 WinRM 伺服器電腦上的 CertMapping 資料表中建立專案。 這會建立一或多個憑證與本機帳戶之間的對應。 使用憑證進行驗證和授權之後，會使用對應的本機帳戶進行 WinRM 服務所執行的作業。

您可以針對特定的資源 URI 來建立對應。 若要深入瞭解，包括如何建立 CertMapping 資料表專案，請在命令提示字元中輸入 **winrm help CertMapping** 。

> [!Note]  
> WinRM 在此內容中可用的憑證大小上限為16KB。

 

## <a name="enabling-or-disabling-authentication-options"></a>啟用或停用驗證選項

系統安裝時的預設驗證選項是 Kerberos。 如需詳細資訊，請參閱[Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。

如果您的腳本或應用程式需要未啟用的特定驗證方法，您必須變更設定，以啟用這種類型的驗證。 您可以使用 **Winrm** 命令列工具，或透過 **Windows 遠端管理群組原則物件** 的群組原則來進行這種變更。 您也可以選擇停用某些驗證方法。

**若要使用 Winrm 工具啟用或停用驗證**

1.  若要設定 WinRM 用戶端的設定，請使用 **Winrm set** 命令並指定用戶端。 例如，下列命令會停用用戶端的摘要式驗證。

    **winrm set winrm/config/client/auth @ {Digest = "false"}**

2.  若要設定 WinRM 伺服器的設定，請使用 **Winrm set** 命令並指定服務。 例如，下列命令會啟用服務的 Kerberos 驗證。

    **winrm set winrm/config/service/auth @ {Kerberos = "true"}**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> </dl>

 

 




