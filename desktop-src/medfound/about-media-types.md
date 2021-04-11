---
description: 關於媒體類型
ms.assetid: 169cdb00-0c1a-4530-90b7-bc89c71d1d04
title: '關於媒體類型 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca1ee75979c5c382e7e4ea458655efb83435a22d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945591"
---
# <a name="about-media-types-microsoft-media-foundation"></a><span data-ttu-id="2ea7e-103">關於媒體類型 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="2ea7e-103">About Media Types (Microsoft Media Foundation)</span></span>

<span data-ttu-id="2ea7e-104">*媒體類型* 描述媒體資料流程的格式。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-104">A *media type* describes the format of a media stream.</span></span> <span data-ttu-id="2ea7e-105">在 Microsoft 媒體基礎中，媒體類型會以 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-105">In Microsoft Media Foundation, media types are represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="2ea7e-106">這個介面會繼承 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-106">This interface inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="2ea7e-107">媒體類型的詳細資料會指定為屬性。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-107">The details of a media type are specified as attributes.</span></span>

<span data-ttu-id="2ea7e-108">若要建立新的媒體類型，請呼叫 [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) 函數。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-108">To create a new media type, call the [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) function.</span></span> <span data-ttu-id="2ea7e-109">此函數會傳回 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-109">This function returns a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="2ea7e-110">媒體類型一開始沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-110">The media type initially has no attributes.</span></span> <span data-ttu-id="2ea7e-111">若要設定格式的詳細資料，請設定相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-111">To set the details of the format, set the relevant attributes.</span></span>

