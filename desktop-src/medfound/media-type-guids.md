---
description: 主要媒體類型
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: 主要媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56553ac635f0e767e43e057b2a468027dcefb730
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549573"
---
# <a name="major-media-types"></a><span data-ttu-id="26603-103">主要媒體類型</span><span class="sxs-lookup"><span data-stu-id="26603-103">Major Media Types</span></span>

<span data-ttu-id="26603-104">在媒體類型中， *主要類型* 會描述資料的整體類別，例如音訊或影片。</span><span class="sxs-lookup"><span data-stu-id="26603-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="26603-105">*子類型*（如果有的話）會進一步調整主要類型。</span><span class="sxs-lookup"><span data-stu-id="26603-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="26603-106">例如，如果主要類型是 video，則子類型可能是32位 RGB video。</span><span class="sxs-lookup"><span data-stu-id="26603-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="26603-107">子類型也可區分編碼格式，例如 h.264 video，從未壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="26603-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="26603-108">主要類型和子類型是由 Guid 所識別，並儲存在下列屬性中：</span><span class="sxs-lookup"><span data-stu-id="26603-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="26603-109">屬性</span><span class="sxs-lookup"><span data-stu-id="26603-109">Attribute</span></span>                                             | <span data-ttu-id="26603-110">描述</span><span class="sxs-lookup"><span data-stu-id="26603-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="26603-111">MF \_ MT \_ 主要 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="26603-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="26603-112">主要類型。</span><span class="sxs-lookup"><span data-stu-id="26603-112">Major type.</span></span> |
| [<span data-ttu-id="26603-113">MF \_ MT \_ 子類型</span><span class="sxs-lookup"><span data-stu-id="26603-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="26603-114">亞。</span><span class="sxs-lookup"><span data-stu-id="26603-114">Subtype.</span></span>    |



 

<span data-ttu-id="26603-115">以下是定義的主要類型。</span><span class="sxs-lookup"><span data-stu-id="26603-115">The following major types are defined.</span></span>



| <span data-ttu-id="26603-116">主要類型</span><span class="sxs-lookup"><span data-stu-id="26603-116">Major Type</span></span>                    | <span data-ttu-id="26603-117">Description</span><span class="sxs-lookup"><span data-stu-id="26603-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="26603-118">子類型</span><span class="sxs-lookup"><span data-stu-id="26603-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26603-119">**MFMediaType \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="26603-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="26603-120">音訊。</span><span class="sxs-lookup"><span data-stu-id="26603-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="26603-121">[音訊子類型 guid](audio-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="26603-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="26603-122">**MFMediaType \_ 二進位檔**</span><span class="sxs-lookup"><span data-stu-id="26603-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="26603-123">二進位資料流程。</span><span class="sxs-lookup"><span data-stu-id="26603-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="26603-124">無。</span><span class="sxs-lookup"><span data-stu-id="26603-124">None.</span></span>                                                |
| <span data-ttu-id="26603-125">**MFMediaType \_ FileTransfer**</span><span class="sxs-lookup"><span data-stu-id="26603-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="26603-126">包含資料檔案的資料流程。</span><span class="sxs-lookup"><span data-stu-id="26603-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="26603-127">無。</span><span class="sxs-lookup"><span data-stu-id="26603-127">None.</span></span>                                                |
| <span data-ttu-id="26603-128">**MFMediaType \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="26603-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="26603-129">HTML 資料流程。</span><span class="sxs-lookup"><span data-stu-id="26603-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="26603-130">無。</span><span class="sxs-lookup"><span data-stu-id="26603-130">None.</span></span>                                                |
| <span data-ttu-id="26603-131">**MFMediaType \_ 影像**</span><span class="sxs-lookup"><span data-stu-id="26603-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="26603-132">靜止影像資料流程。</span><span class="sxs-lookup"><span data-stu-id="26603-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="26603-133">[WIC guid 和 clsid](../wic/-wic-guids-clsids.md)。</span><span class="sxs-lookup"><span data-stu-id="26603-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="26603-134">**MFMediaType \_ 中繼資料**</span><span class="sxs-lookup"><span data-stu-id="26603-134">**MFMediaType\_Metadata**</span></span>        | <span data-ttu-id="26603-135">中繼資料資料流程。</span><span class="sxs-lookup"><span data-stu-id="26603-135">Metadata stream.</span></span>                                                                                                                                        | <span data-ttu-id="26603-136">無。</span><span class="sxs-lookup"><span data-stu-id="26603-136">None.</span></span>       |
| <span data-ttu-id="26603-137">**MFMediaType \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="26603-137">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="26603-138">受保護的媒體。</span><span class="sxs-lookup"><span data-stu-id="26603-138">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="26603-139">子類型指定內容保護設定。</span><span class="sxs-lookup"><span data-stu-id="26603-139">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="26603-140">**MFMediaType \_ 認知**</span><span class="sxs-lookup"><span data-stu-id="26603-140">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="26603-141">從相機感應器或處理單位串流處理，並瞭解原始的影片資料，並瞭解其環境或人類。</span><span class="sxs-lookup"><span data-stu-id="26603-141">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="26603-142">無。</span><span class="sxs-lookup"><span data-stu-id="26603-142">None.</span></span>                                                |
| <span data-ttu-id="26603-143">**MFMediaType \_ 薩米文**</span><span class="sxs-lookup"><span data-stu-id="26603-143">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="26603-144">已同步處理的可存取媒體交換 (薩米) 字幕。</span><span class="sxs-lookup"><span data-stu-id="26603-144">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="26603-145">無。</span><span class="sxs-lookup"><span data-stu-id="26603-145">None.</span></span>                                                |
| <span data-ttu-id="26603-146">**MFMediaType \_ 腳本**</span><span class="sxs-lookup"><span data-stu-id="26603-146">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="26603-147">腳本資料流程。</span><span class="sxs-lookup"><span data-stu-id="26603-147">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="26603-148">無。</span><span class="sxs-lookup"><span data-stu-id="26603-148">None.</span></span>                                                |
| <span data-ttu-id="26603-149">**MFMediaType \_ 資料流程**</span><span class="sxs-lookup"><span data-stu-id="26603-149">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="26603-150">多工資料流程或基本資料流程。</span><span class="sxs-lookup"><span data-stu-id="26603-150">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="26603-151">資料流程子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="26603-151">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="26603-152">**MFMediaType \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="26603-152">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="26603-153">影片。</span><span class="sxs-lookup"><span data-stu-id="26603-153">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="26603-154">[影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="26603-154">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="26603-155">協力廠商元件可以定義新的主要類型和新的子類型。</span><span class="sxs-lookup"><span data-stu-id="26603-155">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26603-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="26603-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26603-157">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="26603-157">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="26603-158">媒體類型</span><span class="sxs-lookup"><span data-stu-id="26603-158">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
