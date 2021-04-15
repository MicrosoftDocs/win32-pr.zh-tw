---
title: 'WM_CAP_SET_CALLBACK_WAVESTREAM 訊息 (Vfw .h) '
description: WM \_ CAP \_ SET \_ 回呼 \_ WAVESTREAM 訊息會在應用程式中設定回呼函數。
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- WM_CAP_SET_CALLBACK_WAVESTREAM message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36abc7848de082e033cfc25d4f15d90c86cf3b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466868"
---
# <a name="wm_cap_set_callback_wavestream-message"></a><span data-ttu-id="3655e-104">WM \_ CAP \_ 設定 \_ 回呼 \_ WAVESTREAM 訊息</span><span class="sxs-lookup"><span data-stu-id="3655e-104">WM\_CAP\_SET\_CALLBACK\_WAVESTREAM message</span></span>

<span data-ttu-id="3655e-105">**WM \_ CAP \_ SET \_ 回呼 \_ WAVESTREAM** 訊息會在應用程式中設定回呼函數。</span><span class="sxs-lookup"><span data-stu-id="3655e-105">The **WM\_CAP\_SET\_CALLBACK\_WAVESTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="3655e-106">當新的音訊緩衝區可供使用時，AVICap 會在串流處理期間呼叫此程式。</span><span class="sxs-lookup"><span data-stu-id="3655e-106">AVICap calls this procedure during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="3655e-107">您可以使用 [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3655e-107">You can send this message explicitly or by using the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="3655e-108">參數</span><span class="sxs-lookup"><span data-stu-id="3655e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3655e-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="3655e-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="3655e-110">Wave 資料流程回呼函數的指標，其類型為 [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)。</span><span class="sxs-lookup"><span data-stu-id="3655e-110">Pointer to the wave stream callback function, of type [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span></span> <span data-ttu-id="3655e-111">針對此參數指定 **Null** ，以停用先前安裝的 wave stream 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="3655e-111">Specify **NULL** for this parameter to disable a previously installed wave stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3655e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3655e-112">Return Value</span></span>

<span data-ttu-id="3655e-113">如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3655e-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="3655e-114">備註</span><span class="sxs-lookup"><span data-stu-id="3655e-114">Remarks</span></span>

<span data-ttu-id="3655e-115">「捕獲視窗」會在將音訊緩衝區寫入磁片之前呼叫程式。</span><span class="sxs-lookup"><span data-stu-id="3655e-115">The capture window calls the procedure before writing the audio buffer to disk.</span></span> <span data-ttu-id="3655e-116">這可讓應用程式視需要修改音訊緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3655e-116">This allows applications to modify the audio buffer if desired.</span></span>

<span data-ttu-id="3655e-117">如果使用 wave 資料流程回呼函式，則必須先安裝該函式，才能啟動 capture 會話，且必須在會話持續時間內保持啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="3655e-117">If a wave stream callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="3655e-118">您可以在串流處理的結束之後停用此功能。</span><span class="sxs-lookup"><span data-stu-id="3655e-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="3655e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3655e-119">Requirements</span></span>



| <span data-ttu-id="3655e-120">需求</span><span class="sxs-lookup"><span data-stu-id="3655e-120">Requirement</span></span> | <span data-ttu-id="3655e-121">值</span><span class="sxs-lookup"><span data-stu-id="3655e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3655e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3655e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3655e-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3655e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3655e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3655e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3655e-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3655e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3655e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3655e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3655e-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="3655e-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3655e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3655e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3655e-129">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="3655e-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3655e-130">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="3655e-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





