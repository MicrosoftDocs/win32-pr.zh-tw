---
title: 'TTM_SETMAXTIPWIDTH 訊息 (Commctrl .h) '
description: 設定工具提示視窗的最大寬度。
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- TTM_SETMAXTIPWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ce930b289205b5fb0d2768068b8cb28cd11aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187284"
---
# <a name="ttm_setmaxtipwidth-message"></a><span data-ttu-id="43651-104">TTM \_ SETMAXTIPWIDTH 訊息</span><span class="sxs-lookup"><span data-stu-id="43651-104">TTM\_SETMAXTIPWIDTH message</span></span>

<span data-ttu-id="43651-105">設定工具提示視窗的最大寬度。</span><span class="sxs-lookup"><span data-stu-id="43651-105">Sets the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="43651-106">參數</span><span class="sxs-lookup"><span data-stu-id="43651-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43651-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43651-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="43651-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="43651-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="43651-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43651-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43651-110">最大工具提示視窗寬度，或-1 可允許任何寬度。</span><span class="sxs-lookup"><span data-stu-id="43651-110">Maximum tooltip window width, or -1 to allow any width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43651-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="43651-111">Return value</span></span>

<span data-ttu-id="43651-112">傳回先前的工具提示最大寬度。</span><span class="sxs-lookup"><span data-stu-id="43651-112">Returns the previous maximum tooltip width.</span></span>

## <a name="remarks"></a><span data-ttu-id="43651-113">備註</span><span class="sxs-lookup"><span data-stu-id="43651-113">Remarks</span></span>

<span data-ttu-id="43651-114">最大寬度值不會指出工具提示視窗的實際寬度。</span><span class="sxs-lookup"><span data-stu-id="43651-114">The maximum width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="43651-115">相反地，如果工具提示字串超過最大寬度，控制項會將文字分成多行，使用空格來決定分行符號。</span><span class="sxs-lookup"><span data-stu-id="43651-115">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="43651-116">如果無法將文字分割成多行，它就會顯示在一行中，可能會超過工具提示寬度上限。</span><span class="sxs-lookup"><span data-stu-id="43651-116">If the text cannot be segmented into multiple lines, it is displayed on a single line, which may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="43651-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="43651-117">Requirements</span></span>



| <span data-ttu-id="43651-118">需求</span><span class="sxs-lookup"><span data-stu-id="43651-118">Requirement</span></span> | <span data-ttu-id="43651-119">值</span><span class="sxs-lookup"><span data-stu-id="43651-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43651-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43651-120">Minimum supported client</span></span><br/> | <span data-ttu-id="43651-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43651-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43651-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43651-122">Minimum supported server</span></span><br/> | <span data-ttu-id="43651-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43651-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43651-124">標頭</span><span class="sxs-lookup"><span data-stu-id="43651-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="43651-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="43651-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43651-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43651-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43651-127">**TTM \_ GETMAXTIPWIDTH**</span><span class="sxs-lookup"><span data-stu-id="43651-127">**TTM\_GETMAXTIPWIDTH**</span></span>](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





