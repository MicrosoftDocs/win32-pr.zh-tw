---
description: 指出是否已針對捕捉的框架觸發快閃。
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: 'MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974182"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a><span data-ttu-id="8e51e-103">MF \_ CAPTURE \_ METADATA \_ PHOTO \_ FRAME \_ FLASH 屬性</span><span class="sxs-lookup"><span data-stu-id="8e51e-103">MF\_CAPTURE\_METADATA\_PHOTO\_FRAME\_FLASH attribute</span></span>

<span data-ttu-id="8e51e-104">指出是否已針對捕捉的框架觸發快閃。</span><span class="sxs-lookup"><span data-stu-id="8e51e-104">Indicates if a flash was triggered for the captured frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="8e51e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="8e51e-105">Data type</span></span>

<span data-ttu-id="8e51e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8e51e-106">**UINT32**</span></span>



| <span data-ttu-id="8e51e-107">值</span><span class="sxs-lookup"><span data-stu-id="8e51e-107">Value</span></span>                                                                               | <span data-ttu-id="8e51e-108">意義</span><span class="sxs-lookup"><span data-stu-id="8e51e-108">Meaning</span></span>                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e51e-109"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8e51e-109"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="8e51e-110">未在此框架上觸發 flash。</span><span class="sxs-lookup"><span data-stu-id="8e51e-110">A flash was not triggered on this frame.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="8e51e-111"><dt>非零</dt></span><span class="sxs-lookup"><span data-stu-id="8e51e-111"><dt>non-zero</dt></span></span> </dl> | <span data-ttu-id="8e51e-112">此框架上已觸發 flash。</span><span class="sxs-lookup"><span data-stu-id="8e51e-112">A flash was triggered on this frame.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="8e51e-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8e51e-113"><dt>1</dt></span></span> </dl>        | <span data-ttu-id="8e51e-114">保留</span><span class="sxs-lookup"><span data-stu-id="8e51e-114">Reserved</span></span><br/> <span data-ttu-id="8e51e-115">請勿明確檢查值1。</span><span class="sxs-lookup"><span data-stu-id="8e51e-115">Do not explicitly check for a value of 1.</span></span> <span data-ttu-id="8e51e-116">應用程式應該只檢查！ = 0，以指出是否已觸發 flash。</span><span class="sxs-lookup"><span data-stu-id="8e51e-116">Applications should only check for !=0 to indicate if a flash was triggered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8e51e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e51e-117">Requirements</span></span>



| <span data-ttu-id="8e51e-118">需求</span><span class="sxs-lookup"><span data-stu-id="8e51e-118">Requirement</span></span> | <span data-ttu-id="8e51e-119">值</span><span class="sxs-lookup"><span data-stu-id="8e51e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e51e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e51e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8e51e-121">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e51e-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8e51e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e51e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8e51e-123">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e51e-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8e51e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8e51e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e51e-125"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="8e51e-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e51e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e51e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e51e-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="8e51e-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




