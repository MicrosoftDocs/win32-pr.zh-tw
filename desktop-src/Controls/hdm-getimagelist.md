---
title: 'HDM_GETIMAGELIST 訊息 (Commctrl .h) '
description: 取得已針對現有標題控制項設定之影像清單的控制碼。 您可以明確地傳送此訊息，或使用標頭 \_ GetImageList 或標頭 \_ GetStateImageList 宏。
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- HDM_GETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686102"
---
# <a name="hdm_getimagelist-message"></a><span data-ttu-id="36dae-105">HDM \_ GETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="36dae-105">HDM\_GETIMAGELIST message</span></span>

<span data-ttu-id="36dae-106">取得已針對現有標題控制項設定之影像清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="36dae-106">Gets the handle to the image list that has been set for an existing header control.</span></span> <span data-ttu-id="36dae-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) 或 [**標頭 \_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) 宏。</span><span class="sxs-lookup"><span data-stu-id="36dae-107">You can send this message explicitly or use the [**Header\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) or [**Header\_GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="36dae-108">參數</span><span class="sxs-lookup"><span data-stu-id="36dae-108">Parameters</span></span>

<dl> <span data-ttu-id="36dae-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="36dae-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="36dae-110">下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="36dae-110">One of the following values:</span></span>

| <span data-ttu-id="36dae-111">值</span><span class="sxs-lookup"><span data-stu-id="36dae-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="36dae-112">意義</span><span class="sxs-lookup"><span data-stu-id="36dae-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="36dae-113"><dt>**HDSIL \_ 正常**</dt></span><span class="sxs-lookup"><span data-stu-id="36dae-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="36dae-114">表示這是一般的影像清單。</span><span class="sxs-lookup"><span data-stu-id="36dae-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="36dae-115"><dt>**HDSIL \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="36dae-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="36dae-116">表示這是狀態影像清單。</span><span class="sxs-lookup"><span data-stu-id="36dae-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="36dae-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36dae-117">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="36dae-118">必須為零。</span><span class="sxs-lookup"><span data-stu-id="36dae-118">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36dae-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="36dae-119">Return value</span></span>

<span data-ttu-id="36dae-120">傳回標題控制項之影像清單集的控制碼。</span><span class="sxs-lookup"><span data-stu-id="36dae-120">Returns a handle to the image list set for the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="36dae-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="36dae-121">Requirements</span></span>



| <span data-ttu-id="36dae-122">需求</span><span class="sxs-lookup"><span data-stu-id="36dae-122">Requirement</span></span> | <span data-ttu-id="36dae-123">值</span><span class="sxs-lookup"><span data-stu-id="36dae-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36dae-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36dae-124">Minimum supported client</span></span><br/> | <span data-ttu-id="36dae-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36dae-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36dae-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36dae-126">Minimum supported server</span></span><br/> | <span data-ttu-id="36dae-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36dae-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36dae-128">標頭</span><span class="sxs-lookup"><span data-stu-id="36dae-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="36dae-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="36dae-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





