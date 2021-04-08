---
description: 若要取得每個辨識結果的信賴層級，您可以取得 RecognitionAlternate 物件的信賴屬性或手勢物件的信賴屬性。
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: 信賴屬性 [關於辨識]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f436d17d5cb83901c7d19ef4beb6dfb7ce6199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847690"
---
# <a name="confidence-property-about-recognition"></a><span data-ttu-id="b3c30-103">關於辨識的信賴財產 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3c30-103">Confidence Property \[About Recognition\]</span></span>

<span data-ttu-id="b3c30-104">若要取得每個辨識結果的信賴層級，您可以取得 [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate)物件的 [**信賴**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence)屬性或 [**手勢**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)物件的 [**信賴**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence)屬性。</span><span class="sxs-lookup"><span data-stu-id="b3c30-104">To obtain a level of confidence for each recognition result, you can get either the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) property of the [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object or the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) property of the [**Gesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object.</span></span> <span data-ttu-id="b3c30-105">信賴等級是一個數位，指出辨識器針對對應辨識區段傳回的每個替代辨識結果的信賴程度。</span><span class="sxs-lookup"><span data-stu-id="b3c30-105">The confidence level is a number that indicates the degree of confidence for each alternate recognition result that the recognizer returns for a corresponding recognition segment.</span></span>

<span data-ttu-id="b3c30-106">信賴度會以低、平均或高的方式傳回。</span><span class="sxs-lookup"><span data-stu-id="b3c30-106">Confidence is returned as low, average, or high.</span></span> <span data-ttu-id="b3c30-107">應用程式會使用這些結果來：</span><span class="sxs-lookup"><span data-stu-id="b3c30-107">The application uses these results to:</span></span>

-   <span data-ttu-id="b3c30-108">向使用者表示有多個可能存在。</span><span class="sxs-lookup"><span data-stu-id="b3c30-108">Indicate to the user that multiple possibilities exist.</span></span>
-   <span data-ttu-id="b3c30-109">依信賴等級排列替代項的次序。</span><span class="sxs-lookup"><span data-stu-id="b3c30-109">Rank the alternates by confidence level.</span></span>

## <a name="what-affects-confidence"></a><span data-ttu-id="b3c30-110">信賴度的影響</span><span class="sxs-lookup"><span data-stu-id="b3c30-110">What Affects Confidence</span></span>

<span data-ttu-id="b3c30-111">某些讓手寫辨識難以和影響信賴的事項包括：</span><span class="sxs-lookup"><span data-stu-id="b3c30-111">Some of the things that make handwriting recognition difficult and affect confidence include:</span></span>

-   <span data-ttu-id="b3c30-112">難以判斷文字分割</span><span class="sxs-lookup"><span data-stu-id="b3c30-112">Difficulty determining word segmentation</span></span>

![顯示寫入太近的影像](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   <span data-ttu-id="b3c30-114">案例問題</span><span class="sxs-lookup"><span data-stu-id="b3c30-114">Case difficulties</span></span>

![顯示「案例」一字手寫版本問題的影像](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   <span data-ttu-id="b3c30-116">不常見的書寫樣式</span><span class="sxs-lookup"><span data-stu-id="b3c30-116">Uncommon writing styles</span></span>
-   <span data-ttu-id="b3c30-117">獨立標點符號</span><span class="sxs-lookup"><span data-stu-id="b3c30-117">Isolated punctuation</span></span>

![顯示太遠離文字之引號的影像](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   <span data-ttu-id="b3c30-119">英文辨識器中的重音字元</span><span class="sxs-lookup"><span data-stu-id="b3c30-119">Accented characters in English recognizers</span></span>

> [!Note]  
> <span data-ttu-id="b3c30-120">信賴評估僅適用于美國英文和此版本中的所有手勢辨識器。</span><span class="sxs-lookup"><span data-stu-id="b3c30-120">Confidence evaluation is available only for United States English and all gesture recognizers in this release.</span></span> <span data-ttu-id="b3c30-121">提供其他辨識器信賴屬性的方法會傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="b3c30-121">Methods that provide the confidence property for any other recognizer will return **E\_NOTIMPL**.</span></span>

 

 

 



