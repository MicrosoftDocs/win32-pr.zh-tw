---
title: 'CB_GETDROPPEDWIDTH 訊息 (Winuser .h) '
description: 取得具有 CBS \_ 下拉式清單或 cbs DROPDOWNLIST 樣式之下拉式方塊清單方塊的最小允許寬度（以圖元為單位） \_ 。
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- CB_GETDROPPEDWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025094"
---
# <a name="cb_getdroppedwidth-message"></a><span data-ttu-id="265f2-104">CB \_ GETDROPPEDWIDTH 訊息</span><span class="sxs-lookup"><span data-stu-id="265f2-104">CB\_GETDROPPEDWIDTH message</span></span>

<span data-ttu-id="265f2-105">取得具有 [**CBS \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式之下拉式方塊清單方塊的最小允許寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="265f2-105">Gets the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="265f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="265f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="265f2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="265f2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="265f2-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="265f2-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="265f2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="265f2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="265f2-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="265f2-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="265f2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="265f2-111">Return value</span></span>

<span data-ttu-id="265f2-112">如果訊息成功，則傳回值為寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="265f2-112">If the message succeeds, the return value is the width, in pixels.</span></span>

<span data-ttu-id="265f2-113">如果訊息失敗，則傳回值為 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="265f2-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="265f2-114">備註</span><span class="sxs-lookup"><span data-stu-id="265f2-114">Remarks</span></span>

<span data-ttu-id="265f2-115">根據預設，下拉式清單方塊的最小允許寬度為零。</span><span class="sxs-lookup"><span data-stu-id="265f2-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="265f2-116">清單方塊的寬度可以是允許的最小寬度或下拉式方塊寬度（以較大者為准）。</span><span class="sxs-lookup"><span data-stu-id="265f2-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="265f2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="265f2-117">Requirements</span></span>



| <span data-ttu-id="265f2-118">需求</span><span class="sxs-lookup"><span data-stu-id="265f2-118">Requirement</span></span> | <span data-ttu-id="265f2-119">值</span><span class="sxs-lookup"><span data-stu-id="265f2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="265f2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="265f2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="265f2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="265f2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="265f2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="265f2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="265f2-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="265f2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="265f2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="265f2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="265f2-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="265f2-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="265f2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="265f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="265f2-127">**CB \_ SETDROPPEDWIDTH**</span><span class="sxs-lookup"><span data-stu-id="265f2-127">**CB\_SETDROPPEDWIDTH**</span></span>](cb-setdroppedwidth.md)
</dt> </dl>

 

 





