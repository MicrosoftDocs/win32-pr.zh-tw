---
title: 效能特色
description: 呼叫 IPropertySetStorage 介面的 COM 複合檔案執行以建立屬性集，會導致透過呼叫 IStorage CreateStream 或 IStorage CreateStorage 來建立資料流程或儲存體。
ms.assetid: 7773e649-19a4-4df2-84ed-027d73283140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac11200b021cae1ea1d60438b57530f0dbc8c02ea3d26b5622ab859a99224aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960828"
---
# <a name="performance-characteristics"></a>效能特色

呼叫 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面的 COM 複合檔案執行以建立屬性集，會導致透過呼叫 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) 或 [**IStorage：： CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)來建立資料流程或儲存體。 預設屬性集是在記憶體中建立的，但不會排清到磁片。 當呼叫 [**IPropertyStorage：： WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)時，它會在緩衝區內運作。

當屬性集開啟時，就會使用 [IStorage：： OpenStream](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 或 [IStorage：： OpenStorage](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) 。 整個屬性集資料流程會讀入連續的記憶體中。 [**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) 作業接著會讀取記憶體緩衝區來操作。 因此，第一次存取的時間很昂貴 (因為磁片讀取) 但後續的存取非常有效率。 寫入可能會稍微昂貴，因為在新增資料時，可能需要基礎資料流程上的 SetSize 作業，以保證磁碟空間可供使用。

無論 [**IPropertyStorage：： WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) 是否會排清更新，都不會做出任何保證。 一般而言，用戶端應該假設 **IPropertyStorage：： WriteMultiple** 只會更新記憶體緩衝區中的。 若要排清資料，應該呼叫 [**IPropertyStorage：： Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) 或 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (上一個發行) 。

此設計表示 [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) 可能會成功，但不會實際持續寫入資料。

> [!Note]  
> 這個屬性集資料流程的大小不能超過256K 個位元組。

 

 

 