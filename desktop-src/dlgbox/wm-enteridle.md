---
title: 'WM_ENTERIDLE 訊息 (Winuser .h) '
description: 傳送至進入閒置狀態之強制回應對話方塊或功能表的擁有者視窗。 強制回應對話方塊或功能表在處理一或多個先前的訊息之後，就會進入閒置狀態，當佇列中沒有任何訊息在佇列中等候時。
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- WM_ENTERIDLE 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385037"
---
# <a name="wm_enteridle-message"></a><span data-ttu-id="22bf4-105">WM \_ ENTERIDLE 訊息</span><span class="sxs-lookup"><span data-stu-id="22bf4-105">WM\_ENTERIDLE message</span></span>

<span data-ttu-id="22bf4-106">傳送至進入閒置狀態之強制回應對話方塊或功能表的擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="22bf4-106">Sent to the owner window of a modal dialog box or menu that is entering an idle state.</span></span> <span data-ttu-id="22bf4-107">強制回應對話方塊或功能表在處理一或多個先前的訊息之後，就會進入閒置狀態，當佇列中沒有任何訊息在佇列中等候時。</span><span class="sxs-lookup"><span data-stu-id="22bf4-107">A modal dialog box or menu enters an idle state when no messages are waiting in its queue after it has processed one or more previous messages.</span></span>


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a><span data-ttu-id="22bf4-108">參數</span><span class="sxs-lookup"><span data-stu-id="22bf4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22bf4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22bf4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22bf4-110">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="22bf4-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="22bf4-111">值</span><span class="sxs-lookup"><span data-stu-id="22bf4-111">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="22bf4-112">意義</span><span class="sxs-lookup"><span data-stu-id="22bf4-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <span data-ttu-id="22bf4-113"><dt>**MSGF \_對話方塊**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="22bf4-113"><dt>**MSGF\_DIALOGBOX**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="22bf4-114">系統閒置，因為顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="22bf4-114">The system is idle because a dialog box is displayed.</span></span><br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <span data-ttu-id="22bf4-115"><dt>**MSGF \_功能表**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="22bf4-115"><dt>**MSGF\_MENU**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="22bf4-116">系統閒置，因為顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="22bf4-116">The system is idle because a menu is displayed.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="22bf4-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22bf4-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22bf4-118">對話方塊的控制碼 (如果 *wParam* 是 **MSGF \_ 對話方塊**) 或包含所顯示功能表的視窗 (如果 *wParam* 是 **MSGF \_ 功能表**) 。</span><span class="sxs-lookup"><span data-stu-id="22bf4-118">A handle to the dialog box (if *wParam* is **MSGF\_DIALOGBOX**) or window containing the displayed menu (if *wParam* is **MSGF\_MENU**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22bf4-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="22bf4-119">Return value</span></span>

<span data-ttu-id="22bf4-120">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="22bf4-120">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="22bf4-121">備註</span><span class="sxs-lookup"><span data-stu-id="22bf4-121">Remarks</span></span>

<span data-ttu-id="22bf4-122">您可以藉由建立具有 **DS \_ NOIDLEMSG** 樣式的對話方塊來隱藏對話方塊的 **WM \_ ENTERIDLE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="22bf4-122">You can suppress the **WM\_ENTERIDLE** message for a dialog box by creating the dialog box with the **DS\_NOIDLEMSG** style.</span></span>

## <a name="requirements"></a><span data-ttu-id="22bf4-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="22bf4-123">Requirements</span></span>



| <span data-ttu-id="22bf4-124">需求</span><span class="sxs-lookup"><span data-stu-id="22bf4-124">Requirement</span></span> | <span data-ttu-id="22bf4-125">值</span><span class="sxs-lookup"><span data-stu-id="22bf4-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22bf4-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22bf4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="22bf4-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22bf4-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="22bf4-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22bf4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="22bf4-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22bf4-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="22bf4-130">標頭</span><span class="sxs-lookup"><span data-stu-id="22bf4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="22bf4-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="22bf4-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22bf4-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22bf4-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="22bf4-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="22bf4-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="22bf4-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="22bf4-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="22bf4-135">**概念**</span><span class="sxs-lookup"><span data-stu-id="22bf4-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="22bf4-136">對話方塊</span><span class="sxs-lookup"><span data-stu-id="22bf4-136">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

