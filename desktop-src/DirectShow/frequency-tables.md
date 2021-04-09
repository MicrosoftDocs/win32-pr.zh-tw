---
description: 頻率資料表
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: 頻率資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108541"
---
# <a name="frequency-tables"></a><span data-ttu-id="3ff8b-103">頻率資料表</span><span class="sxs-lookup"><span data-stu-id="3ff8b-103">Frequency Tables</span></span>

<span data-ttu-id="3ff8b-104">電視調諧器篩選器 (kstvtune.ax) 具有頻率資料表的內部清單。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-104">The TV Tuner filter (kstvtune.ax) has an internal list of frequency tables.</span></span> <span data-ttu-id="3ff8b-105">每個頻率資料表都包含頻率清單，並且對應至特定國家/地區的廣播或纜線頻率。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-105">Each frequency table contains a list of frequencies, and corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="3ff8b-106">應用程式會藉由呼叫 [**IAMTuner：:p ui \_ 通道**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) 方法，並以所需的頻率索引來調整為特定的頻率。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-106">An application tunes to a particular frequency by calling the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method with the index of the desired frequency.</span></span>

<span data-ttu-id="3ff8b-107">在某些國家/地區中，頻率資料表的索引編號會直接對應至頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-107">For some countries/regions, the index numbers of the frequency tables map directly to channel numbers.</span></span> <span data-ttu-id="3ff8b-108">不過，固定的通道號碼並非適用于所有市場。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-108">Fixed channel numbers are not appropriate for all markets, however.</span></span> <span data-ttu-id="3ff8b-109">例如，取用者實際上不會使用歐洲頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-109">For instance, the European channel numbers are not actually used by consumers.</span></span> <span data-ttu-id="3ff8b-110">相反地，消費者預期會選擇並為其區域中的廣播或纜線操作員所使用的頻率，指派自己的頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-110">Instead, consumers expect to choose and assign their own channel numbers for the frequencies that are used by the broadcast or cable operators in their area.</span></span> <span data-ttu-id="3ff8b-111">針對這些國家/地區，應用程式不應該直接向使用者公開索引編號。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-111">For these countries/regions, applications should not expose the index numbers directly to the user.</span></span> <span data-ttu-id="3ff8b-112">Instread，應用程式應該將通道號碼之間的內部對應 (呈現給使用者) 和頻率索引 (以進行微調) 。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-112">Instread, the application should keep an internal mapping between channel numbers (presented to the user) and frequency indexes (for tuning).</span></span>

<span data-ttu-id="3ff8b-113">大部分的非美國纜線運算子都可自由地在其選擇的頻率上進行廣播，通常會將不同標準的頻率混合為相同的頻道組合。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-113">Most non-US cable operators are free to broadcast on frequencies of their choosing, often mixing frequencies from different standards into the same channel lineup.</span></span> <span data-ttu-id="3ff8b-114">因此，所有缺少標準纜線通道標準授權單位的國家/地區，都會使用 "Unicable" 頻率表。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-114">Therefore, a "Unicable" frequency table is used for any country/region that lacks a standard cable channel standards authority.</span></span> <span data-ttu-id="3ff8b-115">此外，也會提供一種機制來覆寫頻率資料表中的個別頻率。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-115">Also, a mechanism is provided to override individual frequencies in the frequency tables.</span></span> <span data-ttu-id="3ff8b-116">下一節的 [頻率覆寫](frequency-overrides.md)會說明這項機制。</span><span class="sxs-lookup"><span data-stu-id="3ff8b-116">This mechanism is described in the following section, [Frequency Overrides](frequency-overrides.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ff8b-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ff8b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ff8b-118">國際類比電視微調</span><span class="sxs-lookup"><span data-stu-id="3ff8b-118">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



