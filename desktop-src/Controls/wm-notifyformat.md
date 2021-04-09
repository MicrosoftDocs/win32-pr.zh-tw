---
title: 'WM_NOTIFYFORMAT 訊息 (Winuser .h) '
description: 判斷視窗是否接受 WM 通知通知訊息中的 ANSI 或 Unicode 結構 \_ 。 \_從通用控制項將 WM NOTIFYFORMAT 訊息傳送至其父視窗，以及從父視窗傳送至通用控制項。
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- WM_NOTIFYFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934618"
---
# <a name="wm_notifyformat-message"></a><span data-ttu-id="718da-105">WM \_ NOTIFYFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="718da-105">WM\_NOTIFYFORMAT message</span></span>

<span data-ttu-id="718da-106">判斷視窗是否接受 [**WM \_ 通知**](wm-notify.md) 通知訊息中的 ANSI 或 Unicode 結構。</span><span class="sxs-lookup"><span data-stu-id="718da-106">Determines if a window accepts ANSI or Unicode structures in the [**WM\_NOTIFY**](wm-notify.md) notification message.</span></span> <span data-ttu-id="718da-107">**WM \_NOTIFYFORMAT** 訊息會從通用控制項傳送至其父視窗，以及從父視窗傳送至通用控制項。</span><span class="sxs-lookup"><span data-stu-id="718da-107">**WM\_NOTIFYFORMAT** messages are sent from a common control to its parent window and from the parent window to the common control.</span></span>

## <a name="parameters"></a><span data-ttu-id="718da-108">參數</span><span class="sxs-lookup"><span data-stu-id="718da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="718da-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="718da-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="718da-110">傳送 **WM \_ NOTIFYFORMAT** 訊息的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="718da-110">A handle to the window that is sending the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="718da-111">如果 *lParam* 為「nf-e \_ 查詢」，這個參數就是控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="718da-111">If *lParam* is NF\_QUERY, this parameter is the handle to a control.</span></span> <span data-ttu-id="718da-112">如果 *lParam* 為 nf-e \_ REQUERY，此參數就是控制項父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="718da-112">If *lParam* is NF\_REQUERY, this parameter is the handle to the parent window of a control.</span></span>

</dd> <dt>

<span data-ttu-id="718da-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="718da-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="718da-114">命令值，指定 **WM \_ NOTIFYFORMAT** 訊息的本質。</span><span class="sxs-lookup"><span data-stu-id="718da-114">The command value that specifies the nature of the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="718da-115">這會是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="718da-115">This will be one of the following values:</span></span>



| <span data-ttu-id="718da-116">值</span><span class="sxs-lookup"><span data-stu-id="718da-116">Value</span></span>                                                                                                                                                | <span data-ttu-id="718da-117">意義</span><span class="sxs-lookup"><span data-stu-id="718da-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <span data-ttu-id="718da-118"><dt>**NF-E \_ 查詢**</dt></span><span class="sxs-lookup"><span data-stu-id="718da-118"><dt>**NF\_QUERY**</dt></span></span> </dl>       | <span data-ttu-id="718da-119">此訊息是用來判斷是否應在 [**WM \_ 通知**](wm-notify.md) 訊息中使用 ANSI 或 Unicode 結構的查詢。</span><span class="sxs-lookup"><span data-stu-id="718da-119">The message is a query to determine whether ANSI or Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="718da-120">此命令會在建立控制項期間從控制項傳送至其父視窗，並回應 NF-E \_ REQUERY 命令。</span><span class="sxs-lookup"><span data-stu-id="718da-120">This command is sent from a control to its parent window during the creation of a control and in response to an NF\_REQUERY command.</span></span><br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <span data-ttu-id="718da-121"><dt>**NF-E \_ 查詢**</dt></span><span class="sxs-lookup"><span data-stu-id="718da-121"><dt>**NF\_REQUERY**</dt></span></span> </dl> | <span data-ttu-id="718da-122">此訊息是控制項的要求，可將 \_ 此訊息的「Nf-e 查詢」表單傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="718da-122">The message is a request for a control to send an NF\_QUERY form of this message to its parent window.</span></span> <span data-ttu-id="718da-123">此命令會從父視窗傳送。</span><span class="sxs-lookup"><span data-stu-id="718da-123">This command is sent from the parent window.</span></span> <span data-ttu-id="718da-124">父視窗會要求控制項對要在 [**WM \_ 通知**](wm-notify.md) 訊息中使用的結構類型進行重新查詢。</span><span class="sxs-lookup"><span data-stu-id="718da-124">The parent window is asking the control to requery it about the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="718da-125">如果 *lParam* 為 nf-e \_ 查詢，則傳回值是重新查詢作業的結果。</span><span class="sxs-lookup"><span data-stu-id="718da-125">If *lParam* is NF\_REQUERY, the return value is the result of the requery operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="718da-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="718da-126">Return value</span></span>

<span data-ttu-id="718da-127">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="718da-127">Returns one of the following values.</span></span>



