---
description: 篩選器要求重新開機圖形。
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: 'EC_NEED_RESTART (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975727"
---
# <a name="ec_need_restart"></a><span data-ttu-id="add75-103">EC \_ 需要 \_ 重新開機</span><span class="sxs-lookup"><span data-stu-id="add75-103">EC\_NEED\_RESTART</span></span>

<span data-ttu-id="add75-104">篩選器要求重新開機圖形。</span><span class="sxs-lookup"><span data-stu-id="add75-104">A filter is requesting that the graph be restarted.</span></span>

## <a name="parameters"></a><span data-ttu-id="add75-105">參數</span><span class="sxs-lookup"><span data-stu-id="add75-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add75-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="add75-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="add75-107">零個。</span><span class="sxs-lookup"><span data-stu-id="add75-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="add75-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="add75-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="add75-109">零個。</span><span class="sxs-lookup"><span data-stu-id="add75-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="add75-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="add75-110">Default Action</span></span>

<span data-ttu-id="add75-111">篩選圖形管理員會暫停並重新啟動圖形。</span><span class="sxs-lookup"><span data-stu-id="add75-111">The filter graph manager pauses and restarts the graph.</span></span> <span data-ttu-id="add75-112">它不會將事件傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="add75-112">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="add75-113">備註</span><span class="sxs-lookup"><span data-stu-id="add75-113">Remarks</span></span>

<span data-ttu-id="add75-114">如果篩選準則拒絕了串流中間的範例，上游釘選將會停止傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="add75-114">If a filter rejects a sample in the middle of a stream, the upstream pin will stop delivering samples.</span></span> <span data-ttu-id="add75-115">篩選可以藉由傳送此事件來重新開機資料流程。</span><span class="sxs-lookup"><span data-stu-id="add75-115">The filter can restart the stream by sending this event.</span></span> <span data-ttu-id="add75-116">例如，音訊轉譯器可能會遺失聲音裝置的存取權，因為影片視窗已遺失焦點。</span><span class="sxs-lookup"><span data-stu-id="add75-116">For example, the audio renderer might lose access to the sound device, because a video window has lost focus.</span></span> <span data-ttu-id="add75-117">屆時，音訊轉譯器會開始拒絕範例。</span><span class="sxs-lookup"><span data-stu-id="add75-117">At that point, the audio renderer starts rejecting samples.</span></span> <span data-ttu-id="add75-118">當它重新取得音效裝置的存取權時，會傳送此事件以重新開機音訊串流。</span><span class="sxs-lookup"><span data-stu-id="add75-118">When it regains access to the sound device, it sends this event to restart the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="add75-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="add75-119">Requirements</span></span>



| <span data-ttu-id="add75-120">需求</span><span class="sxs-lookup"><span data-stu-id="add75-120">Requirement</span></span> | <span data-ttu-id="add75-121">值</span><span class="sxs-lookup"><span data-stu-id="add75-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="add75-122">標頭</span><span class="sxs-lookup"><span data-stu-id="add75-122">Header</span></span><br/> | <dl> <span data-ttu-id="add75-123"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="add75-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="add75-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="add75-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add75-125">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="add75-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="add75-126">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="add75-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




