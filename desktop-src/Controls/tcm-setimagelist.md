---
title: 'TCM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 將影像清單指派給索引標籤控制項。 您可以使用 TabCtrl SetImageList 宏明確地傳送此訊息 \_ 。
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- TCM_SETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024574"
---
# <a name="tcm_setimagelist-message"></a><span data-ttu-id="2d3a2-105">TCM \_ SETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="2d3a2-105">TCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="2d3a2-106">將影像清單指派給索引標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="2d3a2-106">Assigns an image list to a tab control.</span></span> <span data-ttu-id="2d3a2-107">您可以使用 [**TabCtrl \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2d3a2-107">You can send this message explicitly or by using the [**TabCtrl\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d3a2-108">參數</span><span class="sxs-lookup"><span data-stu-id="2d3a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d3a2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d3a2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2d3a2-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2d3a2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2d3a2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d3a2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d3a2-112">要指派給索引標籤控制項的影像清單控制碼。</span><span class="sxs-lookup"><span data-stu-id="2d3a2-112">Handle to the image list to assign to the tab control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d3a2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d3a2-113">Return value</span></span>

<span data-ttu-id="2d3a2-114">傳回上一個影像清單的控制碼; 如果沒有上一個影像清單，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2d3a2-114">Returns the handle to the previous image list, or **NULL** if there is no previous image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d3a2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d3a2-115">Requirements</span></span>



| <span data-ttu-id="2d3a2-116">需求</span><span class="sxs-lookup"><span data-stu-id="2d3a2-116">Requirement</span></span> | <span data-ttu-id="2d3a2-117">值</span><span class="sxs-lookup"><span data-stu-id="2d3a2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d3a2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d3a2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2d3a2-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d3a2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d3a2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d3a2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2d3a2-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d3a2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d3a2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2d3a2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d3a2-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d3a2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





