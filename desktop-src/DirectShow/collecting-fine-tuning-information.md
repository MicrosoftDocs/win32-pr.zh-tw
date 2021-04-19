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
# <a name="collecting-fine-tuning-information"></a><span data-ttu-id="9467c-103">收集 Fine-Tuning 資訊</span><span class="sxs-lookup"><span data-stu-id="9467c-103">Collecting Fine-Tuning Information</span></span>

<span data-ttu-id="9467c-104">雖然纜線頻率通常會是精確的，但廣播頻率可能會由廣播站向上或向下調整數個 kHz，以減少可能與鄰近通道的干擾。</span><span class="sxs-lookup"><span data-stu-id="9467c-104">Although cable frequencies are generally expected to be exact, broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span>

<span data-ttu-id="9467c-105">當電視調諧器篩選器調整至頻道時，它會掃描最精確的信號。</span><span class="sxs-lookup"><span data-stu-id="9467c-105">When the TV Tuner filter tunes to a channel, it scans for the most precise signal.</span></span> <span data-ttu-id="9467c-106">若要在登錄中儲存此資訊以供後續調整作業，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="9467c-106">To save this information in the registry for subsequent tuning operations, do the following:</span></span>

1.  <span data-ttu-id="9467c-107">呼叫 [**IAMTuner：： ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) ，以判斷目前頻率資料表中的頻率專案範圍。</span><span class="sxs-lookup"><span data-stu-id="9467c-107">Call [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) to determine the range of frequency entries in the current frequency table.</span></span>
2.  <span data-ttu-id="9467c-108">針對範圍中的每個頻率索引，呼叫 [**IAMTuner：:p 工作區 \_ 通道**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) 方法一次。</span><span class="sxs-lookup"><span data-stu-id="9467c-108">Call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method once for each frequency index in the range.</span></span>
3.  <span data-ttu-id="9467c-109">呼叫 [**IAMTVTuner：： StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) ，以將微調資訊儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="9467c-109">Call [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) to save the fine-tuning information in the registry.</span></span> <span data-ttu-id="9467c-110">這項資訊會儲存在目前微調空間的登錄機碼下。</span><span class="sxs-lookup"><span data-stu-id="9467c-110">The information is stored under the registry key for the current tuning space.</span></span>

<span data-ttu-id="9467c-111">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="9467c-111">The following code shows these steps:</span></span>


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



