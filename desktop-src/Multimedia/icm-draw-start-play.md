---
title: 'ICM_DRAW_START_PLAY 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ 開始 \_ 播放訊息提供轉譯驅動程式播放作業的開始和結束時間。 您可以使用 ICDrawStartPlay 宏明確地傳送此訊息。
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- ICM_DRAW_START_PLAY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094399"
---
# <a name="icm_draw_start_play-message"></a><span data-ttu-id="af92a-105">ICM \_ DRAW \_ 開始 \_ 播放訊息</span><span class="sxs-lookup"><span data-stu-id="af92a-105">ICM\_DRAW\_START\_PLAY message</span></span>

<span data-ttu-id="af92a-106">**ICM \_ DRAW \_ 開始 \_ 播放** 訊息提供轉譯驅動程式播放作業的開始和結束時間。</span><span class="sxs-lookup"><span data-stu-id="af92a-106">The **ICM\_DRAW\_START\_PLAY** message provides the start and end times of a play operation to a rendering driver.</span></span> <span data-ttu-id="af92a-107">您可以使用 [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="af92a-107">You can send this message explicitly or by using the [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) macro.</span></span>


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a><span data-ttu-id="af92a-108">參數</span><span class="sxs-lookup"><span data-stu-id="af92a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af92a-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span><span class="sxs-lookup"><span data-stu-id="af92a-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span></span>
</dt> <dd>

<span data-ttu-id="af92a-110">開始時間。</span><span class="sxs-lookup"><span data-stu-id="af92a-110">Start time.</span></span>

</dd> <dt>

<span data-ttu-id="af92a-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span><span class="sxs-lookup"><span data-stu-id="af92a-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span></span>
</dt> <dd>

<span data-ttu-id="af92a-112">結束時間。</span><span class="sxs-lookup"><span data-stu-id="af92a-112">End time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af92a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="af92a-113">Return Value</span></span>

<span data-ttu-id="af92a-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="af92a-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af92a-115">備註</span><span class="sxs-lookup"><span data-stu-id="af92a-115">Remarks</span></span>

<span data-ttu-id="af92a-116">這則訊息會在傳送至轉譯驅動程式的任何框架資料之前。</span><span class="sxs-lookup"><span data-stu-id="af92a-116">This message precedes any frame data sent to the rendering driver.</span></span>

<span data-ttu-id="af92a-117">*LFrom* 和 *lTo* 的單位是以 [**ICM \_ 繪製 \_ 開始**](icm-draw-begin.md)訊息來指定。</span><span class="sxs-lookup"><span data-stu-id="af92a-117">Units for *lFrom* and *lTo* are specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span> <span data-ttu-id="af92a-118">對於影片資料，這通常是畫面格編號。</span><span class="sxs-lookup"><span data-stu-id="af92a-118">For video data this is normally a frame number.</span></span> <span data-ttu-id="af92a-119">如需播放速率的詳細資訊，請參閱 [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)結構的 **dwRate** 和 **dwScale** 成員。</span><span class="sxs-lookup"><span data-stu-id="af92a-119">For more information about the playback rate, see the **dwRate** and **dwScale** members of the [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure.</span></span>

<span data-ttu-id="af92a-120">如果結束時間小於開始時間，則會反轉播放方向。</span><span class="sxs-lookup"><span data-stu-id="af92a-120">If the end time is less than the start time, the playback direction is reversed.</span></span>

## <a name="requirements"></a><span data-ttu-id="af92a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="af92a-121">Requirements</span></span>



| <span data-ttu-id="af92a-122">需求</span><span class="sxs-lookup"><span data-stu-id="af92a-122">Requirement</span></span> | <span data-ttu-id="af92a-123">值</span><span class="sxs-lookup"><span data-stu-id="af92a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="af92a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af92a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="af92a-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af92a-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="af92a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af92a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="af92a-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af92a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="af92a-128">標頭</span><span class="sxs-lookup"><span data-stu-id="af92a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="af92a-129"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="af92a-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af92a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af92a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af92a-131">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="af92a-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="af92a-132">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="af92a-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





