---
title: 'HDM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 將影像清單指派給現有的標題控制項。 您可以明確地傳送此訊息，或使用標頭 \_ SetImageList 或標頭 \_ SetStateImageList 宏。
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934317"
---
# <a name="hdm_setimagelist-message"></a><span data-ttu-id="3102c-105">HDM \_ SETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="3102c-105">HDM\_SETIMAGELIST message</span></span>

<span data-ttu-id="3102c-106">將影像清單指派給現有的標題控制項。</span><span class="sxs-lookup"><span data-stu-id="3102c-106">Assigns an image list to an existing header control.</span></span> <span data-ttu-id="3102c-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) 或 [**標頭 \_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) 宏。</span><span class="sxs-lookup"><span data-stu-id="3102c-107">You can send this message explicitly or use the [**Header\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) or [**Header\_SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3102c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3102c-108">Parameters</span></span>

<dl> <span data-ttu-id="3102c-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="3102c-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="3102c-110">下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="3102c-110">One of the following values:</span></span>

| <span data-ttu-id="3102c-111">值</span><span class="sxs-lookup"><span data-stu-id="3102c-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="3102c-112">意義</span><span class="sxs-lookup"><span data-stu-id="3102c-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="3102c-113"><dt>**HDSIL \_ 正常**</dt></span><span class="sxs-lookup"><span data-stu-id="3102c-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="3102c-114">表示這是一般的影像清單。</span><span class="sxs-lookup"><span data-stu-id="3102c-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="3102c-115"><dt>**HDSIL \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="3102c-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="3102c-116">表示這是狀態影像清單。</span><span class="sxs-lookup"><span data-stu-id="3102c-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="3102c-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3102c-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3102c-118">影像清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3102c-118">A handle to an image list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3102c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="3102c-119">Return value</span></span>

<span data-ttu-id="3102c-120">將控制碼傳回至先前與控制項相關聯的影像清單。</span><span class="sxs-lookup"><span data-stu-id="3102c-120">Returns the handle to the image list previously associated with the control.</span></span> <span data-ttu-id="3102c-121">失敗時傳回 Null，如果先前未設定任何影像清單，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="3102c-121">Returns **NULL** upon failure or if no image list was set previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="3102c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3102c-122">Requirements</span></span>



| <span data-ttu-id="3102c-123">需求</span><span class="sxs-lookup"><span data-stu-id="3102c-123">Requirement</span></span> | <span data-ttu-id="3102c-124">值</span><span class="sxs-lookup"><span data-stu-id="3102c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3102c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3102c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3102c-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3102c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3102c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3102c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3102c-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3102c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3102c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3102c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3102c-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3102c-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





