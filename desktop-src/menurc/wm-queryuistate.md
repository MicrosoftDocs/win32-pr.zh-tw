---
title: 'WM_QUERYUISTATE 訊息 (Winuser .h) '
description: 應用程式會傳送 WM \_ QUERYUISTATE 訊息來取得視窗的 UI 狀態。
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969825"
---
# <a name="wm_queryuistate-message"></a><span data-ttu-id="7f52d-104">WM \_ QUERYUISTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="7f52d-104">WM\_QUERYUISTATE message</span></span>

<span data-ttu-id="7f52d-105">應用程式會傳送 **WM \_ QUERYUISTATE** 訊息來取得視窗的 UI 狀態。</span><span class="sxs-lookup"><span data-stu-id="7f52d-105">An application sends the **WM\_QUERYUISTATE** message to retrieve the UI state for a window.</span></span>


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a><span data-ttu-id="7f52d-106">參數</span><span class="sxs-lookup"><span data-stu-id="7f52d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f52d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f52d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f52d-108">未使用此參數，且必須為0。</span><span class="sxs-lookup"><span data-stu-id="7f52d-108">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="7f52d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f52d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f52d-110">未使用此參數，且必須為0。</span><span class="sxs-lookup"><span data-stu-id="7f52d-110">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f52d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f52d-111">Return value</span></span>

<span data-ttu-id="7f52d-112">如果焦點指標和鍵盤快速鍵是可見的，則傳回值為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="7f52d-112">The return value is **NULL** if the focus indicators and the keyboard accelerators are visible.</span></span> <span data-ttu-id="7f52d-113">否則，傳回值可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="7f52d-113">Otherwise, the return value can be one or more of the following values.</span></span>



| <span data-ttu-id="7f52d-114">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="7f52d-114">Return code/value</span></span>                                                                                                                                       | <span data-ttu-id="7f52d-115">Description</span><span class="sxs-lookup"><span data-stu-id="7f52d-115">Description</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f52d-116"><dt>**UISF \_現用**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="7f52d-116"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>    | <span data-ttu-id="7f52d-117">控制項應以用於作用中控制項的樣式來繪製。</span><span class="sxs-lookup"><span data-stu-id="7f52d-117">A control should be drawn in the style used for active controls.</span></span><br/> |
| <dl> <span data-ttu-id="7f52d-118"><dt>**UISF \_HIDEACCEL**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="7f52d-118"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="7f52d-119">鍵盤快捷為隱藏。</span><span class="sxs-lookup"><span data-stu-id="7f52d-119">Keyboard accelerators are hidden.</span></span><br/>                                |
| <dl> <span data-ttu-id="7f52d-120"><dt>**UISF \_HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="7f52d-120"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="7f52d-121">焦點指標是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="7f52d-121">Focus indicators are hidden.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="7f52d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f52d-122">Requirements</span></span>



| <span data-ttu-id="7f52d-123">需求</span><span class="sxs-lookup"><span data-stu-id="7f52d-123">Requirement</span></span> | <span data-ttu-id="7f52d-124">值</span><span class="sxs-lookup"><span data-stu-id="7f52d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f52d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f52d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7f52d-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f52d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7f52d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f52d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7f52d-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f52d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7f52d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="7f52d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f52d-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7f52d-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f52d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f52d-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="7f52d-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="7f52d-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7f52d-133">**WM \_ CHANGEUISTATE**</span><span class="sxs-lookup"><span data-stu-id="7f52d-133">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="7f52d-134">**WM \_ UPDATEUISTATE**</span><span class="sxs-lookup"><span data-stu-id="7f52d-134">**WM\_UPDATEUISTATE**</span></span>](wm-updateuistate.md)
</dt> <dt>

<span data-ttu-id="7f52d-135">**概念**</span><span class="sxs-lookup"><span data-stu-id="7f52d-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7f52d-136">鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="7f52d-136">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

 





