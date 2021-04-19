---
title: 列舉使用者
description: 不同于 Windows NT 4.0 網域，Windows 2000 使用者可以放在任何容器或組織單位 (OU) 在網域中，也可以放在網域的根目錄中。
ms.assetid: 4a35af7a-f43b-4cf9-a030-77f6c2518ae7
ms.tgt_platform: multiple
keywords:
- 列舉使用者廣告
- 使用者廣告，列舉使用者
- Active Directory、使用、使用者、列舉使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e922d92f4313ed0238ff068f7ae1c0fbf693d497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106967254"
---
# <a name="enumerating-users"></a>列舉使用者

不同于 Windows NT 4.0 網域，Windows 2000 使用者可以放在任何容器或組織單位 (OU) 在網域中，也可以放在網域的根目錄中。 這表示使用者可以位於目錄階層中的多個位置。 因此，您有兩個列舉使用者的選擇：

-   列舉直接包含在容器、OU 或網域根目錄中的使用者：

    明確系結至包含您感興趣列舉之使用者的容器物件，使用 [**IADsContainer. filter**](/windows/desktop/ADSI/iadscontainer-property-methods)屬性將包含 "user" 的篩選設定為類別，並使用 [**IADsContainer：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum)方法來列舉使用者物件。

    這項技術可以用來列舉直接包含在容器或 OU 物件中的使用者。 如果容器包含可能包含其他使用者的其他容器，您必須系結至這些容器，並以遞迴方式列舉這些容器上的使用者。 如果您不需要操作使用者物件，且只需要讀取特定屬性，請使用選項2中所述的深層搜尋。

    因為列舉會傳回代表每個使用者物件之 ADSI COM 物件的指標，所以您可以呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得使用者物件的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads)、 [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)和 [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) 介面指標。 這表示您可以取得容器中每個列舉使用者物件的介面指標，而不需要明確地系結至每個使用者物件。 若要直接對容器內的所有使用者執行作業，列舉可避免必須系結至每個使用者，才能呼叫 **IADs** 或 **IADsUser** 方法。 若要取得使用者的特定屬性，請使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) ，如選項2所述。

-   針對 (& (objectClass = user)  (objectCategory = person) ) 尋找樹狀結構中的所有使用者，執行深層搜尋：

    首先，系結至要開始搜尋的容器物件。 例如，若要尋找網域中的所有使用者，請系結至網域的根目錄。若要尋找樹系中的所有使用者，請系結至通用類別目錄，然後從 GC 的根目錄進行搜尋。

    然後使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 來查詢包含 (& 的搜尋篩選準則， (objectClass = User)  (objectCategory = person) ) 和搜尋偏好的 ADS \_ 範圍 \_ 子樹。

    您可以使用 ADS 範圍 ONELEVEL 的搜尋喜好設定來執行搜尋 \_ \_ ，以將搜尋限制為您所系結之容器物件的直接內容。

    [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 只會抓取使用者的特定屬性值。 若要取出值，請使用 **>idirectorysearch**。 若要操作從搜尋傳回的使用者物件，也就是您想要使用 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 或 [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) 方法，您必須明確地系結至這些方法。 若要這樣做，請將 **distinguishedName** 指定為要從搜尋傳回的其中一個屬性，並使用傳回的分辨名稱來系結至搜尋中傳回的每個使用者。

    只會抓取特定屬性。 您無法在未明確指定使用者類別的每個可能屬性的情況下，取得所有屬性。

 

 