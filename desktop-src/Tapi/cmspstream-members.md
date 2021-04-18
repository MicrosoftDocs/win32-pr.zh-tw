---
description: 下列清單包含 CMSPStream 成員。
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: CMSPStream 成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115604"
---
# <a name="cmspstream-members"></a><span data-ttu-id="9144b-103">CMSPStream 成員</span><span class="sxs-lookup"><span data-stu-id="9144b-103">CMSPStream Members</span></span>



| <span data-ttu-id="9144b-104">成員類型</span><span class="sxs-lookup"><span data-stu-id="9144b-104">Member type</span></span>                     | <span data-ttu-id="9144b-105">Name</span><span class="sxs-lookup"><span data-stu-id="9144b-105">Name</span></span>                | <span data-ttu-id="9144b-106">描述</span><span class="sxs-lookup"><span data-stu-id="9144b-106">Description</span></span>                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9144b-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="9144b-107">IUnknown</span></span>                        | <span data-ttu-id="9144b-108">\*m \_ pFTM</span><span class="sxs-lookup"><span data-stu-id="9144b-108">\*m\_pFTM</span></span>           | <span data-ttu-id="9144b-109">無限制執行緒封送處理器的指標。</span><span class="sxs-lookup"><span data-stu-id="9144b-109">Pointer to the free threaded marshaller.</span></span>                                                                                                   |
| <span data-ttu-id="9144b-110">DWORD</span><span class="sxs-lookup"><span data-stu-id="9144b-110">DWORD</span></span>                           | <span data-ttu-id="9144b-111">m \_ dwState</span><span class="sxs-lookup"><span data-stu-id="9144b-111">m\_dwState</span></span>          | <span data-ttu-id="9144b-112">資料流程的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="9144b-112">The current state of the stream.</span></span>                                                                                                           |
| <span data-ttu-id="9144b-113">HANDLE</span><span class="sxs-lookup"><span data-stu-id="9144b-113">HANDLE</span></span>                          | <span data-ttu-id="9144b-114">m \_ hAddress</span><span class="sxs-lookup"><span data-stu-id="9144b-114">m\_hAddress</span></span>         | <span data-ttu-id="9144b-115">使用此資料流程的位址。</span><span class="sxs-lookup"><span data-stu-id="9144b-115">The address on which this stream is being used.</span></span>                                                                                            |
| <span data-ttu-id="9144b-116">DWORD</span><span class="sxs-lookup"><span data-stu-id="9144b-116">DWORD</span></span>                           | <span data-ttu-id="9144b-117">m \_ dwMediaType</span><span class="sxs-lookup"><span data-stu-id="9144b-117">m\_dwMediaType</span></span>      | <span data-ttu-id="9144b-118">此資料流程的 [**媒體類型**](tapimediatype--constants.md) (音訊、影片等 ) 。</span><span class="sxs-lookup"><span data-stu-id="9144b-118">The [**media type**](tapimediatype--constants.md) of this stream (audio, video, etc.).</span></span>                                                    |
| <span data-ttu-id="9144b-119">終端機 \_ 方向</span><span class="sxs-lookup"><span data-stu-id="9144b-119">TERMINAL\_DIRECTION</span></span>             | <span data-ttu-id="9144b-120">m \_ 方向</span><span class="sxs-lookup"><span data-stu-id="9144b-120">m\_Direction</span></span>        | <span data-ttu-id="9144b-121">此資料流程 (傳入或傳出) 的 [**方向**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) 。</span><span class="sxs-lookup"><span data-stu-id="9144b-121">The [**direction**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) of this stream (incoming or outgoing).</span></span>                                                         |
| <span data-ttu-id="9144b-122">CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="9144b-122">CMSPCallBase</span></span>                    | <span data-ttu-id="9144b-123">\*m \_ pMSPCall</span><span class="sxs-lookup"><span data-stu-id="9144b-123">\*m\_pMSPCall</span></span>       | <span data-ttu-id="9144b-124">呼叫物件的指標。</span><span class="sxs-lookup"><span data-stu-id="9144b-124">Pointer to the call object.</span></span>                                                                                                                |
| <span data-ttu-id="9144b-125">IGraphBuilder</span><span class="sxs-lookup"><span data-stu-id="9144b-125">IGraphBuilder</span></span>                   | <span data-ttu-id="9144b-126">\*m \_ pIGraphBuilder</span><span class="sxs-lookup"><span data-stu-id="9144b-126">\*m\_pIGraphBuilder</span></span> | <span data-ttu-id="9144b-127">繪圖物件介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9144b-127">Pointer to graph object interfaces.</span></span>                                                                                                        |
| <span data-ttu-id="9144b-128">IMediaControl</span><span class="sxs-lookup"><span data-stu-id="9144b-128">IMediaControl</span></span>                   | <span data-ttu-id="9144b-129">\*m \_ pIMediaControl</span><span class="sxs-lookup"><span data-stu-id="9144b-129">\*m\_pIMediaControl</span></span> | <span data-ttu-id="9144b-130">媒體控制項介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9144b-130">Pointer to the media control interface.</span></span>                                                                                                    |
| <span data-ttu-id="9144b-131">CMSPArray <ITTerminal \*></span><span class="sxs-lookup"><span data-stu-id="9144b-131">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="9144b-132">m \_ 終端機</span><span class="sxs-lookup"><span data-stu-id="9144b-132">m\_Terminals</span></span>        | <span data-ttu-id="9144b-133">資料流程上的終端機清單。</span><span class="sxs-lookup"><span data-stu-id="9144b-133">The list of terminals on the stream.</span></span>                                                                                                       |
| <span data-ttu-id="9144b-134">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="9144b-134">CMSPCritSection</span></span>                 | <span data-ttu-id="9144b-135">m \_ 鎖定</span><span class="sxs-lookup"><span data-stu-id="9144b-135">m\_lock</span></span>             | <span data-ttu-id="9144b-136">保護資料流程物件的鎖定。</span><span class="sxs-lookup"><span data-stu-id="9144b-136">The lock that protects the stream object.</span></span> <span data-ttu-id="9144b-137">資料流程物件絕對不應該取得鎖定，然後呼叫可能會鎖定的 MSPCall 方法。</span><span class="sxs-lookup"><span data-stu-id="9144b-137">The stream object should never acquire the lock and then call an MSPCall method that might lock.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9144b-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="9144b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9144b-139">**CMSPStream**</span><span class="sxs-lookup"><span data-stu-id="9144b-139">**CMSPStream**</span></span>](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



