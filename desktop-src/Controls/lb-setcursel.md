---
title: 'LB_SETCURSEL 訊息 (Winuser .h) '
description: 視需要選取字串並將它滾動至 view。 選取新的字串時，清單方塊會從先前選取的字串中移除反白顯示。
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- LB_SETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106978599"
---
# <a name="lb_setcursel-message"></a><span data-ttu-id="44be3-105">LB \_ SETCURSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="44be3-105">LB\_SETCURSEL message</span></span>

<span data-ttu-id="44be3-106">視需要選取字串並將它滾動至 view。</span><span class="sxs-lookup"><span data-stu-id="44be3-106">Selects a string and scrolls it into view, if necessary.</span></span> <span data-ttu-id="44be3-107">選取新的字串時，清單方塊會從先前選取的字串中移除反白顯示。</span><span class="sxs-lookup"><span data-stu-id="44be3-107">When the new string is selected, the list box removes the highlight from the previously selected string.</span></span>

## <a name="parameters"></a><span data-ttu-id="44be3-108">參數</span><span class="sxs-lookup"><span data-stu-id="44be3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44be3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44be3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44be3-110">指定所選取之字串以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="44be3-110">Specifies the zero-based index of the string that is selected.</span></span> <span data-ttu-id="44be3-111">如果此參數為-1，則會將清單方塊設定為沒有選取專案。</span><span class="sxs-lookup"><span data-stu-id="44be3-111">If this parameter is -1, the list box is set to have no selection.</span></span>

<span data-ttu-id="44be3-112">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="44be3-112">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="44be3-113">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="44be3-113">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="44be3-114">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="44be3-114">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="44be3-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44be3-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44be3-116">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="44be3-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44be3-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="44be3-117">Return value</span></span>

<span data-ttu-id="44be3-118">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="44be3-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="44be3-119">如果 *wParam* 參數為-1，則 \_ 即使未發生任何錯誤，傳回值也會是 LB ERR。</span><span class="sxs-lookup"><span data-stu-id="44be3-119">If the *wParam* parameter is -1, the return value is LB\_ERR even though no error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="44be3-120">備註</span><span class="sxs-lookup"><span data-stu-id="44be3-120">Remarks</span></span>

<span data-ttu-id="44be3-121">此訊息只適用于單一挑選清單框。</span><span class="sxs-lookup"><span data-stu-id="44be3-121">Use this message only with single-selection list boxes.</span></span> <span data-ttu-id="44be3-122">您無法使用它來設定或移除多重選取清單方塊中的選取專案。</span><span class="sxs-lookup"><span data-stu-id="44be3-122">You cannot use it to set or remove a selection in a multiple-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="44be3-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="44be3-123">Requirements</span></span>



| <span data-ttu-id="44be3-124">需求</span><span class="sxs-lookup"><span data-stu-id="44be3-124">Requirement</span></span> | <span data-ttu-id="44be3-125">值</span><span class="sxs-lookup"><span data-stu-id="44be3-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44be3-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44be3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="44be3-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44be3-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="44be3-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44be3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="44be3-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44be3-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44be3-130">標頭</span><span class="sxs-lookup"><span data-stu-id="44be3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="44be3-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="44be3-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44be3-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44be3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44be3-133">**LB \_ GETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="44be3-133">**LB\_GETCURSEL**</span></span>](lb-getcursel.md)
</dt> </dl>

 

 