<span data-ttu-id="9467c-112">使用舊版 TV 調諧器篩選器時，建議使用 [**IAMTVTuner：：自動調整**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) 方法進行微調。</span><span class="sxs-lookup"><span data-stu-id="9467c-112">With earlier versions of the TV Tuner filter, the [**IAMTVTuner::AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method was recommended for fine-tuning.</span></span> <span data-ttu-id="9467c-113">不過，這個方法會忽略任何頻率覆寫，因此不再建議使用。</span><span class="sxs-lookup"><span data-stu-id="9467c-113">However, this method ignores any frequency overrides, so its use is no longer recommended.</span></span> <span data-ttu-id="9467c-114">下列程式碼相當於 **自動調整** 方法，但使用頻率覆寫可正常運作：</span><span class="sxs-lookup"><span data-stu-id="9467c-114">The following code is equivalent to the **AutoTune** method, but works correctly with frequency overrides:</span></span>


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



<span data-ttu-id="9467c-115">透過廣播接收，雖然可以看到圖片，但不一定可以取得水準鎖定。</span><span class="sxs-lookup"><span data-stu-id="9467c-115">With broadcast reception, it is not always possible to get a horizontal lock, although the picture is viewable.</span></span> <span data-ttu-id="9467c-116">在這些情況下，調諧器硬體會有頻率鎖定，但解碼器不會有水準鎖定。</span><span class="sxs-lookup"><span data-stu-id="9467c-116">In these cases, the tuner hardware will have a frequency lock, but the decoder will not have horizontal lock.</span></span> <span data-ttu-id="9467c-117">藉由檢查傳回碼來使用 [**put \_ 通道**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) 或 [**自動調整**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) 時，可以偵測到此狀況。</span><span class="sxs-lookup"><span data-stu-id="9467c-117">This condition can be detected when using [**put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) or [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) by examining the return code.</span></span>



| <span data-ttu-id="9467c-118">值</span><span class="sxs-lookup"><span data-stu-id="9467c-118">Value</span></span>    | <span data-ttu-id="9467c-119">描述</span><span class="sxs-lookup"><span data-stu-id="9467c-119">Description</span></span>                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9467c-120">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="9467c-120">S\_OK</span></span>    | <span data-ttu-id="9467c-121">調整作業已成功，且調諧器得到頻率鎖定。</span><span class="sxs-lookup"><span data-stu-id="9467c-121">The tune operation succeeded and the tuner got a frequency lock.</span></span>                                                                                                                          |
| <span data-ttu-id="9467c-122">S \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="9467c-122">S\_FALSE</span></span> | <span data-ttu-id="9467c-123">微調操作期間沒有任何錯誤，但調諧器無法取得頻率鎖定。</span><span class="sxs-lookup"><span data-stu-id="9467c-123">There were no errors during the tune operation, but the tuner was not able to get a frequency lock.</span></span> <span data-ttu-id="9467c-124">這項作業不太可能會產生可查看的通道。</span><span class="sxs-lookup"><span data-stu-id="9467c-124">It is highly unlikely that there is a viewable channel resulting from this operation.</span></span> |



 

<span data-ttu-id="9467c-125">任何其他傳回碼會指出發生了一些錯誤。</span><span class="sxs-lookup"><span data-stu-id="9467c-125">Any other return code indicates that some error occurred.</span></span>

<span data-ttu-id="9467c-126">S 的傳回值不 \_ 保證該解碼器具有水準鎖定。</span><span class="sxs-lookup"><span data-stu-id="9467c-126">A return value of S\_OK does not guarantee that the decoder has a horizontal lock.</span></span> <span data-ttu-id="9467c-127">[**自動調整**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune)方法會更新 *FoundSignal* 參數，以指出是否已達到水準鎖定。</span><span class="sxs-lookup"><span data-stu-id="9467c-127">The [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method updates the *FoundSignal* parameter to indicate whether or not horizontal lock was achieved.</span></span> <span data-ttu-id="9467c-128">[**IAMTuner：： SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent)方法會傳回相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="9467c-128">The [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) method returns the same information.</span></span>

<span data-ttu-id="9467c-129">不過，當傳回值為 S 時， \_ 應用程式可以選擇忽略 *FoundSignal* 參數，因為調諧器會回報頻率鎖定。</span><span class="sxs-lookup"><span data-stu-id="9467c-129">When the return value is S\_OK, however, the application has the option of ignoring the *FoundSignal* parameter, because the tuner is reporting a frequency lock.</span></span> <span data-ttu-id="9467c-130">有時可能會發生雜訊鎖定，但這種可能性應該會被視為略過可見通道的可能性。</span><span class="sxs-lookup"><span data-stu-id="9467c-130">There is the possibility of a frequency lock on noise, but this possibility should be weighed against the possibility of skipping viewable channels.</span></span>

## <a name="registry-conversion"></a><span data-ttu-id="9467c-131">登錄轉換</span><span class="sxs-lookup"><span data-stu-id="9467c-131">Registry Conversion</span></span>

<span data-ttu-id="9467c-132">為了支援頻率覆寫，保留微調資訊的登錄機碼內部格式已變更。</span><span class="sxs-lookup"><span data-stu-id="9467c-132">To support frequency overrides, the internal format of the registry key that holds fine-tuning information has changed.</span></span> <span data-ttu-id="9467c-133">仍支援原始格式以提供回溯相容性，但不支援頻率覆寫。</span><span class="sxs-lookup"><span data-stu-id="9467c-133">The original format is still supported for backward compatibility, but it does not support frequency overrides.</span></span>

<span data-ttu-id="9467c-134">當呼叫 [**IAMTVTuner：： StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) 方法時，舊的登錄格式會轉換成新的格式。</span><span class="sxs-lookup"><span data-stu-id="9467c-134">The old registry format is converted to the new format whenever the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method is called.</span></span> <span data-ttu-id="9467c-135">如果您的應用程式加入頻率覆寫，它應該呼叫 **StoreAutoTune** 方法以轉換成新的登錄格式。</span><span class="sxs-lookup"><span data-stu-id="9467c-135">If your application adds frequency overrides, it should call the **StoreAutoTune** method to convert to the new registry format.</span></span> <span data-ttu-id="9467c-136">在呼叫 **StoreAutoTune** 之前，不需要收集任何微調資訊。</span><span class="sxs-lookup"><span data-stu-id="9467c-136">It is not necessary to collect any fine-tuning information before calling **StoreAutoTune**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9467c-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="9467c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9467c-138">國際類比電視微調</span><span class="sxs-lookup"><span data-stu-id="9467c-138">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



