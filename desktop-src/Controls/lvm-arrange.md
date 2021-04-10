---
title: 'LVM_ARRANGE 訊息 (Commctrl .h) '
description: 在圖示視圖中排列專案。 您可以明確地傳送此訊息，或使用 ListView \_ 排列宏來傳送。
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- LVM_ARRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093859"
---
# <a name="lvm_arrange-message"></a><span data-ttu-id="59840-105">LVM \_ 排列訊息</span><span class="sxs-lookup"><span data-stu-id="59840-105">LVM\_ARRANGE message</span></span>

<span data-ttu-id="59840-106">在圖示視圖中排列專案。</span><span class="sxs-lookup"><span data-stu-id="59840-106">Arranges items in icon view.</span></span> <span data-ttu-id="59840-107">您可以明確地傳送此訊息，或使用 [**ListView \_ 排列**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="59840-107">You can send this message explicitly or by using the [**ListView\_Arrange**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="59840-108">參數</span><span class="sxs-lookup"><span data-stu-id="59840-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59840-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59840-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59840-110">下列其中一個值會指定對齊：</span><span class="sxs-lookup"><span data-stu-id="59840-110">One of the following values that specifies alignment:</span></span>



| <span data-ttu-id="59840-111">值</span><span class="sxs-lookup"><span data-stu-id="59840-111">Value</span></span>                                                                                                                                                            | <span data-ttu-id="59840-112">意義</span><span class="sxs-lookup"><span data-stu-id="59840-112">Meaning</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <span data-ttu-id="59840-113"><dt>**LVA \_ ALIGNLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="59840-113"><dt>**LVA\_ALIGNLEFT**</dt></span></span> </dl>    | <span data-ttu-id="59840-114">未實作。</span><span class="sxs-lookup"><span data-stu-id="59840-114">Not implemented.</span></span> <span data-ttu-id="59840-115">請改為套用 [**lvs) \_ ALIGNLEFT**](list-view-window-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="59840-115">Apply the [**LVS\_ALIGNLEFT**](list-view-window-styles.md) style instead.</span></span><br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <span data-ttu-id="59840-116"><dt>**LVA \_ ALIGNTOP**</dt></span><span class="sxs-lookup"><span data-stu-id="59840-116"><dt>**LVA\_ALIGNTOP**</dt></span></span> </dl>       | <span data-ttu-id="59840-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="59840-117">Not implemented.</span></span> <span data-ttu-id="59840-118">請改為套用 [**lvs) \_ ALIGNTOP**](list-view-window-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="59840-118">Apply the [**LVS\_ALIGNTOP**](list-view-window-styles.md) style instead.</span></span><br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <span data-ttu-id="59840-119"><dt>**LVA \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="59840-119"><dt>**LVA\_DEFAULT**</dt></span></span> </dl>          | <span data-ttu-id="59840-120">根據清單視圖控制項的目前對齊樣式來對齊專案 (預設值) 。</span><span class="sxs-lookup"><span data-stu-id="59840-120">Aligns items according to the list-view control's current alignment styles (the default value).</span></span><br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <span data-ttu-id="59840-121"><dt>**LVA \_ 格線**</dt></span><span class="sxs-lookup"><span data-stu-id="59840-121"><dt>**LVA\_SNAPTOGRID**</dt></span></span> </dl> | <span data-ttu-id="59840-122">將所有圖示貼齊最接近的方格位置。</span><span class="sxs-lookup"><span data-stu-id="59840-122">Snaps all icons to the nearest grid position.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="59840-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59840-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59840-124">必須為零。</span><span class="sxs-lookup"><span data-stu-id="59840-124">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59840-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="59840-125">Return value</span></span>

<span data-ttu-id="59840-126">如果成功，則傳回 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="59840-126">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="59840-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="59840-127">Requirements</span></span>



| <span data-ttu-id="59840-128">需求</span><span class="sxs-lookup"><span data-stu-id="59840-128">Requirement</span></span> | <span data-ttu-id="59840-129">值</span><span class="sxs-lookup"><span data-stu-id="59840-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59840-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59840-130">Minimum supported client</span></span><br/> | <span data-ttu-id="59840-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59840-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59840-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59840-132">Minimum supported server</span></span><br/> | <span data-ttu-id="59840-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59840-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59840-134">標頭</span><span class="sxs-lookup"><span data-stu-id="59840-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="59840-135"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="59840-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





