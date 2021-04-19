---
description: 收集 Fine-Tuning 資訊
ms.assetid: 0d9ea896-e0a9-411b-9a10-e366e3686a34
title: 收集 Fine-Tuning 資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d191f677acc9306202bce141ef8f6683b43c61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972102"
---
# <a name="collecting-fine-tuning-information"></a>收集 Fine-Tuning 資訊

雖然纜線頻率通常會是精確的，但廣播頻率可能會由廣播站向上或向下調整數個 kHz，以減少可能與鄰近通道的干擾。

當電視調諧器篩選器調整至頻道時，它會掃描最精確的信號。 若要在登錄中儲存此資訊以供後續調整作業，請執行下列動作：

1.  呼叫 [**IAMTuner：： ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) ，以判斷目前頻率資料表中的頻率專案範圍。
2.  針對範圍中的每個頻率索引，呼叫 [**IAMTuner：:p 工作區 \_ 通道**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) 方法一次。
3.  呼叫 [**IAMTVTuner：： StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) ，以將微調資訊儲存在登錄中。 這項資訊會儲存在目前微調空間的登錄機碼下。

下列程式碼顯示這些步驟：


```C++
long lMin = 0, lMax = 0;
hr = pTuner->ChannelMinMax(&lMin, &lMax);
if (SUCCEEDED(hr))
{
    for (long i = lMin; i <= lMax; i++)
    {
        pTuner->put_Channel(i, AMTUNER_SUBCHAN_DEFAULT,
            AMTUNER_SUBCHAN_DEFAULT)
    }
    pTuner->StoreAutoTune();
}
```



使用舊版 TV 調諧器篩選器時，建議使用 [**IAMTVTuner：：自動調整**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) 方法進行微調。 不過，這個方法會忽略任何頻率覆寫，因此不再建議使用。 下列程式碼相當於 **自動調整** 方法，但使用頻率覆寫可正常運作：


```C++
HRESULT MyAutoTune(IAMTVTuner *pTuner, long lIndex, long *plFoundSignal)
{
    long SignalStrength = AMTUNER_NOSIGNAL;
    HRESULT hr;
    hr = pTuner->put_Channel(lIndex, AMTUNER_SUBCHAN_DEFAULT, AMTUNER_SUBCHAN_DEFAULT);
    if (NOERROR == hr)
        pTuner->SignalPresent(&SignalStrength);
    *plFoundSignal = (SignalStrength != AMTUNER_NOSIGNAL);
        return hr;
}
```



透過廣播接收，雖然可以看到圖片，但不一定可以取得水準鎖定。 在這些情況下，調諧器硬體會有頻率鎖定，但解碼器不會有水準鎖定。 藉由檢查傳回碼來使用 [**put \_ 通道**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) 或 [**自動調整**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) 時，可以偵測到此狀況。



| 值    | 描述                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ 確定    | 調整作業已成功，且調諧器得到頻率鎖定。                                                                                                                          |
| S \_ FALSE | 微調操作期間沒有任何錯誤，但調諧器無法取得頻率鎖定。 這項作業不太可能會產生可查看的通道。 |



 

任何其他傳回碼會指出發生了一些錯誤。

S 的傳回值不 \_ 保證該解碼器具有水準鎖定。 [**自動調整**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune)方法會更新 *FoundSignal* 參數，以指出是否已達到水準鎖定。 [**IAMTuner：： SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent)方法會傳回相同的資訊。

不過，當傳回值為 S 時， \_ 應用程式可以選擇忽略 *FoundSignal* 參數，因為調諧器會回報頻率鎖定。 有時可能會發生雜訊鎖定，但這種可能性應該會被視為略過可見通道的可能性。

## <a name="registry-conversion"></a>登錄轉換

為了支援頻率覆寫，保留微調資訊的登錄機碼內部格式已變更。 仍支援原始格式以提供回溯相容性，但不支援頻率覆寫。

當呼叫 [**IAMTVTuner：： StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) 方法時，舊的登錄格式會轉換成新的格式。 如果您的應用程式加入頻率覆寫，它應該呼叫 **StoreAutoTune** 方法以轉換成新的登錄格式。 在呼叫 **StoreAutoTune** 之前，不需要收集任何微調資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[國際類比電視微調](international-analog-tv-tuning.md)
</dt> </dl>

 

 



