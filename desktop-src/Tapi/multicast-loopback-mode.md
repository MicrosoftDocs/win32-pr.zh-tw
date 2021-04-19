---
description: 多播 \_ 回送 \_ 模式列舉會描述多播回送模式。
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: 'MULTICAST_LOOPBACK_MODE 列舉 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993687"
---
# <a name="multicast_loopback_mode-enumeration"></a><span data-ttu-id="f642c-103">多播 \_ 回送 \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="f642c-103">MULTICAST\_LOOPBACK\_MODE enumeration</span></span>

<span data-ttu-id="f642c-104">\[**多播 \_回送 \_ 模式** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="f642c-104">\[**MULTICAST\_LOOPBACK\_MODE** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f642c-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f642c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f642c-106">**多播 \_ 回送 \_ 模式** 列舉會描述多播回送模式。</span><span class="sxs-lookup"><span data-stu-id="f642c-106">The **MULTICAST\_LOOPBACK\_MODE** enum describes the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="f642c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f642c-107">Syntax</span></span>


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a><span data-ttu-id="f642c-108">常數</span><span class="sxs-lookup"><span data-stu-id="f642c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f642c-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ 無 \_ 回送**</span><span class="sxs-lookup"><span data-stu-id="f642c-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM\_NO\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="f642c-110">多播回送已停用。</span><span class="sxs-lookup"><span data-stu-id="f642c-110">Multicast loopback is disabled.</span></span> <span data-ttu-id="f642c-111">這表示在同一部電腦上聯結相同多播群組的兩個應用程式，可以取得彼此的封包。</span><span class="sxs-lookup"><span data-stu-id="f642c-111">That means two applications on the same machine joining the same multicast group can get each other's packets.</span></span>

</dd> <dt>

<span data-ttu-id="f642c-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM \_ 完整 \_ 回送**</span><span class="sxs-lookup"><span data-stu-id="f642c-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM\_FULL\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="f642c-113">送出的所有封包也會回復。</span><span class="sxs-lookup"><span data-stu-id="f642c-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="f642c-114">此模式只適用于測試。</span><span class="sxs-lookup"><span data-stu-id="f642c-114">This mode is useful only for testing.</span></span>

</dd> <dt>

<span data-ttu-id="f642c-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**MM \_ 選擇性 \_ 回送**</span><span class="sxs-lookup"><span data-stu-id="f642c-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**MM\_SELECTIVE\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="f642c-116">已啟用選擇性回送。</span><span class="sxs-lookup"><span data-stu-id="f642c-116">Selective loopback is enabled.</span></span> <span data-ttu-id="f642c-117">這表示在一部電腦上啟用多個應用程式可以加入相同的多播群組，而不會有混淆。</span><span class="sxs-lookup"><span data-stu-id="f642c-117">That means enabled multiple applications on one machine can join the same multicast group without confusion.</span></span> <span data-ttu-id="f642c-118">封包會從堆疊環回，且每個 RTP 會話都會負責篩選掉不需要的封包。</span><span class="sxs-lookup"><span data-stu-id="f642c-118">The packets are looped back from the stack and each RTP session is responsible for filtering out unwanted packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f642c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f642c-119">Requirements</span></span>



| <span data-ttu-id="f642c-120">需求</span><span class="sxs-lookup"><span data-stu-id="f642c-120">Requirement</span></span> | <span data-ttu-id="f642c-121">值</span><span class="sxs-lookup"><span data-stu-id="f642c-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f642c-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f642c-122">TAPI version</span></span><br/> | <span data-ttu-id="f642c-123">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f642c-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f642c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f642c-124">Header</span></span><br/>       | <dl> <span data-ttu-id="f642c-125"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="f642c-125"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f642c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f642c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f642c-127">**IMulticastControl：： get \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="f642c-127">**IMulticastControl::get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[<span data-ttu-id="f642c-128">**IMulticastControl：:p 的 \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="f642c-128">**IMulticastControl::put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