<span data-ttu-id="2ea7e-112">如需媒體類型屬性的清單，請參閱 [媒體類型屬性](media-type-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-112">For a list of media type attributes, see [Media Type Attributes](media-type-attributes.md).</span></span>

## <a name="major-types-and-subtypes"></a><span data-ttu-id="2ea7e-113">主要類型和子類型</span><span class="sxs-lookup"><span data-stu-id="2ea7e-113">Major Types and Subtypes</span></span>

<span data-ttu-id="2ea7e-114">任何媒體類型的兩項重要資訊是主要類型和子類型。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-114">Two important pieces of information for any media type are the major type and the subtype.</span></span>

-   <span data-ttu-id="2ea7e-115">*主要類型* 是 GUID，可定義媒體資料流程中資料的整體分類。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-115">The *major type* is a GUID that defines the overall category of the data in a media stream.</span></span> <span data-ttu-id="2ea7e-116">主要類型包括影片和音訊。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-116">Major types include video and audio.</span></span> <span data-ttu-id="2ea7e-117">若要指定主要類型，請設定 [ [MF \_ MT \_ 主要 \_ 類型](mf-mt-major-type-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-117">To specify the major type, set the [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md) attribute.</span></span> <span data-ttu-id="2ea7e-118">[**IMFMediaType：： GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)方法會傳回這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-118">The [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) method returns the value of this attribute.</span></span>
-   <span data-ttu-id="2ea7e-119">*子類型* 會進一步定義格式。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-119">The *subtype* further defines the format.</span></span> <span data-ttu-id="2ea7e-120">例如，在影片主要類型中，有 RGB-24、RGB-32、YUY2 等等的子類型。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-120">For example, within the video major type, there are subtypes for RGB-24, RGB-32, YUY2, and so forth.</span></span> <span data-ttu-id="2ea7e-121">在音訊中，有 PCM 音訊、IEEE 浮點音訊及其他。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-121">Within audio, there are PCM audio, IEEE floating-point audio, and others.</span></span> <span data-ttu-id="2ea7e-122">子類型提供的資訊高於主要類型，但不會定義格式的所有內容。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-122">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="2ea7e-123">例如，影片子類型不會定義影像大小或畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-123">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="2ea7e-124">若要指定子類型，請設定 [ [MF \_ MT \_ 子類型](mf-mt-subtype-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-124">To specify the subtype, set the [MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md) attribute.</span></span>

<span data-ttu-id="2ea7e-125">所有媒體類型都應該有主要類型 GUID 和子類型 GUID。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-125">All media types should have a major type GUID and a subtype GUID.</span></span> <span data-ttu-id="2ea7e-126">如需主要類型和子類型 Guid 的清單，請參閱 [媒體類型 guid](media-type-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-126">For a list of major type and subtype GUIDs, see [Media Type GUIDs](media-type-guids.md).</span></span>

## <a name="why-attributes"></a><span data-ttu-id="2ea7e-127">為什麼要有屬性？</span><span class="sxs-lookup"><span data-stu-id="2ea7e-127">Why Attributes?</span></span>

<span data-ttu-id="2ea7e-128">相較于先前的技術（例如 DirectShow 和 Windows Media Format SDK）所使用的格式結構，屬性有幾個優點。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-128">Attributes have several advantages over the format structures that have been used in previous technologies such as DirectShow and the Windows Media Format SDK.</span></span>

-   <span data-ttu-id="2ea7e-129">更容易表示「不知道」或「不在意」的值。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-129">It is easier to represent "don't know" or "don't care" values.</span></span> <span data-ttu-id="2ea7e-130">例如，如果您要撰寫影片轉換，您可能事先知道轉換支援哪些 RGB 和 YUV 格式，而不是影片框架的尺寸，直到您從影片來源取得它們為止。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-130">For example, if you are writing a video transform, you might know in advance which RGB and YUV formats the transform supports, but not the dimensions of the video frame, until you get them from the video source.</span></span> <span data-ttu-id="2ea7e-131">同樣地，您可能不在意特定的詳細資料，例如影片主要複本。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-131">Similarly, you might not care about certain details, such as the video primaries.</span></span> <span data-ttu-id="2ea7e-132">使用格式結構時，每個成員都必須填入 *某個* 值。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-132">With a format structure, every member must be filled with *some* value.</span></span> <span data-ttu-id="2ea7e-133">如此一來，使用零表示未知或預設值會很常見。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-133">As a result, it has become common to use zero to indicate an unknown or default value.</span></span> <span data-ttu-id="2ea7e-134">如果另一個元件將零視為合法值，這種做法可能會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-134">This practice can cause errors if another component treats zero as a legitimate value.</span></span> <span data-ttu-id="2ea7e-135">使用屬性時，您只需要省略未知或與您的元件無關的屬性。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-135">With attributes, you simply omit the attributes that are unknown or not relevant to your component.</span></span>

-   <span data-ttu-id="2ea7e-136">當需求隨著時間變更時，會在結構結尾新增其他資料來擴充格式結構。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-136">As requirements have changed over time, format structures were extended by adding additional data at the end of the structure.</span></span> <span data-ttu-id="2ea7e-137">例如， **WAVEFORMATEXTENSIBLE** 會擴充 **WAVEFORMATEX** 結構。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-137">For example, **WAVEFORMATEXTENSIBLE** extends the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="2ea7e-138">這種作法很容易發生錯誤，因為元件必須將結構指標轉換成其他結構類型。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-138">This practice is prone to error, because components must cast structure pointers to other structure types.</span></span> <span data-ttu-id="2ea7e-139">您可以安全地延伸屬性。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-139">Attributes can be extended safely.</span></span>
-   <span data-ttu-id="2ea7e-140">已定義了互相不相容的格式結構。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-140">Mutually incompatible format structures have been defined.</span></span> <span data-ttu-id="2ea7e-141">例如，DirectShow 定義了 **VIDEOINFOHEADER** 和 **VIDEOINFOHEADER2** 結構。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-141">For example, DirectShow defines the **VIDEOINFOHEADER** and **VIDEOINFOHEADER2** structures.</span></span> <span data-ttu-id="2ea7e-142">彼此獨立設定屬性，因此不會發生此問題。</span><span class="sxs-lookup"><span data-stu-id="2ea7e-142">Attributes are set independently of each other, so this problem does not arise.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ea7e-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ea7e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ea7e-144">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="2ea7e-144">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="2ea7e-145">媒體類型</span><span class="sxs-lookup"><span data-stu-id="2ea7e-145">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



