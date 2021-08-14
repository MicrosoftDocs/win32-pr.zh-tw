---
title: 列舉定義域中的群組
description: 群組可以放在任何容器或組織單位中， (OU) 在網域中，也可以放在網域的根目錄中。
ms.assetid: 7f9d3c90-b6f4-4bfa-960f-58f380aa487c
ms.tgt_platform: multiple
keywords:
- 列舉網域 AD 中的群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3723122ef2ab70a7396b2b2821c96a20b4d92419c1e10d1c00b11ff903cb6719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429844"
---
# <a name="enumerating-groups-in-a-domain"></a>列舉定義域中的群組

群組可以放在任何容器或組織單位中， (OU) 在網域中，也可以放在網域的根目錄中。 這表示群組可以位於目錄階層中的多個位置。 因此，您有兩個列舉群組的選擇：

1.  列舉直接包含在容器、OU 或網域根目錄中的群組。

    明確系結至包含要列舉之群組的容器物件，使用 [**IADsContainer. filter**](/windows/desktop/api/iads/nn-iads-iadscontainer)屬性將包含 "groups" 的篩選器設定為類別，並使用 [**IADsContainer：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum)方法來列舉群組物件。

    這項技術會列舉直接包含在容器或 OU 物件中的群組。 如果容器包含其他可能包含其他群組的容器，您就必須系結至這些容器，並以遞迴方式列舉這些容器上的群組。 若要操作群組物件和唯讀特定屬性，請使用選項2中所述的深層搜尋。

    因為列舉會傳回代表每個群組物件的 ADSI COM 物件的指標，所以您可以呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得群組物件的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads)、 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)和 [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) 介面指標。也就是說，您可以取得容器中每個列舉群組物件的介面指標，而不需要明確地系結至每個群組物件。 若要直接在容器內對所有群組執行作業，列舉不需要系結至每個群組，就能呼叫 **IADs** 或 **IADsGroup** 方法。 若要從群組取出特定屬性，請使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) ，如第二個選項所述。

    當您嘗試列舉包含 W w n 安全性主體之成員的群組（例如 Everyone、已驗證的使用者、批次等等）時，就會發生例外狀況。 由於您無法系結至這些類型的物件，因此當您列舉 WinNT 範圍中的群組時，就不會列出這些物件，因為某些 IADs 方法（例如類別、ADsPath 和名稱）會在列舉成員上叫用時傳回正確的結果。

2.  執行 "objectCategory = group" 的深層搜尋，以尋找樹狀結構中的所有群組。

    首先，系結至要開始搜尋的容器物件。 例如，若要尋找網域中的所有群組，請系結至網域的根目錄。若要尋找樹系中的所有群組，請系結至通用類別目錄，然後從 GC 的根目錄進行搜尋。

    然後使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 來查詢包含 (objectCategory = group) 和搜尋 **ADS \_ 範圍 \_ 子樹** 之喜好設定的搜尋篩選準則。

    > [!Note]  
    > 您可以使用 **ADS \_ 範圍 \_ ONELEVEL** 的搜尋喜好設定來執行搜尋，以將搜尋限制為您所系結之容器物件的直接內容。

     

    [**>Idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 只會抓取群組中特定屬性的值。 若要取出值，請使用 **>idirectorysearch**。 若要操作從搜尋傳回的群組物件，也就是使用 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 或 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) 方法，請明確地系結至這些物件。 若要這樣做，請將 **distinguishedName** 指定為要從搜尋傳回的其中一個屬性，並使用傳回的分辨名稱來系結至搜尋中傳回的每個群組。

    只會抓取特定屬性。 您無法在未明確指定 group 類別的每個可能屬性的情況下，取得所有屬性。

 

 