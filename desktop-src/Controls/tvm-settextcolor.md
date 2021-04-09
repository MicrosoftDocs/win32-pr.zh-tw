---
title: 'TVM_SETTEXTCOLOR 訊息 (Commctrl .h) '
description: 設定控制項的文字色彩。 您可以使用 TreeView SetTextColor 宏明確地傳送此訊息 \_ 。
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- TVM_SETTEXTCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686032"
---
# <a name="tvm_settextcolor-message"></a><span data-ttu-id="0d9ec-105">TVM \_ SETTEXTCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="0d9ec-105">TVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="0d9ec-106">設定控制項的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="0d9ec-106">Sets the text color of the control.</span></span> <span data-ttu-id="0d9ec-107">您可以使用 [**TreeView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="0d9ec-107">You can send this message explicitly or by using the [**TreeView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d9ec-108">參數</span><span class="sxs-lookup"><span data-stu-id="0d9ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d9ec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d9ec-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0d9ec-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0d9ec-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0d9ec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d9ec-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d9ec-112">[**COLORREF**](/windows/desktop/gdi/colorref) 值，其中包含新的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="0d9ec-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new text color.</span></span> <span data-ttu-id="0d9ec-113">如果這個引數是-1，則控制項會還原為使用文字色彩的系統色彩。</span><span class="sxs-lookup"><span data-stu-id="0d9ec-113">If this argument is -1, the control will revert to using the system color for the text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d9ec-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d9ec-114">Return value</span></span>

<span data-ttu-id="0d9ec-115">傳回表示先前文字色彩的 **COLORREF** 值。</span><span class="sxs-lookup"><span data-stu-id="0d9ec-115">Returns a **COLORREF** value that represents the previous text color.</span></span> <span data-ttu-id="0d9ec-116">如果這個值是-1，表示控制項使用的是文字色彩的系統色彩。</span><span class="sxs-lookup"><span data-stu-id="0d9ec-116">If this value is -1, the control was using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d9ec-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d9ec-117">Requirements</span></span>



| <span data-ttu-id="0d9ec-118">需求</span><span class="sxs-lookup"><span data-stu-id="0d9ec-118">Requirement</span></span> | <span data-ttu-id="0d9ec-119">值</span><span class="sxs-lookup"><span data-stu-id="0d9ec-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9ec-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d9ec-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d9ec-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d9ec-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d9ec-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d9ec-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d9ec-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d9ec-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d9ec-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0d9ec-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d9ec-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d9ec-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d9ec-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d9ec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d9ec-127">**TVM \_ GETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="0d9ec-127">**TVM\_GETTEXTCOLOR**</span></span>](tvm-gettextcolor.md)
</dt> </dl>

 

