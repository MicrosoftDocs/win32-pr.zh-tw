---
description: WMI 命名空間及其資料的存取權是由安全描述項控制。
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: 保護 WMI 命名空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3cdf2b6e5c5cf035fed70e3e0dd949a812505f1f1ded8f1599043cdd75ba4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992368"
---
# <a name="securing-wmi-namespaces"></a>保護 WMI 命名空間

WMI 命名空間及其資料的存取權是由 [*安全描述項*](gloss-s.md)控制。 您可以藉由調整命名空間安全描述項來控制誰可以存取資料和方法，以保護 [*命名空間*](gloss-n.md) 中的資料。 如需詳細資訊，請參閱 [存取 WMI 安全物件](access-to-wmi-securable-objects.md)。


下列主題將說明 WMI 命名空間安全性，以及如何控制對命名空間的存取。

<dl> <dt>

<span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[存取 WMI 命名空間](access-to-wmi-namespaces.md)
</dt> <dd>

WMI 命名空間安全性相依于標準 Windows 使用者 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (sid) 和存取控制清單。 系統管理員和使用者有不同的預設許可權。

</dd> <dt>

<span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dd>

在 wmi 存放庫中存在命名空間之後，您可以使用 wmi 控制項或呼叫 [**\_ \_ SystemSecurity**](--systemsecurity.md)的方法，變更命名空間上的安全性。

</dd> <dt>

<span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[需要命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)
</dt> <dd>

命名空間上的 **RequiresEncryption** 限定詞需要 WMI 用戶端應用程式或腳本，才能使用加密遠端程序呼叫的驗證層級。 傳入的資料要求和非同步回呼都必須加密。

</dd> <dt>

<span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[建立命名空間安全性的繼承](establishing-inheritance-of-namespace-security.md)
</dt> <dd>

您可以控制子命名空間是否繼承父命名空間的安全描述項。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> <dt>

[連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[使用 WMI API 建立命名空間](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[WMI 安全描述項物件](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
