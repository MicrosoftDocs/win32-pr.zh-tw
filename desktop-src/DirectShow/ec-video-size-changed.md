---
description: 原生影片大小已變更。
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: 'EC_VIDEO_SIZE_CHANGED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981633"
---
# <a name="ec_video_size_changed"></a><span data-ttu-id="0d206-103">EC \_ 影片 \_ 大小 \_ 已變更</span><span class="sxs-lookup"><span data-stu-id="0d206-103">EC\_VIDEO\_SIZE\_CHANGED</span></span>

<span data-ttu-id="0d206-104">原生影片大小已變更。</span><span class="sxs-lookup"><span data-stu-id="0d206-104">The native video size has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d206-105">參數</span><span class="sxs-lookup"><span data-stu-id="0d206-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d206-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0d206-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0d206-107"> (**DWORD**) 低序位字組指定新的寬度（以圖元為單位）。高序位字指定新的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0d206-107">(**DWORD**) Low-order WORD specifies the new width, in pixels; high-order WORD specifies the new height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0d206-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0d206-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0d206-109">零個。</span><span class="sxs-lookup"><span data-stu-id="0d206-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="0d206-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="0d206-110">Default Action</span></span>

<span data-ttu-id="0d206-111">無。</span><span class="sxs-lookup"><span data-stu-id="0d206-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d206-112">備註</span><span class="sxs-lookup"><span data-stu-id="0d206-112">Remarks</span></span>

<span data-ttu-id="0d206-113">如果影片轉譯器偵測到原生影片大小的變更，則可能會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="0d206-113">Video renderers may send this event if they detect a change in the native video size.</span></span>

<span data-ttu-id="0d206-114">[影片混合](video-mixing-renderer-filter-7.md)轉譯器 7 (VMR-7) 和[影片混合](video-mixing-renderer-filter-9.md)轉譯器 9 (VMR-9) 以視窗模式傳送此事件，而不是在無視窗模式或 renderless 模式下傳送。</span><span class="sxs-lookup"><span data-stu-id="0d206-114">The [Video Mixing Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9) send this event in windowed mode, but not in windowless mode or renderless mode.</span></span> <span data-ttu-id="0d206-115">如需 VMR 中視窗模式模式的詳細資訊，請參閱 [影片](video-rendering.md)轉譯。</span><span class="sxs-lookup"><span data-stu-id="0d206-115">For more information about windowed mode in the VMR, see [Video Rendering](video-rendering.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d206-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d206-116">Requirements</span></span>



| <span data-ttu-id="0d206-117">需求</span><span class="sxs-lookup"><span data-stu-id="0d206-117">Requirement</span></span> | <span data-ttu-id="0d206-118">值</span><span class="sxs-lookup"><span data-stu-id="0d206-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d206-119">標頭</span><span class="sxs-lookup"><span data-stu-id="0d206-119">Header</span></span><br/> | <dl> <span data-ttu-id="0d206-120"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d206-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d206-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d206-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d206-122">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="0d206-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0d206-123">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="0d206-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




