---
title: 'BM_CLICK 訊息 (Winuser .h) '
description: 模擬使用者按一下按鈕。 這則訊息會讓按鈕收到 WM \_ LBUTTONDOWN 和 WM \_ LBUTTONUP 訊息，以及按鈕的父視窗，以接收 BN 按一下的 \_ 通知碼。
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- BM_CLICK message Windows 控制項
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024802"
---
# <a name="bm_click-message"></a><span data-ttu-id="a5260-105">BM \_ 按一下訊息</span><span class="sxs-lookup"><span data-stu-id="a5260-105">BM\_CLICK message</span></span>

<span data-ttu-id="a5260-106">模擬使用者按一下按鈕。</span><span class="sxs-lookup"><span data-stu-id="a5260-106">Simulates the user clicking a button.</span></span> <span data-ttu-id="a5260-107">這則訊息會讓按鈕收到 [**wm \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 和 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) 訊息，以及按鈕的父視窗，以接收 [BN \_ 按一下](bn-clicked.md) 的通知碼。</span><span class="sxs-lookup"><span data-stu-id="a5260-107">This message causes the button to receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) and [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages, and the button's parent window to receive a [BN\_CLICKED](bn-clicked.md) notification code.</span></span>

## <a name="parameters"></a><span data-ttu-id="a5260-108">參數</span><span class="sxs-lookup"><span data-stu-id="a5260-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5260-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a5260-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5260-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="a5260-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a5260-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5260-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5260-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="a5260-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5260-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5260-113">Return value</span></span>

<span data-ttu-id="a5260-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a5260-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5260-115">備註</span><span class="sxs-lookup"><span data-stu-id="a5260-115">Remarks</span></span>

<span data-ttu-id="a5260-116">如果按鈕在對話方塊中，而對話方塊不在使用中，則 **BM \_ 按一下** 訊息可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="a5260-116">If the button is in a dialog box and the dialog box is not active, the **BM\_CLICK** message might fail.</span></span> <span data-ttu-id="a5260-117">為了確保在這種情況下成功，請先呼叫 [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) 函式來啟動對話方塊，然後再傳送 **BM \_ 按一下** [訊息] 至按鈕。</span><span class="sxs-lookup"><span data-stu-id="a5260-117">To ensure success in this situation, call the [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) function to activate the dialog box before sending the **BM\_CLICK** message to the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5260-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5260-118">Requirements</span></span>



| <span data-ttu-id="a5260-119">需求</span><span class="sxs-lookup"><span data-stu-id="a5260-119">Requirement</span></span> | <span data-ttu-id="a5260-120">值</span><span class="sxs-lookup"><span data-stu-id="a5260-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5260-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5260-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5260-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5260-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a5260-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5260-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5260-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5260-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a5260-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a5260-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5260-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a5260-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

