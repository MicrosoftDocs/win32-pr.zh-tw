---
title: 'TBM_CLEARSEL 訊息 (Commctrl .h) '
description: 清除目前選取範圍中的選取範圍。
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- TBM_CLEARSEL message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d2474f3978dc80b2611bd6b454c45e515ee159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844439"
---
# <a name="tbm_clearsel-message"></a><span data-ttu-id="a99eb-104">TBM \_ CLEARSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="a99eb-104">TBM\_CLEARSEL message</span></span>

<span data-ttu-id="a99eb-105">清除目前選取範圍中的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="a99eb-105">Clears the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a99eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="a99eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a99eb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a99eb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a99eb-108">重繪旗標。</span><span class="sxs-lookup"><span data-stu-id="a99eb-108">Redraw flag.</span></span> <span data-ttu-id="a99eb-109">如果此參數為 **TRUE**，則在清除選取專案之後，會重新繪製這些內容。</span><span class="sxs-lookup"><span data-stu-id="a99eb-109">If this parameter is **TRUE**, the trackbar is redrawn after the selection is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="a99eb-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a99eb-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a99eb-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a99eb-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a99eb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a99eb-112">Return value</span></span>

<span data-ttu-id="a99eb-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="a99eb-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a99eb-114">備註</span><span class="sxs-lookup"><span data-stu-id="a99eb-114">Remarks</span></span>

<span data-ttu-id="a99eb-115">只有當您在建立時，如果您已指定 [ [**tb] \_ ENABLESELRANGE**](trackbar-control-styles.md) 樣式，則會有一個選取範圍。</span><span class="sxs-lookup"><span data-stu-id="a99eb-115">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a99eb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a99eb-116">Requirements</span></span>



| <span data-ttu-id="a99eb-117">需求</span><span class="sxs-lookup"><span data-stu-id="a99eb-117">Requirement</span></span> | <span data-ttu-id="a99eb-118">值</span><span class="sxs-lookup"><span data-stu-id="a99eb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a99eb-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a99eb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a99eb-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a99eb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a99eb-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a99eb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a99eb-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a99eb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a99eb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a99eb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a99eb-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a99eb-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a99eb-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a99eb-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="a99eb-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="a99eb-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a99eb-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="a99eb-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="a99eb-128">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="a99eb-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="a99eb-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="a99eb-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





