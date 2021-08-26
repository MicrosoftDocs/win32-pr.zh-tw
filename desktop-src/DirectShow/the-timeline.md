---
description: 時間軸
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: 時間軸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f298c2649a280bf5fd622d5fb5a2aef820d1f340d45f7e2beb83fe9edd6a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049998"
---
# <a name="the-timeline"></a>時間軸

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

時間軸會顯示 [**IAMTimeline**](iamtimeline.md) 介面。 此介面包含在時間軸上設定屬性的方法;將群組新增至時間軸;以及建立時間軸物件，例如群組、追蹤和來源。 若要建立新的時間軸，請呼叫標準 **CoCreateInstance** 函數，如下所示：


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



新的時間軸是空的。 此時您可以載入現有的專案檔 (查看[載入和預覽 Project](loading-and-previewing-a-project.md)) ，或建立和插入新的物件來建立時間軸 (查看[建立時間軸](constructing-a-timeline.md)) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[時間軸元件的總覽](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



