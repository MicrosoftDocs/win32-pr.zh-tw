---
title: 'TVM_GETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 抓取樹狀檢視控制項的延伸樣式。 明確地傳送此訊息，或使用 TreeView \_ GetExtendedStyle 宏。
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- TVM_GETEXTENDEDSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844252"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a><span data-ttu-id="8fa30-105">TVM_GETEXTENDEDSTYLE 訊息 (Commctrl .h) </span><span class="sxs-lookup"><span data-stu-id="8fa30-105">TVM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="8fa30-106">抓取樹狀檢視控制項的延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="8fa30-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="8fa30-107">明確地傳送此訊息，或使用 [**TreeView \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) 宏。</span><span class="sxs-lookup"><span data-stu-id="8fa30-107">Send this message explicitly or by using the [**TreeView\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fa30-108">參數</span><span class="sxs-lookup"><span data-stu-id="8fa30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fa30-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8fa30-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8fa30-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8fa30-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8fa30-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8fa30-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8fa30-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8fa30-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fa30-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fa30-113">Return value</span></span>

<span data-ttu-id="8fa30-114">傳回擴充樣式的值。如需樣式的詳細資訊，請參閱 [樹狀檢視控制項擴充樣式](tree-view-control-window-extended-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="8fa30-114">Returns the value of extended style.For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8fa30-115">備註</span><span class="sxs-lookup"><span data-stu-id="8fa30-115">Remarks</span></span>

<span data-ttu-id="8fa30-116">樹狀檢視控制項的擴充樣式與函數 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 或函數 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)所使用的擴充樣式沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="8fa30-116">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fa30-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fa30-117">Requirements</span></span>



| <span data-ttu-id="8fa30-118">需求</span><span class="sxs-lookup"><span data-stu-id="8fa30-118">Requirement</span></span> | <span data-ttu-id="8fa30-119">值</span><span class="sxs-lookup"><span data-stu-id="8fa30-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fa30-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fa30-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8fa30-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fa30-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8fa30-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fa30-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8fa30-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fa30-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8fa30-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8fa30-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fa30-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8fa30-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

