---
title: 'LVM_INSERTGROUP 訊息 (Commctrl .h) '
description: 將群組插入清單視圖控制項。
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- LVM_INSERTGROUP message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dbae780f7de26a5c791477e1a7321794054056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996186"
---
# <a name="lvm_insertgroup-message"></a><span data-ttu-id="45942-104">LVM \_ INSERTGROUP 訊息</span><span class="sxs-lookup"><span data-stu-id="45942-104">LVM\_INSERTGROUP message</span></span>

<span data-ttu-id="45942-105">將群組插入清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="45942-105">Inserts a group into a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="45942-106">參數</span><span class="sxs-lookup"><span data-stu-id="45942-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45942-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45942-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="45942-108">要加入群組的索引。</span><span class="sxs-lookup"><span data-stu-id="45942-108">Index where the group is to be added.</span></span> <span data-ttu-id="45942-109">如果這是-1，則會將群組新增至清單結尾。</span><span class="sxs-lookup"><span data-stu-id="45942-109">If this is -1, the group is added at the end of the list.</span></span></dd> <dt>

<span data-ttu-id="45942-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45942-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="45942-111"><a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a>結構的指標，其中包含要加入的群組。</span><span class="sxs-lookup"><span data-stu-id="45942-111">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that contains the group to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45942-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="45942-112">Return value</span></span>

<span data-ttu-id="45942-113">傳回群組已加入之專案的索引，如果作業失敗，則為-1。</span><span class="sxs-lookup"><span data-stu-id="45942-113">Returns the index of the item that the group was added to, or -1 if the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="45942-114">備註</span><span class="sxs-lookup"><span data-stu-id="45942-114">Remarks</span></span>

<span data-ttu-id="45942-115">若要開啟群組模式，請呼叫 [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) 或 [**ListView \_ ENABLEGROUPVIEW**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview)。</span><span class="sxs-lookup"><span data-stu-id="45942-115">To turn on group mode, call [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) or [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span></span>

<span data-ttu-id="45942-116">無法將群組插入空白的清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="45942-116">A group cannot be inserted into an empty list-view control.</span></span>

<span data-ttu-id="45942-117">請務必在新增群組 () 的專案中設定 **iGroupId** 。</span><span class="sxs-lookup"><span data-stu-id="45942-117">Be sure to set the **iGroupId** in the item(s) the group was added to.</span></span> <span data-ttu-id="45942-118">否則，當 [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) 訊息處理為 **TRUE** 時，listview 控制項將不會顯示任何專案。</span><span class="sxs-lookup"><span data-stu-id="45942-118">Otherwise after [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) message processing with **TRUE** the listview control will not show any items.</span></span>

> [!Note]  
> <span data-ttu-id="45942-119">若要使用此訊息，您必須提供指定 Comclt32 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="45942-119">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="45942-120">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="45942-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="45942-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="45942-121">Requirements</span></span>



| <span data-ttu-id="45942-122">需求</span><span class="sxs-lookup"><span data-stu-id="45942-122">Requirement</span></span> | <span data-ttu-id="45942-123">值</span><span class="sxs-lookup"><span data-stu-id="45942-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45942-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45942-124">Minimum supported client</span></span><br/> | <span data-ttu-id="45942-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45942-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="45942-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45942-126">Minimum supported server</span></span><br/> | <span data-ttu-id="45942-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45942-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45942-128">標頭</span><span class="sxs-lookup"><span data-stu-id="45942-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="45942-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="45942-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





