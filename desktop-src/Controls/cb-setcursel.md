---
title: 'CB_SETCURSEL 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETCURSEL 訊息，以選取下拉式方塊清單中的字串。
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- CB_SETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025079"
---
# <a name="cb_setcursel-message"></a><span data-ttu-id="8ec8f-104">CB \_ SETCURSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="8ec8f-104">CB\_SETCURSEL message</span></span>

<span data-ttu-id="8ec8f-105">應用程式會傳送 **CB \_ SETCURSEL** 訊息，以選取下拉式方塊清單中的字串。</span><span class="sxs-lookup"><span data-stu-id="8ec8f-105">An application sends a **CB\_SETCURSEL** message to select a string in the list of a combo box.</span></span> <span data-ttu-id="8ec8f-106">如有必要，清單會將字串滾動至 view。</span><span class="sxs-lookup"><span data-stu-id="8ec8f-106">If necessary, the list scrolls the string into view.</span></span> <span data-ttu-id="8ec8f-107">下拉式方塊的編輯控制項中的文字會變更，以反映新的選取專案，並移除清單中的任何先前選取專案。</span><span class="sxs-lookup"><span data-stu-id="8ec8f-107">The text in the edit control of the combo box changes to reflect the new selection, and any previous selection in the list is removed.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ec8f-108">參數</span><span class="sxs-lookup"><span data-stu-id="8ec8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ec8f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ec8f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec8f-110">指定要選取之字串的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="8ec8f-110">Specifies the zero-based index of the string to select.</span></span> <span data-ttu-id="8ec8f-111">如果此參數為-1，則會移除清單中目前的選取範圍，並清除編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="8ec8f-111">If this parameter is -1, any current selection in the list is removed and the edit control is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="8ec8f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ec8f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec8f-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="8ec8f-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ec8f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ec8f-114">Return value</span></span>

<span data-ttu-id="8ec8f-115">如果訊息成功，則傳回值是所選取專案的索引。</span><span class="sxs-lookup"><span data-stu-id="8ec8f-115">If the message is successful, the return value is the index of the item selected.</span></span> <span data-ttu-id="8ec8f-116">如果 *wParam* 大於清單中的專案數，或 *wParam* 為-1，則傳回值為 CB \_ ERR，並且會清除選取專案。</span><span class="sxs-lookup"><span data-stu-id="8ec8f-116">If *wParam* is greater than the number of items in the list or if *wParam* is -1, the return value is CB\_ERR and the selection is cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ec8f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ec8f-117">Requirements</span></span>



| <span data-ttu-id="8ec8f-118">需求</span><span class="sxs-lookup"><span data-stu-id="8ec8f-118">Requirement</span></span> | <span data-ttu-id="8ec8f-119">值</span><span class="sxs-lookup"><span data-stu-id="8ec8f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec8f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ec8f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8ec8f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ec8f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8ec8f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ec8f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8ec8f-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ec8f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8ec8f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8ec8f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ec8f-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8ec8f-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec8f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ec8f-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ec8f-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="8ec8f-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8ec8f-128">**CB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="8ec8f-128">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="8ec8f-129">**CB \_ GETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="8ec8f-129">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="8ec8f-130">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="8ec8f-130">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> </dl>

 

 





