---
description: 類比電視微調
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: 類比電視微調
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b85d0826340b913df88cb20dc538bc85943949b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970895"
---
# <a name="analog-television-tuning"></a><span data-ttu-id="accce-103">類比電視微調</span><span class="sxs-lookup"><span data-stu-id="accce-103">Analog Television Tuning</span></span>

<span data-ttu-id="accce-104">微調是透過 [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) 介面，由電視調諧器篩選器所控制。</span><span class="sxs-lookup"><span data-stu-id="accce-104">Tuning is controlled by the TV Tuner filter, through the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="accce-105">IAMTVTuner 介面會繼承 IAMTuner。</span><span class="sxs-lookup"><span data-stu-id="accce-105">The IAMTVTuner interface inherits IAMTuner.</span></span> <span data-ttu-id="accce-106">若要取得介面的指標，請呼叫 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="accce-106">To obtain a pointer to the interface, call the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method as follows:</span></span>


```C++
IAMTVTuner *pTuner = NULL;
hr = pBuild->FindInterface(
    &LOOK_UPSTREAM_ONLY,  // Look upstream from pCap.
    NULL,                 // No particular media type.
    pCap,                 // Pointer to the capture filter.
    IID_IAMTVTuner, (void**)&pTuner);
if (SUCCEEDED(hr))
{
    // Use pTuner ...
    pTuner->Release();
}
```



<span data-ttu-id="accce-107">第一個參數表示要從 capture 篩選準則搜尋上游。</span><span class="sxs-lookup"><span data-stu-id="accce-107">The first parameter indicates to search upstream from the capture filter.</span></span>

<span data-ttu-id="accce-108">頻率資料表</span><span class="sxs-lookup"><span data-stu-id="accce-108">Frequency Tables</span></span>

<span data-ttu-id="accce-109">就內部而言，TV 調諧器篩選器會保留頻率資料表的清單。</span><span class="sxs-lookup"><span data-stu-id="accce-109">Internally, the TV Tuner filter keeps a list of frequency tables.</span></span> <span data-ttu-id="accce-110">每個頻率資料表都會對應到指定國家/地區的廣播或纜線頻率。</span><span class="sxs-lookup"><span data-stu-id="accce-110">Each frequency table corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="accce-111">另外還有一般的「Unicable」頻率表，當國家/地區沒有一組標準的頻率指派時，就會使用此資料表。</span><span class="sxs-lookup"><span data-stu-id="accce-111">There is also a generic "Unicable" frequency table, which is used when a country/region does not have a standard set of frequency assignments.</span></span>

<span data-ttu-id="accce-112">每個頻率資料表都包含微調頻率的清單。</span><span class="sxs-lookup"><span data-stu-id="accce-112">Each frequency table contains a list of tuning frequencies.</span></span> <span data-ttu-id="accce-113">在某些國家/地區中，資料表中的索引會直接對應至通道編號，換句話說，channel n 的頻率是資料表中的第 n 個專案。</span><span class="sxs-lookup"><span data-stu-id="accce-113">For some countries/regions, the indexes in the table correspond directly to channel numbers — in other words, the frequency for channel n is the n th entry in the table.</span></span> <span data-ttu-id="accce-114">不過，在某些國家/地區中，頻道號碼和頻率之間並沒有直接的對應關係。</span><span class="sxs-lookup"><span data-stu-id="accce-114">For some countries/regions, however, there is no direct correspondence between channel numbers and frequencies.</span></span> <span data-ttu-id="accce-115">在這種情況下，應用程式必須保留一個清單，將通道編號 (通常是由使用者) 的頻率資料表專案所選擇。</span><span class="sxs-lookup"><span data-stu-id="accce-115">In that case, the application must keep a list that maps channel numbers (typically chosen by the user) to frequency table entries.</span></span> <span data-ttu-id="accce-116">例如，使用者在 frequency 資料表中看到的「channel 5」可能是專案編號12。</span><span class="sxs-lookup"><span data-stu-id="accce-116">For example, what the user sees as "channel 5" might be entry number 12 in the frequency table.</span></span>

