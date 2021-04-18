---
title: 'PGM_SETBUTTONSIZE 訊息 (Commctrl .h) '
description: 設定呼機控制項目前的按鈕大小。 您可以明確地傳送此訊息，或使用呼叫器 \_ SetButtonSize 宏。
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- PGM_SETBUTTONSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508487"
---
# <a name="pgm_setbuttonsize-message"></a><span data-ttu-id="a50de-105">PGM \_ SETBUTTONSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="a50de-105">PGM\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="a50de-106">設定呼機控制項目前的按鈕大小。</span><span class="sxs-lookup"><span data-stu-id="a50de-106">Sets the current button size for the pager control.</span></span> <span data-ttu-id="a50de-107">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) 宏。</span><span class="sxs-lookup"><span data-stu-id="a50de-107">You can send this message explicitly or use the [**Pager\_SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a50de-108">參數</span><span class="sxs-lookup"><span data-stu-id="a50de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a50de-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a50de-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a50de-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a50de-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a50de-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a50de-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a50de-112">**Int** 類型的值，其中包含新的按鈕大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a50de-112">Value of type **int** that contains the new button size, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a50de-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a50de-113">Return value</span></span>

<span data-ttu-id="a50de-114">傳回包含上一個按鈕大小的 **int** 值（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a50de-114">Returns an **int** value that contains the previous button size, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="a50de-115">備註</span><span class="sxs-lookup"><span data-stu-id="a50de-115">Remarks</span></span>

<span data-ttu-id="a50de-116">如果呼機控制項有 [**pg \_ HORZ**](pager-control-styles.md) 樣式，則按鈕大小會決定頁面導覽按鈕的寬度。</span><span class="sxs-lookup"><span data-stu-id="a50de-116">If the pager control has the [**PGS\_HORZ**](pager-control-styles.md) style, the button size determines the width of the pager buttons.</span></span> <span data-ttu-id="a50de-117">如果呼機控制項具有 [**pg \_ 垂直**](pager-control-styles.md) 樣式，則按鈕大小會決定頁面導覽按鈕的高度。</span><span class="sxs-lookup"><span data-stu-id="a50de-117">If the pager control has the [**PGS\_VERT**](pager-control-styles.md) style, the button size determines the height of the pager buttons.</span></span> <span data-ttu-id="a50de-118">根據預設，呼機控制項會將其按鈕大小設定為捲軸寬度的三 fourths。</span><span class="sxs-lookup"><span data-stu-id="a50de-118">By default, the pager control sets its button size to three-fourths of the width of the scroll bar.</span></span>

<span data-ttu-id="a50de-119">頁面的最小大小為目前的12圖元。</span><span class="sxs-lookup"><span data-stu-id="a50de-119">There is a minimum size to the pager button, currently 12 pixels.</span></span> <span data-ttu-id="a50de-120">不過，這可能會變更，因此您不應該依賴此值。</span><span class="sxs-lookup"><span data-stu-id="a50de-120">However, this can change so you should not depend on this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a50de-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a50de-121">Requirements</span></span>



| <span data-ttu-id="a50de-122">需求</span><span class="sxs-lookup"><span data-stu-id="a50de-122">Requirement</span></span> | <span data-ttu-id="a50de-123">值</span><span class="sxs-lookup"><span data-stu-id="a50de-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a50de-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a50de-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a50de-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a50de-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a50de-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a50de-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a50de-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a50de-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a50de-128">標頭</span><span class="sxs-lookup"><span data-stu-id="a50de-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a50de-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a50de-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a50de-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a50de-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a50de-131">**PGM \_ GETBUTTONSIZE**</span><span class="sxs-lookup"><span data-stu-id="a50de-131">**PGM\_GETBUTTONSIZE**</span></span>](pgm-getbuttonsize.md)
</dt> </dl>

 

 





