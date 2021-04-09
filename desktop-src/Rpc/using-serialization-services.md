---
title: 使用序列化服務
description: MIDL 會為具有屬性 \ 編碼 \ 和 \ 解碼 \ 的程式產生序列化存根。
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- 使用序列化服務的遠端程序呼叫 RPC、工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317156a2da954e001b687cca12eb0c6df23ef4ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024048"
---
# <a name="using-serialization-services"></a><span data-ttu-id="d41df-104">使用序列化服務</span><span class="sxs-lookup"><span data-stu-id="d41df-104">Using Serialization Services</span></span>

<span data-ttu-id="d41df-105">MIDL 會為具有屬性編碼和解碼的程式產生序列化存根 \[ [](/windows/desktop/Midl/encode) \] \[ [](/windows/desktop/Midl/decode) \] 。</span><span class="sxs-lookup"><span data-stu-id="d41df-105">MIDL generates a serialization stub for the procedure with the attributes \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\].</span></span> <span data-ttu-id="d41df-106">當您呼叫這個常式時，您會執行序列化呼叫，而不是遠端呼叫。</span><span class="sxs-lookup"><span data-stu-id="d41df-106">When you call this routine, you execute a serialization call instead of a remote call.</span></span> <span data-ttu-id="d41df-107">程式引數會以一般方式封送處理到緩衝區或從緩衝區取消封送處理。</span><span class="sxs-lookup"><span data-stu-id="d41df-107">The procedure arguments are marshaled to or unmarshaled from a buffer in the usual way.</span></span> <span data-ttu-id="d41df-108">然後，您就可以完全掌控緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d41df-108">You then have complete control of the buffers.</span></span>

<span data-ttu-id="d41df-109">相反地，當程式執行類型序列化時 (類型會標示序列化屬性) ，MIDL 會產生常式來調整該類型的物件大小、編碼和解碼。</span><span class="sxs-lookup"><span data-stu-id="d41df-109">In contrast, when your program performs type serialization (a type is labeled with serialization attributes), MIDL generates routines to size, encode, and decode objects of that type.</span></span> <span data-ttu-id="d41df-110">若要序列化資料，您必須以適當的方式呼叫這些常式。</span><span class="sxs-lookup"><span data-stu-id="d41df-110">To serialize data, you must call these routines in the appropriate way.</span></span> <span data-ttu-id="d41df-111">類型序列化是 Microsoft 擴充功能，因此當您在 DCE 相容性 ([**/osf**](/windows/desktop/Midl/-osf)) 模式中進行編譯時，就無法使用。</span><span class="sxs-lookup"><span data-stu-id="d41df-111">Type serialization is a Microsoft extension and, as such, is not available when you compile in DCE-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="d41df-112">藉由使用 \[ [**編碼**](/windows/desktop/Midl/encode) \] 和解碼 \[ [](/windows/desktop/Midl/decode) \] 屬性作為介面屬性，RPC 會將編碼套用至 IDL 檔案中定義的所有類型和常式。</span><span class="sxs-lookup"><span data-stu-id="d41df-112">By using the \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\] attributes as interface attributes, RPC applies encoding to all the types and routines defined in the IDL file.</span></span>

<span data-ttu-id="d41df-113">使用序列化服務時，您必須提供適當對齊的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d41df-113">You must supply adequately aligned buffers when using serialization services.</span></span> <span data-ttu-id="d41df-114">緩衝區的開頭必須對齊為8的倍數，或對齊8位元組的位址。</span><span class="sxs-lookup"><span data-stu-id="d41df-114">The beginning of the buffer must be aligned at an address that is a multiple of 8, or 8-byte aligned.</span></span> <span data-ttu-id="d41df-115">在程式序列化中，每個程序呼叫都必須封送處理為8位元組對齊的緩衝區位置或 unmarshal。</span><span class="sxs-lookup"><span data-stu-id="d41df-115">For procedure serialization, each procedure call must marshal into or unmarshal from a buffer position that is 8-byte aligned.</span></span> <span data-ttu-id="d41df-116">針對類型序列化，調整大小、編碼和解碼都必須從以8位元組對齊的位置開始。</span><span class="sxs-lookup"><span data-stu-id="d41df-116">For type serialization, sizing, encoding, and decoding must start at a position that is 8-byte aligned.</span></span>

<span data-ttu-id="d41df-117">讓您的應用程式確保其緩衝區對齊的其中一種方式，是寫入 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Midl/midl-user-allocate-1) 函式，使其建立對齊的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d41df-117">One way for your application to ensure that its buffers are aligned is to write the [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) function such that it creates aligned buffers.</span></span> <span data-ttu-id="d41df-118">下列程式碼範例會示範如何完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="d41df-118">The following code sample demonstrates how this can be done.</span></span>


```C++
#include <windows.h>

#define ALIGN_TO8(p)   (char *)((unsigned long)((char *)p + 7) & ~7)

void __RPC_FAR *__RPC_USER  MIDL_user_allocate(size_t sizeInBytes)
{
    unsigned char *pcAllocated;
    unsigned char *pcUserPtr;

    pcAllocated = (unsigned char *) malloc( sizeInBytes + 15 );
    pcUserPtr =  ALIGN_TO8( pcAllocated );
    if ( pcUserPtr == pcAllocated )
        pcUserPtr = pcAllocated + 8;

    *(pcUserPtr - 1) = pcUserPtr - pcAllocated;

    return( pcUserPtr );
}
```



<span data-ttu-id="d41df-119">下列範例顯示對應的 [**midl \_ 使用者 \_ free**](/windows/desktop/Midl/midl-user-free-1) 函數。</span><span class="sxs-lookup"><span data-stu-id="d41df-119">The following example shows the corresponding [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) function.</span></span>


```C++
void __RPC_USER  MIDL_user_free(void __RPC_FAR *f)
{
    unsigned char * pcAllocated;
    unsigned char * pcUserPtr;

    pcUserPtr = (unsigned char *) f;
    pcAllocated = pcUserPtr - *(pcUserPtr - 1);

    free( pcAllocated );
}
```



 

 