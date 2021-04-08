---
title: AnimationNames 集合
description: AnimationNames 集合
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e0c2c1d42f51f9d50bafaee61b6ab51d5b85f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840052"
---
# <a name="the-animationnames-collection"></a>AnimationNames 集合

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

[**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**)集合是特殊的集合，其中包含針對字元編譯的動畫名稱清單。 您可以使用集合來列舉字元的動畫名稱。 例如，在 Visual Basic 或 VBScript (2.0 或更新版本中) 您可以使用 For Each 的來存取這些名稱 ... **下一個** 語句：


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



集合中的專案沒有屬性，因此無法直接存取個別專案。

出於.ACF 字元，集合會傳回已針對字元定義的所有動畫，而不只是使用 [**Get**](get-method.md) 方法抓取的動畫。

 

 




