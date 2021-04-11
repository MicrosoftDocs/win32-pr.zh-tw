---
title: 'LVM_GETIMAGELIST 訊息 (Commctrl .h) '
description: 抓取用來繪製清單視圖專案的影像清單控制碼。 您可以明確地傳送此訊息，或使用 ListView \_ GetImageList 宏來傳送。
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- LVM_GETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104453"
---
# <a name="lvm_getimagelist-message"></a><span data-ttu-id="6321d-105">LVM \_ GETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="6321d-105">LVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="6321d-106">抓取用來繪製清單視圖專案的影像清單控制碼。</span><span class="sxs-lookup"><span data-stu-id="6321d-106">Retrieves the handle to an image list used for drawing list-view items.</span></span> <span data-ttu-id="6321d-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="6321d-107">You can send this message explicitly or by using the [**ListView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6321d-108">參數</span><span class="sxs-lookup"><span data-stu-id="6321d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6321d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6321d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6321d-110">要取出的影像清單。</span><span class="sxs-lookup"><span data-stu-id="6321d-110">Image list to retrieve.</span></span> <span data-ttu-id="6321d-111">這個參數可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="6321d-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="6321d-112">值</span><span class="sxs-lookup"><span data-stu-id="6321d-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="6321d-113">意義</span><span class="sxs-lookup"><span data-stu-id="6321d-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="6321d-114"><dt>**LVSIL \_ 正常**</dt></span><span class="sxs-lookup"><span data-stu-id="6321d-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="6321d-115">具有大型圖示的影像清單。</span><span class="sxs-lookup"><span data-stu-id="6321d-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="6321d-116"><dt>**LVSIL \_ SMALL**</dt></span><span class="sxs-lookup"><span data-stu-id="6321d-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="6321d-117">具有小圖示的影像清單。</span><span class="sxs-lookup"><span data-stu-id="6321d-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="6321d-118"><dt>**LVSIL \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="6321d-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="6321d-119">具有狀態影像的影像清單。</span><span class="sxs-lookup"><span data-stu-id="6321d-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="6321d-120"><dt>**LVSIL \_ GROUPHEADER**</dt></span><span class="sxs-lookup"><span data-stu-id="6321d-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="6321d-121">群組頁首的影像清單。</span><span class="sxs-lookup"><span data-stu-id="6321d-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="6321d-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6321d-122">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6321d-123">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6321d-123">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6321d-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="6321d-124">Return value</span></span>

<span data-ttu-id="6321d-125">如果成功，則傳回指定之影像清單的控制碼，否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="6321d-125">Returns the handle to the specified image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6321d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="6321d-126">Requirements</span></span>



| <span data-ttu-id="6321d-127">需求</span><span class="sxs-lookup"><span data-stu-id="6321d-127">Requirement</span></span> | <span data-ttu-id="6321d-128">值</span><span class="sxs-lookup"><span data-stu-id="6321d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6321d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6321d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6321d-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6321d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6321d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6321d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6321d-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6321d-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6321d-133">標頭</span><span class="sxs-lookup"><span data-stu-id="6321d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6321d-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6321d-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





