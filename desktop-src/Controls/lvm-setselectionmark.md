---
title: 'LVM_SETSELECTIONMARK 訊息 (Commctrl .h) '
description: 設定清單視圖控制項中的選取專案標記。 您可以明確地傳送此訊息，或使用 ListView \_ SetSelectionMark 宏。
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- LVM_SETSELECTIONMARK message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685516"
---
# <a name="lvm_setselectionmark-message"></a><span data-ttu-id="3a42c-105">LVM \_ SETSELECTIONMARK 訊息</span><span class="sxs-lookup"><span data-stu-id="3a42c-105">LVM\_SETSELECTIONMARK message</span></span>

<span data-ttu-id="3a42c-106">設定清單視圖控制項中的選取專案標記。</span><span class="sxs-lookup"><span data-stu-id="3a42c-106">Sets the selection mark in a list-view control.</span></span> <span data-ttu-id="3a42c-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) 宏。</span><span class="sxs-lookup"><span data-stu-id="3a42c-107">You can send this message explicitly or use the [**ListView\_SetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a42c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a42c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a42c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a42c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3a42c-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3a42c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3a42c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a42c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a42c-112">新選取標記的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="3a42c-112">Zero-based index of the new selection mark.</span></span> <span data-ttu-id="3a42c-113">如果設定為-1，則會移除選取標記。</span><span class="sxs-lookup"><span data-stu-id="3a42c-113">If set to -1, the selection mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a42c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a42c-114">Return value</span></span>

<span data-ttu-id="3a42c-115">傳回先前的選取專案標記，如果沒有上一個選取專案標記，則為-1。</span><span class="sxs-lookup"><span data-stu-id="3a42c-115">Returns the previous selection mark, or -1 if there is no previous selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a42c-116">備註</span><span class="sxs-lookup"><span data-stu-id="3a42c-116">Remarks</span></span>

<span data-ttu-id="3a42c-117">*選取標記* 是從其開始多重選取專案的專案索引。</span><span class="sxs-lookup"><span data-stu-id="3a42c-117">The *selection mark* is the item index from which a multiple selection starts.</span></span> <span data-ttu-id="3a42c-118">此訊息不會影響專案的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="3a42c-118">This message does not affect the selection state of the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a42c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a42c-119">Requirements</span></span>



| <span data-ttu-id="3a42c-120">需求</span><span class="sxs-lookup"><span data-stu-id="3a42c-120">Requirement</span></span> | <span data-ttu-id="3a42c-121">值</span><span class="sxs-lookup"><span data-stu-id="3a42c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a42c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a42c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3a42c-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a42c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a42c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a42c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3a42c-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a42c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a42c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3a42c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a42c-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a42c-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a42c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a42c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a42c-129">**LVM \_ GETSELECTIONMARK**</span><span class="sxs-lookup"><span data-stu-id="3a42c-129">**LVM\_GETSELECTIONMARK**</span></span>](lvm-getselectionmark.md)
</dt> </dl>

 

 





