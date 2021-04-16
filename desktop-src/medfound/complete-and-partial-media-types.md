---
description: 本主題說明完整媒體類型與部分媒體類型之間的差異。
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: 完成和部分媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514344"
---
# <a name="complete-and-partial-media-types"></a><span data-ttu-id="0aaa5-103">完成和部分媒體類型</span><span class="sxs-lookup"><span data-stu-id="0aaa5-103">Complete and Partial Media Types</span></span>

<span data-ttu-id="0aaa5-104">本主題說明完整媒體類型與部分媒體類型之間的差異。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-104">This topic describes the difference between complete media types and partial media types.</span></span>

## <a name="complete-media-types"></a><span data-ttu-id="0aaa5-105">完整媒體類型</span><span class="sxs-lookup"><span data-stu-id="0aaa5-105">Complete Media Types</span></span>

<span data-ttu-id="0aaa5-106">完整的媒體類型是 *完整* 定義媒體資料流程格式的類型。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-106">A *complete* media type is one that fully defines the format of the media stream.</span></span> <span data-ttu-id="0aaa5-107">由於有完整的媒體類型，管線元件可以剖析與媒體類型相關聯的資料流程資料，而不會有任何混淆。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-107">Given a complete media type, a pipeline component can parse the stream data associated with the media type, with no ambiguity.</span></span>

<span data-ttu-id="0aaa5-108">針對未壓縮的格式，下列主題會定義完整媒體類型所需的屬性：</span><span class="sxs-lookup"><span data-stu-id="0aaa5-108">For uncompressed formats, the following topics define the attributes that are required for a complete media type:</span></span>

-   <span data-ttu-id="0aaa5-109">音訊： [未壓縮的音訊媒體類型](uncompressed-audio-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="0aaa5-109">Audio: [Uncompressed Audio Media Types](uncompressed-audio-media-types.md)</span></span>
-   <span data-ttu-id="0aaa5-110">影片： [未壓縮的影片媒體類型](uncompressed-video-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="0aaa5-110">Video: [Uncompressed Video Media Types](uncompressed-video-media-types.md)</span></span>

<span data-ttu-id="0aaa5-111">針對壓縮的 (或 *編碼* 的) 資料流程，完整媒體類型的定義是由編解碼器定義。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-111">For compressed (or *encoded*) streams, the definition of a complete media type is defined by the codec.</span></span> <span data-ttu-id="0aaa5-112">但是，如果壓縮的資料流程知道任何未壓縮的型別屬性，則這些值應該包含在壓縮資料流程的媒體類型中。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-112">However, if any uncompressed type attributes are known for the compressed stream, these values should be included in the media type for the compressed stream.</span></span> <span data-ttu-id="0aaa5-113">例如，如果畫面格大小是已知的，即使技術上已壓縮的資料流程沒有框架大小，也請在媒體類型上設定 [ [**MF \_ MT \_ 框架 \_ 大小**](mf-mt-frame-size-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-113">For example, if the frame size is known, set the [**MF\_MT\_FRAME\_SIZE**](mf-mt-frame-size-attribute.md) attribute on the media type, even though technically a compressed stream does not have a frame size.</span></span>

## <a name="partial-media-types"></a><span data-ttu-id="0aaa5-114">部分媒體類型</span><span class="sxs-lookup"><span data-stu-id="0aaa5-114">Partial Media Types</span></span>

<span data-ttu-id="0aaa5-115">*部分* 媒體類型缺少完整媒體類型所需的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-115">A *partial* media type is lacks one or more of the attributes needed for a complete media type.</span></span> <span data-ttu-id="0aaa5-116">列舉可能的媒體類型時，Microsoft 媒體基礎元件可能會將值保留為未設定，表示它可以處理任何值。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-116">When enumerating possible media types, a Microsoft Media Foundation component may leave a value unset, to indicate that it can handle any value.</span></span> <span data-ttu-id="0aaa5-117">例如，視頻處理器可能會將 [ [**MF \_ MT \_ 幀 \_ 速率**](mf-mt-frame-rate-attribute.md) ] 屬性設定為 [未設定]，表示它可以處理任何畫面播放速率，並且會視需要執行畫面播放速率轉換。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-117">For example, a video processor might leave the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute unset, to indicate that it can handle any frame rate, and will perform a frame-rate conversion if necessary.</span></span>

<span data-ttu-id="0aaa5-118">如果您建立部分媒體類型，您仍然應該包含所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-118">If you create a partial media type, you should still include as much information as you know.</span></span> <span data-ttu-id="0aaa5-119">不過，媒體類型不得包含不確定的資訊。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-119">However, a media type must not include information that is uncertain.</span></span> <span data-ttu-id="0aaa5-120">較不正確的資訊會遺失。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-120">It is better for information to be missing than wrong.</span></span>

<span data-ttu-id="0aaa5-121">部分媒體類型至少應該包含兩個屬性： [**MF \_ mt \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) 和 [**mf \_ mt \_ 子**](mf-mt-subtype-attribute.md)類型。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-121">At a minimum, a partial media type should include just two attributes: [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) and [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md).</span></span>

<span data-ttu-id="0aaa5-122">有時媒體基礎元件必須提供完整的媒體類型：</span><span class="sxs-lookup"><span data-stu-id="0aaa5-122">Sometimes Media Foundation components must provide complete media types:</span></span>

-   <span data-ttu-id="0aaa5-123">媒體來源必須提供完整的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-123">Media sources must provide complete output types.</span></span>
-   <span data-ttu-id="0aaa5-124">在設定輸入類型之後，必須提供完整的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-124">Decoders must provide complete output types, after the input type is set.</span></span> <span data-ttu-id="0aaa5-125">在設定輸入類型之前，解碼器可以提供部分輸出類型。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-125">Before the input type is set, a decoder might provide a partial output type.</span></span>
-   <span data-ttu-id="0aaa5-126">編碼器必須在設定輸出類型之後，提供完整的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-126">Encoders must provide complete input types, after the output type is set.</span></span> <span data-ttu-id="0aaa5-127">在設定輸出類型之前，編碼器可能會提供部分輸入類型。</span><span class="sxs-lookup"><span data-stu-id="0aaa5-127">Before the output type is set, an encoder might provide a partial input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aaa5-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="0aaa5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aaa5-129">媒體類型</span><span class="sxs-lookup"><span data-stu-id="0aaa5-129">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



