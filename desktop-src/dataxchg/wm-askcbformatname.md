---
title: 'WM_ASKCBFORMATNAME 訊息 (Winuser .h) '
description: 由剪貼簿檢視器視窗傳送給剪貼簿擁有者，以要求 CF \_ OWNERDISPLAY 剪貼簿格式的名稱。
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- WM_ASKCBFORMATNAME 訊息資料交換
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094200"
---
# <a name="wm_askcbformatname-message"></a><span data-ttu-id="5b3fb-104">WM \_ ASKCBFORMATNAME 訊息</span><span class="sxs-lookup"><span data-stu-id="5b3fb-104">WM\_ASKCBFORMATNAME message</span></span>

<span data-ttu-id="5b3fb-105">由剪貼簿檢視器視窗傳送給剪貼簿擁有者，以要求 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 剪貼簿格式的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-105">Sent to the clipboard owner by a clipboard viewer window to request the name of a [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) clipboard format.</span></span>

<span data-ttu-id="5b3fb-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a><span data-ttu-id="5b3fb-107">參數</span><span class="sxs-lookup"><span data-stu-id="5b3fb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b3fb-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b3fb-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b3fb-109">*LParam* 參數所指向之緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-109">The size, in characters, of the buffer pointed to by the *lParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5b3fb-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b3fb-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b3fb-111">要接收剪貼簿格式名稱之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-111">A pointer to the buffer that is to receive the clipboard format name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b3fb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b3fb-112">Return value</span></span>

<span data-ttu-id="5b3fb-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b3fb-114">備註</span><span class="sxs-lookup"><span data-stu-id="5b3fb-114">Remarks</span></span>

<span data-ttu-id="5b3fb-115">為了回應這則訊息，剪貼簿擁有者應該將擁有者顯示格式的名稱複製到指定的緩衝區，而不超過 *wParam* 參數所指定的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-115">In response to this message, the clipboard owner should copy the name of the owner-display format to the specified buffer, not exceeding the buffer size specified by the *wParam* parameter.</span></span>

<span data-ttu-id="5b3fb-116">[剪貼簿檢視器] 視窗會將此訊息傳送給剪貼簿擁有者，以判斷 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的名稱，例如，用來初始化功能表清單的可用格式。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-116">A clipboard viewer window sends this message to the clipboard owner to determine the name of the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format   for example, to initialize a menu listing available formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b3fb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b3fb-117">Requirements</span></span>



| <span data-ttu-id="5b3fb-118">需求</span><span class="sxs-lookup"><span data-stu-id="5b3fb-118">Requirement</span></span> | <span data-ttu-id="5b3fb-119">值</span><span class="sxs-lookup"><span data-stu-id="5b3fb-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3fb-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b3fb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5b3fb-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b3fb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5b3fb-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b3fb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5b3fb-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b3fb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b3fb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5b3fb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b3fb-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5b3fb-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b3fb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b3fb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b3fb-127">剪貼簿總覽</span><span class="sxs-lookup"><span data-stu-id="5b3fb-127">Clipboard Overview</span></span>](clipboard.md)
</dt> </dl>

 

