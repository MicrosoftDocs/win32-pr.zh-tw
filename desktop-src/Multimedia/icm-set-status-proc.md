---
title: 'ICM_SET_STATUS_PROC 訊息 (Vfw .h) '
description: ICM \_ SET \_ STATUS \_ PROC 訊息提供狀態回呼函式，其狀態為冗長的作業。
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- ICM_SET_STATUS_PROC message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d7ad2745ab53c2e04a1588ddbf1b1e5d755202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467089"
---
# <a name="icm_set_status_proc-message"></a><span data-ttu-id="3e466-104">ICM \_ 設定 \_ 狀態 \_ 進程訊息</span><span class="sxs-lookup"><span data-stu-id="3e466-104">ICM\_SET\_STATUS\_PROC message</span></span>

<span data-ttu-id="3e466-105">**ICM \_ SET \_ STATUS \_ PROC** 訊息提供狀態回呼函式，其狀態為冗長的作業。</span><span class="sxs-lookup"><span data-stu-id="3e466-105">The **ICM\_SET\_STATUS\_PROC** message provides a status callback function with the status of a lengthy operation.</span></span>


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a><span data-ttu-id="3e466-106">參數</span><span class="sxs-lookup"><span data-stu-id="3e466-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e466-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span><span class="sxs-lookup"><span data-stu-id="3e466-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span></span>
</dt> <dd>

<span data-ttu-id="3e466-108">[**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3e466-108">Pointer to an [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3e466-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e466-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3e466-110">**ICSETSTATUSPROC** 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3e466-110">Size, in bytes, of **ICSETSTATUSPROC**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e466-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e466-111">Return Value</span></span>

<span data-ttu-id="3e466-112">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3e466-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e466-113">備註</span><span class="sxs-lookup"><span data-stu-id="3e466-113">Remarks</span></span>

<span data-ttu-id="3e466-114">此訊息的支援是選擇性的，但強烈建議在壓縮或解壓縮所花的時間超過大約一秒的1秒。</span><span class="sxs-lookup"><span data-stu-id="3e466-114">Support of this message is optional but strongly recommended if compression or decompression takes longer than approximately one-tenth of a second.</span></span>

<span data-ttu-id="3e466-115">應用程式可以在冗長的作業期間，定期將此訊息傳送至狀態回呼函式。</span><span class="sxs-lookup"><span data-stu-id="3e466-115">An application can send this message periodically to a status callback function during lengthy operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e466-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e466-116">Requirements</span></span>



| <span data-ttu-id="3e466-117">需求</span><span class="sxs-lookup"><span data-stu-id="3e466-117">Requirement</span></span> | <span data-ttu-id="3e466-118">值</span><span class="sxs-lookup"><span data-stu-id="3e466-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3e466-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e466-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e466-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e466-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3e466-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e466-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e466-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e466-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3e466-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3e466-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e466-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e466-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e466-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e466-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e466-126">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="3e466-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3e466-127">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="3e466-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





