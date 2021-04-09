---
title: 'HDM_GETITEMDROPDOWNRECT 訊息 (Commctrl .h) '
description: 取得具有樣式 HDF SPLITBUTTON 的標頭專案之分割按鈕的周框 \_ 。 明確地傳送此訊息，或使用標頭 \_ GetItemDropDownRect 宏。
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- HDM_GETITEMDROPDOWNRECT message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025128"
---
# <a name="hdm_getitemdropdownrect-message"></a><span data-ttu-id="ebf8a-105">HDM \_ GETITEMDROPDOWNRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="ebf8a-105">HDM\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="ebf8a-106">取得具有樣式 **HDF \_ SPLITBUTTON** 的標頭專案之分割按鈕的周框。</span><span class="sxs-lookup"><span data-stu-id="ebf8a-106">Gets the bounding rectangle of the split button for a header item with style **HDF\_SPLITBUTTON**.</span></span> <span data-ttu-id="ebf8a-107">明確地傳送此訊息，或使用 [**標頭 \_ GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) 宏。</span><span class="sxs-lookup"><span data-stu-id="ebf8a-107">Send this message explicitly or by using the [**Header\_GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebf8a-108">參數</span><span class="sxs-lookup"><span data-stu-id="ebf8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf8a-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ebf8a-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf8a-110">以零為基底的標頭控制項專案索引，為其取得周框矩形。</span><span class="sxs-lookup"><span data-stu-id="ebf8a-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ebf8a-111">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ebf8a-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf8a-112">[**矩形**](/windows/win32/api/windef/ns-windef-rect)的指標，此結構會接收周框的資訊。</span><span class="sxs-lookup"><span data-stu-id="ebf8a-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="ebf8a-113">訊息寄件者負責配置此結構。</span><span class="sxs-lookup"><span data-stu-id="ebf8a-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="ebf8a-114">在矩形結構中傳回的座標會以相對於標題控制項父系的方式表示。</span><span class="sxs-lookup"><span data-stu-id="ebf8a-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebf8a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebf8a-115">Return value</span></span>

<span data-ttu-id="ebf8a-116">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ebf8a-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf8a-117">備註</span><span class="sxs-lookup"><span data-stu-id="ebf8a-117">Remarks</span></span>

<span data-ttu-id="ebf8a-118">標頭專案必須具有 style **HDF \_ SPLITBUTTON**。</span><span class="sxs-lookup"><span data-stu-id="ebf8a-118">The header item must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf8a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebf8a-119">Requirements</span></span>



| <span data-ttu-id="ebf8a-120">需求</span><span class="sxs-lookup"><span data-stu-id="ebf8a-120">Requirement</span></span> | <span data-ttu-id="ebf8a-121">值</span><span class="sxs-lookup"><span data-stu-id="ebf8a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf8a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebf8a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf8a-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebf8a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ebf8a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebf8a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf8a-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebf8a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ebf8a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ebf8a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebf8a-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ebf8a-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebf8a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebf8a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf8a-129">關於標題控制項</span><span class="sxs-lookup"><span data-stu-id="ebf8a-129">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





