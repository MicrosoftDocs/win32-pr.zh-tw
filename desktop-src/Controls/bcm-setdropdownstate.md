---
title: 'BCM_SETDROPDOWNSTATE 訊息 (Commctrl .h) '
description: 設定具有樣式 TBSTYLE 下拉式清單之按鈕的下拉式狀態 \_ 。 明確地傳送此訊息，或使用按鈕 \_ SetDropDownState 宏。
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- BCM_SETDROPDOWNSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094583"
---
# <a name="bcm_setdropdownstate-message"></a><span data-ttu-id="21e03-105">BCM \_ SETDROPDOWNSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="21e03-105">BCM\_SETDROPDOWNSTATE message</span></span>

<span data-ttu-id="21e03-106">設定具有樣式 [**TBSTYLE 下拉式 \_ 清單**](toolbar-control-and-button-styles.md)之按鈕的下拉式狀態。</span><span class="sxs-lookup"><span data-stu-id="21e03-106">Sets the drop down state for a button with style [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span> <span data-ttu-id="21e03-107">明確地傳送此訊息，或使用 [**按鈕 \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) 宏。</span><span class="sxs-lookup"><span data-stu-id="21e03-107">Send this message explicitly or by using the [**Button\_SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="21e03-108">參數</span><span class="sxs-lookup"><span data-stu-id="21e03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21e03-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21e03-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e03-110">適用于 BST DROPDOWNPUSHED 狀態的 **布林\*\*\*\*值為 TRUE** \_ ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="21e03-110">A **BOOL** that is **TRUE** for state of BST\_DROPDOWNPUSHED, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="21e03-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21e03-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21e03-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="21e03-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21e03-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="21e03-113">Return value</span></span>

<span data-ttu-id="21e03-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="21e03-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="21e03-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="21e03-115">Requirements</span></span>



| <span data-ttu-id="21e03-116">需求</span><span class="sxs-lookup"><span data-stu-id="21e03-116">Requirement</span></span> | <span data-ttu-id="21e03-117">值</span><span class="sxs-lookup"><span data-stu-id="21e03-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21e03-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21e03-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21e03-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21e03-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21e03-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21e03-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21e03-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21e03-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21e03-122">標頭</span><span class="sxs-lookup"><span data-stu-id="21e03-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="21e03-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="21e03-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21e03-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21e03-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="21e03-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="21e03-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="21e03-126">按鈕樣式</span><span class="sxs-lookup"><span data-stu-id="21e03-126">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="21e03-127">**概念**</span><span class="sxs-lookup"><span data-stu-id="21e03-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="21e03-128">按鈕類型</span><span class="sxs-lookup"><span data-stu-id="21e03-128">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





