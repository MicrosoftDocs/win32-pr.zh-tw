---
title: Windows Media 格式 SDK 的媒體類型
description: 瞭解 Windows Media Format SDK 可以使用的媒體類型。 媒體類型是指派給 SDK 中常數的 GUID 值。
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media Format SDK，媒體類型
- Advanced Systems Format (ASF) 、媒體類型
- ASF (Advanced 系統格式) 、媒體類型
- 媒體類型，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106978549"
---
# <a name="media-types-for-windows-media-format-sdk"></a><span data-ttu-id="ecff3-108">Windows Media 格式 SDK 的媒體類型</span><span class="sxs-lookup"><span data-stu-id="ecff3-108">Media Types for Windows Media Format SDK</span></span>

<span data-ttu-id="ecff3-109">媒體類型可識別 Windows Media Format SDK 可以使用的不同類型媒體。</span><span class="sxs-lookup"><span data-stu-id="ecff3-109">Media types identify the different types of media that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="ecff3-110">所有媒體類型都是已指派給 SDK 中常數的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="ecff3-110">All media types are GUID values that have been assigned to constants in the SDK.</span></span> <span data-ttu-id="ecff3-111">本章節所列的常數所代表的 GUID 值，會列在此參考的 [ [媒體類型識別碼](media-type-identifiers.md) ] 區段中。</span><span class="sxs-lookup"><span data-stu-id="ecff3-111">The GUID values represented by the constants listed in this section are listed in the [Media Type Identifiers](media-type-identifiers.md) section of this reference.</span></span>

<span data-ttu-id="ecff3-112">下表列出主要的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="ecff3-112">The following table lists major media types.</span></span> <span data-ttu-id="ecff3-113">這些常數會定義 Windows Media 格式 SDK 所支援之數位媒體的高階分類。</span><span class="sxs-lookup"><span data-stu-id="ecff3-113">These constants define the high level classification of digital media supported by the Windows Media Format SDK.</span></span>



| <span data-ttu-id="ecff3-114">主要類型</span><span class="sxs-lookup"><span data-stu-id="ecff3-114">Major type</span></span>                | <span data-ttu-id="ecff3-115">Description</span><span class="sxs-lookup"><span data-stu-id="ecff3-115">Description</span></span>                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecff3-116">WMMEDIATYPE \_ 影片</span><span class="sxs-lookup"><span data-stu-id="ecff3-116">WMMEDIATYPE\_Video</span></span>        | <span data-ttu-id="ecff3-117">影片串流。</span><span class="sxs-lookup"><span data-stu-id="ecff3-117">A video stream.</span></span>                                                                                         |
| <span data-ttu-id="ecff3-118">WMMEDIATYPE \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="ecff3-118">WMMEDIATYPE\_Audio</span></span>        | <span data-ttu-id="ecff3-119">音訊串流。</span><span class="sxs-lookup"><span data-stu-id="ecff3-119">An audio stream.</span></span>                                                                                        |
| <span data-ttu-id="ecff3-120">WMMEDIATYPE \_ 腳本</span><span class="sxs-lookup"><span data-stu-id="ecff3-120">WMMEDIATYPE\_Script</span></span>       | <span data-ttu-id="ecff3-121">腳本資料流程。</span><span class="sxs-lookup"><span data-stu-id="ecff3-121">A script stream.</span></span>                                                                                        |
| <span data-ttu-id="ecff3-122">WMMEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="ecff3-122">WMMEDIATYPE\_FileTransfer</span></span> | <span data-ttu-id="ecff3-123">包含資料檔案的資料流程。</span><span class="sxs-lookup"><span data-stu-id="ecff3-123">A stream that contains data files.</span></span> <span data-ttu-id="ecff3-124">包含 HTML 檔案的 Web 串流也有此主要類型。</span><span class="sxs-lookup"><span data-stu-id="ecff3-124">Web streams, which consist of HTML files, also have this major type.</span></span> |
| <span data-ttu-id="ecff3-125">WMMEDIATYPE \_ 影像</span><span class="sxs-lookup"><span data-stu-id="ecff3-125">WMMEDIATYPE\_Image</span></span>        | <span data-ttu-id="ecff3-126">說明的音訊檔案的 JPEG 影像串流 (如投影片放映) 所示。</span><span class="sxs-lookup"><span data-stu-id="ecff3-126">A JPEG image stream for an illustrated audio file (as in a slide show).</span></span>                                 |
| <span data-ttu-id="ecff3-127">WMMEDIATYPE \_ 文字</span><span class="sxs-lookup"><span data-stu-id="ecff3-127">WMMEDIATYPE\_Text</span></span>         | <span data-ttu-id="ecff3-128">文字資料流程。</span><span class="sxs-lookup"><span data-stu-id="ecff3-128">A text stream.</span></span>                                                                                          |



 

