---
title: 'CB_RESETCONTENT 訊息 (Winuser .h) '
description: 從清單方塊中移除所有專案，並編輯下拉式方塊的控制項。
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- CB_RESETCONTENT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843564"
---
# <a name="cb_resetcontent-message"></a><span data-ttu-id="988fb-104">CB \_ RESETCONTENT 訊息</span><span class="sxs-lookup"><span data-stu-id="988fb-104">CB\_RESETCONTENT message</span></span>

<span data-ttu-id="988fb-105">從清單方塊中移除所有專案，並編輯下拉式方塊的控制項。</span><span class="sxs-lookup"><span data-stu-id="988fb-105">Removes all items from the list box and edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="988fb-106">參數</span><span class="sxs-lookup"><span data-stu-id="988fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="988fb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="988fb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="988fb-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="988fb-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="988fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="988fb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="988fb-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="988fb-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="988fb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="988fb-111">Return value</span></span>

<span data-ttu-id="988fb-112">此訊息一律會傳回 CB \_ ok。</span><span class="sxs-lookup"><span data-stu-id="988fb-112">This message always returns CB\_OKAY.</span></span>

## <a name="remarks"></a><span data-ttu-id="988fb-113">備註</span><span class="sxs-lookup"><span data-stu-id="988fb-113">Remarks</span></span>

<span data-ttu-id="988fb-114">如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則下拉式方塊的擁有者會收到下拉式方塊中每個專案的 [**WM \_ DELETEITEM**](wm-deleteitem.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="988fb-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the owner of the combo box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="988fb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="988fb-115">Requirements</span></span>



| <span data-ttu-id="988fb-116">需求</span><span class="sxs-lookup"><span data-stu-id="988fb-116">Requirement</span></span> | <span data-ttu-id="988fb-117">值</span><span class="sxs-lookup"><span data-stu-id="988fb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="988fb-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="988fb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="988fb-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="988fb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="988fb-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="988fb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="988fb-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="988fb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="988fb-122">標頭</span><span class="sxs-lookup"><span data-stu-id="988fb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="988fb-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="988fb-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="988fb-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="988fb-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="988fb-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="988fb-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="988fb-126">**CB \_ DELETESTRING**</span><span class="sxs-lookup"><span data-stu-id="988fb-126">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="988fb-127">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="988fb-127">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





