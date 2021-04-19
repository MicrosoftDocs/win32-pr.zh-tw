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
# <a name="implementing-attachproperties"></a><span data-ttu-id="77612-103">執行 AttachProperties</span><span class="sxs-lookup"><span data-stu-id="77612-103">Implementing AttachProperties</span></span>

<span data-ttu-id="77612-104">網路監視器會呼叫 [**AttachProperties**](attachproperties.md) 函數，以對應存在於已辨識資料片段中的屬性。</span><span class="sxs-lookup"><span data-stu-id="77612-104">Network Monitor calls the [**AttachProperties**](attachproperties.md) function to map the properties that exist in a piece of recognized data.</span></span> <span data-ttu-id="77612-105">[**AttachProperties**](attachproperties.md)函式會將屬性對應至特定位置。</span><span class="sxs-lookup"><span data-stu-id="77612-105">The [**AttachProperties**](attachproperties.md) function maps the properties to a specific location.</span></span>

<span data-ttu-id="77612-106">網路監視器會使用下列進程來剖析框架中的資料。</span><span class="sxs-lookup"><span data-stu-id="77612-106">Network Monitor uses the following process to parse the data in a frame.</span></span>

-   <span data-ttu-id="77612-107">首先，網路監視器會呼叫 [RecognizeFrame](recognizeframe.md) 來辨識存在於框架中的所有通訊協定。</span><span class="sxs-lookup"><span data-stu-id="77612-107">First, Network Monitor calls [RecognizeFrame](recognizeframe.md) to recognize all the protocols that exist in a frame.</span></span>
-   <span data-ttu-id="77612-108">然後，網路監視器會針對辨識資料片段的每個剖析器呼叫 [**AttachProperties**](attachproperties.md) 。</span><span class="sxs-lookup"><span data-stu-id="77612-108">Then, Network Monitor calls [**AttachProperties**](attachproperties.md) for each parser that recognizes a piece of data.</span></span>

<span data-ttu-id="77612-109">當網路監視器針對辨識的資料呼叫 [AttachProperties](attachproperties.md) 函式時，呼叫的剖析器必須剖析資料，然後將每個現有的屬性對應至已辨識資料中的位置。</span><span class="sxs-lookup"><span data-stu-id="77612-109">When Network Monitor calls the [AttachProperties](attachproperties.md) function for the recognized data, the parser that is called must parse the data, and then map each existing property to a location in the recognized data.</span></span> <span data-ttu-id="77612-110">剖析器會判斷存在哪些屬性，以及每個屬性在資料中的所在位置。</span><span class="sxs-lookup"><span data-stu-id="77612-110">The parser determines which properties exist, and where each property is located in the data.</span></span> <span data-ttu-id="77612-111">下圖顯示剖析器辨識的資料。</span><span class="sxs-lookup"><span data-stu-id="77612-111">The following figure shows parser-recognized data.</span></span>

![剖析器-辨識的資料](images/attachproperties1.png)

<span data-ttu-id="77612-113">在 [**AttachProperties**](attachproperties.md)的執行期間，您必須針對存在於資料框架中的每個屬性，呼叫下列其中一個函數。</span><span class="sxs-lookup"><span data-stu-id="77612-113">During the implementation of [**AttachProperties**](attachproperties.md), you must call one of the following functions for each property that exists in a data frame.</span></span>

-   <span data-ttu-id="77612-114">當您想要修改框架中的屬性資料時，請呼叫 [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="77612-114">Call the [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function when you want to modify the property data in a frame.</span></span>
-   <span data-ttu-id="77612-115">當您不想要修改框架中的屬性資料時，請呼叫 [**AttachPropertyInstance**](attachpropertyinstance.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="77612-115">Call the [**AttachPropertyInstance**](attachpropertyinstance.md) function when you do not want to modify the property data in a frame.</span></span>

> [!Note]  
> <span data-ttu-id="77612-116">建議您使用存在於捕捉中的資料。</span><span class="sxs-lookup"><span data-stu-id="77612-116">It is recommended that you use the data as it exists in the capture.</span></span>

 

<span data-ttu-id="77612-117">下列程式識別執行 [**AttachProperties**](attachproperties.md)所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="77612-117">The following procedure identifies the steps necessary to implement [**AttachProperties**](attachproperties.md).</span></span>

<span data-ttu-id="77612-118">**若要執行 AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="77612-118">**To implement AttachProperties**</span></span>

1.  <span data-ttu-id="77612-119">判斷哪些屬性存在，以及資料中的屬性位置。</span><span class="sxs-lookup"><span data-stu-id="77612-119">Determine which properties exist, and the property location in the data.</span></span>
2.  <span data-ttu-id="77612-120">使用您想要修改的值，呼叫每個屬性的 [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) 。</span><span class="sxs-lookup"><span data-stu-id="77612-120">Call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) for each property with a value that you want to modify.</span></span>
3.  <span data-ttu-id="77612-121">使用您不想要修改的值，呼叫每個屬性的 [**AttachPropertyInstance**](attachpropertyinstance.md) 。</span><span class="sxs-lookup"><span data-stu-id="77612-121">Call [**AttachPropertyInstance**](attachpropertyinstance.md) for each property with a value that you do not want to modify.</span></span> <span data-ttu-id="77612-122">一般來說，這是您唯一需要呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="77612-122">Typically, this is the only function that you need to call.</span></span>

<span data-ttu-id="77612-123">以下是 [**AttachProperties**](attachproperties.md)的基本執行。</span><span class="sxs-lookup"><span data-stu-id="77612-123">The following is a basic implementation of [**AttachProperties**](attachproperties.md).</span></span> <span data-ttu-id="77612-124">請注意，此範例不包含判斷哪些屬性存在的程式碼，或是用來尋找屬性的程式碼。</span><span class="sxs-lookup"><span data-stu-id="77612-124">Be aware that the example does not include either the code to determine which properties exist, or the code to locate the properties.</span></span>

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

 

 



