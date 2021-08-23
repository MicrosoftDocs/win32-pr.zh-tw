---
title: 遞增處理常式參考計數
description: 遞增處理常式參考計數
ms.assetid: 9e71ce1f-5805-4240-9dcc-7e71fbabfe7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767efbd97525be49c0cf4604d2b90d068a2b81d78589627bf0654f3048e03548
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690588"
---
# <a name="incrementing-the-handler-reference-count"></a>遞增處理常式參考計數

**AddRef** 方法會遞增資料流程處理常式或檔案處理常式的參考計數。


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::AddRef() 
{ 
    return ++m_refs; 
} 

```



 

 




