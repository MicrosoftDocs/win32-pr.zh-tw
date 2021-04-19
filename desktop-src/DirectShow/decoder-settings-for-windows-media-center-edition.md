---
description: Windows Media Center Edition 的解碼器設定
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Windows Media Center Edition 的解碼器設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106975599"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a><span data-ttu-id="02e5d-103">Windows Media Center Edition 的解碼器設定</span><span class="sxs-lookup"><span data-stu-id="02e5d-103">Decoder Settings for Windows Media Center Edition</span></span>

<span data-ttu-id="02e5d-104">Windows XP Media Center Edition 2005 和更新版本會使用 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) 介面來設定音訊解碼篩選器，以進行電視和 DVD 播放。</span><span class="sxs-lookup"><span data-stu-id="02e5d-104">Windows XP Media Center Edition 2005 and later uses the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to configure the audio decoder filter for television and DVD playback.</span></span> <span data-ttu-id="02e5d-105">以下是支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="02e5d-105">The following properties are supported.</span></span>



| <span data-ttu-id="02e5d-106">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="02e5d-106">Property GUID</span></span>                   | <span data-ttu-id="02e5d-107">Description</span><span class="sxs-lookup"><span data-stu-id="02e5d-107">Description</span></span>                                      |
|---------------------------------|--------------------------------------------------|
| <span data-ttu-id="02e5d-108">CODECAPI \_ 音訊 \_ 輸出 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="02e5d-108">CODECAPI\_AUDIO\_OUTPUT\_FORMAT</span></span> | <span data-ttu-id="02e5d-109">設定音訊輸出格式。</span><span class="sxs-lookup"><span data-stu-id="02e5d-109">Configures the audio output format.</span></span> <span data-ttu-id="02e5d-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="02e5d-110">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="02e5d-111">備註</span><span class="sxs-lookup"><span data-stu-id="02e5d-111">Remarks</span></span>

<span data-ttu-id="02e5d-112">CODECAPI \_ 音訊 \_ 輸出格式屬性的值 \_ 是 GUID 的字串表示，儲存為 **BSTR** 值。</span><span class="sxs-lookup"><span data-stu-id="02e5d-112">The value of the CODECAPI\_AUDIO\_OUTPUT\_FORMAT property is a string representation of a GUID, stored as a **BSTR** value.</span></span> <span data-ttu-id="02e5d-113">定義了下列 Guid。</span><span class="sxs-lookup"><span data-stu-id="02e5d-113">The following GUIDs are defined.</span></span>



| <span data-ttu-id="02e5d-114">GUID</span><span class="sxs-lookup"><span data-stu-id="02e5d-114">GUID</span></span>                                                        | <span data-ttu-id="02e5d-115">Description</span><span class="sxs-lookup"><span data-stu-id="02e5d-115">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e5d-116">CODECAPI \_ 音訊 \_ 輸出 \_ 格式 \_ PCM \_ 身歷聲 \_ MATRIXENCODED</span><span class="sxs-lookup"><span data-stu-id="02e5d-116">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO\_MATRIXENCODED</span></span> | <span data-ttu-id="02e5d-117">軟體音訊篩選器應該執行軟體解碼並輸出身歷聲音訊串流，並將多頻道音訊矩陣編碼為兩個通道。</span><span class="sxs-lookup"><span data-stu-id="02e5d-117">The software audio filter should perform software decoding and output a stereo audio stream, with the multichannel audio matrix encoded to the two channels.</span></span>                                                   |
| <span data-ttu-id="02e5d-118">CODECAPI \_ 音訊 \_ 輸出 \_ 格式 \_ PCM \_ 身歷聲</span><span class="sxs-lookup"><span data-stu-id="02e5d-118">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO</span></span>                | <span data-ttu-id="02e5d-119">軟體音訊篩選器應該執行軟體解碼並輸出身歷聲音訊串流。</span><span class="sxs-lookup"><span data-stu-id="02e5d-119">The software audio filter should perform software decoding and output a stereo audio stream.</span></span>                                                                                                                   |
| <span data-ttu-id="02e5d-120">CODECAPI \_ 音訊 \_ 輸出 \_ 格式的 \_ SPDIF \_ PCM</span><span class="sxs-lookup"><span data-stu-id="02e5d-120">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="02e5d-121">軟體音訊篩選器應該執行軟體音訊解碼，雖然電腦的實體輸出可能是數位介面，例如 S/PDIF。</span><span class="sxs-lookup"><span data-stu-id="02e5d-121">The software audio filter should perform software audio decoding, even though the physical output from the PC may be a digital interface, such as S/PDIF.</span></span>                                                      |
| <span data-ttu-id="02e5d-122">CODECAPI \_ 音訊 \_ 輸出 \_ 格式的 \_ SPDIF \_ 位流</span><span class="sxs-lookup"><span data-stu-id="02e5d-122">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_BITSTREAM</span></span>           | <span data-ttu-id="02e5d-123">軟體音訊篩選器不應該執行軟體音訊解碼，但應該透過連接到數位音訊連結的裝置（例如 S/PDIF），傳遞原始數位音訊位流進行外部處理。</span><span class="sxs-lookup"><span data-stu-id="02e5d-123">The software audio filter should not perform software audio decoding, but should pass the raw digital audio bitstream for external processing by a device connected with a digital audio link, such as S/PDIF.</span></span> |
| <span data-ttu-id="02e5d-124">CODECAPI \_ 音訊 \_ 輸出 \_ 格式 \_ PCM \_ 耳機</span><span class="sxs-lookup"><span data-stu-id="02e5d-124">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_HEADPHONES</span></span>            | <span data-ttu-id="02e5d-125">軟體音訊篩選器應該執行軟體音訊解碼，並且應該套用專屬處理以針對耳機進行優化。</span><span class="sxs-lookup"><span data-stu-id="02e5d-125">The software audio filter should perform software audio decoding and should apply proprietary processing to optimize for headphones.</span></span> <span data-ttu-id="02e5d-126">這項設定的支援是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="02e5d-126">Support for this setting is optional.</span></span>                                     |



 

> [!Note]  
> <span data-ttu-id="02e5d-127">**ICodecAPI** 介面會將編解碼器屬性儲存為索引鍵/值組，其中索引鍵是 GUID，而值則是 **VARIANT** 型別。</span><span class="sxs-lookup"><span data-stu-id="02e5d-127">The **ICodecAPI** interface stores codec properties as key/value pairs, where the key is a GUID and the value is a **VARIANT** type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="02e5d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="02e5d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02e5d-129">編碼器和解碼器開發</span><span class="sxs-lookup"><span data-stu-id="02e5d-129">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



