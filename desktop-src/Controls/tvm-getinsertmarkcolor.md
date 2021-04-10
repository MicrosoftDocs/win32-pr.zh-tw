---
title: 'TVM_GETINSERTMARKCOLOR 訊息 (Commctrl .h) '
description: 抓取用來繪製樹狀檢視之插入標記的色彩。 您可以使用 TreeView GetInsertMarkColor 宏明確地傳送此訊息 \_ 。
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- TVM_GETINSERTMARKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935003"
---
# <a name="tvm_getinsertmarkcolor-message"></a><span data-ttu-id="6e957-105">TVM \_ GETINSERTMARKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="6e957-105">TVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="6e957-106">抓取用來繪製樹狀檢視之插入標記的色彩。</span><span class="sxs-lookup"><span data-stu-id="6e957-106">Retrieves the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="6e957-107">您可以使用 [**TreeView \_ GetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="6e957-107">You can send this message explicitly or by using the [**TreeView\_GetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e957-108">參數</span><span class="sxs-lookup"><span data-stu-id="6e957-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e957-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e957-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6e957-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6e957-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6e957-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e957-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6e957-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6e957-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e957-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e957-113">Return value</span></span>

<span data-ttu-id="6e957-114">傳回包含目前插入標記色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。</span><span class="sxs-lookup"><span data-stu-id="6e957-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that contains the current insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e957-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e957-115">Requirements</span></span>



| <span data-ttu-id="6e957-116">需求</span><span class="sxs-lookup"><span data-stu-id="6e957-116">Requirement</span></span> | <span data-ttu-id="6e957-117">值</span><span class="sxs-lookup"><span data-stu-id="6e957-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e957-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e957-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6e957-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e957-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e957-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e957-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6e957-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e957-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e957-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6e957-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e957-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e957-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e957-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e957-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e957-125">**TVM \_ SETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="6e957-125">**TVM\_SETINSERTMARKCOLOR**</span></span>](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

