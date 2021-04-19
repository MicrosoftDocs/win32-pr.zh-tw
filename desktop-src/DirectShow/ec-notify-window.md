---
description: 通知影片轉譯器視窗的篩選。
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: 'EC_NOTIFY_WINDOW (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998672"
---
# <a name="ec_notify_window"></a><span data-ttu-id="ab106-103">EC \_ 通知 \_ 視窗</span><span class="sxs-lookup"><span data-stu-id="ab106-103">EC\_NOTIFY\_WINDOW</span></span>

<span data-ttu-id="ab106-104">通知影片轉譯器視窗的篩選。</span><span class="sxs-lookup"><span data-stu-id="ab106-104">Notifies a filter of the video renderer's window.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab106-105">參數</span><span class="sxs-lookup"><span data-stu-id="ab106-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab106-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ab106-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ab106-107"> (**HWND**) 視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab106-107">(**HWND**) Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="ab106-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ab106-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ab106-109">零個。</span><span class="sxs-lookup"><span data-stu-id="ab106-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ab106-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="ab106-110">Default Action</span></span>

<span data-ttu-id="ab106-111">此事件是由 DirectShow 在內部使用。</span><span class="sxs-lookup"><span data-stu-id="ab106-111">This event is used internally by DirectShow.</span></span> <span data-ttu-id="ab106-112">篩選圖形管理員不會將此事件傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="ab106-112">The filter graph manager does not pass this event to the application.</span></span> <span data-ttu-id="ab106-113">應用程式無法覆寫此事件的預設動作。</span><span class="sxs-lookup"><span data-stu-id="ab106-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab106-114">備註</span><span class="sxs-lookup"><span data-stu-id="ab106-114">Remarks</span></span>

<span data-ttu-id="ab106-115">當影片轉譯器連線時，它會檢查上游輸出釘選是否支援 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面。</span><span class="sxs-lookup"><span data-stu-id="ab106-115">When a video renderer is connected, it checks whether the upstream output pin supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="ab106-116">如果是的話，轉譯器會將此事件傳送到上游篩選器。</span><span class="sxs-lookup"><span data-stu-id="ab106-116">If so, the renderer sends this event to the upstream filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab106-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab106-117">Requirements</span></span>



| <span data-ttu-id="ab106-118">需求</span><span class="sxs-lookup"><span data-stu-id="ab106-118">Requirement</span></span> | <span data-ttu-id="ab106-119">值</span><span class="sxs-lookup"><span data-stu-id="ab106-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab106-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ab106-120">Header</span></span><br/> | <dl> <span data-ttu-id="ab106-121"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab106-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab106-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab106-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab106-123">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="ab106-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ab106-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="ab106-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