<span data-ttu-id="accce-117">如需詳細資訊，請參閱 [國際類比電視微調](international-analog-tv-tuning.md)。</span><span class="sxs-lookup"><span data-stu-id="accce-117">For details, see [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span>

<span data-ttu-id="accce-118">基本調整作業</span><span class="sxs-lookup"><span data-stu-id="accce-118">Basic Tuning Operations</span></span>

<span data-ttu-id="accce-119">如果調諧器支援多種接收模式（例如電視和 FM 電臺），請呼叫 [**IAMTuner：:p ui \_ 模式**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) 來選取模式。</span><span class="sxs-lookup"><span data-stu-id="accce-119">If the tuner supports multiple reception modes, such as television and FM radio, call [**IAMTuner::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) to select the mode.</span></span> <span data-ttu-id="accce-120">[**IAMTuner：： GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes)方法會傳回檔諧器所支援的所有模式。</span><span class="sxs-lookup"><span data-stu-id="accce-120">The [**IAMTuner::GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) method returns all of the modes that the tuner supports.</span></span> <span data-ttu-id="accce-121">例如，下列程式碼會檢查調諧器是否支援 FM 無線電，如果是，則切換至該模式。</span><span class="sxs-lookup"><span data-stu-id="accce-121">For example, the following code checks whether the tuner supports FM radio, and if so, switches to that mode.</span></span>


```C++
// Check whether the mode is supported.
long lModes = 0;
hr = m_pTuner->GetAvailableModes(&lModes);
if (SUCCEEDED(hr) && (lModes & AMTUNER_MODE_FM_RADIO))
{
    // Set the mode.
    hr = pTuner->put_Mode(AMTUNER_MODE_FM_RADIO);
}
```



<span data-ttu-id="accce-122">若要設定國家/地區，請呼叫 [**IAMTuner：:p 的 \_ CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) 方法。</span><span class="sxs-lookup"><span data-stu-id="accce-122">To set the country/region, call the [**IAMTuner::put\_CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) method.</span></span> <span data-ttu-id="accce-123">調諧器會使用此值來選取適當的頻率資料表。</span><span class="sxs-lookup"><span data-stu-id="accce-123">The tuner uses this value to select the appropriate frequency table.</span></span> <span data-ttu-id="accce-124">如需詳細資訊，請參閱 [國家/地區指派](country-region-assignments.md) 。</span><span class="sxs-lookup"><span data-stu-id="accce-124">See [Country/Region Assignments](country-region-assignments.md) for more information.</span></span>

<span data-ttu-id="accce-125">若要設定通道，請呼叫 [**IAMTuner：:p ui \_ 通道**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) 方法。</span><span class="sxs-lookup"><span data-stu-id="accce-125">To set the channel, call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method.</span></span> <span data-ttu-id="accce-126">這個方法的引數實際上不是通道編號，而是目前頻率資料表的索引。</span><span class="sxs-lookup"><span data-stu-id="accce-126">The argument to this method is actually not a channel number, but rather an index into the current frequency table.</span></span> <span data-ttu-id="accce-127">如先前所述，索引編號不一定會對應至頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="accce-127">As described previously, the index number may or may not correspond to a channel number.</span></span> <span data-ttu-id="accce-128">[**IAMTuner：： ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax)方法會傳回目前頻率資料表的最小和最大索引值。</span><span class="sxs-lookup"><span data-stu-id="accce-128">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method returns the minimum and maximum index values for the current frequency table.</span></span>

<span data-ttu-id="accce-129">覆寫頻率專案</span><span class="sxs-lookup"><span data-stu-id="accce-129">Overriding Frequency Entries</span></span>

<span data-ttu-id="accce-130">頻率資料表中的某些專案可能不正確或已過時。</span><span class="sxs-lookup"><span data-stu-id="accce-130">It is possible that some entries in the frequency tables might be incorrect or become obsolete.</span></span> <span data-ttu-id="accce-131">因此，提供使用登錄機碼覆寫個別專案的機制。</span><span class="sxs-lookup"><span data-stu-id="accce-131">Therefore, a mechanism is provided for overriding individual entries using registry keys.</span></span>

<span data-ttu-id="accce-132">「 [國際類比電視微調](international-analog-tv-tuning.md)」主題將說明這些細節。</span><span class="sxs-lookup"><span data-stu-id="accce-132">The specifics are explained in the topic [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span> <span data-ttu-id="accce-133">每個登錄機碼會定義包含一或多個子機碼的「微調空間」。</span><span class="sxs-lookup"><span data-stu-id="accce-133">Each registry key defines a "tuning space" which contains one or more subkeys.</span></span> <span data-ttu-id="accce-134">每個子機碼都會覆寫一個頻率專案。</span><span class="sxs-lookup"><span data-stu-id="accce-134">Each subkey overrides one frequency entry.</span></span> <span data-ttu-id="accce-135">若要設定目前的微調空間，請使用 [**IAMTuner：:p 的 \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) 方法。</span><span class="sxs-lookup"><span data-stu-id="accce-135">To set the current tuning space, use the [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method.</span></span> <span data-ttu-id="accce-136">啟用微調空間會覆寫目前頻率資料表中的頻率專案。</span><span class="sxs-lookup"><span data-stu-id="accce-136">Activating the tuning space overrides the frequency entries in the current frequency table.</span></span> <span data-ttu-id="accce-137">因此，應用程式會負責維護微調空間與國家/地區之間的對應。</span><span class="sxs-lookup"><span data-stu-id="accce-137">Therefore, it is up to the application to maintain a correspondence between tuning spaces and countries/regions.</span></span> <span data-ttu-id="accce-138">最好的方法是使用國家/地區識別碼作為微調空間的名稱。</span><span class="sxs-lookup"><span data-stu-id="accce-138">The best approach is simply to use the country/region identifier as the name of the tuning space.</span></span>

<span data-ttu-id="accce-139">微調頻率專案</span><span class="sxs-lookup"><span data-stu-id="accce-139">Fine Tuning the Frequency Entries</span></span>

<span data-ttu-id="accce-140">廣播頻率可能會由廣播站向上或向下調整數個 kHz，以減少可能與鄰近通道的干擾。</span><span class="sxs-lookup"><span data-stu-id="accce-140">Broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span> <span data-ttu-id="accce-141">根據名義頻率，調諧器介面卡可以掃描確切的頻率。</span><span class="sxs-lookup"><span data-stu-id="accce-141">Given the nominal frequency, the tuner card can scan for the exact frequency.</span></span> <span data-ttu-id="accce-142">電視調諧器篩選器有一種機制，可在登錄中儲存已調整的頻率。</span><span class="sxs-lookup"><span data-stu-id="accce-142">The TV Tuner filter has a mechanism for saving the adjusted frequencies in the registry.</span></span>

<span data-ttu-id="accce-143">針對 frequency 資料表中的每個專案，呼叫 put \_ 通道方法以調整為該頻率。</span><span class="sxs-lookup"><span data-stu-id="accce-143">For each entry in the frequency table, call the put\_Channel method to tune to that frequency.</span></span> <span data-ttu-id="accce-144">調諧器會掃描最精確的頻率。</span><span class="sxs-lookup"><span data-stu-id="accce-144">The tuner will scan for the most precise frequency.</span></span> <span data-ttu-id="accce-145">您可以藉由呼叫 [**IAMTuner：： SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent)，檢查調諧器是否達到水準鎖定。</span><span class="sxs-lookup"><span data-stu-id="accce-145">You can check whether the tuner achieved a horizontal lock by calling [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span></span> <span data-ttu-id="accce-146">電視調諧器篩選器也會在內部儲存結果。</span><span class="sxs-lookup"><span data-stu-id="accce-146">The TV Tuner filter also stores the result internally.</span></span>

<span data-ttu-id="accce-147">掃描所有頻率之後，請呼叫 [**IAMTVTuner：： StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) 方法，將更新的值寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="accce-147">After scanning all of the frequencies, call the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method to write the updated values into the registry.</span></span> <span data-ttu-id="accce-148">更新的值會儲存在目前微調空間的登錄專案下。</span><span class="sxs-lookup"><span data-stu-id="accce-148">The updated values are stored under the registry entry for the current tuning space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="accce-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="accce-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="accce-150">類比電視</span><span class="sxs-lookup"><span data-stu-id="accce-150">Analog Television</span></span>](analog-television.md)
</dt> </dl>

 

 



