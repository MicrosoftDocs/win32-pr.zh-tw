---
description: 篩選圖形的狀態已變更。
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: 'EC_STATE_CHANGE (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989789"
---
# <a name="ec_state_change"></a><span data-ttu-id="9b2e7-103">EC \_ 狀態 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="9b2e7-103">EC\_STATE\_CHANGE</span></span>

<span data-ttu-id="9b2e7-104">篩選圖形的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="9b2e7-104">The filter graph has changed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b2e7-105">參數</span><span class="sxs-lookup"><span data-stu-id="9b2e7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b2e7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9b2e7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9b2e7-107"> (**DWORD**) [**篩選準則 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉類型的成員，表示新的圖形狀態。</span><span class="sxs-lookup"><span data-stu-id="9b2e7-107">(**DWORD**) Member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the new graph state.</span></span>

</dd> <dt>

<span data-ttu-id="9b2e7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9b2e7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9b2e7-109">零個。</span><span class="sxs-lookup"><span data-stu-id="9b2e7-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="9b2e7-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="9b2e7-110">Default Action</span></span>

<span data-ttu-id="9b2e7-111">沒有預設動作。</span><span class="sxs-lookup"><span data-stu-id="9b2e7-111">No default action.</span></span> <span data-ttu-id="9b2e7-112">此事件不會傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="9b2e7-112">The event is not sent to the application.</span></span>

> [!Note]  
> <span data-ttu-id="9b2e7-113">當圖形關閉時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="9b2e7-113">This event can occur when the graph shuts down.</span></span> <span data-ttu-id="9b2e7-114">如果您覆寫預設動作並接聽此事件，您必須特別小心，不要在釋出篩選圖形管理員之後處理事件。</span><span class="sxs-lookup"><span data-stu-id="9b2e7-114">If you override the default action and listen for this event, you must be especially careful not to process events after releasing the Filter Graph Manager.</span></span> <span data-ttu-id="9b2e7-115">否則，您的應用程式可能會參考不正確 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) 指標和損毀。</span><span class="sxs-lookup"><span data-stu-id="9b2e7-115">Otherwise, your application might reference an invalid [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) pointer and crash.</span></span> <span data-ttu-id="9b2e7-116">如需詳細資訊，請參閱 [回應事件](responding-to-events.md)。</span><span class="sxs-lookup"><span data-stu-id="9b2e7-116">For more information, see [Responding to Events](responding-to-events.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b2e7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b2e7-117">Requirements</span></span>



| <span data-ttu-id="9b2e7-118">需求</span><span class="sxs-lookup"><span data-stu-id="9b2e7-118">Requirement</span></span> | <span data-ttu-id="9b2e7-119">值</span><span class="sxs-lookup"><span data-stu-id="9b2e7-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b2e7-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9b2e7-120">Header</span></span><br/> | <dl> <span data-ttu-id="9b2e7-121"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b2e7-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b2e7-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b2e7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b2e7-123">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="9b2e7-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="9b2e7-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="9b2e7-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




