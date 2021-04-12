---
title: 'LVM_SETWORKAREAS 訊息 (Commctrl .h) '
description: 設定清單視圖控制項內的工作區域。 您可以明確地傳送此訊息，或使用 ListView \_ SetWorkAreas 宏。
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- LVM_SETWORKAREAS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934887"
---
# <a name="lvm_setworkareas-message"></a><span data-ttu-id="0132f-105">LVM \_ SETWORKAREAS 訊息</span><span class="sxs-lookup"><span data-stu-id="0132f-105">LVM\_SETWORKAREAS message</span></span>

<span data-ttu-id="0132f-106">設定清單視圖控制項內的工作區域。</span><span class="sxs-lookup"><span data-stu-id="0132f-106">Sets the working areas within a list-view control.</span></span> <span data-ttu-id="0132f-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) 宏。</span><span class="sxs-lookup"><span data-stu-id="0132f-107">You can send this message explicitly or use the [**ListView\_SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0132f-108">參數</span><span class="sxs-lookup"><span data-stu-id="0132f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0132f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0132f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0132f-110">陣列中 *lprc* 的結構數目。</span><span class="sxs-lookup"><span data-stu-id="0132f-110">The number of structures in the array at *lprc*.</span></span> <span data-ttu-id="0132f-111">允許的工作區域數目上限是由 LV \_ MAX \_ WORKAREAS 值定義。</span><span class="sxs-lookup"><span data-stu-id="0132f-111">The maximum number of working areas allowed is defined by the LV\_MAX\_WORKAREAS value.</span></span>

</dd> <dt>

<span data-ttu-id="0132f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0132f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0132f-113">[**矩形**](/previous-versions//dd162897(v=vs.85))結構陣列的指標，其中包含清單視圖控制項的新工作區域。</span><span class="sxs-lookup"><span data-stu-id="0132f-113">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that contain the new working areas of the list-view control.</span></span> <span data-ttu-id="0132f-114">這些結構中的值是在用戶端座標中。</span><span class="sxs-lookup"><span data-stu-id="0132f-114">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="0132f-115">如果這個參數為 **Null**，工作區將會設定為控制項的工作區。</span><span class="sxs-lookup"><span data-stu-id="0132f-115">If this parameter is **NULL**, the working area will be set to the client area of the control.</span></span> <span data-ttu-id="0132f-116">*wParam* 指定此陣列中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="0132f-116">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0132f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0132f-117">Return value</span></span>

<span data-ttu-id="0132f-118">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="0132f-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0132f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="0132f-119">Requirements</span></span>



| <span data-ttu-id="0132f-120">需求</span><span class="sxs-lookup"><span data-stu-id="0132f-120">Requirement</span></span> | <span data-ttu-id="0132f-121">值</span><span class="sxs-lookup"><span data-stu-id="0132f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0132f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0132f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0132f-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0132f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0132f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0132f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0132f-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0132f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0132f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="0132f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0132f-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0132f-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0132f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0132f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0132f-129">使用 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="0132f-129">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

