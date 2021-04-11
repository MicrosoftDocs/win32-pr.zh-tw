---
title: 'ICM_DRAW_SETTIME 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ SETTIME 提供同步處理資訊給轉譯驅動程式，以處理繪製框架的時間。
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- ICM_DRAW_SETTIME message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843404"
---
# <a name="icm_draw_settime-message"></a><span data-ttu-id="01ec8-104">ICM \_ 繪圖 \_ SETTIME 訊息</span><span class="sxs-lookup"><span data-stu-id="01ec8-104">ICM\_DRAW\_SETTIME message</span></span>

<span data-ttu-id="01ec8-105">**ICM \_ DRAW \_ SETTIME** 提供同步處理資訊給轉譯驅動程式，以處理繪製框架的時間。</span><span class="sxs-lookup"><span data-stu-id="01ec8-105">The **ICM\_DRAW\_SETTIME** provides synchronization information to a rendering driver that handles the timing of drawing frames.</span></span> <span data-ttu-id="01ec8-106">同步處理資訊是要繪製的框架樣本數。</span><span class="sxs-lookup"><span data-stu-id="01ec8-106">The synchronization information is the sample number of the frame to draw.</span></span> <span data-ttu-id="01ec8-107">您可以使用 [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="01ec8-107">You can send this message explicitly or by using the [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) macro.</span></span>


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="01ec8-108">參數</span><span class="sxs-lookup"><span data-stu-id="01ec8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01ec8-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span><span class="sxs-lookup"><span data-stu-id="01ec8-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span></span>
</dt> <dd>

<span data-ttu-id="01ec8-110">要轉譯的框架樣本數。</span><span class="sxs-lookup"><span data-stu-id="01ec8-110">Sample number of the frame to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01ec8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="01ec8-111">Return Value</span></span>

<span data-ttu-id="01ec8-112">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="01ec8-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="01ec8-113">備註</span><span class="sxs-lookup"><span data-stu-id="01ec8-113">Remarks</span></span>

<span data-ttu-id="01ec8-114">通常，驅動程式會將指定的值與其內部時鐘的時間相關聯的框架編號進行比較，並在差異很大時嘗試同步處理兩者。</span><span class="sxs-lookup"><span data-stu-id="01ec8-114">Typically, the driver compares the specified value with the frame number associated with the time of its internal clock and attempts to synchronize the two if the difference is significant.</span></span>

<span data-ttu-id="01ec8-115">當硬體執行它自己的非同步解壓縮、時間和繪圖，且硬體依賴外部同步處理信號 (硬體未用來作為同步處理主機) 時，請使用此訊息。</span><span class="sxs-lookup"><span data-stu-id="01ec8-115">Use this message when the hardware performs its own asynchronous decompression, timing, and drawing, and the hardware relies on an external synchronization signal (the hardware is not being used as the synchronization master).</span></span>

## <a name="requirements"></a><span data-ttu-id="01ec8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="01ec8-116">Requirements</span></span>



| <span data-ttu-id="01ec8-117">需求</span><span class="sxs-lookup"><span data-stu-id="01ec8-117">Requirement</span></span> | <span data-ttu-id="01ec8-118">值</span><span class="sxs-lookup"><span data-stu-id="01ec8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01ec8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01ec8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="01ec8-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01ec8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="01ec8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01ec8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="01ec8-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01ec8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="01ec8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="01ec8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="01ec8-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="01ec8-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01ec8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01ec8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01ec8-126">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="01ec8-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="01ec8-127">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="01ec8-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





