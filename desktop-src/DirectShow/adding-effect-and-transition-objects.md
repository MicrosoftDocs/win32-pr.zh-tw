---
description: 新增效果和轉換物件
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: 新增效果和轉換物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025680"
---
# <a name="adding-effect-and-transition-objects"></a>新增效果和轉換物件

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

在 DES 中，效果或轉換會以兩個物件表示：

-   *時間軸物件* 代表時間軸內的效果或轉換。 為了效果，timeline 物件支援 [**IAMTimelineEffect**](iamtimelineeffect.md) 介面。 針對轉換，它支援 [**IAMTimelineTrans**](iamtimelinetrans.md) 介面。 這兩種類型都支援 [**IAMTimelineObj**](iamtimelineobj.md) 介面。
-   子 *物件是一種物件* ，可針對效果或轉換來執行資料處理。 時間軸物件會保存子物件的指標。

若要新增效果或轉換，請執行下列步驟。

**1. 建立時間軸物件**

若要建立時程表物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 方法。 為效果設定等於 **時間軸 \_ 主要 \_ 類型 \_ 效果** 的類型，或轉換的 **時間軸 \_ 主要 \_ 類型 \_ 轉換** 。

下列範例會建立一個轉換物件：


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



**2. 指定子物件**

時間軸物件會作為另一個物件的包裝函 *式，稱為子物件，它* 會執行實際工作。 子物件會執行資料轉換，以產生所需的效果或轉換。 如需 DES 提供的轉換和效果清單，請參閱 [轉換和效果](transitions-and-effects.md)。

若要設定子物件，請在時間軸物件上呼叫 [**IAMTimelineObj：： SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) 方法，並傳遞類別識別碼 (子物件的 CLSID) 。 DirectShow 提供可供您用來取得 CLSID 的影片效果和影片轉換的列舉值。 如需詳細資訊，請參閱 [列舉效果和轉換](enumerating-effects-and-transitions.md)。

下列範例會將「 [SMPTE](smpte-wipe-transition.md) 抹除」轉換設定為子物件：


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



**3. 設定開始和停止時間**

若要設定開始和停止時間，請呼叫 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md) 方法。 這些時間相對於父物件的開始時間。 效果可能會在相同的物件內重迭，但無法轉換。

下列範例會將開始時間設定為5秒，並將停止時間設定為10秒：


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



轉譯轉換時，每個畫面格的轉換進度會根據 **進度** 屬性來計算，該屬性會正規化為0.0 到1.0 的範圍。 DES 會使用每個畫面格的開始時間來計算進度值。 這表示，如果轉換停止時間等於來源停止時間，則 **進度** 值絕對不會達到1.0，因為最後一個畫面格的開始時間與停止時間稍微不同。 若要讓轉換達到1.0，請將轉換停止時間設定為至少一個早于來源停止時間的畫面格。

**4. 將物件插入至時間軸**

若要將物件插入至時間軸，請根據物件類型，在父系上呼叫下列其中一種方法：

-   效果： [ **IAMTimelineEffectable：： EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)
-   轉換： [ **IAMTimelineTransable：： TransAdd**](iamtimelinetransable-transadd.md)

在 [**IAMTimelineEffectable：： EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) 方法中，您必須指定效果的優先順序。 當效果在相同物件上重迭時，會依優先順序套用。 音量信封音訊效果是例外狀況;如需詳細資訊，請參閱 [音量信封效果](volume-envelope-effect.md) 參考。 在組合內，所有音訊播放軌都會在套用該組合的音訊效果之前進行混合。

因為轉換在相同物件上不能重迭，所以它們沒有優先權值。

下列範例會將轉換物件新增至追蹤：


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



此範例會查詢 [**IAMTimelineTransable**](iamtimelinetransable.md) 介面的 track 物件，然後再呼叫 AddTrans。

**5. 設定屬性**

許多效果和轉換都支援自訂屬性。 如需詳細資訊，請參閱 [設定效果和轉換的屬性](setting-properties-on-effects-and-transitions.md)。

範例

下列程式碼範例會將 [SMPTE 抹除轉換](smpte-wipe-transition.md) 新增至追蹤。它會假設播放軌物件已經存在於時間軸中。


```C++
IAMTimeline *pTL;
IAMTimelineTrack *pTrack;

// Create timeline with track (not shown).

// Create the transition object. 
IAMTimelineObj *pTransObj = NULL;
hr = pTL->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);

// Set the subobject. 
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe

// Set the start and stop times. 
hr = pTransObj->SetStartStop(50000000, 100000000);

// Insert the transition object into the timeline. 
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
pTransObj->Release();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用效果和轉換](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