| <span data-ttu-id="718da-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="718da-128">Return code</span></span>                                                                                 | <span data-ttu-id="718da-129">Description</span><span class="sxs-lookup"><span data-stu-id="718da-129">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="718da-130"><dt>**NFR \_ ANSI**</dt></span><span class="sxs-lookup"><span data-stu-id="718da-130"><dt>**NFR\_ANSI**</dt></span></span> </dl>    | <span data-ttu-id="718da-131">ANSI 結構應使用於控制項所傳送的 [**WM \_ 通知**](wm-notify.md) 訊息中。</span><span class="sxs-lookup"><span data-stu-id="718da-131">ANSI structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span><br/>     |
| <dl> <span data-ttu-id="718da-132"><dt>**NFR \_ UNICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="718da-132"><dt>**NFR\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="718da-133">Unicode 結構應使用於控制項所傳送的 [**WM \_ 通知**](wm-notify.md) 訊息中。</span><span class="sxs-lookup"><span data-stu-id="718da-133">Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span> <br/> |
| <dl> <span data-ttu-id="718da-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="718da-134"><dt>**0**</dt></span></span> </dl>            | <span data-ttu-id="718da-135">發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="718da-135">An error occurred.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="718da-136">備註</span><span class="sxs-lookup"><span data-stu-id="718da-136">Remarks</span></span>

<span data-ttu-id="718da-137">建立通用控制項時，控制項會將 **wm \_ NOTIFYFORMAT** 訊息傳送至其父視窗，以判斷要在 [**WM \_ 通知**](wm-notify.md) 訊息中使用的結構類型。</span><span class="sxs-lookup"><span data-stu-id="718da-137">When a common control is created, the control sends a **WM\_NOTIFYFORMAT** message to its parent window to determine the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="718da-138">如果父視窗未處理此訊息，則 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會根據父視窗的型別進行回應。</span><span class="sxs-lookup"><span data-stu-id="718da-138">If the parent window does not handle this message, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function responds according to the type of the parent window.</span></span> <span data-ttu-id="718da-139">也就是說，如果父視窗是 Unicode 視窗， **DefWindowProc** 會傳回 NFR \_ unicode，如果父視窗是 ANSI 視窗， **DefWindowProc** 會傳回 NFR \_ ANSI。</span><span class="sxs-lookup"><span data-stu-id="718da-139">That is, if the parent window is a Unicode window, **DefWindowProc** returns NFR\_UNICODE, and if the parent window is an ANSI window, **DefWindowProc** returns NFR\_ANSI.</span></span> <span data-ttu-id="718da-140">如果父視窗是對話方塊，而且不處理此訊息，則 [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) 函式會根據 (UNICODE 或 ANSI) 的對話方塊類型來做出類似的回應。</span><span class="sxs-lookup"><span data-stu-id="718da-140">If the parent window is a dialog box and does not handle this message, the [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) function similarly responds according to the type of the dialog box (Unicode or ANSI).</span></span>

<span data-ttu-id="718da-141">父視窗可以變更通用控制項在 [**WM \_ 通知**](wm-notify.md) 訊息中使用的結構類型，方法是將 *lParam* 設定為 Nf-e \_ REQUERY，然後將 **WM \_ NOTIFYFORMAT** 訊息傳送至控制項。</span><span class="sxs-lookup"><span data-stu-id="718da-141">A parent window can change the type of structures a common control uses in [**WM\_NOTIFY**](wm-notify.md) messages by setting *lParam* to NF\_REQUERY and sending a **WM\_NOTIFYFORMAT** message to the control.</span></span> <span data-ttu-id="718da-142">這會導致控制項將 \_ **WM \_ NOTIFYFORMAT** 訊息的 nf-e 查詢形式傳送至父視窗。</span><span class="sxs-lookup"><span data-stu-id="718da-142">This causes the control to send an NF\_QUERY form of the **WM\_NOTIFYFORMAT** message to the parent window.</span></span>

<span data-ttu-id="718da-143">所有的通用控制項都會傳送 **WM \_ NOTIFYFORMAT** 訊息。</span><span class="sxs-lookup"><span data-stu-id="718da-143">All common controls will send **WM\_NOTIFYFORMAT** messages.</span></span> <span data-ttu-id="718da-144">但是，標準的 Windows 控制項 (編輯控制項、下拉式方塊、清單方塊、按鈕、捲軸和靜態控制項) 不能。</span><span class="sxs-lookup"><span data-stu-id="718da-144">However, the standard Windows controls (edit controls, combo boxes, list boxes, buttons, scroll bars, and static controls) do not.</span></span>

## <a name="requirements"></a><span data-ttu-id="718da-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="718da-145">Requirements</span></span>



| <span data-ttu-id="718da-146">需求</span><span class="sxs-lookup"><span data-stu-id="718da-146">Requirement</span></span> | <span data-ttu-id="718da-147">值</span><span class="sxs-lookup"><span data-stu-id="718da-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="718da-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="718da-148">Minimum supported client</span></span><br/> | <span data-ttu-id="718da-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="718da-149">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="718da-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="718da-150">Minimum supported server</span></span><br/> | <span data-ttu-id="718da-151">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="718da-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="718da-152">標頭</span><span class="sxs-lookup"><span data-stu-id="718da-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="718da-153"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="718da-153"><dt>Winuser.h</dt></span></span> </dl> |



 

