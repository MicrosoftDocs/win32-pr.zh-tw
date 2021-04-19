---
description: 使用者已結束播放。
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: 'EC_USERABORT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995310"
---
# <a name="ec_userabort"></a><span data-ttu-id="ce4ef-103">EC \_ USERABORT</span><span class="sxs-lookup"><span data-stu-id="ce4ef-103">EC\_USERABORT</span></span>

<span data-ttu-id="ce4ef-104">使用者已結束播放。</span><span class="sxs-lookup"><span data-stu-id="ce4ef-104">The user has terminated playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce4ef-105">參數</span><span class="sxs-lookup"><span data-stu-id="ce4ef-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce4ef-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ce4ef-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ce4ef-107">零個。</span><span class="sxs-lookup"><span data-stu-id="ce4ef-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="ce4ef-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ce4ef-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ce4ef-109">零個。</span><span class="sxs-lookup"><span data-stu-id="ce4ef-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ce4ef-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="ce4ef-110">Default Action</span></span>

<span data-ttu-id="ce4ef-111">無。</span><span class="sxs-lookup"><span data-stu-id="ce4ef-111">None.</span></span> <span data-ttu-id="ce4ef-112">應用程式必須決定是否要停止圖形。</span><span class="sxs-lookup"><span data-stu-id="ce4ef-112">The application must decide whether to stop the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce4ef-113">備註</span><span class="sxs-lookup"><span data-stu-id="ce4ef-113">Remarks</span></span>

<span data-ttu-id="ce4ef-114">此事件程式碼表示使用者已結束正常的圖形播放。</span><span class="sxs-lookup"><span data-stu-id="ce4ef-114">This event code signals that the user has terminated normal graph playback.</span></span> <span data-ttu-id="ce4ef-115">例如，如果使用者關閉影片視窗，影片轉譯器就會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="ce4ef-115">For example, video renderers send this event if the user closes the video window.</span></span>

<span data-ttu-id="ce4ef-116">傳送此事件之後，篩選準則應該會拒絕所有範例，而不會傳送任何 [**EC 重新 \_ 繪製**](ec-repaint.md) 事件，直到篩選停止並重設為止。</span><span class="sxs-lookup"><span data-stu-id="ce4ef-116">After sending this event, the filter should reject all samples and not send any [**EC\_REPAINT**](ec-repaint.md) events, until the filter stops and is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce4ef-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce4ef-117">Requirements</span></span>



| <span data-ttu-id="ce4ef-118">需求</span><span class="sxs-lookup"><span data-stu-id="ce4ef-118">Requirement</span></span> | <span data-ttu-id="ce4ef-119">值</span><span class="sxs-lookup"><span data-stu-id="ce4ef-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4ef-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ce4ef-120">Header</span></span><br/> | <dl> <span data-ttu-id="ce4ef-121"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce4ef-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce4ef-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce4ef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce4ef-123">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="ce4ef-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ce4ef-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="ce4ef-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




