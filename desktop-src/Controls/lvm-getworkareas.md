---
title: 'LVM_GETWORKAREAS 訊息 (Commctrl .h) '
description: 從清單視圖控制項抓取工作區域。 您可以明確地傳送此訊息，或使用 ListView \_ GetWorkAreas 宏。
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- LVM_GETWORKAREAS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466500"
---
# <a name="lvm_getworkareas-message"></a><span data-ttu-id="e23df-105">LVM \_ GETWORKAREAS 訊息</span><span class="sxs-lookup"><span data-stu-id="e23df-105">LVM\_GETWORKAREAS message</span></span>

<span data-ttu-id="e23df-106">從清單視圖控制項抓取工作區域。</span><span class="sxs-lookup"><span data-stu-id="e23df-106">Retrieves the working areas from a list-view control.</span></span> <span data-ttu-id="e23df-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) 宏。</span><span class="sxs-lookup"><span data-stu-id="e23df-107">You can send this message explicitly or use the [**ListView\_GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e23df-108">參數</span><span class="sxs-lookup"><span data-stu-id="e23df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e23df-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e23df-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e23df-110">陣列中 *lParam* 的 [**RECT**](/previous-versions//dd162897(v=vs.85))結構數目。</span><span class="sxs-lookup"><span data-stu-id="e23df-110">The number of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures in the array at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="e23df-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e23df-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e23df-112">[**矩形**](/previous-versions//dd162897(v=vs.85))陣列的指標，此陣列會接收清單視圖控制項目前的工作區域。</span><span class="sxs-lookup"><span data-stu-id="e23df-112">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that receive the current working areas of the list-view control.</span></span> <span data-ttu-id="e23df-113">這些結構中的值是在用戶端座標中。</span><span class="sxs-lookup"><span data-stu-id="e23df-113">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="e23df-114">*wParam* 指定此陣列中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="e23df-114">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e23df-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="e23df-115">Return value</span></span>

<span data-ttu-id="e23df-116">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="e23df-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e23df-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e23df-117">Requirements</span></span>



| <span data-ttu-id="e23df-118">需求</span><span class="sxs-lookup"><span data-stu-id="e23df-118">Requirement</span></span> | <span data-ttu-id="e23df-119">值</span><span class="sxs-lookup"><span data-stu-id="e23df-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e23df-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e23df-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e23df-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e23df-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e23df-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e23df-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e23df-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e23df-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e23df-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e23df-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e23df-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e23df-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e23df-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e23df-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e23df-127">使用 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="e23df-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

