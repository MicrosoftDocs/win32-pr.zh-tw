---
title: 'CB_SETEXTENDEDUI 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETEXTENDEDUI 訊息，以針對具有 CBS \_ 下拉式清單或 cbs DROPDOWNLIST 樣式的下拉式方塊，選取預設的 ui 或擴充的 ui \_ 。
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- CB_SETEXTENDEDUI message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94c31c8bc5457799d0038ecd8340c03c55aed91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465253"
---
# <a name="cb_setextendedui-message"></a><span data-ttu-id="8afec-104">CB \_ SETEXTENDEDUI 訊息</span><span class="sxs-lookup"><span data-stu-id="8afec-104">CB\_SETEXTENDEDUI message</span></span>

<span data-ttu-id="8afec-105">應用程式會傳送 **CB \_ SETEXTENDEDUI** 訊息，以針對具有 [**CBS \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式的下拉式方塊，選取預設的 ui 或擴充的 ui。</span><span class="sxs-lookup"><span data-stu-id="8afec-105">An application sends a **CB\_SETEXTENDEDUI** message to select either the default UI or the extended UI for a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="8afec-106">參數</span><span class="sxs-lookup"><span data-stu-id="8afec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8afec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8afec-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8afec-108">**布林** 值，指定下拉式方塊是否使用擴充的 Ui (**TRUE**) 或預設的 ui (**FALSE**) 。</span><span class="sxs-lookup"><span data-stu-id="8afec-108">A **BOOL** that specifies whether the combo box uses the extended UI (**TRUE**) or the default UI (**FALSE**).</span></span>

</dd> <dt>

<span data-ttu-id="8afec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8afec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8afec-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="8afec-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8afec-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8afec-111">Return value</span></span>

<span data-ttu-id="8afec-112">如果作業成功，則傳回值為 CB \_ ok。</span><span class="sxs-lookup"><span data-stu-id="8afec-112">If the operation succeeds, the return value is CB\_OKAY.</span></span> <span data-ttu-id="8afec-113">如果發生錯誤，則為 CB \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="8afec-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="8afec-114">備註</span><span class="sxs-lookup"><span data-stu-id="8afec-114">Remarks</span></span>

<span data-ttu-id="8afec-115">依預設，F4 鍵會開啟或關閉清單，而向下箭號會變更目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="8afec-115">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="8afec-116">在擴充的 UI 中，會停用 F4 鍵，而向下鍵則會開啟下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="8afec-116">In the extended UI, the F4 key is disabled and the DOWN ARROW key opens the drop-down list.</span></span> <span data-ttu-id="8afec-117">當設定擴充 UI 時，滑鼠滾輪（通常會在清單中的專案中滾動）沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="8afec-117">The mouse wheel, which normally scrolls through the items in the list, has no effect when the extended UI is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="8afec-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8afec-118">Requirements</span></span>



| <span data-ttu-id="8afec-119">需求</span><span class="sxs-lookup"><span data-stu-id="8afec-119">Requirement</span></span> | <span data-ttu-id="8afec-120">值</span><span class="sxs-lookup"><span data-stu-id="8afec-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8afec-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8afec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8afec-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8afec-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8afec-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8afec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8afec-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8afec-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8afec-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8afec-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8afec-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8afec-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8afec-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8afec-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="8afec-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="8afec-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8afec-129">**CB \_ GETEXTENDEDUI**</span><span class="sxs-lookup"><span data-stu-id="8afec-129">**CB\_GETEXTENDEDUI**</span></span>](cb-getextendedui.md)
</dt> <dt>

<span data-ttu-id="8afec-130">**概念**</span><span class="sxs-lookup"><span data-stu-id="8afec-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8afec-131">下拉式列示方塊功能</span><span class="sxs-lookup"><span data-stu-id="8afec-131">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





