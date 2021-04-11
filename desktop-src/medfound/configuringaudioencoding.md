---
description: 設定音訊編碼
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: '設定音訊編碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191078"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a><span data-ttu-id="4c1b6-103">設定音訊編碼 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="4c1b6-103">Configuring Audio Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="4c1b6-104">Windows Media 音訊編碼器會以其完整格式列舉所有支援的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-104">The Windows Media Audio encoder enumerates all of its supported output types in their complete form.</span></span> <span data-ttu-id="4c1b6-105">藉由呼叫 **IMediaObject：： GetOutputType** 或 **IMFTransform：： GetAvailableOutputType** 來取出您想要的類型，然後藉由呼叫 **IMediaObject：： SetOutputType** 或 **IMFTransform：： SetOutputType**，將未改變的取出型別設定為輸出類型。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-105">Retrieve the type that you want by calling **IMediaObject::GetOutputType** or **IMFTransform::GetAvailableOutputType**, and then set the retrieved type, unaltered, as the output type by calling **IMediaObject::SetOutputType** or **IMFTransform::SetOutputType**.</span></span>

<span data-ttu-id="4c1b6-106">音訊編碼器變更支援的輸出媒體類型已設定為編碼器屬性。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-106">The output media types supported by the audio encoder change as encoder properties are configured.</span></span> <span data-ttu-id="4c1b6-107">您必須在列舉輸出類型之前，設定您想要使用的所有編碼器屬性。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-107">You must configure all of the encoder properties you want to use before you enumerate the output type.</span></span>

<span data-ttu-id="4c1b6-108">音訊編碼器支援雙通路和 VBR 模式，但其設定方式不同于影片。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-108">Two-pass and VBR modes are supported by the audio encoders, but are configured differently than for video.</span></span> <span data-ttu-id="4c1b6-109">如需詳細資訊，請參閱 [列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-109">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="4c1b6-110">除非您設定輸出類型，否則無法使用音訊編碼器所支援的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-110">The input types supported by the audio encoder are not available until you set the output type.</span></span> <span data-ttu-id="4c1b6-111">如果您在設定輸出類型之前呼叫 **IMediaObject：： GetInputType** 或 **IMFTransform：： GetInputType** ，此方法會分別傳回 " \_ e \_ no no ITEMS" \_ \_ 或 MFT \_ e no 其他 \_ \_ \_ 類型。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-111">If you call **IMediaObject::GetInputType** or **IMFTransform::GetInputType** before setting an output type, the method returns DMO\_E\_NO\_MORE\_ITEMS or MFT\_E\_NO\_MORE\_TYPES respectively.</span></span> <span data-ttu-id="4c1b6-112">設定輸出類型之後，編碼器會列舉針對所選取輸出類型所支援的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-112">After the output type is set, the encoder enumerates the input types that it supports for the selected output type.</span></span>

<span data-ttu-id="4c1b6-113">Windows Media 音訊編碼器不會執行任何音訊重新取樣。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-113">No audio resampling is performed by the Windows Media Audio encoder.</span></span> <span data-ttu-id="4c1b6-114">這表示編碼器輸出類型和編碼器輸入類型必須有相同數目的通道、每個樣本的位數，以及取樣率。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-114">This means that the encoder output type and the encoder input type must have the same number of channels, bits per sample, and sample rate.</span></span> <span data-ttu-id="4c1b6-115">如需詳細資訊，請參閱 [尋找音訊編碼器輸出類型](findingaudioencoderoutputtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-115">For more information, see [Finding Audio Encoder Output Types](findingaudioencoderoutputtypes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="4c1b6-116">音訊編碼器所列舉的每個輸出類型都包含 **WAVEFORMATEX** 結構， (由 **AM \_ 媒體 \_ 類型指向。 pbFormat**) 並附加擴充的資料。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-116">Each output type enumerated by the audio encoder contains a **WAVEFORMATEX** structure (pointed to by **AM\_MEDIA\_TYPE.pbFormat**) with extended data appended to it.</span></span> <span data-ttu-id="4c1b6-117">擴充資料的大小是由 **WAVEFORMATEX. cbSize** 所指定。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-117">The size of the extended data is specified by **WAVEFORMATEX.cbSize**.</span></span> <span data-ttu-id="4c1b6-118">這種資料必須與編碼的內容一起保存，才能傳遞給解碼器。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-118">This data must be kept with the encoded content so that it can be delivered to the decoder.</span></span> <span data-ttu-id="4c1b6-119">如果沒有延伸格式資料，就無法解壓縮內容。</span><span class="sxs-lookup"><span data-stu-id="4c1b6-119">The content cannot be decompressed without the extended format data.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4c1b6-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c1b6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c1b6-121">使用音訊</span><span class="sxs-lookup"><span data-stu-id="4c1b6-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



