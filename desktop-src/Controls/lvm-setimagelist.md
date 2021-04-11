---
title: 'LVM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 將影像清單指派給清單視圖控制項。 您可以明確地傳送此訊息，或使用 ListView \_ SetImageList 宏來傳送。
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- LVM_SETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 779d31fd781a72dbdfbc4738e091482ca4a08528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933918"
---
# <a name="lvm_setimagelist-message"></a><span data-ttu-id="b6b9a-105">LVM \_ SETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="b6b9a-105">LVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="b6b9a-106">將影像清單指派給清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="b6b9a-106">Assigns an image list to a list-view control.</span></span> <span data-ttu-id="b6b9a-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="b6b9a-107">You can send this message explicitly or by using the [**ListView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6b9a-108">參數</span><span class="sxs-lookup"><span data-stu-id="b6b9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b9a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6b9a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b9a-110">影像清單的類型。</span><span class="sxs-lookup"><span data-stu-id="b6b9a-110">Type of image list.</span></span> <span data-ttu-id="b6b9a-111">這個參數可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="b6b9a-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="b6b9a-112">值</span><span class="sxs-lookup"><span data-stu-id="b6b9a-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="b6b9a-113">意義</span><span class="sxs-lookup"><span data-stu-id="b6b9a-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="b6b9a-114"><dt>**LVSIL \_ 正常**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9a-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="b6b9a-115">具有大型圖示的影像清單。</span><span class="sxs-lookup"><span data-stu-id="b6b9a-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="b6b9a-116"><dt>**LVSIL \_ SMALL**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9a-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="b6b9a-117">具有小圖示的影像清單。</span><span class="sxs-lookup"><span data-stu-id="b6b9a-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="b6b9a-118"><dt>**LVSIL \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9a-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="b6b9a-119">具有狀態影像的影像清單。</span><span class="sxs-lookup"><span data-stu-id="b6b9a-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="b6b9a-120"><dt>**LVSIL \_ GROUPHEADER**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9a-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="b6b9a-121">群組頁首的影像清單。</span><span class="sxs-lookup"><span data-stu-id="b6b9a-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="b6b9a-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6b9a-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b9a-123">要指派之影像清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b6b9a-123">Handle to the image list to assign.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b9a-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6b9a-124">Return value</span></span>

<span data-ttu-id="b6b9a-125">如果成功，則傳回與控制項相關聯之影像清單的控制碼; 否則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b6b9a-125">Returns the handle to the image list previously associated with the control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6b9a-126">備註</span><span class="sxs-lookup"><span data-stu-id="b6b9a-126">Remarks</span></span>

<span data-ttu-id="b6b9a-127">除非設定了 [**lvs) \_ SHAREIMAGELISTS**](list-view-window-styles.md) 樣式，否則當清單視圖控制項終結時，目前的影像清單將會終結。</span><span class="sxs-lookup"><span data-stu-id="b6b9a-127">The current image list will be destroyed when the list-view control is destroyed unless the [**LVS\_SHAREIMAGELISTS**](list-view-window-styles.md) style is set.</span></span> <span data-ttu-id="b6b9a-128">如果您使用此訊息將一個影像清單取代為另一個，則您的應用程式必須明確地終結目前以外的所有影像清單。</span><span class="sxs-lookup"><span data-stu-id="b6b9a-128">If you use this message to replace one image list with another, your application must explicitly destroy all image lists other than the current one.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6b9a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6b9a-129">Requirements</span></span>



| <span data-ttu-id="b6b9a-130">需求</span><span class="sxs-lookup"><span data-stu-id="b6b9a-130">Requirement</span></span> | <span data-ttu-id="b6b9a-131">值</span><span class="sxs-lookup"><span data-stu-id="b6b9a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b9a-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6b9a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b9a-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6b9a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6b9a-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6b9a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b9a-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6b9a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6b9a-136">標頭</span><span class="sxs-lookup"><span data-stu-id="b6b9a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6b9a-137"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6b9a-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





