---
title: 'LVM_ENSUREVISIBLE 訊息 (Commctrl .h) '
description: 確定清單視圖專案是完全或部分可見的，視需要滾動清單視圖控制項。 您可以明確地傳送此訊息，或使用 ListView \_ EnsureVisible 宏來傳送。
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- LVM_ENSUREVISIBLE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933925"
---
# <a name="lvm_ensurevisible-message"></a><span data-ttu-id="80df7-105">LVM \_ ENSUREVISIBLE 訊息</span><span class="sxs-lookup"><span data-stu-id="80df7-105">LVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="80df7-106">確定清單視圖專案是完全或部分可見的，視需要滾動清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="80df7-106">Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary.</span></span> <span data-ttu-id="80df7-107">您可以明確地傳送此訊息，或使用 [**ListView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="80df7-107">You can send this message explicitly or by using the [**ListView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="80df7-108">參數</span><span class="sxs-lookup"><span data-stu-id="80df7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80df7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80df7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80df7-110">清單視圖專案的索引。</span><span class="sxs-lookup"><span data-stu-id="80df7-110">The index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="80df7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80df7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80df7-112">值，指定是否必須完全看見專案。</span><span class="sxs-lookup"><span data-stu-id="80df7-112">A value specifying whether the item must be entirely visible.</span></span> <span data-ttu-id="80df7-113">如果此參數為 **TRUE**，則如果專案至少為部分可見，就不會發生任何滾動。</span><span class="sxs-lookup"><span data-stu-id="80df7-113">If this parameter is **TRUE**, no scrolling occurs if the item is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80df7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="80df7-114">Return value</span></span>

<span data-ttu-id="80df7-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="80df7-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="80df7-116">備註</span><span class="sxs-lookup"><span data-stu-id="80df7-116">Remarks</span></span>

<span data-ttu-id="80df7-117">如果視窗樣式包含 [**lvs) \_ NOSCROLL**](list-view-window-styles.md)，則訊息會失敗。</span><span class="sxs-lookup"><span data-stu-id="80df7-117">The message fails if the window style includes [**LVS\_NOSCROLL**](list-view-window-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80df7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="80df7-118">Requirements</span></span>



| <span data-ttu-id="80df7-119">需求</span><span class="sxs-lookup"><span data-stu-id="80df7-119">Requirement</span></span> | <span data-ttu-id="80df7-120">值</span><span class="sxs-lookup"><span data-stu-id="80df7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80df7-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80df7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="80df7-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80df7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80df7-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80df7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="80df7-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80df7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80df7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="80df7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="80df7-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="80df7-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





