---
title: 虛擬函式資料表
description: 虛擬函式資料表
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966180"
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



 

 




