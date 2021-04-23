---
description: 記憶體配置器
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: 記憶體配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909417"
---
# <a name="memory-allocator"></a>記憶體配置器

記憶體配置器物件會配置媒體範例的緩衝區。 篩選器可以使用此物件來配置共用記憶體緩衝區;不過，具有特殊需求的篩選也可以執行它自己的記憶體配置器物件。 藉由呼叫 **CoCreateInstance** 來建立此物件。



| 標籤 | 值 |
|------------------|----------------------------------------|
| 類別識別碼 | CLSID \_ MemoryAllocator                 |
| 介面       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 物件](directshow-objects.md)
</dt> </dl>

 

 



