---
title: 使用 otherWellKnownObjects 屬性啟用 Rename-Safe 系結
description: 容器類別的物件具有 otherWellKnownObjects 屬性，可讓您用來建立 GUID 與容器中子物件 (DN) 的分辨名稱之間的關聯。
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- otherWellKnownObjects 屬性
- otherWellKnownObjects 屬性，用於重新命名安全系結
- Active Directory、using、binding、重新命名安全的系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446f669adc9a59f9f8aba93e852546fe3991952857469d6f37978d9cf91a7666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695317"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a>使用 otherWellKnownObjects 屬性啟用 Rename-Safe 系結

容器類別的物件具有 **otherWellKnownObjects** 屬性，可讓您用來建立 GUID 與容器中子物件 (DN) 的分辨名稱之間的關聯。 如果移動或重新命名子物件，Active Directory 伺服器會更新該子物件之 **otherWellKnownObjects** 值中的 DN。 這可讓您使用 WKGUID 系結功能，利用容器的 GUID 和 DN 來系結至子物件，而非子物件的 DN。

**OtherWellKnownObjects** 屬性相當於 **wellKnownObjects** 屬性，但應用程式和服務可以寫入 **otherWellKnownObjects** 值，但只有系統才能寫入 **wellKnownObjects**。

在下列情況下，使用 **otherWellKnownObjects** 屬性和 WKGUID 系結會很有説明：在需要重新命名安全系結的情況下，相對於特定的容器物件。

如果容器物件包含其他重要物件，或可以重新命名或移動重要物件。

如果容器物件的每個實例都有重要的物件。 例如，系統會使用每個 **domainDNS** 物件的 **wellKnownObjects** 屬性來儲存 [使用者] 容器的值（存在於 **domainDNS** 物件的每個實例中）。 這可讓應用程式藉由指定知名的 GUID 和 **domainDNS** 容器的 DN，以重新命名安全的方式系結至 Users 容器。 應用程式可以使用類似的容器 **otherWellKnownObjects** 屬性。

如果您需要重要物件的重新命名安全系結和/或搜尋功能。

**新增重新命名安全系結和搜尋功能**

1.  在該容器內建立重要物件時，將值新增至容器物件的 **otherWellKnownObjects** 屬性。 值包含表示已知物件的 GUID。 請注意，這不是該物件的 **objectGUID** 和 **distinguishedName** 。
2.  使用 WKGUID 系結功能來系結或搜尋重要的物件。

**OtherWellKnownObjects** 屬性可以有多個值，並在其所設定的容器內包含已知物件的 GUID/DN 元組。 **OtherWellKnownObjects** 屬性具有 DNWithBinary 語法，其中的值具有下列格式：


```C++
B:<char count>:<well known GUID>:<object DN>
```



在此範例中，「 &lt; char count」 &gt; 是「知名 GUID」中的十六進位數位計數 &lt; ，也 &gt; 就是 32 (GUID 中的十六進位位數) **otherWellKnownObjects** 和 **wellKnownObjects** 的數目。 「 &lt; 知名 guid」 &gt; 是已知 guid 的十六進位數位標記法。 「 &lt; 物件 DN」 &gt; 是此 WKO 值所代表之物件的辨別名稱。 伺服器會維護每個 **wellKnownObjects** 和 **OtherWellKnownObjects** 值的 ObjectDN 部分，使其包含最初在建立值時所指定之物件的目前分辨名稱。

例如，如果 {df447b5e-aa5b-11d2-8d53-00c04f79ab81} 是 Fabrikam.com 網域中 MyContainer 容器中 MyObject 物件的已知 GUID，則 **otherWellKnownObjects** 值會指定已知的 Guid 和 MYOBJECT 的 DN：


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



若要系結至此物件，請使用下列 WKGUID 系結字串，以指定物件的已知 GUID 以及容器的 DN：


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



系結至此物件之後，您可以使用 ADSI COM 介面來搜尋、讀取、修改或刪除物件。

如需詳細資訊和示範如何將物件加入至 **otherWellKnownObjects** 屬性的程式碼範例，請參閱 [建立容器物件的範例程式碼](example-code-for-creating-a-container-object.md)。

 

 




