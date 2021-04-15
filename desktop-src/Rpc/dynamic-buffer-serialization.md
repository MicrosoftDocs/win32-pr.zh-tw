---
title: 動態緩衝區序列化
description: 使用動態緩衝區的序列化樣式時，會由存根配置封送處理緩衝區，並將資料編碼到這個緩衝區，並傳回給您。 當您進行封送時，您會提供包含資料的緩衝區。
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462216"
---
# <a name="dynamic-buffer-serialization"></a><span data-ttu-id="5dd78-104">動態緩衝區序列化</span><span class="sxs-lookup"><span data-stu-id="5dd78-104">Dynamic Buffer Serialization</span></span>

<span data-ttu-id="5dd78-105">使用動態緩衝區的序列化樣式時，會由存根配置封送處理緩衝區，並將資料編碼到這個緩衝區，並傳回給您。</span><span class="sxs-lookup"><span data-stu-id="5dd78-105">When using the dynamic buffer style of serialization, the marshalling buffer is allocated by the stub, and the data is encoded into this buffer and passed back to you.</span></span> <span data-ttu-id="5dd78-106">當您進行封送時，您會提供包含資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5dd78-106">When unmarshaling, you supply the buffer that contains the data.</span></span>

<span data-ttu-id="5dd78-107">動態緩衝區的序列化樣式使用下列常式：</span><span class="sxs-lookup"><span data-stu-id="5dd78-107">The dynamic buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="5dd78-108">**MesEncodeDynBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="5dd78-108">**MesEncodeDynBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [<span data-ttu-id="5dd78-109">**MesDecodeBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="5dd78-109">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="5dd78-110">**MesBufferHandleReset**</span><span class="sxs-lookup"><span data-stu-id="5dd78-110">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="5dd78-111">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="5dd78-111">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="5dd78-112">[**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)函式會配置編碼控制碼所需的記憶體，然後將它初始化。</span><span class="sxs-lookup"><span data-stu-id="5dd78-112">The [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) function allocates the memory needed for the encoding handle and then initializes it.</span></span> <span data-ttu-id="5dd78-113">應用程式可以呼叫 [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) 來重新初始化控制碼。</span><span class="sxs-lookup"><span data-stu-id="5dd78-113">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle.</span></span> <span data-ttu-id="5dd78-114">它會呼叫 [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) 來釋放控制碼的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5dd78-114">It calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="5dd78-115">若要建立對應于動態緩衝區編碼控制碼的解碼控制碼，請使用 [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)。</span><span class="sxs-lookup"><span data-stu-id="5dd78-115">To create a decoding handle corresponding to the dynamic buffer encoding handle, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

 

 




