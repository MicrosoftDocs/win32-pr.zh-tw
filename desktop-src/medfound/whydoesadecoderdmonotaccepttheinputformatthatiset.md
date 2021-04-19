---
description: 為什麼解碼器不接受我設定的輸入格式？
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: 為什麼解碼器不接受我設定的輸入格式？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977840"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a><span data-ttu-id="9c568-103">為什麼解碼器不接受我設定的輸入格式？</span><span class="sxs-lookup"><span data-stu-id="9c568-103">Why does a decoder not accept the input format that I set?</span></span>

<span data-ttu-id="9c568-104">有許多原因會導致解碼器拒絕格式。</span><span class="sxs-lookup"><span data-stu-id="9c568-104">There are many reasons why a decoder might reject a format.</span></span> <span data-ttu-id="9c568-105">最常見的是遺失或不正確的延伸格式資料。</span><span class="sxs-lookup"><span data-stu-id="9c568-105">The most common is missing or incorrect extended format data.</span></span> <span data-ttu-id="9c568-106">擴充格式資料是附加至描述媒體類型結構的編解碼器特定資訊。</span><span class="sxs-lookup"><span data-stu-id="9c568-106">The extended format data is codec-specific information that is appended to the structure describing the media type.</span></span>

<span data-ttu-id="9c568-107">當您使用編碼器物件來列舉輸出型別時， **pbFormat** 成員會指向 **WAVEFORMATEX** [**結構。 \_ \_**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)</span><span class="sxs-lookup"><span data-stu-id="9c568-107">When you enumerate an output type using an encoder object, the **pbFormat** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure will point to a **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="9c568-108">此結構會附加延伸格式資料，而該資料的大小會儲存在 **WAVEFORMATEX. cbSize** 成員中。</span><span class="sxs-lookup"><span data-stu-id="9c568-108">This structure has extended format data appended to it, and the size of that data is stored in the **WAVEFORMATEX.cbSize** member.</span></span> <span data-ttu-id="9c568-109">無論使用哪一個容器來儲存壓縮的資料，您都必須保存 **WAVEFORMATEX** 結構，並將它用於此解碼器的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="9c568-109">Regardless of the container used to store the compressed data, you must persist the **WAVEFORMATEX** structure and use it in the input type for the decoder.</span></span> <span data-ttu-id="9c568-110">如果沒有延伸格式資料，則解碼器無法解壓縮內容。</span><span class="sxs-lookup"><span data-stu-id="9c568-110">Without the extended format data, the decoder cannot decompress the content.</span></span>

<span data-ttu-id="9c568-111">針對影片格式，您必須手動抓取延伸格式的資料，並將其附加至 **VIDEOINFOHEADER** 結構。</span><span class="sxs-lookup"><span data-stu-id="9c568-111">For video formats, you must manually retrieve the extended format data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="9c568-112">如需詳細資訊，請參閱 [使用影片編解碼器私用資料](usingvideocodecprivatedata.md)。</span><span class="sxs-lookup"><span data-stu-id="9c568-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c568-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c568-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c568-114">常見問題集</span><span class="sxs-lookup"><span data-stu-id="9c568-114">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 
