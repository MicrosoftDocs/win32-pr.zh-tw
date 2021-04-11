---
description: 這些方法必須由衍生類別覆寫。
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: CMSPCallBase 純虛擬方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d8dea4c1a240e362a4dc3a19b3c09a37a318947
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849421"
---
# <a name="cmspcallbase-pure-virtual-methods"></a><span data-ttu-id="ecb58-103">CMSPCallBase 純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="ecb58-103">CMSPCallBase Pure Virtual Methods</span></span>

<span data-ttu-id="ecb58-104">這些方法必須由衍生類別覆寫。</span><span class="sxs-lookup"><span data-stu-id="ecb58-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="ecb58-105">CMSPCallBase 純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="ecb58-105">CMSPCallBase pure virtual methods</span></span>                                 | <span data-ttu-id="ecb58-106">Description</span><span class="sxs-lookup"><span data-stu-id="ecb58-106">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecb58-107">**MSPCallAddRef**</span><span class="sxs-lookup"><span data-stu-id="ecb58-107">**MSPCallAddRef**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | <span data-ttu-id="ecb58-108">Call 物件的私用 AddRef 方法。</span><span class="sxs-lookup"><span data-stu-id="ecb58-108">Private AddRef method for the call object.</span></span>                                                                                              |
| [<span data-ttu-id="ecb58-109">**MSPCallRelease**</span><span class="sxs-lookup"><span data-stu-id="ecb58-109">**MSPCallRelease**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | <span data-ttu-id="ecb58-110">呼叫物件的私用版本方法。</span><span class="sxs-lookup"><span data-stu-id="ecb58-110">Private Release method for the call object.</span></span>                                                                                             |
| [<span data-ttu-id="ecb58-111">**Init**</span><span class="sxs-lookup"><span data-stu-id="ecb58-111">**Init**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | <span data-ttu-id="ecb58-112">由 MSP 位址物件呼叫 (在方法 [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall) 中) 初始化 MSP 呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="ecb58-112">Called by the MSP address object (in the method [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) to initialize the MSP call object.</span></span> |
| [<span data-ttu-id="ecb58-113">**關閉**</span><span class="sxs-lookup"><span data-stu-id="ecb58-113">**ShutDown**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | <span data-ttu-id="ecb58-114">由 MSP 位址物件呼叫，以關閉呼叫。</span><span class="sxs-lookup"><span data-stu-id="ecb58-114">Called by the MSP address object to shut down the call..</span></span>                                                                                |
| [<span data-ttu-id="ecb58-115">**InternalCreateStream**</span><span class="sxs-lookup"><span data-stu-id="ecb58-115">**InternalCreateStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | <span data-ttu-id="ecb58-116">由 [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) 呼叫以建立資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="ecb58-116">Called by [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) to create a stream object.</span></span>                                               |
| [<span data-ttu-id="ecb58-117">**CreateStreamObject**</span><span class="sxs-lookup"><span data-stu-id="ecb58-117">**CreateStreamObject**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | <span data-ttu-id="ecb58-118">由 [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) 呼叫以建立資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="ecb58-118">Called by [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) to create a stream object.</span></span>                                  |
| [<span data-ttu-id="ecb58-119">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="ecb58-119">**RemoveStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | <span data-ttu-id="ecb58-120">由應用程式呼叫以從呼叫中移除資料流程</span><span class="sxs-lookup"><span data-stu-id="ecb58-120">Called by the application to remove a stream from the call</span></span>                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="ecb58-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="ecb58-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecb58-122">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="ecb58-122">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
