---
title: 'WM_CAP_SET_PREVIEWRATE 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ PREVIEWRATE 訊息會以預覽模式設定畫面格顯示速率。 您可以使用 capPreviewRate 宏明確地傳送此訊息。
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- WM_CAP_SET_PREVIEWRATE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935042"
---
# <a name="wm_cap_set_previewrate-message"></a><span data-ttu-id="24985-105">WM \_ CAP \_ 設定 \_ PREVIEWRATE 訊息</span><span class="sxs-lookup"><span data-stu-id="24985-105">WM\_CAP\_SET\_PREVIEWRATE message</span></span>

<span data-ttu-id="24985-106">**WM \_ CAP \_ 設定 \_ PREVIEWRATE** 訊息會以預覽模式設定畫面格顯示速率。</span><span class="sxs-lookup"><span data-stu-id="24985-106">The **WM\_CAP\_SET\_PREVIEWRATE** message sets the frame display rate in preview mode.</span></span> <span data-ttu-id="24985-107">您可以使用 [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="24985-107">You can send this message explicitly or by using the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro.</span></span>


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="24985-108">參數</span><span class="sxs-lookup"><span data-stu-id="24985-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24985-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*Wms*</span><span class="sxs-lookup"><span data-stu-id="24985-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span></span>
</dt> <dd>

<span data-ttu-id="24985-110">捕捉及顯示新框架的速率（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="24985-110">Rate, in milliseconds, at which new frames are captured and displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24985-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="24985-111">Return Value</span></span>

<span data-ttu-id="24985-112">如果成功，則傳回 **TRUE** ，如果捕捉視窗未連接到 capture 驅動程式，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="24985-112">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="24985-113">備註</span><span class="sxs-lookup"><span data-stu-id="24985-113">Remarks</span></span>

<span data-ttu-id="24985-114">預覽模式會使用大量的 CPU 資源。</span><span class="sxs-lookup"><span data-stu-id="24985-114">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="24985-115">當另一個應用程式具有焦點時，應用程式可以停用預覽或降低預覽率。</span><span class="sxs-lookup"><span data-stu-id="24985-115">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="24985-116">在串流處理影片捕獲期間，預覽工作的優先順序高於將畫面格寫入磁片的優先順序，而且只有在沒有其他緩衝區可供寫入時，才會顯示預覽畫面格。</span><span class="sxs-lookup"><span data-stu-id="24985-116">During streaming video capture, the previewing task is lower priority than writing frames to disk, and preview frames are displayed only if no other buffers are available for writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="24985-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="24985-117">Requirements</span></span>



| <span data-ttu-id="24985-118">需求</span><span class="sxs-lookup"><span data-stu-id="24985-118">Requirement</span></span> | <span data-ttu-id="24985-119">值</span><span class="sxs-lookup"><span data-stu-id="24985-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="24985-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24985-120">Minimum supported client</span></span><br/> | <span data-ttu-id="24985-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24985-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="24985-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24985-122">Minimum supported server</span></span><br/> | <span data-ttu-id="24985-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24985-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="24985-124">標頭</span><span class="sxs-lookup"><span data-stu-id="24985-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="24985-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="24985-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24985-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24985-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24985-127">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="24985-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="24985-128">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="24985-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





