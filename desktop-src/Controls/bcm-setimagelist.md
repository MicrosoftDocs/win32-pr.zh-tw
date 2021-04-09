---
title: 'BCM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 將影像清單指派給按鈕控制項。 您可以明確地傳送此訊息，或使用按鈕 \_ SetImageList 宏。
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- BCM_SETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024998"
---
# <a name="bcm_setimagelist-message"></a><span data-ttu-id="1c62f-105">BCM \_ SETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="1c62f-105">BCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="1c62f-106">將影像清單指派給按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="1c62f-106">Assigns an image list to a button control.</span></span> <span data-ttu-id="1c62f-107">您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) 宏。</span><span class="sxs-lookup"><span data-stu-id="1c62f-107">You can send this message explicitly or use the [**Button\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c62f-108">參數</span><span class="sxs-lookup"><span data-stu-id="1c62f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c62f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c62f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c62f-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="1c62f-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1c62f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c62f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c62f-112">[**按鈕 \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist)結構的指標，其中包含影像清單資訊。</span><span class="sxs-lookup"><span data-stu-id="1c62f-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c62f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c62f-113">Return value</span></span>

<span data-ttu-id="1c62f-114">如果訊息成功，則會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="1c62f-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="1c62f-115">否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1c62f-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c62f-116">備註</span><span class="sxs-lookup"><span data-stu-id="1c62f-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1c62f-117">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="1c62f-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1c62f-118">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="1c62f-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="1c62f-119">[**按鈕 \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist)結構的 **himl** 成員中所參考的影像清單，應包含要用於所有狀態的單一影像，或每個狀態的個別影像。</span><span class="sxs-lookup"><span data-stu-id="1c62f-119">The image list referred to in the **himl** member of the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure should contain either a single image to be used for all states or individual images for each state.</span></span> <span data-ttu-id="1c62f-120">下列是在 vssym32 中定義的狀態。</span><span class="sxs-lookup"><span data-stu-id="1c62f-120">The following states are defined in vssym32.h.</span></span>

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

<span data-ttu-id="1c62f-121">請注意，PBS \_ STYLUSHOT 只會用於 tablet 電腦。</span><span class="sxs-lookup"><span data-stu-id="1c62f-121">Note that PBS\_STYLUSHOT is used only on tablet computers.</span></span>

<span data-ttu-id="1c62f-122">每個值都是影像清單中適當影像的索引。</span><span class="sxs-lookup"><span data-stu-id="1c62f-122">Each value is an index to the appropriate image in the image list.</span></span> <span data-ttu-id="1c62f-123">如果只有一個映射存在，則會用於所有狀態。</span><span class="sxs-lookup"><span data-stu-id="1c62f-123">If only one image is present, it is used for all states.</span></span> <span data-ttu-id="1c62f-124">如果影像清單包含一個以上的影像，每個索引都會對應至按鈕的一個狀態。</span><span class="sxs-lookup"><span data-stu-id="1c62f-124">If the image list contains more than one image, each index corresponds to one state of the button.</span></span> <span data-ttu-id="1c62f-125">如果未針對每個狀態提供映射，則不會針對沒有影像的狀態繪製任何專案。</span><span class="sxs-lookup"><span data-stu-id="1c62f-125">If an image is not provided for each state, nothing is drawn for those states without images.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c62f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c62f-126">Requirements</span></span>



| <span data-ttu-id="1c62f-127">需求</span><span class="sxs-lookup"><span data-stu-id="1c62f-127">Requirement</span></span> | <span data-ttu-id="1c62f-128">值</span><span class="sxs-lookup"><span data-stu-id="1c62f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c62f-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c62f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1c62f-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c62f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c62f-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c62f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1c62f-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c62f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c62f-133">標頭</span><span class="sxs-lookup"><span data-stu-id="1c62f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c62f-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c62f-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





