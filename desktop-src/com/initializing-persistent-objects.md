---
title: 初始化持續性物件
description: 初始化持續性物件
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549194"
---
# <a name="initializing-persistent-objects"></a>初始化持續性物件

數個持續性物件介面 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)、 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))和 [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)，可讓用戶端將物件初始化為「全新」或「預設」狀態。 這個初始狀態與新建立的物件（沒有狀態）不同。

將物件的狀態（甚至是預設狀態）初始化可能是需要大量計算或需要大量資源的作業。 藉由分隔建立與初始化，只有在實際需要時才會執行初始化，用戶端可以避免將物件初始化為預設狀態，以立即載入先前儲存的資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[持續性物件介面](persistent-object-interfaces.md)
</dt> </dl>

 

 