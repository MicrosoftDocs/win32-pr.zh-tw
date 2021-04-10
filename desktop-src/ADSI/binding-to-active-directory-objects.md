---
title: 系結至 Active Directory 物件
description: 繼續進行此案例之前，您必須先瞭解 ADSI 物件在 Active Directory 中的命名方式，以及如何加以系結。 系結 ADSI 物件會將物件與目錄服務連接，並可讓您存取物件的方法。
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020807"
---
# <a name="binding-to-active-directory-objects"></a>系結至 Active Directory 物件

繼續進行此案例之前，您必須先瞭解 ADSI 物件在 Active Directory 中的命名方式，以及如何加以系結。 系結 ADSI 物件會將物件與目錄服務連接，並可讓您存取物件的方法。

## <a name="adspath"></a>ADsPath

ADSI 物件是由其系結字串（也稱為 ADsPath）唯一識別。 ADsPath 是 ADSI 提供者的程式設計識別碼 (progID) 的組合，以及物件的分辨名稱 (DN) 。

以下是 ADsPath 的格式：

"progID://DN"

-   pogID： ADSI 提供者的程式設計識別碼，例如 LDAP 或 WinNT。

-   ：//-分隔 progID 與 DN。

-   DN-ADSI 物件的辨別名稱，也就是物件的完整路徑，其中路徑是由 (RDNs) 的相對辨別名稱所組成。

RDN 是沒有路徑的物件名稱，而且在其同級物件中是唯一的。 RDN 包含屬性識別碼和值（例如 "DC = Fabrikam"），其中 DC 是屬性，而 Fabrikam 是值。 DC 是代表網域元件的 RDN 屬性識別碼。

以下是 ADsPath 的範例：

"LDAP：//DC = Fabrikam，DC = Com"

## <a name="binding-the-object"></a>系結物件

以下是您可以在此案例中系結網域物件的方式：


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



當您執行此程式碼範例時，ADSI 會使用 DN 來判斷要系結的 ADSI 物件。 ADSI 系結這些物件之後，您就可以存取它們的方法。 先前的程式碼範例會將網域物件系結至 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 和 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)。 您現在可以在這些介面上使用方法，例如 [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get)、 [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put)、 [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)、 [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)和 [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere)。

系結網域物件之後，您可以列印其部分屬性：


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



如需 ADsPath 的詳細資訊，請參閱系結 [字串](binding-string.md)。 如需系結的詳細資訊，請參閱系結 [至 ADSI 物件](binding-to-an-adsi-object.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立組織單位](creating-an-organizational-unit.md)
</dt> </dl>

 

 




