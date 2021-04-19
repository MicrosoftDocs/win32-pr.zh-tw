---
title: 'TCM_REMOVEIMAGE 訊息 (Commctrl .h) '
description: 從索引標籤控制項的影像清單中移除影像。 您可以使用 TabCtrl RemoveImage 宏明確地傳送此訊息 \_ 。
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- TCM_REMOVEIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbc51aa0efed847e39e735443c0d42e288bbaab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965528"
---
# <a name="tcm_removeimage-message"></a><span data-ttu-id="d777d-105">TCM \_ REMOVEIMAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="d777d-105">TCM\_REMOVEIMAGE message</span></span>

<span data-ttu-id="d777d-106">從索引標籤控制項的影像清單中移除影像。</span><span class="sxs-lookup"><span data-stu-id="d777d-106">Removes an image from a tab control's image list.</span></span> <span data-ttu-id="d777d-107">您可以使用 [**TabCtrl \_ RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d777d-107">You can send this message explicitly or by using the [**TabCtrl\_RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d777d-108">參數</span><span class="sxs-lookup"><span data-stu-id="d777d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d777d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d777d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d777d-110">要移除之映射的索引。</span><span class="sxs-lookup"><span data-stu-id="d777d-110">Index of the image to remove.</span></span>

</dd> <dt>

<span data-ttu-id="d777d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d777d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d777d-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d777d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d777d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d777d-113">Return value</span></span>

<span data-ttu-id="d777d-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="d777d-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d777d-115">備註</span><span class="sxs-lookup"><span data-stu-id="d777d-115">Remarks</span></span>

<span data-ttu-id="d777d-116">索引標籤控制項會更新每個索引標籤的影像索引，因此每個索引標籤都會與之前的映射保持相關聯。</span><span class="sxs-lookup"><span data-stu-id="d777d-116">The tab control updates each tab's image index, so each tab remains associated with the same image as before.</span></span> <span data-ttu-id="d777d-117">如果索引標籤使用正在移除的影像，索引標籤將設定為沒有影像。</span><span class="sxs-lookup"><span data-stu-id="d777d-117">If a tab is using the image being removed, the tab will be set to have no image.</span></span>

## <a name="requirements"></a><span data-ttu-id="d777d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d777d-118">Requirements</span></span>



| <span data-ttu-id="d777d-119">需求</span><span class="sxs-lookup"><span data-stu-id="d777d-119">Requirement</span></span> | <span data-ttu-id="d777d-120">值</span><span class="sxs-lookup"><span data-stu-id="d777d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d777d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d777d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d777d-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d777d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d777d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d777d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d777d-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d777d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d777d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d777d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d777d-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d777d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





