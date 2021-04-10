---
description: 當我從相同物件取出格式時，為什麼影片編碼器會拒絕我嘗試設定的輸出格式？
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: 當我從相同物件取出格式時，為什麼影片編碼器會拒絕我嘗試設定的輸出格式？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026525"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a><span data-ttu-id="e2c3b-103">當我從相同物件取出格式時，為什麼影片編碼器會拒絕我嘗試設定的輸出格式？</span><span class="sxs-lookup"><span data-stu-id="e2c3b-103">Why does the video encoder reject an output format that I try to set, when I retrieved the format from the same object?</span></span>

<span data-ttu-id="e2c3b-104">與音訊編碼器輸出類型不同的是，影片編碼器所列舉的支援輸出不會如傳遞完成。</span><span class="sxs-lookup"><span data-stu-id="e2c3b-104">Unlike audio encoder output types, the supported outputs enumerated by the video encoders are not complete as delivered.</span></span> <span data-ttu-id="e2c3b-105">您必須在 **VIDEOINFOHEADER** 結構的 **dwBitrate** 成員中設定資料流程的位元速率，以符合針對 [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)屬性所設定的值。</span><span class="sxs-lookup"><span data-stu-id="e2c3b-105">You must set the bit rate of the stream in the **dwBitrate** member of the **VIDEOINFOHEADER** structure to match the value set for the [MFPKEY\_RAVG](mfpkey-ravgproperty.md) property.</span></span>

<span data-ttu-id="e2c3b-106">當所有選項都設定為您想要的方式之後，您必須抓取編解碼器私用資料，並將它附加至 **VIDEOINFOHEADER** 結構。</span><span class="sxs-lookup"><span data-stu-id="e2c3b-106">After all of the options are set the way that you want them, you must retrieve the codec private data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="e2c3b-107">如需詳細資訊，請參閱 [使用影片編解碼器私用資料](usingvideocodecprivatedata.md)。</span><span class="sxs-lookup"><span data-stu-id="e2c3b-107">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2c3b-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="e2c3b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2c3b-109">常見問題集</span><span class="sxs-lookup"><span data-stu-id="e2c3b-109">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



