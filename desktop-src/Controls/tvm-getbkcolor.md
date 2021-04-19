---
title: 'TVM_GETBKCOLOR 訊息 (Commctrl .h) '
description: 抓取控制項目前的背景色彩。 您可以使用 TreeView GetBkColor 宏明確地傳送此訊息 \_ 。
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- TVM_GETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966140"
---
# <a name="tvm_getbkcolor-message"></a><span data-ttu-id="332d1-105">TVM \_ GETBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="332d1-105">TVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="332d1-106">抓取控制項目前的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="332d1-106">Retrieves the current background color of the control.</span></span> <span data-ttu-id="332d1-107">您可以使用 [**TreeView \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="332d1-107">You can send this message explicitly or by using the [**TreeView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="332d1-108">參數</span><span class="sxs-lookup"><span data-stu-id="332d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="332d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="332d1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="332d1-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="332d1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="332d1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="332d1-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="332d1-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="332d1-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="332d1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="332d1-113">Return value</span></span>

<span data-ttu-id="332d1-114">傳回代表目前背景色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。</span><span class="sxs-lookup"><span data-stu-id="332d1-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current background color.</span></span> <span data-ttu-id="332d1-115">如果這個值是-1，表示控制項使用背景色彩的系統色彩。</span><span class="sxs-lookup"><span data-stu-id="332d1-115">If this value is -1, the control is using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="332d1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="332d1-116">Requirements</span></span>



| <span data-ttu-id="332d1-117">需求</span><span class="sxs-lookup"><span data-stu-id="332d1-117">Requirement</span></span> | <span data-ttu-id="332d1-118">值</span><span class="sxs-lookup"><span data-stu-id="332d1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="332d1-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="332d1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="332d1-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="332d1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="332d1-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="332d1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="332d1-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="332d1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="332d1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="332d1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="332d1-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="332d1-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="332d1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="332d1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332d1-126">**TVM \_ SETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="332d1-126">**TVM\_SETBKCOLOR**</span></span>](tvm-setbkcolor.md)
</dt> </dl>

 

