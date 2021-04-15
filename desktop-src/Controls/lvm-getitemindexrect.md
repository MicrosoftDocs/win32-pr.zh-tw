---
title: 'LVM_GETITEMINDEXRECT 訊息 (Commctrl .h) '
description: 在清單視圖控制項的目前視圖中，抓取所有或部分子部分的周框。 明確地傳送此訊息，或使用 ListView \_ GetItemIndexRect 宏。
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- LVM_GETITEMINDEXRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466512"
---
# <a name="lvm_getitemindexrect-message"></a><span data-ttu-id="8ecea-105">LVM \_ GETITEMINDEXRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="8ecea-105">LVM\_GETITEMINDEXRECT message</span></span>

<span data-ttu-id="8ecea-106">在清單視圖控制項的目前視圖中，抓取所有或部分子部分的周框。</span><span class="sxs-lookup"><span data-stu-id="8ecea-106">Retrieves the bounding rectangle for all or part of a subitem in the current view of a list-view control.</span></span> <span data-ttu-id="8ecea-107">明確地傳送此訊息，或使用 [**ListView \_ GetItemIndexRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) 宏。</span><span class="sxs-lookup"><span data-stu-id="8ecea-107">Send this message explicitly or by using the [**ListView\_GetItemIndexRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ecea-108">參數</span><span class="sxs-lookup"><span data-stu-id="8ecea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ecea-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ecea-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ecea-110">子專案父專案的 [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="8ecea-110">A pointer to a [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the parent item of the subitem.</span></span> <span data-ttu-id="8ecea-111">呼叫進程負責配置此結構並設定其成員。</span><span class="sxs-lookup"><span data-stu-id="8ecea-111">The calling process is responsible for allocating this structure and setting its members.</span></span> <span data-ttu-id="8ecea-112">*wParam* 不得為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8ecea-112">*wParam* must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8ecea-113">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8ecea-113">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ecea-114">要接收座標的 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="8ecea-114">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="8ecea-115">呼叫進程負責配置此結構。</span><span class="sxs-lookup"><span data-stu-id="8ecea-115">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="8ecea-116">*lParam* 不得為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8ecea-116">*lParam* must not be **NULL**.</span></span> <span data-ttu-id="8ecea-117">將 **最上層** 成員設為子工作的索引。</span><span class="sxs-lookup"><span data-stu-id="8ecea-117">Set the **top** member to the index of the subitem.</span></span> <span data-ttu-id="8ecea-118">將 **左邊** 的成員設定為下列其中一個值，表示要抓取周框的子部分。</span><span class="sxs-lookup"><span data-stu-id="8ecea-118">Set the **left** member to one of the following values, indicating the part of the subitem for which the bounding rectangle is to be retrieved.</span></span>



| <span data-ttu-id="8ecea-119">值</span><span class="sxs-lookup"><span data-stu-id="8ecea-119">Value</span></span>                                                                                                                                                   | <span data-ttu-id="8ecea-120">意義</span><span class="sxs-lookup"><span data-stu-id="8ecea-120">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="8ecea-121"><dt>**LVIR \_ 界限**</dt></span><span class="sxs-lookup"><span data-stu-id="8ecea-121"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl> | <span data-ttu-id="8ecea-122">傳回整個子工作的周框，包括圖示和標籤。</span><span class="sxs-lookup"><span data-stu-id="8ecea-122">Returns the bounding rectangle of the entire subitem, including the icon and label.</span></span><br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="8ecea-123"><dt>**LVIR \_ 圖示**</dt></span><span class="sxs-lookup"><span data-stu-id="8ecea-123"><dt>**LVIR\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="8ecea-124">傳回子工作圖示或小圖示的周框。</span><span class="sxs-lookup"><span data-stu-id="8ecea-124">Returns the bounding rectangle of the icon or small icon of the subitem.</span></span><br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="8ecea-125"><dt>**LVIR \_ 標籤**</dt></span><span class="sxs-lookup"><span data-stu-id="8ecea-125"><dt>**LVIR\_LABEL**</dt></span></span> </dl>    | <span data-ttu-id="8ecea-126">傳回子文字的周框。</span><span class="sxs-lookup"><span data-stu-id="8ecea-126">Returns the bounding rectangle of the subitem text.</span></span><br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ecea-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ecea-127">Return value</span></span>

<span data-ttu-id="8ecea-128">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8ecea-128">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ecea-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ecea-129">Requirements</span></span>



| <span data-ttu-id="8ecea-130">需求</span><span class="sxs-lookup"><span data-stu-id="8ecea-130">Requirement</span></span> | <span data-ttu-id="8ecea-131">值</span><span class="sxs-lookup"><span data-stu-id="8ecea-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ecea-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ecea-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8ecea-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ecea-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ecea-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ecea-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8ecea-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ecea-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ecea-136">標頭</span><span class="sxs-lookup"><span data-stu-id="8ecea-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ecea-137"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ecea-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

