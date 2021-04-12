---
title: 'CB_SHOWDROPDOWN 訊息 (Winuser .h) '
description: 應用程式傳送 CB \_ SHOWDROPDOWN 訊息，以顯示或隱藏具有 CBS \_ 下拉式清單或 cbs DROPDOWNLIST 樣式之下拉式方塊的清單方塊 \_ 。
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- CB_SHOWDROPDOWN message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105605"
---
# <a name="cb_showdropdown-message"></a><span data-ttu-id="69b14-104">CB \_ SHOWDROPDOWN 訊息</span><span class="sxs-lookup"><span data-stu-id="69b14-104">CB\_SHOWDROPDOWN message</span></span>

<span data-ttu-id="69b14-105">應用程式傳送 **CB \_ SHOWDROPDOWN** 訊息，以顯示或隱藏具有 [**CBS \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式之下拉式方塊的清單方塊。</span><span class="sxs-lookup"><span data-stu-id="69b14-105">An application sends a **CB\_SHOWDROPDOWN** message to show or hide the list box of a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="69b14-106">參數</span><span class="sxs-lookup"><span data-stu-id="69b14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b14-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69b14-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69b14-108">指定是否要顯示或隱藏下拉式清單方塊的 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="69b14-108">A **BOOL** that specifies whether the drop-down list box is to be shown or hidden.</span></span> <span data-ttu-id="69b14-109">值為 **TRUE** 會顯示清單方塊; **FALSE** 值會將它隱藏。</span><span class="sxs-lookup"><span data-stu-id="69b14-109">A value of **TRUE** shows the list box; a value of **FALSE** hides it.</span></span>

</dd> <dt>

<span data-ttu-id="69b14-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69b14-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69b14-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="69b14-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b14-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="69b14-112">Return value</span></span>

<span data-ttu-id="69b14-113">傳回值一律為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="69b14-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="69b14-114">備註</span><span class="sxs-lookup"><span data-stu-id="69b14-114">Remarks</span></span>

<span data-ttu-id="69b14-115">此訊息不會影響以 [**CBS \_ 簡單**](combo-box-styles.md) 樣式建立的下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="69b14-115">This message has no effect on a combo box created with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b14-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="69b14-116">Requirements</span></span>



| <span data-ttu-id="69b14-117">需求</span><span class="sxs-lookup"><span data-stu-id="69b14-117">Requirement</span></span> | <span data-ttu-id="69b14-118">值</span><span class="sxs-lookup"><span data-stu-id="69b14-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b14-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69b14-119">Minimum supported client</span></span><br/> | <span data-ttu-id="69b14-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69b14-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="69b14-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69b14-121">Minimum supported server</span></span><br/> | <span data-ttu-id="69b14-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69b14-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="69b14-123">標頭</span><span class="sxs-lookup"><span data-stu-id="69b14-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b14-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="69b14-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b14-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69b14-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b14-126">**CB \_ GETDROPPEDSTATE**</span><span class="sxs-lookup"><span data-stu-id="69b14-126">**CB\_GETDROPPEDSTATE**</span></span>](cb-getdroppedstate.md)
</dt> </dl>

 

 





