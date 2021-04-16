---
title: 儲存體介面
description: 儲存體介面
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab06d8d0920ca7b29619df2173aaa0897c6eef6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508156"
---
# <a name="storage-interfaces"></a>儲存體介面

控制項容器必須能夠支援執行 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)或 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)的控制項。 （選擇性）容器可支援任何其他持續性介面，例如 [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))、 [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))和 [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) 提供支援的控制項。

當 ActiveX 控制項容器選擇並初始化儲存介面以使用 ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)、 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)等) 之後，該儲存體介面將會在控制項的存留期內維持主要儲存介面，也就是控制項將仍擁有儲存體。 這並不會阻止容器儲存到其他儲存介面。

ActiveX 控制項容器不需要支援另存為文字機制，因此使用 [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) 和相關聯的容器端介面 [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) 是選擇性的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[容器](containers.md)
</dt> </dl>

 

 