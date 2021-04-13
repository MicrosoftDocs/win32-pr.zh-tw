---
title: 格式識別碼/位移組
description: 屬性集資料流程的第二個部分包含一組格式識別碼/位移配對。
ms.assetid: cc3a748d-e81c-45da-b04f-ea986158a4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f80a85175278b92fedbfd7b2d50d94007b7e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300648"
---
# <a name="format-identifieroffset-pair"></a>格式識別碼/位移組

屬性集資料流程的第二個部分包含一組格式識別碼/位移配對。 FMTID 是屬性集的名稱;它會唯一識別如何解讀下一節的內容。 位移是從整個資料流程開始到區段開始位置的距離（以位元組為單位）。

下列結構對處理格式識別碼/位移組很有説明。

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




