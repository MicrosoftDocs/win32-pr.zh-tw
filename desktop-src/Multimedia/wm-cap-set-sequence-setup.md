---
title: 'WM_CAP_SET_SEQUENCE_SETUP 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 順序 \_ 安裝程式訊息會設定用於串流處理捕獲的設定參數。 您可以使用 capCaptureSetSetup 宏明確地傳送此訊息。
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- WM_CAP_SET_SEQUENCE_SETUP message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509359"
---
# <a name="wm_cap_set_sequence_setup-message"></a><span data-ttu-id="c9203-105">WM \_ CAP \_ 設定 \_ 順序設定 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="c9203-105">WM\_CAP\_SET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="c9203-106">**WM \_ CAP \_ 設定 \_ 順序 \_ 安裝程式** 訊息會設定用於串流處理捕獲的設定參數。</span><span class="sxs-lookup"><span data-stu-id="c9203-106">The **WM\_CAP\_SET\_SEQUENCE\_SETUP** message sets the configuration parameters used with streaming capture.</span></span> <span data-ttu-id="c9203-107">您可以使用 [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c9203-107">You can send this message explicitly or by using the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro.</span></span>


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a><span data-ttu-id="c9203-108">參數</span><span class="sxs-lookup"><span data-stu-id="c9203-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9203-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="c9203-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="c9203-110">**S** 所參考之結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c9203-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="c9203-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span><span class="sxs-lookup"><span data-stu-id="c9203-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span></span>
</dt> <dd>

<span data-ttu-id="c9203-112">[**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c9203-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9203-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9203-113">Return Value</span></span>

<span data-ttu-id="c9203-114">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c9203-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9203-115">備註</span><span class="sxs-lookup"><span data-stu-id="c9203-115">Remarks</span></span>

<span data-ttu-id="c9203-116">如需用來控制串流處理捕獲之參數的相關資訊，請參閱 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) 結構。</span><span class="sxs-lookup"><span data-stu-id="c9203-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9203-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9203-117">Requirements</span></span>



| <span data-ttu-id="c9203-118">需求</span><span class="sxs-lookup"><span data-stu-id="c9203-118">Requirement</span></span> | <span data-ttu-id="c9203-119">值</span><span class="sxs-lookup"><span data-stu-id="c9203-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c9203-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9203-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c9203-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9203-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c9203-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9203-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c9203-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9203-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c9203-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c9203-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9203-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9203-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9203-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9203-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9203-127">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="c9203-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c9203-128">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="c9203-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





