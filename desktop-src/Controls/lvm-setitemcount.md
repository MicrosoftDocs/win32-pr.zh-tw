---
title: 'LVM_SETITEMCOUNT 訊息 (Commctrl .h) '
description: 讓清單視圖控制項配置記憶體給指定的專案數，或設定虛擬清單視圖控制項中的虛擬專案數。
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- LVM_SETITEMCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094176"
---
# <a name="lvm_setitemcount-message"></a><span data-ttu-id="3fda2-104">LVM \_ SETITEMCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="3fda2-104">LVM\_SETITEMCOUNT message</span></span>

<span data-ttu-id="3fda2-105">讓清單視圖控制項配置記憶體給指定的專案數，或設定 [虛擬清單視圖控制項](list-view-controls-overview.md)中的虛擬專案數。</span><span class="sxs-lookup"><span data-stu-id="3fda2-105">Causes the list-view control to allocate memory for the specified number of items or sets the virtual number of items in a [virtual list-view control](list-view-controls-overview.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="3fda2-106">參數</span><span class="sxs-lookup"><span data-stu-id="3fda2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fda2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fda2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fda2-108">清單視圖控制項最終將包含的專案數目。</span><span class="sxs-lookup"><span data-stu-id="3fda2-108">Number of items that the list-view control will ultimately contain.</span></span>

</dd> <dt>

<span data-ttu-id="3fda2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fda2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fda2-110">[版本 4.70](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="3fda2-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="3fda2-111">值，指定在重設專案計數之後，清單視圖控制項的行為。</span><span class="sxs-lookup"><span data-stu-id="3fda2-111">Values that specify the behavior of the list-view control after resetting the item count.</span></span> <span data-ttu-id="3fda2-112">這個值可以是下列各項的組合：</span><span class="sxs-lookup"><span data-stu-id="3fda2-112">This value can be a combination of the following:</span></span>



| <span data-ttu-id="3fda2-113">值</span><span class="sxs-lookup"><span data-stu-id="3fda2-113">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="3fda2-114">意義</span><span class="sxs-lookup"><span data-stu-id="3fda2-114">Meaning</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <span data-ttu-id="3fda2-115"><dt>**LVSICF \_ NOINVALIDATEALL**</dt></span><span class="sxs-lookup"><span data-stu-id="3fda2-115"><dt>**LVSICF\_NOINVALIDATEALL**</dt></span></span> </dl> | <span data-ttu-id="3fda2-116">除非受影響的專案目前為 view，否則不會重新繪製清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="3fda2-116">The list-view control will not repaint unless affected items are currently in view.</span></span><br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <span data-ttu-id="3fda2-117"><dt>**LVSICF \_ NOSCROLL**</dt></span><span class="sxs-lookup"><span data-stu-id="3fda2-117"><dt>**LVSICF\_NOSCROLL**</dt></span></span> </dl>                      | <span data-ttu-id="3fda2-118">當專案計數變更時，清單視圖控制項不會變更捲軸位置。</span><span class="sxs-lookup"><span data-stu-id="3fda2-118">The list-view control will not change the scroll position when the item count changes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fda2-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="3fda2-119">Return value</span></span>

<span data-ttu-id="3fda2-120">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="3fda2-120">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fda2-121">備註</span><span class="sxs-lookup"><span data-stu-id="3fda2-121">Remarks</span></span>

<span data-ttu-id="3fda2-122">記憶體的配置方式取決於建立清單視圖控制項的方式。</span><span class="sxs-lookup"><span data-stu-id="3fda2-122">How the memory is allocated depends on how the list-view control was created.</span></span> <span data-ttu-id="3fda2-123">您可以明確地傳送此訊息，或使用 [**listview \_ SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) 或 [**listview \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) 宏。</span><span class="sxs-lookup"><span data-stu-id="3fda2-123">You can send this message explicitly or use the [**ListView\_SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) or [**ListView\_SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) macros.</span></span> <span data-ttu-id="3fda2-124">如需詳細資訊，請參閱 [虛擬 List-View 樣式](/windows/desktop/Controls/list-view-controls-overview)。</span><span class="sxs-lookup"><span data-stu-id="3fda2-124">For more information, see [Virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).</span></span>

<span data-ttu-id="3fda2-125">如果未在 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式下建立清單視圖控制項，則傳送此訊息會導致控制項為指定的專案數配置其內部資料結構。</span><span class="sxs-lookup"><span data-stu-id="3fda2-125">If the list-view control was created without the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, sending this message causes the control to allocate its internal data structures for the specified number of items.</span></span> <span data-ttu-id="3fda2-126">這可防止控制項在每次加入專案時都必須配置資料結構。</span><span class="sxs-lookup"><span data-stu-id="3fda2-126">This prevents the control from having to allocate the data structures every time an item is added.</span></span>

<span data-ttu-id="3fda2-127">如果使用 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式建立清單視圖控制項 (虛擬清單視圖) ，則傳送此訊息會設定控制項包含的虛擬專案數目。</span><span class="sxs-lookup"><span data-stu-id="3fda2-127">If the list-view control was created with the [**LVS\_OWNERDATA**](list-view-window-styles.md) style (a virtual list view), sending this message sets the virtual number of items that the control contains.</span></span>

<span data-ttu-id="3fda2-128">*LParam* 參數僅適用于使用 [**Lvs) \_ OWNERDATA**](list-view-window-styles.md)和 [**lvs) \_ 報表**](list-view-window-styles.md)或 [**lvs) \_ 清單**](list-view-window-styles.md)樣式的清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="3fda2-128">The *lParam* parameter is intended only for list-view controls that use the [**LVS\_OWNERDATA**](list-view-window-styles.md) and [**LVS\_REPORT**](list-view-window-styles.md) or [**LVS\_LIST**](list-view-window-styles.md) styles.</span></span>

<span data-ttu-id="3fda2-129">當通用控制項清單視圖為虛擬化清單-view ([**lvs) \_ OWNERDATA**](list-view-window-styles.md)) 時，清單視圖上會有100000000專案的限制。</span><span class="sxs-lookup"><span data-stu-id="3fda2-129">When the common control list-view is a virtualized list-view ([**LVS\_OWNERDATA**](list-view-window-styles.md)), there is a 100,000,000 item limit on the list-view.</span></span> <span data-ttu-id="3fda2-130">在此案例中，當 **LVM \_ SETITEMCOUNT** 的 *wParam* 為100000001時，會傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="3fda2-130">In this scenario, **LVM\_SETITEMCOUNT** will return FALSE when it has a *wParam* of 100,000,001.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fda2-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fda2-131">Requirements</span></span>



| <span data-ttu-id="3fda2-132">需求</span><span class="sxs-lookup"><span data-stu-id="3fda2-132">Requirement</span></span> | <span data-ttu-id="3fda2-133">值</span><span class="sxs-lookup"><span data-stu-id="3fda2-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fda2-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3fda2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3fda2-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fda2-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fda2-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3fda2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3fda2-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fda2-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fda2-138">標頭</span><span class="sxs-lookup"><span data-stu-id="3fda2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fda2-139"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3fda2-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

