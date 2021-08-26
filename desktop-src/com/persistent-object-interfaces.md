---
title: COM)  (持續性物件介面
description: 持續性物件會執行一個或多個持續性物件介面。
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ee1062c80a5c40d139965e0e3bebf96cbda534062322e218e2f5a7da586ff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120408"
---
# <a name="persistent-object-interfaces"></a>持續性物件介面

持續性物件會執行一個或多個 *持續性物件介面*。 用戶端會使用持續性物件介面，來告知這些物件何時以及要儲存其狀態的位置。 所有的持續性物件介面都是衍生自 [**IPersist**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist)，因此任何實作為持續性物件介面的物件也會實作為 **IPersist**。

目前已定義下列持續性物件介面：

-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))
-   [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))
-   [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))

實施者會根據物件的使用方式，選擇物件支援的持續性物件介面。 藉由不支援任何持續性物件介面，實施者實際上會說：「這個物件的狀態無法持續儲存」。 藉由支援一或多個持續性物件介面，實施者實際上會說：「這個物件的狀態可以持續儲存在一或多個資料存放區媒體中」。

例如，下表列出數個允許不同持續性物件介面支援的物件類型。



| 類別                            | 通常支援持續性物件介面                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 名字<br/>                 | [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| OLE 內嵌物件<br/>   | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |
| ActiveX 控制項<br/>         | [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)、 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、IPersistMemory、IPersistPropertyBag、 [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/> |
| ActiveX 檔物件<br/> | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |



 

用戶端實施者也可以選擇用戶端可以使用的持續性物件介面。 用戶端使用的介面通常是由用戶端可以儲存本身資料的位置所決定。 只能將其資料儲存在一般檔案中的用戶端，可能只會使用 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)、 [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))和 IPersistPropertyBag。  (**IPersistStreamInit** 可以在大部分的應用程式中取代 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ，因為它包含該定義並新增初始化方法。 ) 可將其資料儲存至結構化儲存體檔案的用戶端，也會使用 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[初始化持續性物件](initializing-persistent-objects.md)
</dt> </dl>

 

