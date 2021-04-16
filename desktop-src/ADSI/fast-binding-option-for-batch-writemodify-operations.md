---
title: 批次寫入/修改作業的快速系結選項
description: 當目錄服務物件系結至時，ADSI 會建立代表指定目錄物件的 COM 物件。
ms.assetid: cf41b0c4-7459-49cf-945b-8462c7d19947
ms.tgt_platform: multiple
keywords:
- 批次寫入/修改作業的快速系結選項 ADSI
- 適用于批次寫入/修改作業的 ADSI ADSI、Using、Fast Binding 選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322cf3c8b5f40dc43304f95d08ff53a7c5c14217
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508132"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a>批次寫入/修改作業的快速系結選項

當目錄服務物件系結至時，ADSI 會建立代表指定目錄物件的 COM 物件。 當系結時，ADSI 通常會取出 **objectClass** 屬性，讓 adsi 能夠公開適用于該物件類別的 COM 介面。 例如，除了支援所有物件的基底 ADSI 介面外，使用者物件也會公開 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) 介面。 針對單一作業，這應該不會影響效能。 但是，如果執行的批次作業需要數百個或數千個系結，而且這些作業正在將資料寫入目錄服務，則可能需要交換完整物件支援以加快系結的速度。 這就是所謂的快速系結，可在呼叫 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)或 [**IADsOpenDSObject：： Objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)時指定 **ADS \_ fast \_ bind** 旗標來完成。

快速系結具有下列限制：

-   系結作業必須使用 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 函數或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 方法來執行。 系結作業會移至目錄伺服器一次，而不是兩次。 ADSI 不會取出 **objectClass** 屬性，因此只會公開物件的基底 ADSI 介面。
-   COM 物件支援下列介面：

    -   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
    -   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
    -   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
    -   [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
    -   [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
    -   [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
    -   [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
    -   [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)

-   如果使用 [**IADsContainer：： GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) 方法系結至子物件，子物件就會具有與父系相同的快速系結特性。
-   系結作業期間不會驗證要系結的物件，因此，如果物件不存在，後續的方法呼叫會失敗。 因此，快速系結應僅用於已知存在的物件，例如，在執行傳回所系結之物件辨別名稱的查詢之後，直接系結。
-   ADSI 擴充功能會公開給 **top** 類別的物件。 因此，只會公開上面所列之基底 ADSI 介面的延伸模組。

 

 