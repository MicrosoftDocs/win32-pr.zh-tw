---
title: 'WM_CAP_SET_AUDIOFORMAT 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ AUDIOFORMAT 訊息會設定執行串流或步驟捕捉時使用的音訊格式。 您可以使用 capSetAudioFormat 宏明確地傳送此訊息。
ms.assetid: 8bffa401-3d36-43bb-9f69-988ebc69b860
keywords:
- WM_CAP_SET_AUDIOFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c519ed936d2e71d9eee88435a94acc8c567a9a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104153"
---
# <a name="wm_cap_set_audioformat-message"></a><span data-ttu-id="10e7e-105">WM \_ CAP \_ 設定 \_ AUDIOFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="10e7e-105">WM\_CAP\_SET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="10e7e-106">**WM \_ CAP \_ 設定 \_ AUDIOFORMAT** 訊息會設定執行串流或步驟捕捉時使用的音訊格式。</span><span class="sxs-lookup"><span data-stu-id="10e7e-106">The **WM\_CAP\_SET\_AUDIOFORMAT** message sets the audio format to use when performing streaming or step capture.</span></span> <span data-ttu-id="10e7e-107">您可以使用 [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="10e7e-107">You can send this message explicitly or by using the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro.</span></span>


```C++
WM_CAP_SET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="10e7e-108">參數</span><span class="sxs-lookup"><span data-stu-id="10e7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10e7e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="10e7e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="10e7e-110">**S** 所參考之結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="10e7e-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="10e7e-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span><span class="sxs-lookup"><span data-stu-id="10e7e-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="10e7e-112">定義音訊格式的 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) 或 [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="10e7e-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure that defines the audio format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10e7e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="10e7e-113">Return Value</span></span>

<span data-ttu-id="10e7e-114">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="10e7e-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="10e7e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="10e7e-115">Requirements</span></span>



| <span data-ttu-id="10e7e-116">需求</span><span class="sxs-lookup"><span data-stu-id="10e7e-116">Requirement</span></span> | <span data-ttu-id="10e7e-117">值</span><span class="sxs-lookup"><span data-stu-id="10e7e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="10e7e-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10e7e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10e7e-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10e7e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="10e7e-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10e7e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10e7e-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10e7e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="10e7e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="10e7e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="10e7e-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="10e7e-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10e7e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10e7e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10e7e-125">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="10e7e-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="10e7e-126">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="10e7e-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

