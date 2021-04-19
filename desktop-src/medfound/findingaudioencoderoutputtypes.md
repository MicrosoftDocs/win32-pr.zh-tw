---
description: 尋找音訊編碼器輸出類型
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: '尋找音訊編碼器輸出類型 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972581"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a><span data-ttu-id="771f3-103">尋找音訊編碼器輸出類型 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="771f3-103">Finding Audio Encoder Output Types (Microsoft Media Foundation)</span></span>

<span data-ttu-id="771f3-104">因為您必須使用音訊編碼器所列舉的音訊編碼器輸出格式，所以您需要尋找最適合您需求的格式。</span><span class="sxs-lookup"><span data-stu-id="771f3-104">Because you must use an audio encoder output format that is enumerated by the audio encoder, you need to have a way of finding the format that is most suited to your needs.</span></span> <span data-ttu-id="771f3-105">您所選擇之輸出的通道數目、每個樣本位數，以及所選輸出的取樣率必須符合您壓縮之內容的值。</span><span class="sxs-lookup"><span data-stu-id="771f3-105">The number of channels, bits per sample, and sample rate of the output that you choose must match the values for the content that you compress.</span></span> <span data-ttu-id="771f3-106">不過，編碼器可能會支援這些條件約束中的數種類型。</span><span class="sxs-lookup"><span data-stu-id="771f3-106">However, the encoder may support several types within these constraints.</span></span>

<span data-ttu-id="771f3-107">選擇類型的決定因素是編碼資料流程的位元速率。您想要尋找符合輸入的媒體類型，並具有比目標值更接近的位元速率。</span><span class="sxs-lookup"><span data-stu-id="771f3-107">The deciding factor for choosing a type is the bit rate of the encoded stream; you want to find a media type that matches your input and has a bit rate that is as close as possible to a target value.</span></span> <span data-ttu-id="771f3-108">如果您要列舉一次執行的 VBR 輸出類型，它是決定您所使用類型的品質值。</span><span class="sxs-lookup"><span data-stu-id="771f3-108">If you are enumerating one-pass VBR output types, it is the quality value that will decide the type you use.</span></span> <span data-ttu-id="771f3-109">如需有關列舉輸出型別中之品質值的詳細資訊，請參閱 [列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)。</span><span class="sxs-lookup"><span data-stu-id="771f3-109">For more information about quality values in enumerated output types, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="771f3-110">音訊編碼器以幾乎所有方式列舉其他類型的部分類型。</span><span class="sxs-lookup"><span data-stu-id="771f3-110">The audio encoder enumerates some types that are duplicates of other types in almost all ways.</span></span> <span data-ttu-id="771f3-111">這些重複的格式存在，其中每秒的封包數不符合在與影片同步時，ASF 檔案中儲存的需求。</span><span class="sxs-lookup"><span data-stu-id="771f3-111">These duplicates exist for formats where the number of packets per second does not meet the requirements for storage in ASF files when synchronized with video.</span></span> <span data-ttu-id="771f3-112">在 ASF 檔案中與影片同步處理的音訊，每秒必須有3個或更多的封包，而且位元速率小於32000，每秒5個或更多個封包的位元速率大於或等於32000。</span><span class="sxs-lookup"><span data-stu-id="771f3-112">Audio synchronized with video in an ASF file must have 3 or more packets per second for bit rates less than 32000, and 5 or more packets per second for bit rates greater than or equal to 32000.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="771f3-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="771f3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="771f3-114">設定音訊編碼</span><span class="sxs-lookup"><span data-stu-id="771f3-114">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="771f3-115">列舉特定編碼模式的音訊類型</span><span class="sxs-lookup"><span data-stu-id="771f3-115">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



