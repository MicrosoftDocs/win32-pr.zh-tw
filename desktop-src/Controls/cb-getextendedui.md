---
title: 'CB_GETEXTENDEDUI 訊息 (Winuser .h) '
description: 決定下拉式方塊是否有預設使用者介面或擴充的使用者介面。
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- CB_GETEXTENDEDUI message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465268"
---
# <a name="cb_getextendedui-message"></a><span data-ttu-id="84119-104">CB \_ GETEXTENDEDUI 訊息</span><span class="sxs-lookup"><span data-stu-id="84119-104">CB\_GETEXTENDEDUI message</span></span>

<span data-ttu-id="84119-105">決定下拉式方塊是否有預設使用者介面或擴充的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="84119-105">Determines whether a combo box has the default user interface or the extended user interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="84119-106">參數</span><span class="sxs-lookup"><span data-stu-id="84119-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84119-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84119-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84119-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="84119-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="84119-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84119-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84119-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="84119-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84119-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="84119-111">Return value</span></span>

<span data-ttu-id="84119-112">如果下拉式方塊有擴充的使用者介面，則傳回值為 **TRUE**;否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="84119-112">If the combo box has the extended user interface, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="84119-113">備註</span><span class="sxs-lookup"><span data-stu-id="84119-113">Remarks</span></span>

<span data-ttu-id="84119-114">依預設，F4 鍵會開啟或關閉清單，而向下箭號會變更目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="84119-114">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="84119-115">在具有擴充使用者介面的下拉式方塊中，會停用 F4 鍵，然後按向下鍵以開啟下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="84119-115">In a combo box with the extended user interface, the F4 key is disabled and pressing the DOWN ARROW key opens the drop-down list.</span></span>

## <a name="requirements"></a><span data-ttu-id="84119-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="84119-116">Requirements</span></span>



| <span data-ttu-id="84119-117">需求</span><span class="sxs-lookup"><span data-stu-id="84119-117">Requirement</span></span> | <span data-ttu-id="84119-118">值</span><span class="sxs-lookup"><span data-stu-id="84119-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84119-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84119-119">Minimum supported client</span></span><br/> | <span data-ttu-id="84119-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84119-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="84119-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84119-121">Minimum supported server</span></span><br/> | <span data-ttu-id="84119-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84119-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="84119-123">標頭</span><span class="sxs-lookup"><span data-stu-id="84119-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="84119-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="84119-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84119-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84119-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="84119-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="84119-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="84119-127">**CB \_ SETEXTENDEDUI**</span><span class="sxs-lookup"><span data-stu-id="84119-127">**CB\_SETEXTENDEDUI**</span></span>](cb-setextendedui.md)
</dt> <dt>

<span data-ttu-id="84119-128">**概念**</span><span class="sxs-lookup"><span data-stu-id="84119-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="84119-129">下拉式列示方塊功能</span><span class="sxs-lookup"><span data-stu-id="84119-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





