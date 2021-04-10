---
title: 'LVM_SETITEMSTATE 訊息 (Commctrl .h) '
description: 變更清單視圖控制項中專案的狀態。 您可以明確地傳送此訊息，或使用 ListView \_ SetItemState 宏來傳送。
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- LVM_SETITEMSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2120d6d1d2cd3044368ebb343cdf0fe240d805c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103925"
---
# <a name="lvm_setitemstate-message"></a><span data-ttu-id="f6f78-105">LVM \_ SETITEMSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="f6f78-105">LVM\_SETITEMSTATE message</span></span>

<span data-ttu-id="f6f78-106">變更清單視圖控制項中專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="f6f78-106">Changes the state of an item in a list-view control.</span></span> <span data-ttu-id="f6f78-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="f6f78-107">You can send this message explicitly or by using the [**ListView\_SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6f78-108">參數</span><span class="sxs-lookup"><span data-stu-id="f6f78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6f78-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6f78-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f78-110">清單視圖專案的索引。</span><span class="sxs-lookup"><span data-stu-id="f6f78-110">Index of the list-view item.</span></span> <span data-ttu-id="f6f78-111">如果此參數為-1，則狀態變更會套用至所有專案。</span><span class="sxs-lookup"><span data-stu-id="f6f78-111">If this parameter is -1, then the state change is applied to all items.</span></span>

</dd> <dt>

<span data-ttu-id="f6f78-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6f78-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f78-113">[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f6f78-113">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="f6f78-114">**StateMask** 成員會指定要變更的狀態位，而且 **狀態** 成員會包含這些位的新值。</span><span class="sxs-lookup"><span data-stu-id="f6f78-114">The **stateMask** member specifies which state bits to change, and the **state** member contains the new values for those bits.</span></span> <span data-ttu-id="f6f78-115">其他成員則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f6f78-115">The other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6f78-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6f78-116">Return value</span></span>

<span data-ttu-id="f6f78-117">如果您明確傳送此訊息，則會在成功時傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f6f78-117">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6f78-118">備註</span><span class="sxs-lookup"><span data-stu-id="f6f78-118">Remarks</span></span>

<span data-ttu-id="f6f78-119">專案的狀態值包含一組位旗標，指出專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="f6f78-119">An item's state value includes a set of bit flags that indicate the item's state.</span></span> <span data-ttu-id="f6f78-120">狀態值也可以包含表示專案狀態影像和重迭影像的影像清單索引。</span><span class="sxs-lookup"><span data-stu-id="f6f78-120">The state value can also include image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f78-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6f78-121">Requirements</span></span>



| <span data-ttu-id="f6f78-122">需求</span><span class="sxs-lookup"><span data-stu-id="f6f78-122">Requirement</span></span> | <span data-ttu-id="f6f78-123">值</span><span class="sxs-lookup"><span data-stu-id="f6f78-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f78-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6f78-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f6f78-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6f78-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6f78-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6f78-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f6f78-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6f78-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6f78-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f6f78-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6f78-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f78-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





