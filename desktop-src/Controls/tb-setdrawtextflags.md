---
title: 'TB_SETDRAWTEXTFLAGS 訊息 (Commctrl .h) '
description: 設定工具列的文字繪圖旗標。
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- TB_SETDRAWTEXTFLAGS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934785"
---
# <a name="tb_setdrawtextflags-message"></a><span data-ttu-id="9e81e-104">TB \_ SETDRAWTEXTFLAGS 訊息</span><span class="sxs-lookup"><span data-stu-id="9e81e-104">TB\_SETDRAWTEXTFLAGS message</span></span>

<span data-ttu-id="9e81e-105">設定工具列的文字繪圖旗標。</span><span class="sxs-lookup"><span data-stu-id="9e81e-105">Sets the text drawing flags for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e81e-106">參數</span><span class="sxs-lookup"><span data-stu-id="9e81e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e81e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e81e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e81e-108">在 DrawText 中指定的一或多個 DT \_ 旗標，表示在繪製 [](/windows/desktop/api/winuser/nf-winuser-drawtext)文字時，將使用 *lParam* 中的哪個位。</span><span class="sxs-lookup"><span data-stu-id="9e81e-108">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate which bits in *lParam* will be used when drawing the text.</span></span>

</dd> <dt>

<span data-ttu-id="9e81e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e81e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e81e-110">在 DrawText 中指定的一或多個 DT \_ 旗標，指出按鈕文字的繪製方式。 [](/windows/desktop/api/winuser/nf-winuser-drawtext)</span><span class="sxs-lookup"><span data-stu-id="9e81e-110">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate how the button text will be drawn.</span></span> <span data-ttu-id="9e81e-111">此值會在繪製按鈕文字時傳遞至 **DrawText** 函式。</span><span class="sxs-lookup"><span data-stu-id="9e81e-111">This value will be passed to the **DrawText** function when the button text is drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e81e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e81e-112">Return value</span></span>

<span data-ttu-id="9e81e-113">傳回先前的文字繪圖旗標。</span><span class="sxs-lookup"><span data-stu-id="9e81e-113">Returns the previous text drawing flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e81e-114">備註</span><span class="sxs-lookup"><span data-stu-id="9e81e-114">Remarks</span></span>

<span data-ttu-id="9e81e-115">*WParam* 參數可讓您指定在繪製文字時要使用的旗標，即使這些旗標已關閉也是一樣。</span><span class="sxs-lookup"><span data-stu-id="9e81e-115">The *wParam* parameter allows you to specify which flags will be used when drawing the text, even if these flags are turned off.</span></span> <span data-ttu-id="9e81e-116">例如，如果您不想要在 \_ 繪製文字時使用 dt center 旗標，您可以將 dt \_ center 旗標新增至 *wParam* ，而不要 \_ 在 *lParam* 中指定 dt center 旗標。</span><span class="sxs-lookup"><span data-stu-id="9e81e-116">For example, if you do not want the DT\_CENTER flag used when drawing text, you would add the DT\_CENTER flag to *wParam* and not specify the DT\_CENTER flag in *lParam*.</span></span> <span data-ttu-id="9e81e-117">這可防止控制項將 DT \_ CENTER 旗標傳遞給 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) 函數。</span><span class="sxs-lookup"><span data-stu-id="9e81e-117">This prevents the control from passing the DT\_CENTER flag to the [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e81e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e81e-118">Requirements</span></span>



| <span data-ttu-id="9e81e-119">需求</span><span class="sxs-lookup"><span data-stu-id="9e81e-119">Requirement</span></span> | <span data-ttu-id="9e81e-120">值</span><span class="sxs-lookup"><span data-stu-id="9e81e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e81e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e81e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9e81e-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e81e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e81e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e81e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9e81e-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e81e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e81e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9e81e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e81e-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9e81e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

