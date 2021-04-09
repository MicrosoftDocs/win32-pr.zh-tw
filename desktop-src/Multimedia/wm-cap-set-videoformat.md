---
title: 'WM_CAP_SET_VIDEOFORMAT 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ VIDEOFORMAT 訊息會設定所捕獲影片資料的格式。 您可以使用 capSetVideoFormat 宏明確地傳送此訊息。
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- WM_CAP_SET_VIDEOFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba6154ec1532bd83f482eb81a0e286795aa3341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935041"
---
# <a name="wm_cap_set_videoformat-message"></a><span data-ttu-id="e2b36-105">WM \_ CAP \_ 設定 \_ VIDEOFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="e2b36-105">WM\_CAP\_SET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="e2b36-106">**WM \_ CAP \_ 設定 \_ VIDEOFORMAT** 訊息會設定所捕獲影片資料的格式。</span><span class="sxs-lookup"><span data-stu-id="e2b36-106">The **WM\_CAP\_SET\_VIDEOFORMAT** message sets the format of captured video data.</span></span> <span data-ttu-id="e2b36-107">您可以使用 [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e2b36-107">You can send this message explicitly or by using the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro.</span></span>


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="e2b36-108">參數</span><span class="sxs-lookup"><span data-stu-id="e2b36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2b36-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="e2b36-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="e2b36-110">**S** 所參考之結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2b36-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b36-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span><span class="sxs-lookup"><span data-stu-id="e2b36-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="e2b36-112">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e2b36-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2b36-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2b36-113">Return Value</span></span>

<span data-ttu-id="e2b36-114">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e2b36-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2b36-115">備註</span><span class="sxs-lookup"><span data-stu-id="e2b36-115">Remarks</span></span>

<span data-ttu-id="e2b36-116">由於影片格式是裝置特定的，因此應用程式應該檢查此函式的傳回值，以判斷驅動程式是否接受格式。</span><span class="sxs-lookup"><span data-stu-id="e2b36-116">Because video formats are device-specific, applications should check the return value from this function to determine if the format is accepted by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b36-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2b36-117">Requirements</span></span>



| <span data-ttu-id="e2b36-118">需求</span><span class="sxs-lookup"><span data-stu-id="e2b36-118">Requirement</span></span> | <span data-ttu-id="e2b36-119">值</span><span class="sxs-lookup"><span data-stu-id="e2b36-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e2b36-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2b36-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b36-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2b36-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e2b36-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2b36-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b36-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2b36-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e2b36-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e2b36-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2b36-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2b36-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b36-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2b36-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b36-127">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="e2b36-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e2b36-128">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="e2b36-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

