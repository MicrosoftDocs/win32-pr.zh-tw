---
description: 使用 Windows Media 視訊9.1 影像類別
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: 使用 Windows Media 視訊9.1 影像類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b545d37b61a1c89ffdd69615b28f636aa98b32
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106985818"
---
# <a name="using-the-windows-media-video-91-image-category"></a><span data-ttu-id="e77c9-103">使用 Windows Media 視訊9.1 影像類別</span><span class="sxs-lookup"><span data-stu-id="e77c9-103">Using the Windows Media Video 9.1 Image Category</span></span>

<span data-ttu-id="e77c9-104">Windows Media 視訊9.1 影像類別與 Windows Media 視訊9編碼器和解碼器所支援的其他輸出分類不同。</span><span class="sxs-lookup"><span data-stu-id="e77c9-104">The Windows Media Video 9.1 Image category is different from the other output categories supported by the Windows Media Video 9 encoder and decoder.</span></span> <span data-ttu-id="e77c9-105">它不會處理未壓縮的影片，而是採用特殊的輸入範例，其中包含結構化轉換資料，以及在其上執行轉換的 RGB 點陣圖影像。</span><span class="sxs-lookup"><span data-stu-id="e77c9-105">Instead of processing uncompressed video, it takes special input samples that consist of structured transformation data and, occasionally, RGB bitmap images on which the transformations are performed.</span></span>

<span data-ttu-id="e77c9-106">編碼的 Windows Media 視訊9.1 影像內容幾乎與一般 Windows Media 視訊9編碼的內容相同，但它是由自己的 FOURCC ( "WMVP" ) 所識別。</span><span class="sxs-lookup"><span data-stu-id="e77c9-106">The encoded Windows Media Video 9.1 Image content is virtually identical to regular Windows Media Video 9 encoded content, but it is identified by its own FOURCC ("WMVP").</span></span>

<span data-ttu-id="e77c9-107">影片影像的編碼器輸出類型是以與標準 Windows Media 影片完全相同的方式來設定，不同之處在于子類型和壓縮值必須設定為影片影像識別碼。</span><span class="sxs-lookup"><span data-stu-id="e77c9-107">The encoder output type for video image is set in exactly the same way as standard Windows Media video, except that the subtype and compression values must be set to the video image identifiers.</span></span> <span data-ttu-id="e77c9-108">這包括取得編解碼器私用資料，並將其附加至 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構的需求。</span><span class="sxs-lookup"><span data-stu-id="e77c9-108">This includes the need to obtain codec private data and append it to the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="e77c9-109">如需詳細資訊，請參閱設定 [影片編碼](configuringvideoencoding.md)。</span><span class="sxs-lookup"><span data-stu-id="e77c9-109">For more information, see [Configuring Video Encoding](configuringvideoencoding.md).</span></span>

<span data-ttu-id="e77c9-110">影片影像的輸入類型設定也非常類似于其他影片編碼器的輸入設定。</span><span class="sxs-lookup"><span data-stu-id="e77c9-110">The input type configuration for video image is also very similar to input configuration for the other video encoders.</span></span> <span data-ttu-id="e77c9-111">您可以藉由呼叫 [**IMediaObject：： GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)，或使用媒體基礎 SDK，藉由呼叫 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) ，並使用 [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)來取得的 **\_ 媒體 \_ 類型**，以從編碼器取出部分完成的 [**sql-dmo \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)。</span><span class="sxs-lookup"><span data-stu-id="e77c9-111">You can retrieve a partially completed [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) from the encoder by calling [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype), or if you are using the Media Foundation SDK, by calling [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) and retrieving the **DMO\_MEDIA\_TYPE** by using [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span></span> <span data-ttu-id="e77c9-112">然後，您可以設定畫面格大小和 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 格式結構，就像標準影片一樣。</span><span class="sxs-lookup"><span data-stu-id="e77c9-112">You then set the frame size and the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format structure, just as you would for standard video.</span></span> <span data-ttu-id="e77c9-113">如同輸出型別，您必須確定子類型和壓縮值已正確設定。</span><span class="sxs-lookup"><span data-stu-id="e77c9-113">As with the output type, you need to ensure that the subtype and compression values are set appropriately.</span></span>

## <a name="creating-input-samples"></a><span data-ttu-id="e77c9-114">建立輸入範例</span><span class="sxs-lookup"><span data-stu-id="e77c9-114">Creating Input Samples</span></span>

<span data-ttu-id="e77c9-115">影片影像編解碼器的輸入範例是結構化的。</span><span class="sxs-lookup"><span data-stu-id="e77c9-115">The input samples for the video image codec are structured.</span></span> <span data-ttu-id="e77c9-116">影片影像所用的結構和常數定義不包含在 Windows Media 音訊和影片編解碼器介面中。</span><span class="sxs-lookup"><span data-stu-id="e77c9-116">The definition of the structure and constants used for video image are not included with the Windows Media Audio and Video codec interfaces.</span></span> <span data-ttu-id="e77c9-117">這些定義包含在 Windows Media 格式 SDK 中，在 Windows Media 格式 SDK 檔中也會完整說明其使用方式。</span><span class="sxs-lookup"><span data-stu-id="e77c9-117">These definitions are included in the Windows Media Format SDK, and their use is fully explained in the Windows Media Format SDK documentation.</span></span>

## <a name="decoding"></a><span data-ttu-id="e77c9-118">解碼</span><span class="sxs-lookup"><span data-stu-id="e77c9-118">Decoding</span></span>

<span data-ttu-id="e77c9-119">解碼螢幕擷取畫面影片沒有特殊需求。</span><span class="sxs-lookup"><span data-stu-id="e77c9-119">There are no special requirements for decoding screen capture video.</span></span> <span data-ttu-id="e77c9-120">除了不同的子類型 (MEDIASUBTYPE \_ WMVP) 用於解碼輸入，壓縮的影片影像資料流程基本上與標準 Windows Media 視訊資料流程相同。</span><span class="sxs-lookup"><span data-stu-id="e77c9-120">Other than a different subtype (MEDIASUBTYPE\_WMVP) used for decoder input, the compressed video image stream is essentially identical to a standard Windows Media Video stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e77c9-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="e77c9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e77c9-122">使用影片</span><span class="sxs-lookup"><span data-stu-id="e77c9-122">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