<span data-ttu-id="ecff3-129">除了明確支援的主要媒體類型之外，您還可以建立自己的任意資料類型。</span><span class="sxs-lookup"><span data-stu-id="ecff3-129">In addition to the explicitly supported major media types, you can create your own arbitrary data types.</span></span> <span data-ttu-id="ecff3-130">針對自訂任意資料類型，您必須確定您使用的 GUID 不符合現有的主要類型。</span><span class="sxs-lookup"><span data-stu-id="ecff3-130">For custom arbitrary data types, you must ensure that the GUID you use does not match an existing major type.</span></span>

<span data-ttu-id="ecff3-131">除了主要類型之外，媒體資料流程通常會有子類型。</span><span class="sxs-lookup"><span data-stu-id="ecff3-131">A media stream will often have a subtype in addition to its major type.</span></span> <span data-ttu-id="ecff3-132">下列各節列出支援的子類型。</span><span class="sxs-lookup"><span data-stu-id="ecff3-132">The following sections list the supported subtypes.</span></span>



| <span data-ttu-id="ecff3-133">區段</span><span class="sxs-lookup"><span data-stu-id="ecff3-133">Section</span></span>                                                        | <span data-ttu-id="ecff3-134">描述</span><span class="sxs-lookup"><span data-stu-id="ecff3-134">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecff3-135">未壓縮的媒體子類型</span><span class="sxs-lookup"><span data-stu-id="ecff3-135">Uncompressed Media Subtypes</span></span>](uncompressed-media-subtypes.md) | <span data-ttu-id="ecff3-136">描述適用于未壓縮媒體的子類型。</span><span class="sxs-lookup"><span data-stu-id="ecff3-136">Describes the subtypes available for uncompressed media.</span></span> <span data-ttu-id="ecff3-137">這些類型通常與輸入或輸出媒體相關聯。</span><span class="sxs-lookup"><span data-stu-id="ecff3-137">These are the types typically associated with input or output media.</span></span>              |
| [<span data-ttu-id="ecff3-138">壓縮的媒體子類型</span><span class="sxs-lookup"><span data-stu-id="ecff3-138">Compressed Media Subtypes</span></span>](compressed-media-subtypes.md)     | <span data-ttu-id="ecff3-139">描述適用于壓縮媒體的子類型。</span><span class="sxs-lookup"><span data-stu-id="ecff3-139">Describes the subtypes available for compressed media.</span></span> <span data-ttu-id="ecff3-140">這些類型通常與 ASF 檔案內串流中的媒體相關聯。</span><span class="sxs-lookup"><span data-stu-id="ecff3-140">These are the types typically associated with media in a stream within an ASF file.</span></span> |
| [<span data-ttu-id="ecff3-141">影片輸入格式</span><span class="sxs-lookup"><span data-stu-id="ecff3-141">Video Input Formats</span></span>](video-input-formats.md)                 | <span data-ttu-id="ecff3-142">列出接受 Windows Media 視訊9編解碼器輸入的影片格式。</span><span class="sxs-lookup"><span data-stu-id="ecff3-142">Lists the video formats accepted as inputs for the Windows Media Video 9 codec.</span></span>                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="ecff3-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="ecff3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecff3-144">**媒體類型識別碼**</span><span class="sxs-lookup"><span data-stu-id="ecff3-144">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="ecff3-145">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="ecff3-145">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




