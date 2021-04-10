---
title: 'LVM_GETITEMRECT 訊息 (Commctrl .h) '
description: 抓取目前視圖中所有或部分專案的周框。 您可以明確地傳送此訊息，或使用 ListView \_ GetItemRect 宏來傳送。
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- LVM_GETITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025378"
---
# <a name="lvm_getitemrect-message"></a><span data-ttu-id="1e5c6-105">LVM \_ GETITEMRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="1e5c6-105">LVM\_GETITEMRECT message</span></span>

<span data-ttu-id="1e5c6-106">抓取目前視圖中所有或部分專案的周框。</span><span class="sxs-lookup"><span data-stu-id="1e5c6-106">Retrieves the bounding rectangle for all or part of an item in the current view.</span></span> <span data-ttu-id="1e5c6-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="1e5c6-107">You can send this message explicitly or by using the [**ListView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e5c6-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e5c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e5c6-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e5c6-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e5c6-110">清單視圖專案的索引。</span><span class="sxs-lookup"><span data-stu-id="1e5c6-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="1e5c6-111">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1e5c6-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e5c6-112">接收周框 [**的矩形結構指標**](/previous-versions//dd162897(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="1e5c6-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="1e5c6-113">傳送訊息時，會使用此結構的 **左側** 成員來指定清單視圖專案的部分，以從中取出周框。</span><span class="sxs-lookup"><span data-stu-id="1e5c6-113">When the message is sent, the **left** member of this structure is used to specify the portion of the list-view item from which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="1e5c6-114">它必須設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="1e5c6-114">It must be set to one of the following values:</span></span>



| <span data-ttu-id="1e5c6-115">值</span><span class="sxs-lookup"><span data-stu-id="1e5c6-115">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="1e5c6-116">意義</span><span class="sxs-lookup"><span data-stu-id="1e5c6-116">Meaning</span></span>                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="1e5c6-117"><dt>**LVIR \_ 界限**</dt></span><span class="sxs-lookup"><span data-stu-id="1e5c6-117"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl>                   | <span data-ttu-id="1e5c6-118">傳回整個專案的周框，包括圖示和標籤。</span><span class="sxs-lookup"><span data-stu-id="1e5c6-118">Returns the bounding rectangle of the entire item, including the icon and label.</span></span><br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="1e5c6-119"><dt>**LVIR \_ 圖示**</dt></span><span class="sxs-lookup"><span data-stu-id="1e5c6-119"><dt>**LVIR\_ICON**</dt></span></span> </dl>                         | <span data-ttu-id="1e5c6-120">傳回圖示或小圖示的周框。</span><span class="sxs-lookup"><span data-stu-id="1e5c6-120">Returns the bounding rectangle of the icon or small icon.</span></span><br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="1e5c6-121"><dt>**LVIR \_ 標籤**</dt></span><span class="sxs-lookup"><span data-stu-id="1e5c6-121"><dt>**LVIR\_LABEL**</dt></span></span> </dl>                      | <span data-ttu-id="1e5c6-122">傳回專案文字的周框。</span><span class="sxs-lookup"><span data-stu-id="1e5c6-122">Returns the bounding rectangle of the item text.</span></span><br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <span data-ttu-id="1e5c6-123"><dt>**LVIR \_ SELECTBOUNDS**</dt></span><span class="sxs-lookup"><span data-stu-id="1e5c6-123"><dt>**LVIR\_SELECTBOUNDS**</dt></span></span> </dl> | <span data-ttu-id="1e5c6-124">傳回 LVIR \_ 圖示和 LVIR \_ 標籤矩形的聯集，但在報表檢視中排除資料行。</span><span class="sxs-lookup"><span data-stu-id="1e5c6-124">Returns the union of the LVIR\_ICON and LVIR\_LABEL rectangles, but excludes columns in report view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e5c6-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e5c6-125">Return value</span></span>

<span data-ttu-id="1e5c6-126">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1e5c6-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e5c6-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e5c6-127">Requirements</span></span>



| <span data-ttu-id="1e5c6-128">需求</span><span class="sxs-lookup"><span data-stu-id="1e5c6-128">Requirement</span></span> | <span data-ttu-id="1e5c6-129">值</span><span class="sxs-lookup"><span data-stu-id="1e5c6-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5c6-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e5c6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1e5c6-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e5c6-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e5c6-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e5c6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1e5c6-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e5c6-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e5c6-134">標頭</span><span class="sxs-lookup"><span data-stu-id="1e5c6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e5c6-135"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e5c6-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

