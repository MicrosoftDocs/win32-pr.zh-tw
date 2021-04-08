---
title: 使用 WKGUID 系結至 Well-Known 物件
description: 本主題說明如何使用 WKGUID 系結字串系結至物件。
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- 使用 WKGUID AD 系結至 Well-Known 物件
- Active Directory、使用、系結，以及使用 WKGUID 系結至已知的物件
- 知名物件廣告
- 已知物件 AD，系結至使用 WKGUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681694"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a>使用 WKGUID 系結至 Well-Known 物件

容器可以有一個或多個重要的子類型可以重新命名或移動。 可能很難追蹤這些子字串並為其建立正確的系結字串，特別是當重新命名或移動時。

為了支援這些容器內這些物件的重新命名安全系結，Active Directory Domain Services 有兩個屬性： **wellKnownObjects** 和 **otherWellKnownObjects**。 這些屬性具有具有二進位的 ADSTYPE DN 屬性語法 \_ \_ \_ 。 它們允許多個值，並在其所設定的容器內包含已知物件的 GUID/DN 元組。 Active Directory 伺服器會維護每個 **wellKnownObjects** 和 **otherWellKnownObjects** 專案的分辨名稱部分，使其包含建立專案時所指定之物件的目前分辨名稱。

**OtherWellKnownObjects** 屬性可以在任何物件上設定和使用。

**WellKnownObjects** 屬性是在 domainDNS 和設定容器上使用。 **WellKnownObjects** 屬性是僅限系統的屬性，只能由作業系統修改。

**DomainDNS** 容器具有下列知名物件：

-   使用者
-   電腦
-   系統
-   網域控制站
-   基礎結構
-   已刪除的物件
-   遺失並找到

設定容器具有已知的物件：已刪除的物件。

這些物件位於 Active Directory 網域服務中的每個 **domainDNS** 和設定容器中。

您可以使用 WKGUID 系結格式來系結至已知的物件。 只有 Active Directory Domain Services （也就是 LDAP 提供者）支援與 WKGUID 的系結。

> [!IMPORTANT]
> 請一律使用 WKGUID 系結格式來系結至網域和設定容器中的已知物件（如上所列）。 這樣可確保這些容器可以系結至，即使它們已移動或重新命名也一樣。

 

WKGUID 系結字串格式如下所示：


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



「 &lt; 伺服器名稱」 &gt; 是目錄伺服器名稱。 「 &lt; 伺服器名稱」 &gt; 是選擇性的。

" &lt; XXXXX &gt; " 是 GUID 的十六進位值的字串標記法，代表已知的物件。 GUID 字串是在 "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" 表單中指定，而且與 [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) 函數所產生的 guid 字串格式不同，其格式為 "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"。 如需詳細資訊和示範如何從 GUID 建立可系結字串的程式碼範例，請參閱 [建立 guid 之可系結字串表示的範例程式碼](example-code-for-creating-a-bindable-string-representation-of-a-guid.md)。

若要系結至物件中 **otherWellKnownObjects** 所指定的物件，請指定 " &lt; XXXXX &gt; " 作為物件已知物件 GUID 的系結字串形式。 如需詳細資訊，請參閱 [讀取物件的 objectGUID 和建立 GUID 的字串表示](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md)。 如需有關在物件上設定 **otherWellKnownObjects** 屬性的詳細資訊，請參閱 [使用 otherWellKnownObjects 屬性啟用 Rename-Safe](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)系結。

若要系結至 domainDNS 或設定容器中的 **wellKnownObjects** 所指定的物件，請指定 " &lt; XXXXX &gt; " 作為下列其中一個常數（如下表所示），如 Ntdsapi. h 中所定義。



| 容器          | GUID 識別碼                         |
|--------------------|-----------------------------------------|
| 使用者              | GUID \_ 使用者 \_ 容器 \_ W               |
| 電腦          | GUID \_ COMPUTRS \_ 容器 \_ W            |
| 系統             | GUID \_ 系統 \_ 容器 \_ W             |
| 網域控制站 | GUID \_ 域 \_ 控制器 \_ 容器 \_ W |
| 基礎結構     | GUID \_ 基礎結構 \_ 容器 \_ W      |
| 已刪除的物件    | GUID \_ 刪除的 \_ 物件 \_ 容器 \_ W    |
| 遺失並找到     | GUID \_ LOSTANDFOUND \_ 容器 \_ W        |



 

例如，若要系結至網域中的使用者容器，請指定 **GUID \_ 使用者容器（ \_ \_ W** ）作為 " &lt; XXXXX &gt; "。

「 &lt; 容器 DN」 &gt; 是容器物件的辨別名稱，此物件在其 **wellKnownObjects** 屬性中會以值表示。 例如，若要系結至網域中的使用者容器，請將網域辨別名稱指定為「 &lt; 容器 DN」 &gt; 。

例如，若要系結至網域 Fabrikam.com 的 users 容器，請使用下列系結字串。

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

如需詳細資訊和示範如何系結至已知 GUID 的程式碼範例，請參閱系結 [至已知物件的範例程式碼](example-code-for-binding-to-well-known-objects.md)。

 

 