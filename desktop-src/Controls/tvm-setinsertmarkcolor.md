---
title: 'TVM_SETINSERTMARKCOLOR 訊息 (Commctrl .h) '
description: 設定用來繪製樹狀檢視之插入標記的色彩。 您可以使用 TreeView SetInsertMarkColor 宏明確地傳送此訊息 \_ 。
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- TVM_SETINSERTMARKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104177"
---
# <a name="tvm_setinsertmarkcolor-message"></a><span data-ttu-id="fffde-105">TVM \_ SETINSERTMARKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="fffde-105">TVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="fffde-106">設定用來繪製樹狀檢視之插入標記的色彩。</span><span class="sxs-lookup"><span data-stu-id="fffde-106">Sets the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="fffde-107">您可以使用 [**TreeView \_ SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="fffde-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fffde-108">參數</span><span class="sxs-lookup"><span data-stu-id="fffde-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fffde-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fffde-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fffde-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="fffde-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fffde-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fffde-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fffde-112">[**COLORREF**](/windows/desktop/gdi/colorref) 值，其中包含新的插入標記色彩。</span><span class="sxs-lookup"><span data-stu-id="fffde-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fffde-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fffde-113">Return value</span></span>

<span data-ttu-id="fffde-114">傳回包含先前插入標記色彩的 **COLORREF** 值。</span><span class="sxs-lookup"><span data-stu-id="fffde-114">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="fffde-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fffde-115">Requirements</span></span>



| <span data-ttu-id="fffde-116">需求</span><span class="sxs-lookup"><span data-stu-id="fffde-116">Requirement</span></span> | <span data-ttu-id="fffde-117">值</span><span class="sxs-lookup"><span data-stu-id="fffde-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fffde-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fffde-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fffde-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fffde-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fffde-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fffde-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fffde-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fffde-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fffde-122">標頭</span><span class="sxs-lookup"><span data-stu-id="fffde-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fffde-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fffde-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fffde-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fffde-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fffde-125">**TVM \_ GETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="fffde-125">**TVM\_GETINSERTMARKCOLOR**</span></span>](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

