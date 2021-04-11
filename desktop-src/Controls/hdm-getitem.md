---
title: 'HDM_GETITEM 訊息 (Commctrl .h) '
description: 取得標題控制項中的專案相關資訊。 您可以明確地傳送此訊息，或使用標頭 \_ GetItem 宏。
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- HDM_GETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2073602121480930e0f7d9d2e5a904c0dea77ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103776"
---
# <a name="hdm_getitem-message"></a><span data-ttu-id="e398e-105">HDM \_ GETITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="e398e-105">HDM\_GETITEM message</span></span>

<span data-ttu-id="e398e-106">取得標題控制項中的專案相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e398e-106">Gets information about an item in a header control.</span></span> <span data-ttu-id="e398e-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) 宏。</span><span class="sxs-lookup"><span data-stu-id="e398e-107">You can send this message explicitly or use the [**Header\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e398e-108">參數</span><span class="sxs-lookup"><span data-stu-id="e398e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e398e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e398e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e398e-110">要取得其資訊之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="e398e-110">The index of the item for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="e398e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e398e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e398e-112">[**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e398e-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="e398e-113">傳送訊息時， **遮罩** 成員會指出所要求的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="e398e-113">When the message is sent, the **mask** member indicates the type of information being requested.</span></span> <span data-ttu-id="e398e-114">當訊息傳回時，其他成員會收到要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="e398e-114">When the message returns, the other members receive the requested information.</span></span> <span data-ttu-id="e398e-115">如果 **遮罩** 成員指定為零，則訊息會傳回 **TRUE** ，但不會將任何資訊複製到結構中。</span><span class="sxs-lookup"><span data-stu-id="e398e-115">If the **mask** member specifies zero, the message returns **TRUE** but copies no information to the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e398e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e398e-116">Return value</span></span>

<span data-ttu-id="e398e-117">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e398e-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e398e-118">備註</span><span class="sxs-lookup"><span data-stu-id="e398e-118">Remarks</span></span>

<span data-ttu-id="e398e-119">如果在 \_ [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema)結構的 **MASK** 成員中設定 HDI 文字旗標，控制項可能會變更結構的 **pszText** 成員以指向新的文字，而不是以要求的文字填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e398e-119">If the HDI\_TEXT flag is set in the **mask** member of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="e398e-120">應用程式不應假設文字一定會放在要求的緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="e398e-120">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e398e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e398e-121">Requirements</span></span>



| <span data-ttu-id="e398e-122">需求</span><span class="sxs-lookup"><span data-stu-id="e398e-122">Requirement</span></span> | <span data-ttu-id="e398e-123">值</span><span class="sxs-lookup"><span data-stu-id="e398e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e398e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e398e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e398e-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e398e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e398e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e398e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e398e-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e398e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e398e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e398e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e398e-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e398e-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e398e-130">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e398e-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e398e-131">**HDM \_GETITEMW** (Unicode) 和 **HDM \_ GETITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e398e-131">**HDM\_GETITEMW** (Unicode) and **HDM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





