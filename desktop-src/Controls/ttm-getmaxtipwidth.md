---
title: 'TTM_GETMAXTIPWIDTH 訊息 (Commctrl .h) '
description: 抓取工具提示視窗的最大寬度。
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- TTM_GETMAXTIPWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934395"
---
# <a name="ttm_getmaxtipwidth-message"></a><span data-ttu-id="b4b1d-104">TTM \_ GETMAXTIPWIDTH 訊息</span><span class="sxs-lookup"><span data-stu-id="b4b1d-104">TTM\_GETMAXTIPWIDTH message</span></span>

<span data-ttu-id="b4b1d-105">抓取工具提示視窗的最大寬度。</span><span class="sxs-lookup"><span data-stu-id="b4b1d-105">Retrieves the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4b1d-106">參數</span><span class="sxs-lookup"><span data-stu-id="b4b1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4b1d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4b1d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b4b1d-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b4b1d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b4b1d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4b1d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b4b1d-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b4b1d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4b1d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4b1d-111">Return value</span></span>

<span data-ttu-id="b4b1d-112">傳回 **INT** 值，表示最大工具提示寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b4b1d-112">Returns an **INT** value that represents the maximum tooltip width, in pixels.</span></span> <span data-ttu-id="b4b1d-113">如果先前未設定最大寬度，則訊息會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="b4b1d-113">If no maximum width was set previously, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4b1d-114">備註</span><span class="sxs-lookup"><span data-stu-id="b4b1d-114">Remarks</span></span>

<span data-ttu-id="b4b1d-115">工具提示寬度值的最大值不會指出工具提示視窗的實際寬度。</span><span class="sxs-lookup"><span data-stu-id="b4b1d-115">The maximum tooltip width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="b4b1d-116">相反地，如果工具提示字串超過最大寬度，控制項會將文字分成多行，使用空格來決定分行符號。</span><span class="sxs-lookup"><span data-stu-id="b4b1d-116">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="b4b1d-117">如果無法將文字分割成多行，它就會顯示在同一行上。</span><span class="sxs-lookup"><span data-stu-id="b4b1d-117">If the text cannot be segmented into multiple lines, it will be displayed on a single line.</span></span> <span data-ttu-id="b4b1d-118">此行的長度可能會超過工具提示寬度上限。</span><span class="sxs-lookup"><span data-stu-id="b4b1d-118">The length of this line may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b1d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4b1d-119">Requirements</span></span>



| <span data-ttu-id="b4b1d-120">需求</span><span class="sxs-lookup"><span data-stu-id="b4b1d-120">Requirement</span></span> | <span data-ttu-id="b4b1d-121">值</span><span class="sxs-lookup"><span data-stu-id="b4b1d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b1d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4b1d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b1d-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4b1d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4b1d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4b1d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b1d-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4b1d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4b1d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b4b1d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4b1d-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b1d-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b1d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4b1d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b1d-129">**TTM \_ SETMAXTIPWIDTH**</span><span class="sxs-lookup"><span data-stu-id="b4b1d-129">**TTM\_SETMAXTIPWIDTH**</span></span>](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





