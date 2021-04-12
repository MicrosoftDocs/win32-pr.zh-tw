---
title: 'LVM_ENABLEGROUPVIEW 訊息 (Commctrl .h) '
description: 啟用或停用清單視圖控制項中的專案是否顯示為群組。
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- LVM_ENABLEGROUPVIEW message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024600"
---
# <a name="lvm_enablegroupview-message"></a><span data-ttu-id="cce9d-104">LVM \_ ENABLEGROUPVIEW 訊息</span><span class="sxs-lookup"><span data-stu-id="cce9d-104">LVM\_ENABLEGROUPVIEW message</span></span>

<span data-ttu-id="cce9d-105">啟用或停用清單視圖控制項中的專案是否顯示為群組。</span><span class="sxs-lookup"><span data-stu-id="cce9d-105">Enables or disables whether the items in a list-view control display as a group.</span></span>

## <a name="parameters"></a><span data-ttu-id="cce9d-106">參數</span><span class="sxs-lookup"><span data-stu-id="cce9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cce9d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cce9d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cce9d-108">**布林** 值，指出是否要啟用清單視圖控制項來群組顯示的專案。</span><span class="sxs-lookup"><span data-stu-id="cce9d-108">A **BOOL** that indicates whether to enable a list-view control to group displayed items.</span></span> <span data-ttu-id="cce9d-109">使用 **TRUE** 可啟用群組， **FALSE** 則會停用。</span><span class="sxs-lookup"><span data-stu-id="cce9d-109">Use **TRUE** to enable grouping, **FALSE** to disable it.</span></span> </dd> <dt>

<span data-ttu-id="cce9d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cce9d-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cce9d-111">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cce9d-111">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cce9d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cce9d-112">Return value</span></span>

<span data-ttu-id="cce9d-113">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cce9d-113">Returns one of the following values.</span></span>



| <span data-ttu-id="cce9d-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cce9d-114">Return code</span></span>                                                                       | <span data-ttu-id="cce9d-115">Description</span><span class="sxs-lookup"><span data-stu-id="cce9d-115">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cce9d-116"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="cce9d-116"><dt>**0**</dt></span></span> </dl>  | <span data-ttu-id="cce9d-117">將清單視圖專案顯示為群組的功能已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="cce9d-117">The ability to display list-view items as a group is already enabled or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="cce9d-118"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="cce9d-118"><dt>**1**</dt></span></span> </dl>  | <span data-ttu-id="cce9d-119">已成功變更控制項的狀態。</span><span class="sxs-lookup"><span data-stu-id="cce9d-119">The state of the control was successfully changed.</span></span><br/>                                |
| <dl> <span data-ttu-id="cce9d-120"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="cce9d-120"><dt>**-1**</dt></span></span> </dl> | <span data-ttu-id="cce9d-121">作業失敗。</span><span class="sxs-lookup"><span data-stu-id="cce9d-121">The operation failed.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="cce9d-122">備註</span><span class="sxs-lookup"><span data-stu-id="cce9d-122">Remarks</span></span>

<span data-ttu-id="cce9d-123">**LVM \_** [**Lvs) \_ OWNERDATA**](list-view-window-styles.md)樣式下不支援 ENABLEGROUPVIEW。</span><span class="sxs-lookup"><span data-stu-id="cce9d-123">**LVM\_ENABLEGROUPVIEW** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="cce9d-124">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="cce9d-124">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="cce9d-125">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="cce9d-125">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cce9d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="cce9d-126">Requirements</span></span>



| <span data-ttu-id="cce9d-127">需求</span><span class="sxs-lookup"><span data-stu-id="cce9d-127">Requirement</span></span> | <span data-ttu-id="cce9d-128">值</span><span class="sxs-lookup"><span data-stu-id="cce9d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cce9d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cce9d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cce9d-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cce9d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cce9d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cce9d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cce9d-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cce9d-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cce9d-133">標頭</span><span class="sxs-lookup"><span data-stu-id="cce9d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cce9d-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cce9d-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





