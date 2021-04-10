---
title: 'ICM_GETBUFFERSWANTED 訊息 (Vfw .h) '
description: ICM \_ GETBUFFERSWANTED 訊息會查詢驅動程式，以取得要配置的緩衝區數目。 您可以使用 ICGetBuffersWanted 宏明確地傳送此訊息。
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- ICM_GETBUFFERSWANTED message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06de8cc3bcfe463d0318651c8e2d51b269504769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934037"
---
# <a name="icm_getbufferswanted-message"></a><span data-ttu-id="98323-105">ICM \_ GETBUFFERSWANTED 訊息</span><span class="sxs-lookup"><span data-stu-id="98323-105">ICM\_GETBUFFERSWANTED message</span></span>

<span data-ttu-id="98323-106">**ICM \_ GETBUFFERSWANTED** 訊息會查詢驅動程式，以取得要配置的緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="98323-106">The **ICM\_GETBUFFERSWANTED** message queries a driver for the number of buffers to allocate.</span></span> <span data-ttu-id="98323-107">您可以使用 [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="98323-107">You can send this message explicitly or by using the [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) macro.</span></span>


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="98323-108">參數</span><span class="sxs-lookup"><span data-stu-id="98323-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98323-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span><span class="sxs-lookup"><span data-stu-id="98323-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span></span>
</dt> <dd>

<span data-ttu-id="98323-110">包含驅動程式所需的樣本數目，以有效率地轉譯資料的位址。</span><span class="sxs-lookup"><span data-stu-id="98323-110">Address to contain the number of samples the driver needs to efficiently render the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98323-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="98323-111">Return Value</span></span>

<span data-ttu-id="98323-112">\_如果成功或 ICERR 不支援，則會傳回 ICERR OK \_ 。</span><span class="sxs-lookup"><span data-stu-id="98323-112">Returns ICERR\_OK if successful or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="98323-113">備註</span><span class="sxs-lookup"><span data-stu-id="98323-113">Remarks</span></span>

<span data-ttu-id="98323-114">使用硬體轉譯資料的驅動程式會使用這個訊息，並想要確保等待緩衝區抵達時所造成的時間延遲降到一。</span><span class="sxs-lookup"><span data-stu-id="98323-114">This message is used by drivers that use hardware to render data and want to ensure a minimal time lag caused by waiting for buffers to arrive.</span></span> <span data-ttu-id="98323-115">例如，如果驅動程式控制的影片解壓縮面板可以容納10個畫面格，則會傳回此訊息的10。</span><span class="sxs-lookup"><span data-stu-id="98323-115">For example, if a driver controls a video decompression board that can hold 10 frames of video, it could return 10 for this message.</span></span> <span data-ttu-id="98323-116">這會指示應用程式在目前需要的畫面格之前，嘗試保留10個框架。</span><span class="sxs-lookup"><span data-stu-id="98323-116">This instructs applications to try to stay 10 frames ahead of the frame it currently needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="98323-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="98323-117">Requirements</span></span>



| <span data-ttu-id="98323-118">需求</span><span class="sxs-lookup"><span data-stu-id="98323-118">Requirement</span></span> | <span data-ttu-id="98323-119">值</span><span class="sxs-lookup"><span data-stu-id="98323-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="98323-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98323-120">Minimum supported client</span></span><br/> | <span data-ttu-id="98323-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98323-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="98323-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98323-122">Minimum supported server</span></span><br/> | <span data-ttu-id="98323-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98323-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="98323-124">標頭</span><span class="sxs-lookup"><span data-stu-id="98323-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="98323-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="98323-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98323-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98323-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98323-127">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="98323-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="98323-128">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="98323-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





