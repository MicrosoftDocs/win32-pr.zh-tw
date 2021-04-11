---
title: 'LVM_GETSUBITEMRECT 訊息 (Commctrl .h) '
description: 針對清單視圖控制項中的子工作，取得周框矩形的相關資訊。
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- LVM_GETSUBITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105491"
---
# <a name="lvm_getsubitemrect-message"></a><span data-ttu-id="56b25-104">LVM \_ GETSUBITEMRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="56b25-104">LVM\_GETSUBITEMRECT message</span></span>

<span data-ttu-id="56b25-105">針對清單視圖控制項中的子工作，取得周框矩形的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="56b25-105">Retrieves information about the bounding rectangle for a subitem in a list-view control.</span></span> <span data-ttu-id="56b25-106">您可以明確地傳送此訊息，或使用 [**ListView \_ GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) 宏 (建議的) 。</span><span class="sxs-lookup"><span data-stu-id="56b25-106">You can send this message explicitly or by using the [**ListView\_GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) macro (recommended).</span></span> <span data-ttu-id="56b25-107">此訊息僅供使用 [**lvs) \_ 報表**](list-view-window-styles.md) 樣式的清單視圖控制項使用。</span><span class="sxs-lookup"><span data-stu-id="56b25-107">This message is intended to be used only with list-view controls that use the [**LVS\_REPORT**](list-view-window-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="56b25-108">參數</span><span class="sxs-lookup"><span data-stu-id="56b25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56b25-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56b25-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56b25-110">子專案父專案的索引。</span><span class="sxs-lookup"><span data-stu-id="56b25-110">Index of the subitem's parent item.</span></span>

</dd> <dt>

<span data-ttu-id="56b25-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56b25-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56b25-112">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收子內容周框的資訊。</span><span class="sxs-lookup"><span data-stu-id="56b25-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the subitem bounding rectangle information.</span></span> <span data-ttu-id="56b25-113">其成員必須根據下列成員/值關聯性進行初始化：</span><span class="sxs-lookup"><span data-stu-id="56b25-113">Its members must be initialized according to the following member/value relationships:</span></span>



| <span data-ttu-id="56b25-114">值</span><span class="sxs-lookup"><span data-stu-id="56b25-114">Value</span></span>                                                                                                                             | <span data-ttu-id="56b25-115">意義</span><span class="sxs-lookup"><span data-stu-id="56b25-115">Meaning</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="56b25-116"><dt>**top**</dt></span><span class="sxs-lookup"><span data-stu-id="56b25-116"><dt>**top**</dt></span></span> </dl>    | <span data-ttu-id="56b25-117">子索引的以一為基礎的索引。</span><span class="sxs-lookup"><span data-stu-id="56b25-117">The one-based index of the subitem.</span></span><br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="56b25-118"><dt>**離開**</dt></span><span class="sxs-lookup"><span data-stu-id="56b25-118"><dt>**left**</dt></span></span> </dl> | <span data-ttu-id="56b25-119">旗標值 (查看備註) 。</span><span class="sxs-lookup"><span data-stu-id="56b25-119">Flag value (see remarks).</span></span> <span data-ttu-id="56b25-120">表示要取得周框矩形的清單-view 子下拉式清單部分。</span><span class="sxs-lookup"><span data-stu-id="56b25-120">Indicates the portion of the list-view subitem for which to retrieve the bounding rectangle.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56b25-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="56b25-121">Return value</span></span>

<span data-ttu-id="56b25-122">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="56b25-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="56b25-123">備註</span><span class="sxs-lookup"><span data-stu-id="56b25-123">Remarks</span></span>

<span data-ttu-id="56b25-124">以下是可以設定的旗標值。</span><span class="sxs-lookup"><span data-stu-id="56b25-124">Following are the flag values that may be set.</span></span>



| <span data-ttu-id="56b25-125">需求</span><span class="sxs-lookup"><span data-stu-id="56b25-125">Requirement</span></span> | <span data-ttu-id="56b25-126">值</span><span class="sxs-lookup"><span data-stu-id="56b25-126">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56b25-127">**旗標值**</span><span class="sxs-lookup"><span data-stu-id="56b25-127">**Flag Value**</span></span> | <span data-ttu-id="56b25-128">**意義**</span><span class="sxs-lookup"><span data-stu-id="56b25-128">**Meaning**</span></span>                                                                                                         |
| <span data-ttu-id="56b25-129">LVIR \_ 界限</span><span class="sxs-lookup"><span data-stu-id="56b25-129">LVIR\_BOUNDS</span></span>   | <span data-ttu-id="56b25-130">傳回整個專案的周框，包括圖示和標籤。</span><span class="sxs-lookup"><span data-stu-id="56b25-130">Returns the bounding rectangle of the entire item, including the icon and label.</span></span>                                    |
| <span data-ttu-id="56b25-131">LVIR \_ 圖示</span><span class="sxs-lookup"><span data-stu-id="56b25-131">LVIR\_ICON</span></span>     | <span data-ttu-id="56b25-132">傳回圖示或小圖示的周框。</span><span class="sxs-lookup"><span data-stu-id="56b25-132">Returns the bounding rectangle of the icon or small icon.</span></span>                                                           |
| <span data-ttu-id="56b25-133">LVIR \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="56b25-133">LVIR\_LABEL</span></span>    | <span data-ttu-id="56b25-134">傳回整個專案的周框，包括圖示和標籤。</span><span class="sxs-lookup"><span data-stu-id="56b25-134">Returns the bounding rectangle of the entire item, including the icon and label.</span></span> <span data-ttu-id="56b25-135">這與 LVIR 界限相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="56b25-135">This is identical to LVIR\_BOUNDS.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="56b25-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="56b25-136">Requirements</span></span>



| <span data-ttu-id="56b25-137">需求</span><span class="sxs-lookup"><span data-stu-id="56b25-137">Requirement</span></span> | <span data-ttu-id="56b25-138">值</span><span class="sxs-lookup"><span data-stu-id="56b25-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56b25-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56b25-139">Minimum supported client</span></span><br/> | <span data-ttu-id="56b25-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56b25-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56b25-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56b25-141">Minimum supported server</span></span><br/> | <span data-ttu-id="56b25-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56b25-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56b25-143">標頭</span><span class="sxs-lookup"><span data-stu-id="56b25-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="56b25-144"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="56b25-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

