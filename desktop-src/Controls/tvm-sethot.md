---
title: 'TVM_SETHOT 訊息 (Commctrl .h) '
description: 設定樹狀檢視控制項的熱專案。 您可以使用 TreeView SetHot 宏明確地傳送此訊息 \_ 。
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- TVM_SETHOT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934944"
---
# <a name="tvm_sethot-message"></a><span data-ttu-id="54393-105">TVM \_ SETHOT 訊息</span><span class="sxs-lookup"><span data-stu-id="54393-105">TVM\_SETHOT message</span></span>

<span data-ttu-id="54393-106">\[適用于內部用途;不建議在應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="54393-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="54393-107">未來的 Windows 版本可能不支援此訊息。\]</span><span class="sxs-lookup"><span data-stu-id="54393-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="54393-108">設定樹狀檢視控制項的熱專案。</span><span class="sxs-lookup"><span data-stu-id="54393-108">Sets the hot item for a tree-view control.</span></span> <span data-ttu-id="54393-109">您可以使用 [**TreeView \_ SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="54393-109">You can send this message explicitly or by using the [**TreeView\_SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="54393-110">參數</span><span class="sxs-lookup"><span data-stu-id="54393-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54393-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54393-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54393-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="54393-112">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="54393-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54393-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54393-114">新熱專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="54393-114">Handle to the new hot item.</span></span> <span data-ttu-id="54393-115">如果這個值為 **Null**，則樹狀檢視控制項將設定為沒有熱專案。</span><span class="sxs-lookup"><span data-stu-id="54393-115">If this value is **NULL**, the tree-view control will be set to have no hot item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54393-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="54393-116">Return value</span></span>

<span data-ttu-id="54393-117">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="54393-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="54393-118">安全性考量</span><span class="sxs-lookup"><span data-stu-id="54393-118">Security Considerations</span></span>

<span data-ttu-id="54393-119">使用此訊息可能會危害程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="54393-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="54393-120">備註</span><span class="sxs-lookup"><span data-stu-id="54393-120">Remarks</span></span>

<span data-ttu-id="54393-121">*熱專案* 是滑鼠停留在上方的專案。</span><span class="sxs-lookup"><span data-stu-id="54393-121">The *hot item* is the item that the mouse is hovering over.</span></span> <span data-ttu-id="54393-122">這則訊息會讓專案看起來像是最忙碌的專案，即使滑鼠未停留在其上也一樣。</span><span class="sxs-lookup"><span data-stu-id="54393-122">This message makes an item look like it is the hot item even if the mouse is not hovering over it.</span></span>

<span data-ttu-id="54393-123">如果未設定 [**電視 \_ TRACKSELECT**](tree-view-control-window-styles.md) 樣式，則此訊息不會顯示任何效果。</span><span class="sxs-lookup"><span data-stu-id="54393-123">This message has no visible effect if the [**TVS\_TRACKSELECT**](tree-view-control-window-styles.md) style is not set.</span></span>

<span data-ttu-id="54393-124">如果成功，此訊息將會重新繪製熱專案。</span><span class="sxs-lookup"><span data-stu-id="54393-124">If it succeeds, this message causes the hot item to be redrawn.</span></span>

<span data-ttu-id="54393-125">如果 *lParam* 為 **Null** ，而且樹狀檢視控制項正在追蹤滑鼠，則會忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="54393-125">This message is ignored if *lParam* is **NULL** and the tree-view control is tracking the mouse.</span></span>

## <a name="requirements"></a><span data-ttu-id="54393-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="54393-126">Requirements</span></span>



| <span data-ttu-id="54393-127">需求</span><span class="sxs-lookup"><span data-stu-id="54393-127">Requirement</span></span> | <span data-ttu-id="54393-128">值</span><span class="sxs-lookup"><span data-stu-id="54393-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54393-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54393-129">Minimum supported client</span></span><br/> | <span data-ttu-id="54393-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54393-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54393-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54393-131">Minimum supported server</span></span><br/> | <span data-ttu-id="54393-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54393-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54393-133">標頭</span><span class="sxs-lookup"><span data-stu-id="54393-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="54393-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="54393-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54393-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54393-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54393-136">**TreeView \_ SetHot**</span><span class="sxs-lookup"><span data-stu-id="54393-136">**TreeView\_SetHot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





