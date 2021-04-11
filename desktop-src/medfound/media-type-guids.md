---
description: 主要媒體類型
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: 主要媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a93a1aa430a720ff4b2f3591071d0bc8b178d6a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945686"
---
# <a name="major-media-types"></a><span data-ttu-id="d387d-103">主要媒體類型</span><span class="sxs-lookup"><span data-stu-id="d387d-103">Major Media Types</span></span>

<span data-ttu-id="d387d-104">在媒體類型中， *主要類型* 會描述資料的整體類別，例如音訊或影片。</span><span class="sxs-lookup"><span data-stu-id="d387d-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="d387d-105">*子類型*（如果有的話）會進一步調整主要類型。</span><span class="sxs-lookup"><span data-stu-id="d387d-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="d387d-106">例如，如果主要類型是 video，則子類型可能是32位 RGB video。</span><span class="sxs-lookup"><span data-stu-id="d387d-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="d387d-107">子類型也可區分編碼格式，例如 h.264 video，從未壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="d387d-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="d387d-108">主要類型和子類型是由 Guid 所識別，並儲存在下列屬性中：</span><span class="sxs-lookup"><span data-stu-id="d387d-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="d387d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d387d-109">Attribute</span></span>                                             | <span data-ttu-id="d387d-110">描述</span><span class="sxs-lookup"><span data-stu-id="d387d-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="d387d-111">MF \_ MT \_ 主要 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d387d-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="d387d-112">主要類型。</span><span class="sxs-lookup"><span data-stu-id="d387d-112">Major type.</span></span> |
| [<span data-ttu-id="d387d-113">MF \_ MT \_ 子類型</span><span class="sxs-lookup"><span data-stu-id="d387d-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="d387d-114">亞。</span><span class="sxs-lookup"><span data-stu-id="d387d-114">Subtype.</span></span>    |



 

<span data-ttu-id="d387d-115">以下是定義的主要類型。</span><span class="sxs-lookup"><span data-stu-id="d387d-115">The following major types are defined.</span></span>



| <span data-ttu-id="d387d-116">主要類型</span><span class="sxs-lookup"><span data-stu-id="d387d-116">Major Type</span></span>                    | <span data-ttu-id="d387d-117">Description</span><span class="sxs-lookup"><span data-stu-id="d387d-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="d387d-118">子類型</span><span class="sxs-lookup"><span data-stu-id="d387d-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d387d-119">**MFMediaType \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="d387d-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="d387d-120">音訊。</span><span class="sxs-lookup"><span data-stu-id="d387d-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="d387d-121">[音訊子類型 guid](audio-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="d387d-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="d387d-122">**MFMediaType \_ 二進位檔**</span><span class="sxs-lookup"><span data-stu-id="d387d-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="d387d-123">二進位資料流程。</span><span class="sxs-lookup"><span data-stu-id="d387d-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="d387d-124">無。</span><span class="sxs-lookup"><span data-stu-id="d387d-124">None.</span></span>                                                |
| <span data-ttu-id="d387d-125">**MFMediaType \_ FileTransfer**</span><span class="sxs-lookup"><span data-stu-id="d387d-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="d387d-126">包含資料檔案的資料流程。</span><span class="sxs-lookup"><span data-stu-id="d387d-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="d387d-127">無。</span><span class="sxs-lookup"><span data-stu-id="d387d-127">None.</span></span>                                                |
| <span data-ttu-id="d387d-128">**MFMediaType \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="d387d-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="d387d-129">HTML 資料流程。</span><span class="sxs-lookup"><span data-stu-id="d387d-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="d387d-130">無。</span><span class="sxs-lookup"><span data-stu-id="d387d-130">None.</span></span>                                                |
| <span data-ttu-id="d387d-131">**MFMediaType \_ 影像**</span><span class="sxs-lookup"><span data-stu-id="d387d-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="d387d-132">靜止影像資料流程。</span><span class="sxs-lookup"><span data-stu-id="d387d-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="d387d-133">[WIC guid 和 clsid](../wic/-wic-guids-clsids.md)。</span><span class="sxs-lookup"><span data-stu-id="d387d-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="d387d-134">**MFMediaType \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="d387d-134">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="d387d-135">受保護的媒體。</span><span class="sxs-lookup"><span data-stu-id="d387d-135">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="d387d-136">子類型指定內容保護設定。</span><span class="sxs-lookup"><span data-stu-id="d387d-136">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="d387d-137">**MFMediaType \_ 認知**</span><span class="sxs-lookup"><span data-stu-id="d387d-137">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="d387d-138">從相機感應器或處理單位串流處理，並瞭解原始的影片資料，並瞭解其環境或人類。</span><span class="sxs-lookup"><span data-stu-id="d387d-138">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="d387d-139">無。</span><span class="sxs-lookup"><span data-stu-id="d387d-139">None.</span></span>                                                |
| <span data-ttu-id="d387d-140">**MFMediaType \_ 薩米文**</span><span class="sxs-lookup"><span data-stu-id="d387d-140">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="d387d-141">已同步處理的可存取媒體交換 (薩米) 字幕。</span><span class="sxs-lookup"><span data-stu-id="d387d-141">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="d387d-142">無。</span><span class="sxs-lookup"><span data-stu-id="d387d-142">None.</span></span>                                                |
| <span data-ttu-id="d387d-143">**MFMediaType \_ 腳本**</span><span class="sxs-lookup"><span data-stu-id="d387d-143">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="d387d-144">腳本資料流程。</span><span class="sxs-lookup"><span data-stu-id="d387d-144">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="d387d-145">無。</span><span class="sxs-lookup"><span data-stu-id="d387d-145">None.</span></span>                                                |
| <span data-ttu-id="d387d-146">**MFMediaType \_ 資料流程**</span><span class="sxs-lookup"><span data-stu-id="d387d-146">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="d387d-147">多工資料流程或基本資料流程。</span><span class="sxs-lookup"><span data-stu-id="d387d-147">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="d387d-148">資料流程子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="d387d-148">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="d387d-149">**MFMediaType \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="d387d-149">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="d387d-150">影片。</span><span class="sxs-lookup"><span data-stu-id="d387d-150">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="d387d-151">[影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="d387d-151">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="d387d-152">協力廠商元件可以定義新的主要類型和新的子類型。</span><span class="sxs-lookup"><span data-stu-id="d387d-152">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d387d-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="d387d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d387d-154">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d387d-154">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="d387d-155">媒體類型</span><span class="sxs-lookup"><span data-stu-id="d387d-155">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
