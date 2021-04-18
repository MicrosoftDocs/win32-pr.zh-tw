---
title: 'LVM_GETSELECTIONMARK 訊息 (Commctrl .h) '
description: 從清單視圖控制項抓取選取標記。 您可以明確地傳送此訊息，或使用 ListView \_ GetSelectionMark 宏。
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- LVM_GETSELECTIONMARK message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965749"
---
# <a name="lvm_getselectionmark-message"></a><span data-ttu-id="0d245-105">LVM \_ GETSELECTIONMARK 訊息</span><span class="sxs-lookup"><span data-stu-id="0d245-105">LVM\_GETSELECTIONMARK message</span></span>

<span data-ttu-id="0d245-106">從清單視圖控制項抓取選取標記。</span><span class="sxs-lookup"><span data-stu-id="0d245-106">Retrieves the selection mark from a list-view control.</span></span> <span data-ttu-id="0d245-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) 宏。</span><span class="sxs-lookup"><span data-stu-id="0d245-107">You can send this message explicitly or use the [**ListView\_GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d245-108">參數</span><span class="sxs-lookup"><span data-stu-id="0d245-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d245-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d245-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0d245-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0d245-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0d245-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d245-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0d245-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0d245-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d245-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d245-113">Return value</span></span>

<span data-ttu-id="0d245-114">傳回以零為基底的選取標記; 如果沒有選取專案標記，則為-1。</span><span class="sxs-lookup"><span data-stu-id="0d245-114">Returns the zero-based selection mark, or -1 if there is no selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d245-115">備註</span><span class="sxs-lookup"><span data-stu-id="0d245-115">Remarks</span></span>

<span data-ttu-id="0d245-116">*選取標記* 是從其開始多重選取專案的專案索引。</span><span class="sxs-lookup"><span data-stu-id="0d245-116">The *selection mark* is the item index from which a multiple selection starts.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d245-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d245-117">Requirements</span></span>



| <span data-ttu-id="0d245-118">需求</span><span class="sxs-lookup"><span data-stu-id="0d245-118">Requirement</span></span> | <span data-ttu-id="0d245-119">值</span><span class="sxs-lookup"><span data-stu-id="0d245-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d245-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d245-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d245-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d245-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d245-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d245-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d245-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d245-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d245-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0d245-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d245-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d245-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d245-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d245-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d245-127">**LVM \_ SETSELECTIONMARK**</span><span class="sxs-lookup"><span data-stu-id="0d245-127">**LVM\_SETSELECTIONMARK**</span></span>](lvm-setselectionmark.md)
</dt> </dl>

 

 





