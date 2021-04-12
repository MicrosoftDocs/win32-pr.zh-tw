---
description: 下列清單包含 CMSPCAllBase 成員。
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: CMSPCallBase 成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192928"
---
# <a name="cmspcallbase-members"></a><span data-ttu-id="44206-103">CMSPCallBase 成員</span><span class="sxs-lookup"><span data-stu-id="44206-103">CMSPCallBase Members</span></span>



| <span data-ttu-id="44206-104">成員類型</span><span class="sxs-lookup"><span data-stu-id="44206-104">Member type</span></span>                   | <span data-ttu-id="44206-105">Name</span><span class="sxs-lookup"><span data-stu-id="44206-105">Name</span></span>             | <span data-ttu-id="44206-106">描述</span><span class="sxs-lookup"><span data-stu-id="44206-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44206-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="44206-107">IUnknown</span></span>                      | <span data-ttu-id="44206-108">\*m \_ pFTM</span><span class="sxs-lookup"><span data-stu-id="44206-108">\*m\_pFTM</span></span>        | <span data-ttu-id="44206-109">無限制執行緒封送處理器的指標。</span><span class="sxs-lookup"><span data-stu-id="44206-109">Pointer to the free threaded marshaller.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="44206-110">CMSPAddress\*</span><span class="sxs-lookup"><span data-stu-id="44206-110">CMSPAddress\*</span></span>                 | <span data-ttu-id="44206-111">\*m \_ pMSPAddress</span><span class="sxs-lookup"><span data-stu-id="44206-111">\*m\_pMSPAddress</span></span> | <span data-ttu-id="44206-112">MSP 位址物件的指標。</span><span class="sxs-lookup"><span data-stu-id="44206-112">The pointer to the MSP address object.</span></span> <span data-ttu-id="44206-113">如果應用程式未選取任何值，則會使用它來取得預設的終端機。</span><span class="sxs-lookup"><span data-stu-id="44206-113">It is used to get the default terminals if the application doesn't select any.</span></span> <span data-ttu-id="44206-114">它也會透過 [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)攜帶 refcount (，而不是 AddRef) ，如此一來，當通話仍在運作時，匯總的位址就不會消失，但 TAPI 3 的位址不會 AddRef'ed。</span><span class="sxs-lookup"><span data-stu-id="44206-114">It also carries a refcount (via [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), not AddRef) so that the aggregated address will not go away while the call is still alive, but TAPI 3's address is not AddRef'ed.</span></span> |
| <span data-ttu-id="44206-115">MSP \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="44206-115">MSP\_HANDLE</span></span>                   | <span data-ttu-id="44206-116">\*m \_ htCall</span><span class="sxs-lookup"><span data-stu-id="44206-116">\*m\_htCall</span></span>      | <span data-ttu-id="44206-117">TAPI3's 呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="44206-117">The handle to TAPI3's call.</span></span> <span data-ttu-id="44206-118">用來引發呼叫事件。</span><span class="sxs-lookup"><span data-stu-id="44206-118">Used to fire call events.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="44206-119">DWORD</span><span class="sxs-lookup"><span data-stu-id="44206-119">DWORD</span></span>                         | <span data-ttu-id="44206-120">m \_ dwMediaType</span><span class="sxs-lookup"><span data-stu-id="44206-120">m\_dwMediaType</span></span>   | <span data-ttu-id="44206-121">此呼叫之媒體類型的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="44206-121">Bitmask of the media types on this call.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="44206-122">CMSPArray <ITStream \*></span><span class="sxs-lookup"><span data-stu-id="44206-122">CMSPArray <ITStream \*></span></span> | <span data-ttu-id="44206-123">m \_ 資料流程</span><span class="sxs-lookup"><span data-stu-id="44206-123">m\_Streams</span></span>       | <span data-ttu-id="44206-124">呼叫中的資料流程物件清單。</span><span class="sxs-lookup"><span data-stu-id="44206-124">The list of stream objects in the call.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="44206-125">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="44206-125">CMSPCritSection</span></span>               | <span data-ttu-id="44206-126">m \_ 鎖定</span><span class="sxs-lookup"><span data-stu-id="44206-126">m\_lock</span></span>          | <span data-ttu-id="44206-127">保護資料流程清單的鎖定。</span><span class="sxs-lookup"><span data-stu-id="44206-127">The lock that protects the stream lists.</span></span>                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="44206-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="44206-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44206-129">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="44206-129">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



