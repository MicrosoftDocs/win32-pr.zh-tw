---
title: 'CB_GETCURSEL 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ GETCURSEL 訊息，以抓取下拉式方塊清單方塊中目前選取之專案的索引（如果有的話）。
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- CB_GETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844499"
---
# <a name="cb_getcursel-message"></a><span data-ttu-id="1630f-104">CB \_ GETCURSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="1630f-104">CB\_GETCURSEL message</span></span>

<span data-ttu-id="1630f-105">應用程式會傳送 **CB \_ GETCURSEL** 訊息，以抓取下拉式方塊清單方塊中目前選取之專案的索引（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="1630f-105">An application sends a **CB\_GETCURSEL** message to retrieve the index of the currently selected item, if any, in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="1630f-106">參數</span><span class="sxs-lookup"><span data-stu-id="1630f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1630f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1630f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1630f-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="1630f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1630f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1630f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1630f-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="1630f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1630f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1630f-111">Return value</span></span>

<span data-ttu-id="1630f-112">傳回值是目前選取專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="1630f-112">The return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="1630f-113">如果未選取任何專案，則會是 CB \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="1630f-113">If no item is selected, it is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="1630f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1630f-114">Requirements</span></span>



| <span data-ttu-id="1630f-115">需求</span><span class="sxs-lookup"><span data-stu-id="1630f-115">Requirement</span></span> | <span data-ttu-id="1630f-116">值</span><span class="sxs-lookup"><span data-stu-id="1630f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1630f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1630f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1630f-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1630f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1630f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1630f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1630f-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1630f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1630f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1630f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1630f-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1630f-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1630f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1630f-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="1630f-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="1630f-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1630f-125">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="1630f-125">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="1630f-126">**CB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="1630f-126">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> </dl>

 

 





