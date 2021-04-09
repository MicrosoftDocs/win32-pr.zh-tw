---
title: 'WM_CAP_GET_STATUS 訊息 (Vfw .h) '
description: WM \_ CAP \_ 取得 \_ 狀態訊息會抓取捕捉視窗的狀態。 您可以使用 capGetStatus 宏明確地傳送此訊息。
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- WM_CAP_GET_STATUS message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024558"
---
# <a name="wm_cap_get_status-message"></a><span data-ttu-id="1229e-105">WM \_ CAP \_ 取得 \_ 狀態訊息</span><span class="sxs-lookup"><span data-stu-id="1229e-105">WM\_CAP\_GET\_STATUS message</span></span>

<span data-ttu-id="1229e-106">**WM \_ CAP \_ 取得 \_ 狀態** 消息會抓取捕捉視窗的狀態。</span><span class="sxs-lookup"><span data-stu-id="1229e-106">The **WM\_CAP\_GET\_STATUS** message retrieves the status of the capture window.</span></span> <span data-ttu-id="1229e-107">您可以使用 [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1229e-107">You can send this message explicitly or by using the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro.</span></span>


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="1229e-108">參數</span><span class="sxs-lookup"><span data-stu-id="1229e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1229e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="1229e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="1229e-110">**S** 所參考之結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1229e-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="1229e-111"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="1229e-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="1229e-112">[**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1229e-112">Pointer to a [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1229e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1229e-113">Return Value</span></span>

<span data-ttu-id="1229e-114">如果成功，則傳回 **TRUE** ，如果捕捉視窗未連接到 capture 驅動程式，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1229e-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="1229e-115">備註</span><span class="sxs-lookup"><span data-stu-id="1229e-115">Remarks</span></span>

<span data-ttu-id="1229e-116">[**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)結構包含 [capture] 視窗的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1229e-116">The [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure contains the current state of the capture window.</span></span> <span data-ttu-id="1229e-117">由於這個狀態是動態的，且因回應各種訊息而變更，因此應用程式應該在傳送 [**WM \_ CAP \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) 訊息之後初始化此結構 (或使用 [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) 宏) ，以及每次需要啟用功能表項目或判斷視窗的實際狀態。</span><span class="sxs-lookup"><span data-stu-id="1229e-117">Since this state is dynamic and changes in response to various messages, the application should initialize this structure after sending the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro) and whenever it needs to enable menu items or determine the actual state of the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="1229e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1229e-118">Requirements</span></span>



| <span data-ttu-id="1229e-119">需求</span><span class="sxs-lookup"><span data-stu-id="1229e-119">Requirement</span></span> | <span data-ttu-id="1229e-120">值</span><span class="sxs-lookup"><span data-stu-id="1229e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1229e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1229e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1229e-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1229e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1229e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1229e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1229e-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1229e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1229e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1229e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1229e-126"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="1229e-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1229e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1229e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1229e-128">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="1229e-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="1229e-129">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="1229e-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





