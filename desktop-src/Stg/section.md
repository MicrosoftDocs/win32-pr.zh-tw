---
title: 區段
description: 區段是屬性集資料流程的第三個部分，而且包含實際的屬性集值。
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f51891d14a9690e295379b7bcf619fe0fbe19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966187"
---
# <a name="section"></a>區段

區段是屬性集資料流程的第三個部分，而且包含實際的屬性集值。

區段包含：

-   區段的位元組計數（包含位元組計數本身）。
-   32位屬性識別碼/位移組的陣列。
-   屬性類型指標/值組的陣列。

位移是從區段開頭到屬性開頭的距離 (類型、值) 組。 這可讓您以位元組陣列的形式複製區段，而不需要任何內部結構的轉譯。

下列虛擬結構說明區段的格式。

``` syntax
typedef struct tagPROPERTYSECTIONHEADER 
{ 
    DWORD  cbSection ;    // Size of Section 
    DWORD  cProperties ;  // Count of Properties in section 
} PROPERTYSECTIONHEADER; 
 
typedef struct tagPROPERTYIDOFFSET 
{ 
    DWORD  propid;    // Name of property 
    DWORD  dwOffset;  // Offset from start of section to property 
} PROPERTYIDOFFSET; 
 
typedef struct tagSERIALIZEDPROPERTYVALUE 
{ 
    DWORD  dwType;    // Property Type 
    BYTE   rgb[];     // Property Value 
} SERIALIZEDPROPERTYVALUE ;
```

 

 




