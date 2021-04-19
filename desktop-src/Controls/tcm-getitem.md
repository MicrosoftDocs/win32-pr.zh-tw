---
title: 'TCM_GETITEM 訊息 (Commctrl .h) '
description: 抓取索引標籤控制項中索引標籤的相關資訊。 您可以使用 TabCtrl GetItem 宏明確地傳送此訊息 \_ 。
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- TCM_GETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f94f26a0893416847df052ff47731391a86f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969202"
---
# <a name="tcm_getitem-message"></a><span data-ttu-id="dca8d-105">TCM \_ GETITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="dca8d-105">TCM\_GETITEM message</span></span>

<span data-ttu-id="dca8d-106">抓取索引標籤控制項中索引標籤的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dca8d-106">Retrieves information about a tab in a tab control.</span></span> <span data-ttu-id="dca8d-107">您可以使用 [**TabCtrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="dca8d-107">You can send this message explicitly or by using the [**TabCtrl\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dca8d-108">參數</span><span class="sxs-lookup"><span data-stu-id="dca8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dca8d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dca8d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dca8d-110">索引標籤的索引。</span><span class="sxs-lookup"><span data-stu-id="dca8d-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="dca8d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dca8d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dca8d-112">[**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)結構的指標，此結構會指定要取出的資訊，並接收索引標籤的相關資訊。傳送訊息時，**遮罩** 成員會指定要傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="dca8d-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the information to retrieve and receives information about the tab. When the message is sent, the **mask** member specifies which attributes to return.</span></span> <span data-ttu-id="dca8d-113">如果 **遮罩** 成員指定 TCIF \_ 文字值， **pszText** 成員必須包含接收專案文字的緩衝區位址，而且 **cchTextMax** 成員必須指定緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="dca8d-113">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text, and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dca8d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="dca8d-114">Return value</span></span>

<span data-ttu-id="dca8d-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="dca8d-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dca8d-116">備註</span><span class="sxs-lookup"><span data-stu-id="dca8d-116">Remarks</span></span>

<span data-ttu-id="dca8d-117">如果在 \_ [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)結構的 **MASK** 成員中設定 TCIF 文字旗標，控制項可能會變更結構的 **pszText** 成員以指向新的文字，而不是以要求的文字填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dca8d-117">If the TCIF\_TEXT flag is set in the **mask** member of the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="dca8d-118">控制項可以將 **pszText** 成員設為 **Null** ，表示沒有任何文字與專案相關聯。</span><span class="sxs-lookup"><span data-stu-id="dca8d-118">The control may set the **pszText** member to **NULL** to indicate that no text is associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="dca8d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dca8d-119">Requirements</span></span>



| <span data-ttu-id="dca8d-120">需求</span><span class="sxs-lookup"><span data-stu-id="dca8d-120">Requirement</span></span> | <span data-ttu-id="dca8d-121">值</span><span class="sxs-lookup"><span data-stu-id="dca8d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dca8d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dca8d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dca8d-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dca8d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dca8d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dca8d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dca8d-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dca8d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dca8d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="dca8d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dca8d-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dca8d-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="dca8d-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="dca8d-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dca8d-129">**TCM \_GETITEMW** (Unicode) 和 **TCM \_ GETITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="dca8d-129">**TCM\_GETITEMW** (Unicode) and **TCM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





