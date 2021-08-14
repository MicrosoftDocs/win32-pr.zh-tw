---
description: 類比電視微調
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: 類比電視微調
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ae14407b1e0c9e7062e7813d88a832cc29bd926ff57b17f2933abeef44b21dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001576"
---
# <a name="analog-television-tuning"></a>類比電視微調

微調是透過 [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) 介面，由電視調諧器篩選器所控制。 IAMTVTuner 介面會繼承 IAMTuner。 若要取得介面的指標，請呼叫 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 方法，如下所示：


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



第一個參數表示要從 capture 篩選準則搜尋上游。

頻率資料表

就內部而言，TV 調諧器篩選器會保留頻率資料表的清單。 每個頻率資料表都會對應到指定國家/地區的廣播或纜線頻率。 另外還有一般的「Unicable」頻率表，當國家/地區沒有一組標準的頻率指派時，就會使用此資料表。

每個頻率資料表都包含微調頻率的清單。 在某些國家/地區中，資料表中的索引會直接對應至通道編號，換句話說，channel n 的頻率是資料表中的第 n 個專案。 不過，在某些國家/地區中，頻道號碼和頻率之間並沒有直接的對應關係。 在這種情況下，應用程式必須保留一個清單，將通道編號 (通常是由使用者) 的頻率資料表專案所選擇。 例如，使用者在 frequency 資料表中看到的「channel 5」可能是專案編號12。

如需詳細資訊，請參閱 [國際類比電視微調](international-analog-tv-tuning.md)。

基本調整作業

如果調諧器支援多種接收模式（例如電視和 FM 電臺），請呼叫 [**IAMTuner：:p ui \_ 模式**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) 來選取模式。 [**IAMTuner：： GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes)方法會傳回檔諧器所支援的所有模式。 例如，下列程式碼會檢查調諧器是否支援 FM 無線電，如果是，則切換至該模式。


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



若要設定國家/地區，請呼叫 [**IAMTuner：:p 的 \_ CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) 方法。 調諧器會使用此值來選取適當的頻率資料表。 如需詳細資訊，請參閱 [國家/地區指派](country-region-assignments.md) 。

若要設定通道，請呼叫 [**IAMTuner：:p ui \_ 通道**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) 方法。 這個方法的引數實際上不是通道編號，而是目前頻率資料表的索引。 如先前所述，索引編號不一定會對應至頻道號碼。 [**IAMTuner：： ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax)方法會傳回目前頻率資料表的最小和最大索引值。

覆寫頻率專案

頻率資料表中的某些專案可能不正確或已過時。 因此，提供使用登錄機碼覆寫個別專案的機制。

「 [國際類比電視微調](international-analog-tv-tuning.md)」主題將說明這些細節。 每個登錄機碼會定義包含一或多個子機碼的「微調空間」。 每個子機碼都會覆寫一個頻率專案。 若要設定目前的微調空間，請使用 [**IAMTuner：:p 的 \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) 方法。 啟用微調空間會覆寫目前頻率資料表中的頻率專案。 因此，應用程式會負責維護微調空間與國家/地區之間的對應。 最好的方法是使用國家/地區識別碼作為微調空間的名稱。

微調頻率專案

廣播頻率可能會由廣播站向上或向下調整數個 kHz，以減少可能與鄰近通道的干擾。 根據名義頻率，調諧器介面卡可以掃描確切的頻率。 電視調諧器篩選器有一種機制，可在登錄中儲存已調整的頻率。

針對 frequency 資料表中的每個專案，呼叫 put \_ 通道方法以調整為該頻率。 調諧器會掃描最精確的頻率。 您可以藉由呼叫 [**IAMTuner：： SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent)，檢查調諧器是否達到水準鎖定。 電視調諧器篩選器也會在內部儲存結果。

掃描所有頻率之後，請呼叫 [**IAMTVTuner：： StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) 方法，將更新的值寫入登錄中。 更新的值會儲存在目前微調空間的登錄專案下。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[類比電視](analog-television.md)
</dt> </dl>

 

 



