---
title: IPropertyBag 和 IPersistPropertyBag
description: IPropertyBag 和 IPersistPropertyBag
ms.assetid: 128e847b-99f9-44a3-9176-56eb34f3dddc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de08d8af50ae9a0b91166a4f41c8a11d8c6eb69c4ffd77f93b2566c901342ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048086"
---
# <a name="ipropertybag-and-ipersistpropertybag"></a>IPropertyBag 和 IPersistPropertyBag

[**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag)和 [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)會將 [另存新檔] 機制優化，因此建議用於執行「另存為文字」機制的 ActiveX 控制容器。 **IPropertyBag** 是由容器所執行，大致類似于 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)。 **IPersistPropertyBag** 是由控制項所執行，大致上與 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)類似。

 

 