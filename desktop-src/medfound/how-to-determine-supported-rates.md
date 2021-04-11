---
description: 如何判斷支援的費率
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: 如何判斷支援的費率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191708"
---
# <a name="how-to-determine-supported-rates"></a>如何判斷支援的費率

在變更播放速率之前，應用程式應該檢查管線中的物件是否支援播放速率。 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)介面會提供方法來取得最大的向前和反向速率、最接近所要求速率的支援速率，以及最慢的速率。 每個速率查詢都可以指定播放方向，以及是否使用 thinning。 您可以使用 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面來查詢確切的播放速率。

如需變更播放速率的詳細資訊，請參閱 [如何設定媒體會話的播放速度](how-to-set-the-playback-rate-on-the-media-session.md)。

如需播放速率的一般資訊，請參閱 [關於速率控制](about-rate-control.md)。

## <a name="to-determine-the-current-playback-rate"></a>判斷目前的播放速率

1.  取得媒體會話的速率控制服務。

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    在 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)的 *>punkobject* 參數中傳遞初始化的 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)介面指標。

    應用程式必須透過媒體會話來查詢速率控制服務。 就內部而言，媒體會話會查詢拓撲中的物件。

2.  呼叫 [**IMFRateControl：： GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) 方法，以取得目前的播放速率。

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate)的 *pfThin* 參數會接收 **BOOL** 值，指出資料流程目前是否正在 thinned。 如果應用程式不想查詢資料流程的 thinning 支援，則必須傳遞 **Null** 。 *PflRate* 參數會接收目前的播放速率。

## <a name="to-determine-the-nearest-supported-rate"></a>判斷最接近的支援速率

1.  取得媒體會話的費率支援服務。

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    在 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)的 *>punkobject* 參數中傳遞初始化的 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)介面指標。

2.  呼叫 [**IMFRateSupport：： IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) 方法，以取得最接近所要求播放速率的支援速率。

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    此範例會查詢 thinning 是否支援播放速率4.0。 這是藉由在 [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported)的 *fThin* 參數中傳遞 **TRUE** 來表示。 如果支援此速率， *actualRate* 會包含播放速率4.0，而呼叫會成功，且傳回值為 \_ [正常]。 如果不支援確切的播放速率，則會在 *actualRate* 中收到最接近的支援速率。 如果速率不受支援，而且沒有最接近的播放速率，則呼叫會傳回適當的錯誤碼。

    這些值可能會隨著載入的管線元件而變更。 因此，您應該在每次載入新的 topololgy 時，重新查詢這些值。

    如果不支援所需的播放率，有一個選項是個別查詢拓撲中的每個物件，以找出特定的元件是否不支援費率。 您可以在沒有此元件的情況下重建拓撲，然後以所需的速率進行播放。 例如，如果音訊轉譯器以外的每個元件都支援指定的速率，您就可以重建沒有音訊分支的拓撲，並以所需的速率來播放（沒有音訊）。

## <a name="to-determine-the-slowest-supported-rate"></a>判斷最慢的支援速率

1.  取得媒體會話的費率支援服務。

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    在 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)的 *>punkobject* 參數中傳遞初始化的 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)介面指標。

2.  呼叫 [**IMFRateSupport：： GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) 方法，以取得最慢的支援速率。

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    此範例會使用 thinning 來查詢最慢的反向播放速率。 [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)的 *slowestRate* 參數中會收到下限速率。

    如果不支援反向播放或 thinning，呼叫會傳回適當的錯誤碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話](media-session.md)
</dt> <dt>

[速率控制](rate-control.md)
</dt> <dt>

[搜尋、向前快轉及反向播放](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



