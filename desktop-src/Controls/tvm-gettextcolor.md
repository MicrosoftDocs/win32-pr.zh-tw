---
title: 'TVM_GETTEXTCOLOR 訊息 (Commctrl .h) '
description: 抓取控制項目前的文字色彩。 您可以使用 TreeView GetTextColor 宏明確地傳送此訊息 \_ 。
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- TVM_GETTEXTCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024839"
---
# <a name="tvm_gettextcolor-message"></a><span data-ttu-id="3a557-105">TVM \_ GETTEXTCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="3a557-105">TVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="3a557-106">抓取控制項目前的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="3a557-106">Retrieves the current text color of the control.</span></span> <span data-ttu-id="3a557-107">您可以使用 [**TreeView \_ GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3a557-107">You can send this message explicitly or by using the [**TreeView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a557-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a557-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a557-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a557-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3a557-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3a557-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3a557-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a557-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3a557-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3a557-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a557-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a557-113">Return value</span></span>

<span data-ttu-id="3a557-114">傳回代表目前文字色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。</span><span class="sxs-lookup"><span data-stu-id="3a557-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current text color.</span></span> <span data-ttu-id="3a557-115">如果這個值是-1，表示控制項使用的是文字色彩的系統色彩。</span><span class="sxs-lookup"><span data-stu-id="3a557-115">If this value is -1, the control is using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a557-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a557-116">Requirements</span></span>



| <span data-ttu-id="3a557-117">需求</span><span class="sxs-lookup"><span data-stu-id="3a557-117">Requirement</span></span> | <span data-ttu-id="3a557-118">值</span><span class="sxs-lookup"><span data-stu-id="3a557-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a557-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a557-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3a557-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a557-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a557-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a557-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3a557-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a557-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a557-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3a557-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a557-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a557-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a557-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a557-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a557-126">**TVM \_ SETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="3a557-126">**TVM\_SETTEXTCOLOR**</span></span>](tvm-settextcolor.md)
</dt> </dl>

 

