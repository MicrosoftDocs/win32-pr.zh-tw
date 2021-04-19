---
description: 應用程式會將 WM \_ MDISETMENU 訊息傳送至多重文件介面 (mdi) 用戶端視窗來取代 mdi 框架視窗的整個功能表、取代框架視窗的視窗功能表，或兩者都是。
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: 'WM_MDISETMENU 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974688"
---
# <a name="wm_mdisetmenu-message"></a><span data-ttu-id="05e93-103">WM \_ MDISETMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="05e93-103">WM\_MDISETMENU message</span></span>

<span data-ttu-id="05e93-104">應用程式會將 **WM \_ MDISETMENU** 訊息傳送至多重文件介面 (mdi) 用戶端視窗來取代 mdi 框架視窗的整個功能表、取代框架視窗的視窗功能表，或兩者都是。</span><span class="sxs-lookup"><span data-stu-id="05e93-104">An application sends the **WM\_MDISETMENU** message to a multiple-document interface (MDI) client window to replace the entire menu of an MDI frame window, to replace the window menu of the frame window, or both.</span></span>


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a><span data-ttu-id="05e93-105">參數</span><span class="sxs-lookup"><span data-stu-id="05e93-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05e93-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05e93-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05e93-107">新框架視窗功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="05e93-107">A handle to the new frame window menu.</span></span> <span data-ttu-id="05e93-108">如果此參數為 **Null**，則不會變更框架視窗功能表。</span><span class="sxs-lookup"><span data-stu-id="05e93-108">If this parameter is **NULL**, the frame window menu is not changed.</span></span>

</dd> <dt>

<span data-ttu-id="05e93-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05e93-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05e93-110">新視窗功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="05e93-110">A handle to the new window menu.</span></span> <span data-ttu-id="05e93-111">如果此參數為 **Null**，則不會變更視窗功能表。</span><span class="sxs-lookup"><span data-stu-id="05e93-111">If this parameter is **NULL**, the window menu is not changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05e93-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="05e93-112">Return value</span></span>

<span data-ttu-id="05e93-113">類型： **HMENU**</span><span class="sxs-lookup"><span data-stu-id="05e93-113">Type: **HMENU**</span></span>

<span data-ttu-id="05e93-114">如果訊息成功，傳回值就是舊框架視窗功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="05e93-114">If the message succeeds, the return value is the handle to the old frame window menu.</span></span>

<span data-ttu-id="05e93-115">如果訊息失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="05e93-115">If the message fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="05e93-116">備註</span><span class="sxs-lookup"><span data-stu-id="05e93-116">Remarks</span></span>

<span data-ttu-id="05e93-117">傳送此訊息之後，應用程式必須呼叫 [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) 函式來更新功能表列。</span><span class="sxs-lookup"><span data-stu-id="05e93-117">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

<span data-ttu-id="05e93-118">如果此訊息取代了 [視窗] 功能表，則會從上一個 [視窗] 功能表中移除 MDI 子視窗功能表項目，並將其加入至新的 [視窗] 功能表。</span><span class="sxs-lookup"><span data-stu-id="05e93-118">If this message replaces the window menu, the MDI child window menu items are removed from the previous window menu and added to the new window menu.</span></span>

<span data-ttu-id="05e93-119">如果 MDI 子視窗最大化，而此訊息取代了 MDI 框架視窗功能表，則會從先前的框架視窗功能表中移除 [視窗] 功能表圖示和還原圖示，並將其加入至新的框架視窗功能表。</span><span class="sxs-lookup"><span data-stu-id="05e93-119">If an MDI child window is maximized and this message replaces the MDI frame window menu, the window menu icon and restore icon are removed from the previous frame window menu and added to the new frame window menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="05e93-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="05e93-120">Requirements</span></span>



| <span data-ttu-id="05e93-121">需求</span><span class="sxs-lookup"><span data-stu-id="05e93-121">Requirement</span></span> | <span data-ttu-id="05e93-122">值</span><span class="sxs-lookup"><span data-stu-id="05e93-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05e93-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05e93-123">Minimum supported client</span></span><br/> | <span data-ttu-id="05e93-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05e93-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="05e93-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05e93-125">Minimum supported server</span></span><br/> | <span data-ttu-id="05e93-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05e93-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05e93-127">標頭</span><span class="sxs-lookup"><span data-stu-id="05e93-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="05e93-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="05e93-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05e93-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05e93-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="05e93-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="05e93-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="05e93-131">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="05e93-131">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="05e93-132">**WM \_ MDIREFRESHMENU**</span><span class="sxs-lookup"><span data-stu-id="05e93-132">**WM\_MDIREFRESHMENU**</span></span>](wm-mdirefreshmenu.md)
</dt> <dt>

<span data-ttu-id="05e93-133">**概念**</span><span class="sxs-lookup"><span data-stu-id="05e93-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="05e93-134">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="05e93-134">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
