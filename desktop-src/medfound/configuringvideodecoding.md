---
description: 設定影片解碼
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: '設定影片解碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973197"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a><span data-ttu-id="0c698-103">設定影片解碼 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="0c698-103">Configuring Video Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="0c698-104">解碼基本上與編碼方式相反，因為設定方面。</span><span class="sxs-lookup"><span data-stu-id="0c698-104">Decoding is essentially the opposite of encoding in terms of configuration.</span></span> <span data-ttu-id="0c698-105">此解碼器支援極少的屬性，而且不需要它們。</span><span class="sxs-lookup"><span data-stu-id="0c698-105">The decoder supports very few properties, and none of them is required.</span></span> <span data-ttu-id="0c698-106">將輸入類型設定為用於解碼器輸出的類型 (包括編解碼器私用資料) 。</span><span class="sxs-lookup"><span data-stu-id="0c698-106">Set the input type to the type used for the decoder output (including the codec private data).</span></span> <span data-ttu-id="0c698-107">然後，將輸出設定為所需的未壓縮格式、設定 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構以反映適當的框架大小，以及開始處理範例。</span><span class="sxs-lookup"><span data-stu-id="0c698-107">Then set the output to the desired uncompressed format, set the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to reflect the proper frame size, and start processing samples.</span></span>

<span data-ttu-id="0c698-108">您必須提供具有媒體類型的解碼器，其中包含緊接在 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構後面的編解碼器私用資料。</span><span class="sxs-lookup"><span data-stu-id="0c698-108">You must supply the decoder with a media type that includes the codec private data positioned immediately after the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="0c698-109">如果沒有此資料，則無法將內容解碼。</span><span class="sxs-lookup"><span data-stu-id="0c698-109">The decoder cannot decode the content without this data.</span></span> <span data-ttu-id="0c698-110">此解碼器所執行的格式驗證不會驗證私用資料。</span><span class="sxs-lookup"><span data-stu-id="0c698-110">The format validation performed by the decoder does not validate the private data.</span></span> <span data-ttu-id="0c698-111">如果編解碼器私用資料遺失或不正確，則編碼器會以位資料流程損毀的方式回應。</span><span class="sxs-lookup"><span data-stu-id="0c698-111">If the codec private data is missing or incorrect, the decoder responds as if the bit stream is corrupted.</span></span> <span data-ttu-id="0c698-112">如需詳細資訊，請參閱 [使用影片編解碼器私用資料](usingvideocodecprivatedata.md)。</span><span class="sxs-lookup"><span data-stu-id="0c698-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c698-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c698-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c698-114">使用影片編解碼器私用資料</span><span class="sxs-lookup"><span data-stu-id="0c698-114">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="0c698-115">使用影片</span><span class="sxs-lookup"><span data-stu-id="0c698-115">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
