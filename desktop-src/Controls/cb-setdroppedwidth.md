---
title: 'CB_SETDROPPEDWIDTH 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETDROPPEDWIDTH 訊息，以使用 cbs \_ 下拉式清單或 cbs DROPDOWNLIST 樣式來設定下拉式方塊清單方塊的最小允許寬度（以圖元為單位） \_ 。
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- CB_SETDROPPEDWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843560"
---
# <a name="cb_setdroppedwidth-message"></a><span data-ttu-id="fa22f-104">CB \_ SETDROPPEDWIDTH 訊息</span><span class="sxs-lookup"><span data-stu-id="fa22f-104">CB\_SETDROPPEDWIDTH message</span></span>

<span data-ttu-id="fa22f-105">應用程式會傳送 **CB \_ SETDROPPEDWIDTH** 訊息，以使用 [**Cbs \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式來設定下拉式方塊清單方塊的最小允許寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="fa22f-105">An application sends the **CB\_SETDROPPEDWIDTH** message to set the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa22f-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa22f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa22f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa22f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa22f-108">清單方塊的允許寬度下限（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="fa22f-108">The minimum allowable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="fa22f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa22f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa22f-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="fa22f-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa22f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa22f-111">Return value</span></span>

<span data-ttu-id="fa22f-112">如果訊息成功，傳回值就是清單方塊的新寬度。</span><span class="sxs-lookup"><span data-stu-id="fa22f-112">If the message is successful, The return value is the new width of the list box.</span></span>

<span data-ttu-id="fa22f-113">如果訊息失敗，則傳回值為 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="fa22f-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa22f-114">備註</span><span class="sxs-lookup"><span data-stu-id="fa22f-114">Remarks</span></span>

<span data-ttu-id="fa22f-115">根據預設，下拉式清單方塊的最小允許寬度為零。</span><span class="sxs-lookup"><span data-stu-id="fa22f-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="fa22f-116">清單方塊的寬度可以是允許的最小寬度或下拉式方塊寬度（以較大者為准）。</span><span class="sxs-lookup"><span data-stu-id="fa22f-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa22f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa22f-117">Requirements</span></span>



| <span data-ttu-id="fa22f-118">需求</span><span class="sxs-lookup"><span data-stu-id="fa22f-118">Requirement</span></span> | <span data-ttu-id="fa22f-119">值</span><span class="sxs-lookup"><span data-stu-id="fa22f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa22f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa22f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fa22f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa22f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa22f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa22f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fa22f-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa22f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa22f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="fa22f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa22f-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fa22f-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa22f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa22f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa22f-127">**CB \_ GETDROPPEDWIDTH**</span><span class="sxs-lookup"><span data-stu-id="fa22f-127">**CB\_GETDROPPEDWIDTH**</span></span>](cb-getdroppedwidth.md)
</dt> </dl>

 

 





