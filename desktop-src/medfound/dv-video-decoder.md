---
description: 媒體基礎 DV 影片解碼是可解碼 DV 影片的媒體基礎轉換。
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: DV 影片解碼
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689307"
---
# <a name="dv-video-decoder"></a><span data-ttu-id="6da81-103">DV 影片解碼</span><span class="sxs-lookup"><span data-stu-id="6da81-103">DV Video Decoder</span></span>

<span data-ttu-id="6da81-104">媒體基礎 DV 影片解碼是可解碼 DV 影片的 [媒體基礎轉換](media-foundation-transforms.md) 。</span><span class="sxs-lookup"><span data-stu-id="6da81-104">The Media Foundation DV video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes DV video.</span></span>

<span data-ttu-id="6da81-105">DV 影片解碼支援下列輸入類型：</span><span class="sxs-lookup"><span data-stu-id="6da81-105">The DV video decoder supports the following input types:</span></span>



| <span data-ttu-id="6da81-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="6da81-106">Subtype</span></span>                 | <span data-ttu-id="6da81-107">Description</span><span class="sxs-lookup"><span data-stu-id="6da81-107">Description</span></span>                  |
|-------------------------|------------------------------|
| <span data-ttu-id="6da81-108">**MFVideoFormat \_ DVC**</span><span class="sxs-lookup"><span data-stu-id="6da81-108">**MFVideoFormat\_DVC**</span></span>  | <span data-ttu-id="6da81-109">DVC/DV 影片</span><span class="sxs-lookup"><span data-stu-id="6da81-109">DVC/DV Video</span></span>                 |
| <span data-ttu-id="6da81-110">**MFVideoFormat \_ DVHD**</span><span class="sxs-lookup"><span data-stu-id="6da81-110">**MFVideoFormat\_DVHD**</span></span> | <span data-ttu-id="6da81-111">HD-DVCR (1125-60 或 1250-50) </span><span class="sxs-lookup"><span data-stu-id="6da81-111">HD-DVCR (1125-60 or 1250-50)</span></span> |
| <span data-ttu-id="6da81-112">**MFVideoFormat \_ DVSD**</span><span class="sxs-lookup"><span data-stu-id="6da81-112">**MFVideoFormat\_DVSD**</span></span> | <span data-ttu-id="6da81-113">SDL-DVCR (525-60 或 625-50) </span><span class="sxs-lookup"><span data-stu-id="6da81-113">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="6da81-114">**MFVideoFormat \_ DVSL**</span><span class="sxs-lookup"><span data-stu-id="6da81-114">**MFVideoFormat\_DVSL**</span></span> | <span data-ttu-id="6da81-115">SD-DVCR (525-60 或 625-50) </span><span class="sxs-lookup"><span data-stu-id="6da81-115">SD-DVCR (525-60 or 625-50)</span></span>   |



 

<span data-ttu-id="6da81-116">它支援單一輸出類型：</span><span class="sxs-lookup"><span data-stu-id="6da81-116">It supports a single output type:</span></span>



| <span data-ttu-id="6da81-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="6da81-117">Subtype</span></span>             | <span data-ttu-id="6da81-118">Description</span><span class="sxs-lookup"><span data-stu-id="6da81-118">Description</span></span> |
|---------------------|-------------|
| <span data-ttu-id="6da81-119">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="6da81-119">MFVideoFormat\_YUY2</span></span> | <span data-ttu-id="6da81-120">YUY2 影片</span><span class="sxs-lookup"><span data-stu-id="6da81-120">YUY2 video</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="6da81-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6da81-121">Requirements</span></span>



| <span data-ttu-id="6da81-122">需求</span><span class="sxs-lookup"><span data-stu-id="6da81-122">Requirement</span></span> | <span data-ttu-id="6da81-123">值</span><span class="sxs-lookup"><span data-stu-id="6da81-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6da81-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6da81-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6da81-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6da81-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6da81-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6da81-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6da81-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6da81-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6da81-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6da81-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6da81-129"><dt>Mfdvdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6da81-129"><dt>Mfdvdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6da81-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6da81-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da81-131">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="6da81-131">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="6da81-132">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="6da81-132">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6da81-133">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="6da81-133">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 




