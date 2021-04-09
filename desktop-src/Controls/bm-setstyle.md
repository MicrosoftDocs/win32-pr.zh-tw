---
title: 'BM_SETSTYLE 訊息 (Winuser .h) '
description: 設定按鈕的樣式。 您可以明確地傳送此訊息，或使用按鈕 \_ >setstyle 宏。
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- BM_SETSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934099"
---
# <a name="bm_setstyle-message"></a><span data-ttu-id="55e0a-105">BM \_ >setstyle 訊息</span><span class="sxs-lookup"><span data-stu-id="55e0a-105">BM\_SETSTYLE message</span></span>

<span data-ttu-id="55e0a-106">設定按鈕的樣式。</span><span class="sxs-lookup"><span data-stu-id="55e0a-106">Sets the style of a button.</span></span> <span data-ttu-id="55e0a-107">您可以明確地傳送此訊息，或使用 [**按鈕 \_ >setstyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) 宏。</span><span class="sxs-lookup"><span data-stu-id="55e0a-107">You can send this message explicitly or use the [**Button\_SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="55e0a-108">參數</span><span class="sxs-lookup"><span data-stu-id="55e0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55e0a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55e0a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55e0a-110">按鈕樣式。</span><span class="sxs-lookup"><span data-stu-id="55e0a-110">The button style.</span></span> <span data-ttu-id="55e0a-111">這個參數可以是按鈕樣式的組合。</span><span class="sxs-lookup"><span data-stu-id="55e0a-111">This parameter can be a combination of button styles.</span></span> <span data-ttu-id="55e0a-112">如需按鈕樣式的表格，請參閱 [按鈕樣式](button-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="55e0a-112">For a table of button styles, see [Button Styles](button-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="55e0a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55e0a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55e0a-114">*LParam* 的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是一個 **布林** 值，指定是否要重繪按鈕。</span><span class="sxs-lookup"><span data-stu-id="55e0a-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* is a **BOOL** that specifies whether the button is to be redrawn.</span></span> <span data-ttu-id="55e0a-115">**TRUE** 值會重繪按鈕;值為 **FALSE** 時，不會重繪按鈕。</span><span class="sxs-lookup"><span data-stu-id="55e0a-115">A value of **TRUE** redraws the button; a value of **FALSE** does not redraw the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55e0a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="55e0a-116">Return value</span></span>

<span data-ttu-id="55e0a-117">此訊息一律會傳回零。</span><span class="sxs-lookup"><span data-stu-id="55e0a-117">This message always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="55e0a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="55e0a-118">Requirements</span></span>



| <span data-ttu-id="55e0a-119">需求</span><span class="sxs-lookup"><span data-stu-id="55e0a-119">Requirement</span></span> | <span data-ttu-id="55e0a-120">值</span><span class="sxs-lookup"><span data-stu-id="55e0a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55e0a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55e0a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="55e0a-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55e0a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="55e0a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55e0a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="55e0a-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55e0a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="55e0a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="55e0a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="55e0a-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="55e0a-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

