---
title: 'TCM_GETIMAGELIST 訊息 (Commctrl .h) '
description: 抓取與索引標籤控制項相關聯的影像清單。 您可以使用 TabCtrl GetImageList 宏明確地傳送此訊息 \_ 。
ms.assetid: 86a0d8c7-ff3d-4e16-994e-4c72d1e62e9f
keywords:
- TCM_GETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c4d471ef4d072e4305507f4f5ebc4a8f2745ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844183"
---
# <a name="tcm_getimagelist-message"></a><span data-ttu-id="8b6ce-105">TCM \_ GETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="8b6ce-105">TCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="8b6ce-106">抓取與索引標籤控制項相關聯的影像清單。</span><span class="sxs-lookup"><span data-stu-id="8b6ce-106">Retrieves the image list associated with a tab control.</span></span> <span data-ttu-id="8b6ce-107">您可以使用 [**TabCtrl \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8b6ce-107">You can send this message explicitly or by using the [**TabCtrl\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b6ce-108">參數</span><span class="sxs-lookup"><span data-stu-id="8b6ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b6ce-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b6ce-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8b6ce-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8b6ce-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8b6ce-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b6ce-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8b6ce-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8b6ce-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b6ce-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b6ce-113">Return value</span></span>

<span data-ttu-id="8b6ce-114">如果成功，則傳回影像清單的控制碼，否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8b6ce-114">Returns the handle to the image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b6ce-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b6ce-115">Requirements</span></span>



| <span data-ttu-id="8b6ce-116">需求</span><span class="sxs-lookup"><span data-stu-id="8b6ce-116">Requirement</span></span> | <span data-ttu-id="8b6ce-117">值</span><span class="sxs-lookup"><span data-stu-id="8b6ce-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b6ce-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b6ce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8b6ce-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b6ce-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b6ce-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b6ce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8b6ce-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b6ce-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b6ce-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8b6ce-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b6ce-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8b6ce-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





