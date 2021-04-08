---
title: 'WM_DRAWITEM 訊息 (Winuser .h) '
description: 當按鈕、下拉式方塊、清單方塊或功能表的視覺外觀已變更時，傳送至主控描繪按鈕、下拉式方塊、清單方塊或功能表的父視窗。
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- WM_DRAWITEM message Windows 控制項
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685873"
---
# <a name="wm_drawitem-message"></a><span data-ttu-id="c0519-104">WM \_ DRAWITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="c0519-104">WM\_DRAWITEM message</span></span>

<span data-ttu-id="c0519-105">當按鈕、下拉式方塊、清單方塊或功能表的視覺外觀已變更時，傳送至主控描繪按鈕、下拉式方塊、清單方塊或功能表的父視窗。</span><span class="sxs-lookup"><span data-stu-id="c0519-105">Sent to the parent window of an owner-drawn button, combo box, list box, or menu when a visual aspect of the button, combo box, list box, or menu has changed.</span></span>

<span data-ttu-id="c0519-106">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="c0519-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c0519-107">參數</span><span class="sxs-lookup"><span data-stu-id="c0519-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0519-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0519-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0519-109">指定傳送 **WM \_ DRAWITEM** 訊息之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0519-109">Specifies the identifier of the control that sent the **WM\_DRAWITEM** message.</span></span> <span data-ttu-id="c0519-110">如果訊息是由功能表傳送，此參數為零。</span><span class="sxs-lookup"><span data-stu-id="c0519-110">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="c0519-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0519-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0519-112">[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的指標，其中包含要繪製之專案的相關資訊，以及所需的繪圖類型。</span><span class="sxs-lookup"><span data-stu-id="c0519-112">Pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0519-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0519-113">Return value</span></span>

<span data-ttu-id="c0519-114">如果應用程式處理此訊息，則應該傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c0519-114">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0519-115">備註</span><span class="sxs-lookup"><span data-stu-id="c0519-115">Remarks</span></span>

<span data-ttu-id="c0519-116">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會繪製主控描繪清單方塊專案的焦點矩形。</span><span class="sxs-lookup"><span data-stu-id="c0519-116">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the focus rectangle for an owner-drawn list box item.</span></span>

<span data-ttu-id="c0519-117">[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 *itemAction* 成員會指定應用程式應該執行的繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="c0519-117">The *itemAction* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="c0519-118">從處理此訊息傳回之前，應用程式應該確定 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 *hDC* 成員所識別的裝置內容為預設狀態。</span><span class="sxs-lookup"><span data-stu-id="c0519-118">Before returning from processing this message, an application should ensure that the device context identified by the *hDC* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0519-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0519-119">Requirements</span></span>



| <span data-ttu-id="c0519-120">需求</span><span class="sxs-lookup"><span data-stu-id="c0519-120">Requirement</span></span> | <span data-ttu-id="c0519-121">值</span><span class="sxs-lookup"><span data-stu-id="c0519-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0519-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0519-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c0519-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0519-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c0519-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0519-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c0519-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0519-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c0519-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c0519-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0519-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c0519-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0519-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0519-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c0519-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="c0519-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c0519-130">**DRAWITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c0519-130">**DRAWITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

<span data-ttu-id="c0519-131">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="c0519-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c0519-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c0519-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

