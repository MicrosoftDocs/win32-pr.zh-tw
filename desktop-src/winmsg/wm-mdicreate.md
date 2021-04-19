---
description: 應用程式會將 WM \_ MDICREATE 訊息傳送至多重文件介面， (mdi) 用戶端視窗來建立 mdi 子視窗。
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: 'WM_MDICREATE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975358"
---
# <a name="wm_mdicreate-message"></a><span data-ttu-id="41b1a-103">WM \_ MDICREATE 訊息</span><span class="sxs-lookup"><span data-stu-id="41b1a-103">WM\_MDICREATE message</span></span>

<span data-ttu-id="41b1a-104">應用程式會將 **WM \_ MDICREATE** 訊息傳送至多重文件介面， (mdi) 用戶端視窗來建立 mdi 子視窗。</span><span class="sxs-lookup"><span data-stu-id="41b1a-104">An application sends the **WM\_MDICREATE** message to a multiple-document interface (MDI) client window to create an MDI child window.</span></span>


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a><span data-ttu-id="41b1a-105">參數</span><span class="sxs-lookup"><span data-stu-id="41b1a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41b1a-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41b1a-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41b1a-107">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="41b1a-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41b1a-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41b1a-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41b1a-109">[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)結構的指標，其中包含系統用來建立 MDI 子視窗的資訊。</span><span class="sxs-lookup"><span data-stu-id="41b1a-109">A pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure containing information that the system uses to create the MDI child window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41b1a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="41b1a-110">Return value</span></span>

<span data-ttu-id="41b1a-111">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="41b1a-111">Type: **HWND**</span></span>

<span data-ttu-id="41b1a-112">如果訊息成功，傳回值就是新子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="41b1a-112">If the message succeeds, the return value is the handle to the new child window.</span></span>

<span data-ttu-id="41b1a-113">如果訊息失敗，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="41b1a-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="41b1a-114">備註</span><span class="sxs-lookup"><span data-stu-id="41b1a-114">Remarks</span></span>

<span data-ttu-id="41b1a-115">MDI 子視窗會以 [**視窗樣式**](window-styles.md) 的 **ws \_ child**、 **ws \_ CLIPSIBLINGS**、 **ws \_ CLIPCHILDREN**、 **Ws \_ SYSMENU**、 **ws \_ CAPTION**、 **ws \_ THICKFRAME**、 **ws \_ MINIMIZEBOX** 和 **ws \_ MAXIMIZEBOX** 來建立，再加上 [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) 結構中指定的其他樣式位。</span><span class="sxs-lookup"><span data-stu-id="41b1a-115">The MDI child window is created with the [**window style**](window-styles.md) bits **WS\_CHILD**, **WS\_CLIPSIBLINGS**, **WS\_CLIPCHILDREN**, **WS\_SYSMENU**, **WS\_CAPTION**, **WS\_THICKFRAME**, **WS\_MINIMIZEBOX**, and **WS\_MAXIMIZEBOX**, plus additional style bits specified in the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="41b1a-116">系統會將新子視窗的標題新增至框架視窗的 [視窗] 功能表。</span><span class="sxs-lookup"><span data-stu-id="41b1a-116">The system adds the title of the new child window to the window menu of the frame window.</span></span> <span data-ttu-id="41b1a-117">應用程式應該使用此訊息來建立用戶端視窗的所有子視窗。</span><span class="sxs-lookup"><span data-stu-id="41b1a-117">An application should use this message to create all child windows of the client window.</span></span>

<span data-ttu-id="41b1a-118">如果 MDI 用戶端視窗收到任何訊息，而該訊息會在作用中的子視窗最大化時變更其子視窗的啟用，系統會還原使用中的子視窗，並將新啟用的子視窗最大化。</span><span class="sxs-lookup"><span data-stu-id="41b1a-118">If an MDI client window receives any message that changes the activation of its child windows while the active child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

<span data-ttu-id="41b1a-119">建立 MDI 子視窗時，系統會將 [**WM \_ 建立**](wm-create.md) 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="41b1a-119">When an MDI child window is created, the system sends the [**WM\_CREATE**](wm-create.md) message to the window.</span></span> <span data-ttu-id="41b1a-120">**WM \_ 建立** 訊息的 *lParam* 參數包含 [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="41b1a-120">The *lParam* parameter of the **WM\_CREATE** message contains a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="41b1a-121">此結構的 *lpCreateParams* 成員包含 [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) 結構的指標，該結構會與建立 MDI 子視窗的 **WM \_ MDICREATE** 訊息一起傳遞。</span><span class="sxs-lookup"><span data-stu-id="41b1a-121">The *lpCreateParams* member of this structure contains a pointer to the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure passed with the **WM\_MDICREATE** message that created the MDI child window.</span></span>

<span data-ttu-id="41b1a-122">當您仍在處理 **wm \_ MDICREATE** 訊息時，應用程式不應該傳送第二個 **wm \_ MDICREATE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="41b1a-122">An application should not send a second **WM\_MDICREATE** message while a **WM\_MDICREATE** message is still being processed.</span></span> <span data-ttu-id="41b1a-123">例如，在 MDI 子視窗處理其 **wm \_ MDICREATE** 訊息時，它不應該傳送 **wm \_ MDICREATE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="41b1a-123">For example, it should not send a **WM\_MDICREATE** message while an MDI child window is processing its **WM\_MDICREATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b1a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="41b1a-124">Requirements</span></span>



| <span data-ttu-id="41b1a-125">需求</span><span class="sxs-lookup"><span data-stu-id="41b1a-125">Requirement</span></span> | <span data-ttu-id="41b1a-126">值</span><span class="sxs-lookup"><span data-stu-id="41b1a-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b1a-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41b1a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="41b1a-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41b1a-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="41b1a-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41b1a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="41b1a-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41b1a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41b1a-131">標頭</span><span class="sxs-lookup"><span data-stu-id="41b1a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="41b1a-132"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="41b1a-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41b1a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41b1a-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="41b1a-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="41b1a-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="41b1a-135">**CreateMDIWindow**</span><span class="sxs-lookup"><span data-stu-id="41b1a-135">**CreateMDIWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[<span data-ttu-id="41b1a-136">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="41b1a-136">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="41b1a-137">**MDICREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="41b1a-137">**MDICREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[<span data-ttu-id="41b1a-138">**WM \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="41b1a-138">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

[<span data-ttu-id="41b1a-139">**WM \_ MDIDESTROY**</span><span class="sxs-lookup"><span data-stu-id="41b1a-139">**WM\_MDIDESTROY**</span></span>](wm-mdidestroy.md)
</dt> <dt>

<span data-ttu-id="41b1a-140">**概念**</span><span class="sxs-lookup"><span data-stu-id="41b1a-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="41b1a-141">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="41b1a-141">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
