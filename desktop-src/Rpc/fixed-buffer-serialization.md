---
title: 固定緩衝區序列化
description: 修正緩衝區序列化。
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87e3cad0a272ccd493cf9088fedeb272f1206b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372268"
---
# <a name="fixed-buffer-serialization"></a><span data-ttu-id="b9472-103">固定緩衝區序列化</span><span class="sxs-lookup"><span data-stu-id="b9472-103">Fixed Buffer Serialization</span></span>

<span data-ttu-id="b9472-104">使用固定的緩衝區樣式時，請指定夠大的緩衝區來容納編碼 (封送處理以控制碼執行的) 作業。</span><span class="sxs-lookup"><span data-stu-id="b9472-104">When using the fixed buffer style, specify a buffer that is large enough to accommodate the encoding (marshalling) operations performed with the handle.</span></span> <span data-ttu-id="b9472-105">當您進行封送時，您會提供包含要解碼之所有資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b9472-105">When unmarshaling, you provide the buffer that contains all of the data to decode.</span></span>

<span data-ttu-id="b9472-106">序列化的固定緩衝區樣式使用下列常式：</span><span class="sxs-lookup"><span data-stu-id="b9472-106">The fixed buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="b9472-107">**MesEncodeFixedBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="b9472-107">**MesEncodeFixedBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [<span data-ttu-id="b9472-108">**MesDecodeBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="b9472-108">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="b9472-109">**MesBufferHandleReset**</span><span class="sxs-lookup"><span data-stu-id="b9472-109">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="b9472-110">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="b9472-110">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="b9472-111">**MesEncodeFixedBufferHandleCreate** 函式會配置編碼控制碼所需的記憶體，然後將它初始化。</span><span class="sxs-lookup"><span data-stu-id="b9472-111">The **MesEncodeFixedBufferHandleCreate** function allocates the memory needed for the encoding handle, and then initializes it.</span></span> <span data-ttu-id="b9472-112">應用程式可以呼叫 [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) 來重新初始化控制碼，也可以呼叫 [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) 來釋放控制碼的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b9472-112">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle, or it can call [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="b9472-113">若要建立對應于固定樣式（編碼控制碼）的解碼控制碼，您必須使用 [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)。</span><span class="sxs-lookup"><span data-stu-id="b9472-113">To create a decoding handle corresponding to the fixed style–encoding handle, you must use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

<span data-ttu-id="b9472-114">應用程式會呼叫 [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) 來釋放編碼或解碼緩衝區控制碼。</span><span class="sxs-lookup"><span data-stu-id="b9472-114">The application calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the encoding or decoding buffer handle.</span></span>

## <a name="examples-of-fixed-buffer-encoding"></a><span data-ttu-id="b9472-115">固定緩衝區編碼的範例</span><span class="sxs-lookup"><span data-stu-id="b9472-115">Examples of Fixed Buffer Encoding</span></span>

<span data-ttu-id="b9472-116">下一節提供如何使用固定緩衝區樣式的範例–序列化進程編碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b9472-116">The following section provides an example of how to use a fixed buffer style–serializing handle for procedure encoding.</span></span>

``` syntax
/*This is a fragment of the IDL file defining MooProc */

...
void __RPC_USER
MyProc( [in] handle_t Handle, [in,out] MyType * pMyObject,
        [in, out] ThisType * pThisObject);
...

/*This is an ACF file. MyProc is defined in the IDL file */

[
    explicit_handle
]
interface regress
{
    [ encode,decode ] MyProc();
}
```

<span data-ttu-id="b9472-117">下列摘要表示應用程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="b9472-117">The following excerpt represents a part of an application.</span></span>

``` syntax
if (MesEncodeFixedBufferHandleCreate (
        Buffer, BufferSize, 
        pEncodedSize, &Handle) == RPC_S_OK)
{
    ...
    /* Manufacture a MyObject and a ThisObject */
    ...
    /* The serialization works from the beginning of the buffer because 
   the handle is in the initial state. The function MyProc does the    
   following when called with an encoding handle:
     - sizes all the parameters for marshalling,
     - marshalls into the buffer (and sets the internal state 
    appropriately) 
    */

    MyProc ( Handle, pMyObject, pThisObject );
    ...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK)
{

    /* The MooProc does the following for you when called with a decoding 
    handle:
     - unmarshalls the objects from the buffer into *pMooObject and 
       *pBarObject
*/

MyProc ( Handle, pMyObject, pThisObject);
...
MesHandleFree ( Handle );
}
```

<span data-ttu-id="b9472-118">下一節提供如何使用固定緩衝區樣式的範例–序列化類型編碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b9472-118">The following section provides an example of how to use a fixed buffer style–serializing handle for type encoding.</span></span>

``` syntax
/* This is an ACF file. MyType is defined in the IDL file */

[    
    explicit_handle
]
interface regress
{
    typedef [ encode,decode ] MyType;
}
```

<span data-ttu-id="b9472-119">下列摘要表示相關的應用程式片段。</span><span class="sxs-lookup"><span data-stu-id="b9472-119">The following excerpt represents the relevant application fragments.</span></span>


```C++
if (MesEncodeFixedBufferHandleCreate (Buffer, BufferSize, 
    pEncodedSize, &Handle) == RPC_S_OK)
{
    //...
    /* Manufacture a MyObject and a pMyObject */
    //...
    MyType_Encode ( Handle, pMyObject );
    //...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK )
{
    MooType_Decode (Handle, pMooObject);
    //...
    MesHandleFree ( Handle );
}
```



 

 




