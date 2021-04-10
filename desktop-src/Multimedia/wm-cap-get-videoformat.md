---
title: 'WM_CAP_GET_VIDEOFORMAT 訊息 (Vfw .h) '
description: WM \_ CAP \_ GET \_ VIDEOFORMAT 訊息會取得使用中的影片格式或影片格式所需大小的複本。 您可以使用 capGetVideoFormat 和 capGetVideoFormatSize 宏明確地傳送此訊息。
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- WM_CAP_GET_VIDEOFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934343"
---
# <a name="wm_cap_get_videoformat-message"></a><span data-ttu-id="9eedc-105">WM \_ CAP \_ 取得 \_ VIDEOFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="9eedc-105">WM\_CAP\_GET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="9eedc-106">**WM \_ CAP \_ GET \_ VIDEOFORMAT** 訊息會取得使用中的影片格式或影片格式所需大小的複本。</span><span class="sxs-lookup"><span data-stu-id="9eedc-106">The **WM\_CAP\_GET\_VIDEOFORMAT** message retrieves a copy of the video format in use or the size required for the video format.</span></span> <span data-ttu-id="9eedc-107">您可以使用 [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) 和 [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="9eedc-107">You can send this message explicitly or by using the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) and [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macros.</span></span>


```C++
WM_CAP_GET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="9eedc-108">參數</span><span class="sxs-lookup"><span data-stu-id="9eedc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eedc-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="9eedc-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="9eedc-110">**S** 所參考之結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9eedc-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="9eedc-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span><span class="sxs-lookup"><span data-stu-id="9eedc-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="9eedc-112">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9eedc-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span> <span data-ttu-id="9eedc-113">您也可以指定 **Null** 來取得所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9eedc-113">You can also specify **NULL** to retrieve the number of bytes needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eedc-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9eedc-114">Return Value</span></span>

<span data-ttu-id="9eedc-115">傳回影片格式的大小（以位元組為單位），如果捕捉視窗未連接到 capture 驅動程式，則傳回零。</span><span class="sxs-lookup"><span data-stu-id="9eedc-115">Returns the size, in bytes, of the video format or zero if the capture window is not connected to a capture driver.</span></span> <span data-ttu-id="9eedc-116">對於需要調色板的影片格式，也會傳回目前的調色板。</span><span class="sxs-lookup"><span data-stu-id="9eedc-116">For video formats that require a palette, the current palette is also returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eedc-117">備註</span><span class="sxs-lookup"><span data-stu-id="9eedc-117">Remarks</span></span>

<span data-ttu-id="9eedc-118">由於壓縮的影片格式大小需求不同，因此應用程式必須先取出大小，然後配置記憶體，最後要求影片格式資料。</span><span class="sxs-lookup"><span data-stu-id="9eedc-118">Because compressed video formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the video format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eedc-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9eedc-119">Requirements</span></span>



| <span data-ttu-id="9eedc-120">需求</span><span class="sxs-lookup"><span data-stu-id="9eedc-120">Requirement</span></span> | <span data-ttu-id="9eedc-121">值</span><span class="sxs-lookup"><span data-stu-id="9eedc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9eedc-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9eedc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9eedc-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9eedc-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9eedc-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9eedc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9eedc-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9eedc-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9eedc-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9eedc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eedc-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="9eedc-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eedc-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9eedc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eedc-129">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="9eedc-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9eedc-130">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="9eedc-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

