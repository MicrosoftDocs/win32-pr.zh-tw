---
title: 虛擬函式資料表
description: 虛擬函式資料表
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b403debddeecbbfe099224943ac6cdf0a1875dff9c19ea08a96e9cb029875a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135495"
---
# <a name="virtual-function-tables"></a>虛擬函式資料表

虛擬函式資料表是物件所支援之方法的指標陣列。 如果您使用的是 C，則物件會顯示為結構，其第一個成員是虛擬函式資料表的指標 (**lpVtbl**) ;也就是說，第一個成員指向包含函式指標的陣列。 所有方法都採用函式資料表的指標做為第一個參數。 因此，下列範例會呼叫 **pStream** 物件的 **Read** 方法：


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



在 C + + 中，虛擬函式資料表的指標（ *this* 指標）是隱含的。 下列程式相當於使用 C + + 時的上一個範例：


```C++
pStream->Read(parameters) 
 
```



 

 




