---
title: 'LVM_GETGROUPRECT 訊息 (Commctrl .h) '
description: 取得指定群組的矩形。 明確地傳送此訊息，或使用 ListView \_ GetGroupRect 宏。
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- LVM_GETGROUPRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2cbdfb1ec6e670e7b5d333694f3a1ca56d287b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933961"
---
# <a name="lvm_getgrouprect-message"></a><span data-ttu-id="44d98-105">LVM \_ GETGROUPRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="44d98-105">LVM\_GETGROUPRECT message</span></span>

<span data-ttu-id="44d98-106">取得指定群組的矩形。</span><span class="sxs-lookup"><span data-stu-id="44d98-106">Gets the rectangle for a specified group.</span></span> <span data-ttu-id="44d98-107">明確地傳送此訊息，或使用 [**ListView \_ GetGroupRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) 宏。</span><span class="sxs-lookup"><span data-stu-id="44d98-107">Send this message explicitly or by using the [**ListView\_GetGroupRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="44d98-108">參數</span><span class="sxs-lookup"><span data-stu-id="44d98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d98-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44d98-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d98-110">指定 group by **iGroupId** (參閱 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) 結構) 。</span><span class="sxs-lookup"><span data-stu-id="44d98-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="44d98-111">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="44d98-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="44d98-112">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，用來接收 *wParam* 所指定之群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="44d98-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="44d98-113">訊息接收者負責為結構成員設定 *wParam* 所指定之群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="44d98-113">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

<span data-ttu-id="44d98-114">呼叫進程負責為結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="44d98-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="44d98-115">將矩形的 **頂端** 成員設定 [**為下列**](/previous-versions//dd162897(v=vs.85)) 其中一個旗標，以指定要取得的矩形座標。</span><span class="sxs-lookup"><span data-stu-id="44d98-115">Set the **top** member of the [**RECT**](/previous-versions//dd162897(v=vs.85)) to one of the following flags to specify the coordinates of the rectangle to get.</span></span>



| <span data-ttu-id="44d98-116">值</span><span class="sxs-lookup"><span data-stu-id="44d98-116">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="44d98-117">意義</span><span class="sxs-lookup"><span data-stu-id="44d98-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <span data-ttu-id="44d98-118"><dt>**LVGGR \_ 群組**</dt></span><span class="sxs-lookup"><span data-stu-id="44d98-118"><dt>**LVGGR\_GROUP**</dt></span></span> </dl>                | <span data-ttu-id="44d98-119">整個展開群組的座標。</span><span class="sxs-lookup"><span data-stu-id="44d98-119">Coordinates of the entire expanded group.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <span data-ttu-id="44d98-120"><dt>**LVGGR \_ 標頭**</dt></span><span class="sxs-lookup"><span data-stu-id="44d98-120"><dt>**LVGGR\_HEADER**</dt></span></span> </dl>             | <span data-ttu-id="44d98-121">僅 (折迭的群組) 的標頭座標。</span><span class="sxs-lookup"><span data-stu-id="44d98-121">Coordinates of the header only (collapsed group).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <span data-ttu-id="44d98-122"><dt>**LVGGR \_ 標籤**</dt></span><span class="sxs-lookup"><span data-stu-id="44d98-122"><dt>**LVGGR\_LABEL**</dt></span></span> </dl>                | <span data-ttu-id="44d98-123">標籤的座標。</span><span class="sxs-lookup"><span data-stu-id="44d98-123">Coordinates of the label only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <span data-ttu-id="44d98-124"><dt>**LVGGR \_ SUBSETLINK**</dt></span><span class="sxs-lookup"><span data-stu-id="44d98-124"><dt>**LVGGR\_SUBSETLINK**</dt></span></span> </dl> | <span data-ttu-id="44d98-125">子集連結的座標只 (標記子集) 。</span><span class="sxs-lookup"><span data-stu-id="44d98-125">Coordinates of the subset link only (markup subset).</span></span> <span data-ttu-id="44d98-126">清單視圖控制項可以限制每個群組中顯示的可見專案數目。</span><span class="sxs-lookup"><span data-stu-id="44d98-126">A list-view control can limit the number of visible items displayed in each group.</span></span> <span data-ttu-id="44d98-127">使用者會看到連結，讓使用者可以展開群組。</span><span class="sxs-lookup"><span data-stu-id="44d98-127">A link is presented to the user to allow the user to expand the group.</span></span> <span data-ttu-id="44d98-128">如果群組是 LVGS SUBSETED 的子集 (群組狀態，此旗標將會傳回子集連結的周框 \_ ，請參閱結構 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)、成員 **狀態**) 。</span><span class="sxs-lookup"><span data-stu-id="44d98-128">This flag will return the bounding rectangle of the subset link if the group is a subset (group state of LVGS\_SUBSETED, see structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), member **state**).</span></span> <span data-ttu-id="44d98-129">提供此旗標，讓協助工具應用程式可以找到連結。</span><span class="sxs-lookup"><span data-stu-id="44d98-129">This flag is provided so that accessibility applications can located the link.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d98-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="44d98-130">Return value</span></span>

<span data-ttu-id="44d98-131">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="44d98-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d98-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="44d98-132">Requirements</span></span>



| <span data-ttu-id="44d98-133">需求</span><span class="sxs-lookup"><span data-stu-id="44d98-133">Requirement</span></span> | <span data-ttu-id="44d98-134">值</span><span class="sxs-lookup"><span data-stu-id="44d98-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44d98-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44d98-135">Minimum supported client</span></span><br/> | <span data-ttu-id="44d98-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44d98-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44d98-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44d98-137">Minimum supported server</span></span><br/> | <span data-ttu-id="44d98-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44d98-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44d98-139">標頭</span><span class="sxs-lookup"><span data-stu-id="44d98-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="44d98-140"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="44d98-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

