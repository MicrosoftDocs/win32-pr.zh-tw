---
description: CMSPCallBase 純虛擬方法-這些方法必須由衍生類別覆寫。
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: CMSPCallBase 純虛擬方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094456"
---
# <a name="cmspcallbase-pure-virtual-methods"></a><span data-ttu-id="e14f4-103">CMSPCallBase 純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="e14f4-103">CMSPCallBase Pure Virtual Methods</span></span>

<span data-ttu-id="e14f4-104">這些方法必須由衍生類別覆寫。</span><span class="sxs-lookup"><span data-stu-id="e14f4-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="e14f4-105">CMSPCallBase 純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="e14f4-105">CMSPCallBase pure virtual methods</span></span>                                 | <span data-ttu-id="e14f4-106">Description</span><span class="sxs-lookup"><span data-stu-id="e14f4-106">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e14f4-107">**MSPCallAddRef**</span><span class="sxs-lookup"><span data-stu-id="e14f4-107">**MSPCallAddRef**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | <span data-ttu-id="e14f4-108">Call 物件的私用 AddRef 方法。</span><span class="sxs-lookup"><span data-stu-id="e14f4-108">Private AddRef method for the call object.</span></span>                                                                                              |
| [<span data-ttu-id="e14f4-109">**MSPCallRelease**</span><span class="sxs-lookup"><span data-stu-id="e14f4-109">**MSPCallRelease**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | <span data-ttu-id="e14f4-110">呼叫物件的私用版本方法。</span><span class="sxs-lookup"><span data-stu-id="e14f4-110">Private Release method for the call object.</span></span>                                                                                             |
| [<span data-ttu-id="e14f4-111">**Init**</span><span class="sxs-lookup"><span data-stu-id="e14f4-111">**Init**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | <span data-ttu-id="e14f4-112">由 MSP 位址物件呼叫 (在方法 [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall) 中) 初始化 MSP 呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="e14f4-112">Called by the MSP address object (in the method [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) to initialize the MSP call object.</span></span> |
| [<span data-ttu-id="e14f4-113">**關閉**</span><span class="sxs-lookup"><span data-stu-id="e14f4-113">**ShutDown**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | <span data-ttu-id="e14f4-114">由 MSP 位址物件呼叫，以關閉呼叫。</span><span class="sxs-lookup"><span data-stu-id="e14f4-114">Called by the MSP address object to shut down the call..</span></span>                                                                                |
| [<span data-ttu-id="e14f4-115">**InternalCreateStream**</span><span class="sxs-lookup"><span data-stu-id="e14f4-115">**InternalCreateStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | <span data-ttu-id="e14f4-116">由 [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) 呼叫以建立資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="e14f4-116">Called by [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) to create a stream object.</span></span>                                               |
| [<span data-ttu-id="e14f4-117">**CreateStreamObject**</span><span class="sxs-lookup"><span data-stu-id="e14f4-117">**CreateStreamObject**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | <span data-ttu-id="e14f4-118">由 [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) 呼叫以建立資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="e14f4-118">Called by [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) to create a stream object.</span></span>                                  |
| [<span data-ttu-id="e14f4-119">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="e14f4-119">**RemoveStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | <span data-ttu-id="e14f4-120">由應用程式呼叫以從呼叫中移除資料流程</span><span class="sxs-lookup"><span data-stu-id="e14f4-120">Called by the application to remove a stream from the call</span></span>                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="e14f4-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="e14f4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e14f4-122">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="e14f4-122">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
