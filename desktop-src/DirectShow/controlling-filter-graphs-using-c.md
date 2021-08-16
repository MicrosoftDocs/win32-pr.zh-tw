---
description: 使用 C 控制篩選圖形
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: 使用 C 控制篩選圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e234413f7642d7349c2bf378d1aded97b399e252117b0793f90335de8643912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073752"
---
# <a name="controlling-filter-graphs-using-c"></a>使用 C 控制篩選圖形

如果您要使用 c (（而不是 c + +) ）撰寫 DirectShow 的應用程式，則必須使用 vtable 指標來呼叫方法。 下列範例說明如何從以 C 撰寫的應用程式呼叫 **IUnknown：： QueryInterface** 方法：


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



以下顯示 c + + 中的對等呼叫：


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



在 C 中，COM 介面會定義為結構。 **LpVtbl** 成員是介面方法資料表的指標， (vtable) 。 所有方法都採用額外的參數，也就是介面的指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[附錄](appendixes.md)
</dt> </dl>

 

 



