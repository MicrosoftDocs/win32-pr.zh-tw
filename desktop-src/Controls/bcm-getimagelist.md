---
title: 'BCM_GETIMAGELIST 訊息 (Commctrl .h) '
description: 取得按鈕 \_ IMAGELIST 結構，描述指派給按鈕控制項的影像清單。 您可以明確地傳送此訊息，或使用按鈕 \_ GetImageList 宏。
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- BCM_GETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465493"
---
# <a name="bcm_getimagelist-message"></a><span data-ttu-id="1b44e-105">BCM \_ GETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="1b44e-105">BCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="1b44e-106">取得 [**按鈕 \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) 結構，描述指派給按鈕控制項的影像清單。</span><span class="sxs-lookup"><span data-stu-id="1b44e-106">Gets the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that describes the image list assigned to a button control.</span></span> <span data-ttu-id="1b44e-107">您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) 宏。</span><span class="sxs-lookup"><span data-stu-id="1b44e-107">You can send this message explicitly or use the [**Button\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b44e-108">參數</span><span class="sxs-lookup"><span data-stu-id="1b44e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b44e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b44e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b44e-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="1b44e-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1b44e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b44e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b44e-112">[**按鈕 \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist)結構的指標，其中包含影像清單資訊。</span><span class="sxs-lookup"><span data-stu-id="1b44e-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b44e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b44e-113">Return value</span></span>

<span data-ttu-id="1b44e-114">如果訊息成功，則會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="1b44e-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="1b44e-115">否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1b44e-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b44e-116">備註</span><span class="sxs-lookup"><span data-stu-id="1b44e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1b44e-117">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="1b44e-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1b44e-118">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="1b44e-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1b44e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b44e-119">Requirements</span></span>



| <span data-ttu-id="1b44e-120">需求</span><span class="sxs-lookup"><span data-stu-id="1b44e-120">Requirement</span></span> | <span data-ttu-id="1b44e-121">值</span><span class="sxs-lookup"><span data-stu-id="1b44e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b44e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b44e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1b44e-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b44e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b44e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b44e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1b44e-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b44e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b44e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="1b44e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b44e-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1b44e-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





