---
title: IReferenceClock 介面
description: IReferenceClock 介面提供外部時鐘的存取。 提供此介面可讓所有轉譯常式同步處理至相同的時鐘。您可以從 reader 物件取得這個介面。
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- IReferenceClock 介面 windows 媒體格式
- IReferenceClock 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965428"
---
# <a name="ireferenceclock-interface"></a><span data-ttu-id="77214-106">IReferenceClock 介面</span><span class="sxs-lookup"><span data-stu-id="77214-106">IReferenceClock interface</span></span>

<span data-ttu-id="77214-107">**IReferenceClock** 介面提供外部時鐘的存取。</span><span class="sxs-lookup"><span data-stu-id="77214-107">The **IReferenceClock** interface provides access to an external clock.</span></span> <span data-ttu-id="77214-108">提供此介面可讓所有轉譯常式同步處理至相同的時鐘。</span><span class="sxs-lookup"><span data-stu-id="77214-108">This interface is provided to enable all rendering routines to be synchronized to the same clock.</span></span>

<span data-ttu-id="77214-109">您可以從 reader 物件取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="77214-109">This interface can be obtained from a reader object.</span></span>

## <a name="members"></a><span data-ttu-id="77214-110">成員</span><span class="sxs-lookup"><span data-stu-id="77214-110">Members</span></span>

<span data-ttu-id="77214-111">**IReferenceClock** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="77214-111">The **IReferenceClock** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="77214-112">**IReferenceClock** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="77214-112">**IReferenceClock** also has these types of members:</span></span>

-   [<span data-ttu-id="77214-113">方法</span><span class="sxs-lookup"><span data-stu-id="77214-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="77214-114">方法</span><span class="sxs-lookup"><span data-stu-id="77214-114">Methods</span></span>

<span data-ttu-id="77214-115">**IReferenceClock** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="77214-115">The **IReferenceClock** interface has these methods.</span></span>



| <span data-ttu-id="77214-116">方法</span><span class="sxs-lookup"><span data-stu-id="77214-116">Method</span></span>                                                   | <span data-ttu-id="77214-117">描述</span><span class="sxs-lookup"><span data-stu-id="77214-117">Description</span></span>                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="77214-118">**AdvisePeriodic**</span><span class="sxs-lookup"><span data-stu-id="77214-118">**AdvisePeriodic**</span></span>](ireferenceclock-adviseperiodic.md) | <span data-ttu-id="77214-119">未由此 SDK 所執行。</span><span class="sxs-lookup"><span data-stu-id="77214-119">Not implemented by this SDK.</span></span><br/>                                   |
| [<span data-ttu-id="77214-120">**AdviseTime**</span><span class="sxs-lookup"><span data-stu-id="77214-120">**AdviseTime**</span></span>](ireferenceclock-advisetime.md)         | <span data-ttu-id="77214-121">要求經過一段時間的非同步通知。</span><span class="sxs-lookup"><span data-stu-id="77214-121">Requests an asynchronous notification that a time has elapsed.</span></span><br/> |
| [<span data-ttu-id="77214-122">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="77214-122">**GetTime**</span></span>](ireferenceclock-gettime.md)               | <span data-ttu-id="77214-123">抓取目前的參考時間。</span><span class="sxs-lookup"><span data-stu-id="77214-123">Retrieves the current reference time.</span></span><br/>                          |
| [<span data-ttu-id="77214-124">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="77214-124">**Unadvise**</span></span>](ireferenceclock-unadvise.md)             | <span data-ttu-id="77214-125">取消通知要求。</span><span class="sxs-lookup"><span data-stu-id="77214-125">Cancels a notification request.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="77214-126">備註</span><span class="sxs-lookup"><span data-stu-id="77214-126">Remarks</span></span>

<span data-ttu-id="77214-127">如需可以使用此介面的 QueryInterface 方法取得之其他介面的詳細資訊，請參閱 Reader 物件。</span><span class="sxs-lookup"><span data-stu-id="77214-127">For information on other interfaces that can be obtained by using the QueryInterface method of this interface, see Reader Object.</span></span>

## <a name="see-also"></a><span data-ttu-id="77214-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77214-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77214-129">**介面**</span><span class="sxs-lookup"><span data-stu-id="77214-129">**Interfaces**</span></span>](interfaces.md)
</dt> </dl>

 

