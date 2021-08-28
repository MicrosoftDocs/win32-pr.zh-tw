---
title: 使用 objectGUID 系結至物件
description: 如果物件已重新命名或移動，則物件辨別名稱會變更，因此辨別名稱不是可靠的物件識別碼。
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- 使用 objectGUID 系結至物件廣告
- objectGUID AD
- objectGUID AD，用來系結至物件
- Active Directory、使用、系結、使用 objectGUID 系結至物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c310ad1041c072dc126a761fab5fa104fa00c4f98e4fa01d45ca7bc24c11b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024486"
---
# <a name="using-objectguid-to-bind-to-an-object"></a>使用 objectGUID 系結至物件

如果物件已重新命名或移動，則物件辨別名稱會變更，因此辨別名稱不是可靠的物件識別碼。 在 Active Directory Domain Services 中，即使物件已重新命名或移動，物件的 **objectGUID** 屬性也永遠不會變更。 如需 **objectGUID** 和識別碼的詳細資訊，請參閱 [物件名稱和](object-names-and-identities.md)識別。

Active Directory LDAP 提供者會提供方法，以使用物件 GUID 系結至物件。 系結字串格式如下所示：


```C++
LDAP://servername/<GUID=XXXXX>
```



在此範例中，"servername" 是目錄伺服器的名稱，而 "XXXXX" 是 GUID 十六進位值的字串表示。 "Servername" 是選擇性的。 GUID 字串是在 "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" 表單中指定。 GUID 字串也可以採用 "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX" 格式，此格式與 [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) 函式所產生的字串相同，沒有周圍的大括弧 " {} "。 如需詳細資訊和示範如何從 GUID 建立可系結字串的程式碼範例，請參閱 [建立 guid 之可系結字串表示的範例程式碼](example-code-for-creating-a-bindable-string-representation-of-a-guid.md)。 [**IADS guid**](/windows/desktop/ADSI/iads-property-methods)屬性可以用來抓取 GUID 的適當字串形式。

使用物件 GUID 進行系結時，不支援某些 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 和 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 方法和屬性。 使用物件 GUID 的系結所取得的物件不支援下列 **IADs** 屬性：

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**名稱**](/windows/desktop/ADSI/iads-property-methods)
-   [**父代**](/windows/desktop/ADSI/iads-property-methods)

使用物件 GUID 的系結所取得的物件不支援下列 **IADsContainer** 方法：

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**建立**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**刪除**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

若要在使用物件 GUID 系結至物件之後使用這些方法和屬性，請使用 [**IADs 取得**](/windows/desktop/api/iads/nf-iads-iads-get) 物件辨別名稱，然後使用辨別名稱再次系結至物件。

如果應用程式儲存或快取識別碼或參考儲存在 Active Directory Domain Services 中的物件，則物件 GUID 是要使用的最佳識別碼，原因如下：

-   即使物件已重新命名或移動，on 物件的 **objectGUID** 屬性也永遠不會變更。
-   使用物件 GUID 系結至物件很容易。
-   如果物件已重新命名或移動， **objectGUID** 屬性會提供單一識別碼，可用來快速尋找和識別物件，而不需要撰寫具有可識別該物件之所有屬性條件的查詢。

 

 