---
description: 在完整系統管理員帳戶下執行的 c + + 應用程式和腳本，都可以變更命名空間安全描述項。
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: 設定命名空間安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877b1dfc0ae1a9467b1beb7d169bfa31fdf7395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000190"
---
# <a name="setting-namespace-security-descriptors"></a>設定命名空間安全描述項

在完整系統管理員帳戶下執行的 c + + 應用程式和腳本，都可以變更命名空間安全描述項。

## <a name="namespace-security-descriptors"></a>命名空間安全描述項

每個 WMI 命名空間都有一個 [*安全描述項*](/windows/desktop/SecGloss/s-gly)，可讓每個命名空間具有唯一的安全性設定，以決定誰可以存取命名空間資料和方法。 如需 WMI 存取安全性的詳細資訊，請參閱 [存取 wmi 安全物件](access-to-wmi-securable-objects.md)。 Wmi[命名空間的存取權](access-to-wmi-namespaces.md)描述 WMI 中 wmi 命名空間和安全性審核的預設安全性設定。

您可以透過下列方式，設定 WMI (CIM) 存放庫中每個 WMI 命名空間的帳戶許可權：

-   在 MOF 檔案中建立命名空間時。 如需詳細資訊，請參閱 [在建立命名空間時設定命名空間安全性](setting-namespace-security-when-the-namespace-is-created.md)。
-   使用 WMI 控制項手動進行。 如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。
-   藉由呼叫 [**\_ \_ SystemSecurity**](--systemsecurity.md)類別的方法，以程式設計方式進行。

與每個命名空間相關聯之 [**\_ \_ SystemSecurity**](--systemsecurity.md)物件的下列方法，可讓您讀取或變更命名空間的安全性。

<dl> <dt>

<span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)
</dt> <dd>

將 *rights* 參數設定為點陣圖，每個位都對應至存取權限。

</dd> <dt>

<span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)
</dt> <dd>

取得使用者所連接之命名空間的安全描述項。 這個方法會以二進位位元組陣列格式傳回安全描述項。 如果您要撰寫腳本，請使用 [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) 方法。

</dd> <dt>

<span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)
</dt> <dd>

針對使用者所連接的命名空間，設定 (SD) 的安全描述項。 這個方法需要二進位位元組陣列格式的安全描述項。 如果您要撰寫腳本，請使用 [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) 方法。

</dd> <dt>

<span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)
</dt> <dd>

取得安全描述項，可控制與 [**\_ \_ SystemSecurity**](--systemsecurity.md)實例相關聯之 WMI 命名空間的存取權。 安全描述項會以 [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)的實例傳回。

</dd> <dt>

<span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)
</dt> <dd>

寫入控制印表機存取權之安全描述項的更新版本。 安全描述項會以 [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)的實例來表示。

</dd> <dt>

<span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)
</dt> <dd>

針對執行過時 Windows 的電腦上的個別使用者清單取得遠端存取許可權，但無法使用透過 Windows 安全描述項的存取控制。

</dd> <dt>

<span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)
</dt> <dd>

針對執行過時 Windows 的電腦上的個別使用者清單設定遠端存取許可權，無法使用透過 Windows 安全描述項的存取控制。

</dd> </dl>

如果您要撰寫腳本，請使用 [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) 和 [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)。 您可以使用 [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) 類別的方法來改變安全描述項。

如果您是使用 c + + 進行程式設計，您可以使用 [安全描述項定義語言 (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)和轉換方法 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 和 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)，來操作二進位安全描述項。

請注意，從 Windows Vista 開始， [使用者帳戶控制](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) 會影響對 wmi 資料的存取權，以及可使用 [*wmi 控制項*](gloss-w.md)設定的內容。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[保護 WMI 命名空間](securing-wmi-namespaces.md)
</dt> <dt>

[WMI 安全性常數](wmi-security-constants.md)
</dt> <dt>

[存取 WMI 命名空間](access-to-wmi-namespaces.md)
</dt> <dt>

[WMI 安全描述項物件](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
