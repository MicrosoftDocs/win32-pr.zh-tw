---
title: 儲存體介面
description: 儲存體介面
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c378b37c020f15e0fe497249b2834faffefc232bc184564f80fdb247550033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129700"
---
# <a name="storage-interfaces"></a>儲存體介面

控制項容器必須能夠支援執行 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)或 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)的控制項。 （選擇性）容器可支援任何其他持續性介面，例如 [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))、 [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)和 [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) 提供支援的控制項。

一旦 ActiveX 的控制項容器選擇並初始化儲存介面以使用 ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)、 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)等) 之後，該儲存體介面將會在控制項的存留期內維持主要儲存介面，也就是控制項仍會保留在儲存體中。 這並不會阻止容器儲存到其他儲存介面。

ActiveX 控制容器不需要支援另存為文字機制，因此使用 [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)和相關聯的容器端介面 [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag)是選擇性的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[容器](containers.md)
</dt> </dl>

 

 