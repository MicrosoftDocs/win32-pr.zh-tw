---
title: 'HDM_GETOVERFLOWRECT 訊息 (Commctrl .h) '
description: 當在 \_ 標題控制項上設定 HDS 溢位樣式，且顯示溢位按鈕時，取得溢位按鈕的周框。 明確地傳送此訊息，或使用標頭 \_ GetOverflowRect 宏。
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- HDM_GETOVERFLOWRECT message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508803"
---
# <a name="hdm_getoverflowrect-message"></a><span data-ttu-id="06958-105">HDM \_ GETOVERFLOWRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="06958-105">HDM\_GETOVERFLOWRECT message</span></span>

<span data-ttu-id="06958-106">當在標題控制項上設定 [**HDS \_ 溢**](header-control-styles.md) 位樣式，且顯示溢位按鈕時，取得溢位按鈕的周框。</span><span class="sxs-lookup"><span data-stu-id="06958-106">Gets the bounding rectangle of the overflow button when the [**HDS\_OVERFLOW**](header-control-styles.md) style is set on the header control and the overflow button is visible.</span></span> <span data-ttu-id="06958-107">明確地傳送此訊息，或使用 [**標頭 \_ GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) 宏。</span><span class="sxs-lookup"><span data-stu-id="06958-107">Send this message explicitly or by using the [**Header\_GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="06958-108">參數</span><span class="sxs-lookup"><span data-stu-id="06958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06958-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06958-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06958-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="06958-110">Not used.</span></span> <span data-ttu-id="06958-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="06958-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="06958-112">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06958-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06958-113">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，用來接收周框的資訊。</span><span class="sxs-lookup"><span data-stu-id="06958-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="06958-114">訊息寄件者負責配置此結構。</span><span class="sxs-lookup"><span data-stu-id="06958-114">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="06958-115">在 **矩形** 結構中傳回的座標會以螢幕座標表示。</span><span class="sxs-lookup"><span data-stu-id="06958-115">The coordinates returned in the **RECT** structure are expressed as screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06958-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="06958-116">Return value</span></span>

<span data-ttu-id="06958-117">如果成功，則傳回 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="06958-117">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="06958-118">備註</span><span class="sxs-lookup"><span data-stu-id="06958-118">Remarks</span></span>

<span data-ttu-id="06958-119">標題控制項必須具有 **HDF \_ SPLITBUTTON** 樣式。</span><span class="sxs-lookup"><span data-stu-id="06958-119">The header control must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="06958-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="06958-120">Requirements</span></span>



| <span data-ttu-id="06958-121">需求</span><span class="sxs-lookup"><span data-stu-id="06958-121">Requirement</span></span> | <span data-ttu-id="06958-122">值</span><span class="sxs-lookup"><span data-stu-id="06958-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06958-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06958-123">Minimum supported client</span></span><br/> | <span data-ttu-id="06958-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06958-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06958-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06958-125">Minimum supported server</span></span><br/> | <span data-ttu-id="06958-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06958-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06958-127">標頭</span><span class="sxs-lookup"><span data-stu-id="06958-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="06958-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="06958-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06958-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06958-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06958-130">關於標題控制項</span><span class="sxs-lookup"><span data-stu-id="06958-130">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

