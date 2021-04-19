---
title: 'ICM_DRAW_GETTIME 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ GETTIME 訊息會要求轉譯驅動程式，以控制繪製畫面格的時間，以傳回其內部時鐘的目前值。 您可以使用 ICDrawGetTime 宏明確地傳送此訊息。
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- ICM_DRAW_GETTIME message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969980"
---
# <a name="icm_draw_gettime-message"></a><span data-ttu-id="4872d-105">ICM \_ 繪圖 \_ GETTIME 訊息</span><span class="sxs-lookup"><span data-stu-id="4872d-105">ICM\_DRAW\_GETTIME message</span></span>

<span data-ttu-id="4872d-106">**ICM \_ DRAW \_ GETTIME** 訊息會要求轉譯驅動程式，以控制繪製畫面格的時間，以傳回其內部時鐘的目前值。</span><span class="sxs-lookup"><span data-stu-id="4872d-106">The **ICM\_DRAW\_GETTIME** message requests a rendering driver that controls the timing of drawing frames to return the current value of its internal clock.</span></span> <span data-ttu-id="4872d-107">您可以使用 [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="4872d-107">You can send this message explicitly or by using the [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) macro.</span></span>


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="4872d-108">參數</span><span class="sxs-lookup"><span data-stu-id="4872d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4872d-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span><span class="sxs-lookup"><span data-stu-id="4872d-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span></span>
</dt> <dd>

<span data-ttu-id="4872d-110">包含目前時間的位址。</span><span class="sxs-lookup"><span data-stu-id="4872d-110">Address to contain the current time.</span></span> <span data-ttu-id="4872d-111">傳回值應該在範例中指定。</span><span class="sxs-lookup"><span data-stu-id="4872d-111">The return value should be specified in samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4872d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4872d-112">Return Value</span></span>

<span data-ttu-id="4872d-113">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4872d-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4872d-114">備註</span><span class="sxs-lookup"><span data-stu-id="4872d-114">Remarks</span></span>

<span data-ttu-id="4872d-115">這則訊息通常是由執行自己的非同步解壓縮、時間和繪圖的硬體所支援。</span><span class="sxs-lookup"><span data-stu-id="4872d-115">This message is generally supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span> <span data-ttu-id="4872d-116">如果使用硬體作為同步處理主機，也可以傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="4872d-116">The message can also be sent if the hardware is being used as the synchronization master.</span></span>

## <a name="requirements"></a><span data-ttu-id="4872d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4872d-117">Requirements</span></span>



| <span data-ttu-id="4872d-118">需求</span><span class="sxs-lookup"><span data-stu-id="4872d-118">Requirement</span></span> | <span data-ttu-id="4872d-119">值</span><span class="sxs-lookup"><span data-stu-id="4872d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4872d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4872d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4872d-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4872d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4872d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4872d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4872d-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4872d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4872d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4872d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4872d-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="4872d-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4872d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4872d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4872d-127">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="4872d-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="4872d-128">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="4872d-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





