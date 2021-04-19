---
description: 關於速率控制
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: 關於速率控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977014"
---
# <a name="about-rate-control"></a>關於速率控制

在媒體基礎中， *播放速率* 會以目前播放速率與正常播放速率的比率表示。 例如，速率2.0 是兩倍的一般速度，而0.5 是半一般的速度。 負數值表示反向播放。 播放速率為-2.0，會以正常速度的兩倍向前播放資料流程。 速率為零會導致一個框架呈現;之後，表示時鐘不會前進。 若要取得零速率的另一個畫面格，應用程式必須搜尋至新的位置。

應用程式會使用下列介面來控制播放速率。

-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)。 用來找出可能最快且最慢的播放速率。
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)。 用來變更播放速率。

若要取得這兩個介面，請呼叫媒體會話上的 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 。 服務識別碼為 MF \_ 速率 \_ 控制 \_ 服務。

藉由使用速率控制服務，應用程式可以執行向前快轉和反向播放。

## <a name="thinning"></a>細化

*Thinning* 是可減少資料流程中樣本數的任何程式，以降低整體的位元速率。 針對影片，通常會藉由卸載 delta 框架並只傳遞主要畫面格來完成 thinning。 管線通常可以使用 thinned 播放支援更快速的播放率，因為資料速率較低，因為差異畫面格未解碼。

Thinning 不會變更樣本上的時間戳記或持續時間。 例如，如果影片資料流程的名義費率為每秒25個畫面格，則每個畫面格的持續時間仍會標示為40毫秒，即使媒體來源正在卸載所有的 delta 框架也一樣。 這表示一個畫面尾和下一個畫面格的開頭之間會有時間間距。

## <a name="scrubbing"></a>Scrubbing

清除 *程式是透過* 與捲軸、時間軸或其他視覺標記法的互動，立即搜尋資料流程中的特定點。 這一期來自于來回滾輪一個磁片區以找出一個區段，就像是使用磁帶來清除播放標頭一樣。

藉由將播放速率設定為零，在媒體基礎中執行清除。 如需詳細資訊，請參閱 [如何執行](how-to-perform-scrubbing.md)清除。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[速率控制](rate-control.md)
</dt> <dt>

[搜尋、向前快轉及反向播放](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[服務介面](service-interfaces.md)
</dt> </dl>

 

 



