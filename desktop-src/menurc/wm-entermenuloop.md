---
title: 'WM_ENTERMENULOOP 訊息 (Winuser .h) '
description: 通知應用程式的主視窗程式，指出已進入功能表強制回應迴圈。
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996176"
---
# <a name="wm_entermenuloop-message"></a><span data-ttu-id="b2764-104">WM \_ ENTERMENULOOP 訊息</span><span class="sxs-lookup"><span data-stu-id="b2764-104">WM\_ENTERMENULOOP message</span></span>

<span data-ttu-id="b2764-105">通知應用程式的主視窗程式，指出已進入功能表強制回應迴圈。</span><span class="sxs-lookup"><span data-stu-id="b2764-105">Notifies an application's main window procedure that a menu modal loop has been entered.</span></span>


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a><span data-ttu-id="b2764-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2764-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2764-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2764-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2764-108">指定是否使用 [**trackpopupmenu 讓**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) 函數輸入視窗功能表。</span><span class="sxs-lookup"><span data-stu-id="b2764-108">Specifies whether the window menu was entered using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function.</span></span> <span data-ttu-id="b2764-109">如果使用 **trackpopupmenu 讓** 輸入視窗功能表，此參數的值為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="b2764-109">This parameter has a value of **TRUE** if the window menu was entered using **TrackPopupMenu**, and **FALSE** if it was not.</span></span>

</dd> <dt>

<span data-ttu-id="b2764-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2764-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2764-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="b2764-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2764-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2764-112">Return value</span></span>

<span data-ttu-id="b2764-113">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="b2764-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2764-114">備註</span><span class="sxs-lookup"><span data-stu-id="b2764-114">Remarks</span></span>

<span data-ttu-id="b2764-115">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="b2764-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2764-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2764-116">Requirements</span></span>



| <span data-ttu-id="b2764-117">需求</span><span class="sxs-lookup"><span data-stu-id="b2764-117">Requirement</span></span> | <span data-ttu-id="b2764-118">值</span><span class="sxs-lookup"><span data-stu-id="b2764-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2764-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2764-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2764-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2764-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b2764-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2764-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2764-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2764-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b2764-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b2764-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2764-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b2764-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2764-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2764-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2764-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="b2764-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2764-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="b2764-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b2764-128">**WM \_ EXITMENULOOP**</span><span class="sxs-lookup"><span data-stu-id="b2764-128">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
</dt> <dt>

<span data-ttu-id="b2764-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="b2764-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b2764-130">功能表</span><span class="sxs-lookup"><span data-stu-id="b2764-130">Menus</span></span>](menus.md)
</dt> </dl>

 

