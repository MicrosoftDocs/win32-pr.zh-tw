---
title: 在資料流程中定位
description: 在資料流程中定位
ms.assetid: 97ab491d-1a58-4b4b-a13a-215be24dac1c
keywords:
- AVIStreamStart 函式
- AVIStreamFindSample 函式
- AVIStreamSampleToTime 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252aa938d32c323da9fcf7ae106d11db0ff2fb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672776"
---
# <a name="positioning-in-streams"></a>在資料流程中定位

AVIFile 提供數種方式來尋找並移至資料流程中的位置。 此區段中的函式和宏可讓您的應用程式找到開始位置、長度和主要畫面格 (在串流內的範例) 中包含完整的影像。 函式和宏也會將時間與資料流程中的位置產生關聯，其方式是計算從其開始到資料流程中任何點播放資料流程所需的經過時間。

## <a name="finding-the-starting-position"></a>尋找開始位置

您可以使用 [**AVIStreamStart**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart) 函式，來取出影片資料流程中第一個框架的樣本數。 根據作者的喜好設定， (電影的畫面格可能會從範例0或1開始。 ) 您也可以使用 [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) 函式來取得此資訊。 此函數會將範例編號儲存在 [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)結構的 **dwStart** 成員中。 您可以使用 [**AVIStreamStartTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime) 宏來取出資料流程第一個範例的開始時間。

您可以使用 [**AVIStreamLength**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength) 函式來取得資料流程長度。 此函數會傳回資料流程中的樣本數。 您也可以使用 **AVIStreamInfo** 函數來取得此資訊。 此函數會將資料流程長度儲存在 **AVISTREAMINFO** 結構的 **dwLength** 成員中。 若要取得資料流程的長度（以毫秒為單位），請使用 [**AVIStreamLengthTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime) 宏。

在影片串流中，每個範例通常會對應至影片畫面。 不過，可能會是沒有任何影片資料的範例。 如果您呼叫 [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) 函式來指定其中一個位置，它會傳回0個位元組的資料長度。 您可以使用 [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) 函式來尋找包含資料的範例，並指定 [尋找 \_ 任何] 旗標。

在音訊串流中，每個範例都對應到音訊資料的一個資料區塊。 例如，如果音訊資料具有 22 kHz ADPCM (彈性差異脈衝程式碼調整) 格式，則每個 **AVIStreamLength** 範例都會對應到256位元組的壓縮音訊資料區塊。 壓縮時，此區塊的音訊資料包含大約500個音訊樣本。 不過，AVIFile 的函式和宏會將每個256位元組區塊視為單一樣本。

> [!Note]  
> 資料流程內的有效位置，從資料流程的開頭到資料流程的結尾，也就是資料流程起點和其長度的總和。 開始位置與長度的總和所表示的位置，會對應到最後一個資料呈現之後的時間;它不包含任何資料。 您可以使用 [**AVIStreamEnd**](/windows/desktop/api/Vfw/nf-vfw-avistreamend) 宏來抓取表示資料流程結尾的範例編號。 您可以使用 [**AVIStreamEndTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime) 宏來取得代表資料流程結尾的時間值（以毫秒為單位）。

 

## <a name="finding-sample-and-key-frames"></a>尋找範例和主要畫面格

您可以使用 [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) 函數，在資料流程中搜尋不同類型的範例。 此函式會在資料流程中向前或向後搜尋適當類型的範例，並以您指定的範例編號為開頭。 您可以在 **AVIStreamFindSample** 呼叫順序中指定旗標，以在資料流程中搜尋不同類型的樣本。 指定 [尋找 \_ 任何] 旗標以找出非空白樣本，或略過缺少資料的樣本。 指定尋找 \_ 金鑰旗標以搜尋包含資料的主要畫面格，而不需要參考先前的畫面格。 指定尋找 \_ 格式旗標以搜尋格式的變更。 **AVIStreamFindSample** 主要用於影片串流。

使用 AVIFile 函式的數個宏會補充資料流程搜尋功能。 下列清單提供每個宏的簡短描述。 搜尋特定位置或資料類型的宏，需要在資料流程中指定開始位置。



| 巨集                                                                | Description                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)                   | 指出指定的資料流程中的範例是否為主要畫面格。                                                            |
| [**AVIStreamNearestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)         | 找出資料流程中指定位置或之前的主要畫面格。                                                     |
| [**AVIStreamNearestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime) | 判斷對應到最接近 (于資料流程中指定時間或之前) 的主要畫面格開始時間。 |
| [**AVIStreamNearestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)             | 在資料流程中的指定位置或之前，找出最接近的非空樣本。                                       |
| [**AVIStreamNearestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)     | 判斷對應到最接近資料流程中指定時間之樣本開頭的時間。             |
| [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)               | 找出資料流程中指定位置之後的下一個主要畫面格。                                                      |
| [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)       | 傳回資料流程中下一個主要畫面格的時間，從指定的時間開始。                                               |
| [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)                   | 從資料流程中的指定位置找出下一個非空白範例。                                                     |
| [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)           | 傳回範例變更為資料流程中下一個範例的時間。                                                    |
| [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)               | 尋找資料流程中指定位置之前的主要畫面格。                                                       |
| [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)       | 傳回資料流程中上一個主要畫面格的時間，從指定的時間開始。                                         |
| [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)                   | 找出資料流程中指定位置之前的非空白樣本。                                                 |
| [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)           | 決定上一個範例取代其在資料流程中前身的時間。                                    |
| [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)           | 傳回資料流程中的範例，此範例會在與第二個數據流中發生的樣本相同的時間發生。                     |



 

## <a name="switching-between-samples-and-time"></a>在範例和時間之間切換

您可以使用 [**AVIStreamSampleToTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime) 函式，判斷從資料流程開頭到範例的經過時間。 此函式會將範例數位轉換成以毫碼錶示的時間值。 如果影片框架 (跨越數毫秒) ，此值代表取樣開始播放的時間，並假設影片剪輯會以正常速度播放。 若為音訊範例 (，其中有數個樣本以毫秒為單位) ，時間值會對應至取樣開始播放的時間，並假設音訊串流以正常速度播放。

相反地，您可以使用 [**AVIStreamTimeToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample) 函數來尋找與時間值相關聯的範例編號。 此函式會將毫秒值轉換成樣本數，並假設影片剪輯會以正常速度播放。

因為 **AVIStreamSampleToTime** 會傳回框架開始播放的時間，所以 **AVIStreamSampleToTime** 和 **AVIStreamTimeToSample** 之間的關聯性不是真正的反向。 它們會判斷檔案中的位置比決定時間更 acurately。 例如，兩個連續的音訊範例可能會在相同的毫秒內播放。 使用 **AVIStreamSampleToTime** 轉換樣本數會產生相同的時間值。 如果您使用 **AVIStreamTimeToSample** 將時間值轉換回樣本數，則會參考單一樣本。

 

 




