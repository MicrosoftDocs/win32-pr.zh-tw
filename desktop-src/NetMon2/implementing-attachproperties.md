---
description: 呼叫 AttachProperties 函數，以對應存在於已辨識資料片段中的屬性。
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: 執行 AttachProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9cc032826a8749630c4951b46d456ca807fd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001347"
---
# <a name="implementing-attachproperties"></a>執行 AttachProperties

網路監視器會呼叫 [**AttachProperties**](attachproperties.md) 函數，以對應存在於已辨識資料片段中的屬性。 [**AttachProperties**](attachproperties.md)函式會將屬性對應至特定位置。

網路監視器會使用下列進程來剖析框架中的資料。

-   首先，網路監視器會呼叫 [RecognizeFrame](recognizeframe.md) 來辨識存在於框架中的所有通訊協定。
-   然後，網路監視器會針對辨識資料片段的每個剖析器呼叫 [**AttachProperties**](attachproperties.md) 。

當網路監視器針對辨識的資料呼叫 [AttachProperties](attachproperties.md) 函式時，呼叫的剖析器必須剖析資料，然後將每個現有的屬性對應至已辨識資料中的位置。 剖析器會判斷存在哪些屬性，以及每個屬性在資料中的所在位置。 下圖顯示剖析器辨識的資料。

![剖析器-辨識的資料](images/attachproperties1.png)

在 [**AttachProperties**](attachproperties.md)的執行期間，您必須針對存在於資料框架中的每個屬性，呼叫下列其中一個函數。

-   當您想要修改框架中的屬性資料時，請呼叫 [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) 函數。
-   當您不想要修改框架中的屬性資料時，請呼叫 [**AttachPropertyInstance**](attachpropertyinstance.md) 函數。

> [!Note]  
> 建議您使用存在於捕捉中的資料。

 

下列程式識別執行 [**AttachProperties**](attachproperties.md)所需的步驟。

**若要執行 AttachProperties**

1.  判斷哪些屬性存在，以及資料中的屬性位置。
2.  使用您想要修改的值，呼叫每個屬性的 [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) 。
3.  使用您不想要修改的值，呼叫每個屬性的 [**AttachPropertyInstance**](attachpropertyinstance.md) 。 一般來說，這是您唯一需要呼叫的函式。

以下是 [**AttachProperties**](attachproperties.md)的基本執行。 請注意，此範例不包含判斷哪些屬性存在的程式碼，或是用來尋找屬性的程式碼。

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



