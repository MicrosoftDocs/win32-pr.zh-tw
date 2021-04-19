---
description: 指定元件排程處理範例的進度。
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: 'EC_SAMPLE_LATENCY (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999073"
---
# <a name="ec_sample_latency"></a><span data-ttu-id="58e5c-103">EC \_ 範例 \_ 延遲</span><span class="sxs-lookup"><span data-stu-id="58e5c-103">EC\_SAMPLE\_LATENCY</span></span>

<span data-ttu-id="58e5c-104">指定元件排程處理範例的進度。</span><span class="sxs-lookup"><span data-stu-id="58e5c-104">Specifies how far behind schedule a component is for processing samples.</span></span>

## <a name="parameters"></a><span data-ttu-id="58e5c-105">參數</span><span class="sxs-lookup"><span data-stu-id="58e5c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e5c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="58e5c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="58e5c-107"> (**CONST 參考 \_ 時間** \*) 元件背後的距離，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="58e5c-107">(**const REFERENCE\_TIME**\*) How far behind the component is, in 100-nanosecond units.</span></span> <span data-ttu-id="58e5c-108">如果這個值是正數，則元件會落後排程。</span><span class="sxs-lookup"><span data-stu-id="58e5c-108">If this value is positive, the component is behind schedule.</span></span> <span data-ttu-id="58e5c-109">如果這個值是負數，則元件會預先排程。</span><span class="sxs-lookup"><span data-stu-id="58e5c-109">If this value is negative, the component is ahead of schedule.</span></span>

</dd> <dt>

<span data-ttu-id="58e5c-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="58e5c-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="58e5c-111">零個。</span><span class="sxs-lookup"><span data-stu-id="58e5c-111">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="58e5c-112">預設動作</span><span class="sxs-lookup"><span data-stu-id="58e5c-112">Default Action</span></span>

<span data-ttu-id="58e5c-113">無。</span><span class="sxs-lookup"><span data-stu-id="58e5c-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="58e5c-114">備註</span><span class="sxs-lookup"><span data-stu-id="58e5c-114">Remarks</span></span>

<span data-ttu-id="58e5c-115">[**增強型影片**](enhanced-video-renderer-filter.md)轉譯器的自訂展示者 (EVR) 篩選器可以將此訊息傳送至 EVR，以通知 EVR 簡報者是在排程或預先排程的後方。</span><span class="sxs-lookup"><span data-stu-id="58e5c-115">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR, to notify the EVR whether the presenter is behind schedule or ahead of schedule.</span></span>

<span data-ttu-id="58e5c-116">計算 *lParam1* 的最簡單方式是：立即 *QPC*   *QPC 目標*，其中 *QPC 現在* 是目前的時鐘時間，而 *QPC 目標* 是展示時間。</span><span class="sxs-lookup"><span data-stu-id="58e5c-116">The simplest way to calculate *lParam1* is: *QPC now*   *QPC target*, where *QPC now* is the clock time now, and *QPC target* is the presentation time.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e5c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="58e5c-117">Requirements</span></span>



| <span data-ttu-id="58e5c-118">需求</span><span class="sxs-lookup"><span data-stu-id="58e5c-118">Requirement</span></span> | <span data-ttu-id="58e5c-119">值</span><span class="sxs-lookup"><span data-stu-id="58e5c-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58e5c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="58e5c-120">Header</span></span><br/> | <dl> <span data-ttu-id="58e5c-121"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="58e5c-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e5c-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58e5c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e5c-123">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="58e5c-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="58e5c-124">如何撰寫 EVR 展示者</span><span class="sxs-lookup"><span data-stu-id="58e5c-124">How to Write an EVR Presenter</span></span>](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

