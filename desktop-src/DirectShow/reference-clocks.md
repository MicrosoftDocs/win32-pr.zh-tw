---
description: 參考時鐘
ms.assetid: 43f1a4d6-dbed-4940-a301-d863ddd34bce
title: 參考時鐘
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ad0a262b36ce78c6a2f355b30b3c6876c7e78a7807970592b6f15287c0e2c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697108"
---
# <a name="reference-clocks"></a>參考時鐘

篩選 Graph 管理員的其中一個函式，是將圖形中的所有篩選器同步至相同的時鐘，稱為 *參考時鐘*。

公開 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 介面的任何物件都可以作為參考時鐘。 參考時鐘可能會由 DirectShow 篩選（通常是音訊轉譯器）提供，這是可存取硬體計時器的輸出。 做為回復，Graph 管理員的篩選器可以使用系統時間。

名義上，參考時鐘會以 100-毫微秒間隔來測量時間，雖然時鐘的實際精確度可能較少。 若要取出時鐘的目前時間，請呼叫 [**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) 方法。 時鐘的基準（從開始計算算起的時間）取決於執行，因此 **GetTime** 傳回的值不會有任何意義。 重要的是當圖形開始執行時的差異。

雖然參考時鐘的精確度可能不同，但 [**GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) 方法所傳回的時間保證會以單純方式增加。 換句話說，時鐘時間永遠不會反向。 如果參考時鐘產生的是硬體來源的時鐘時間，而硬體時鐘會向後跳躍 (例如，如果有對時鐘) 的調整， **GetTime** 方法應該會繼續傳回上次回報的時間，直到硬體時鐘趕上為止。 如需詳細資訊，請參閱 [**CBaseReferenceClock 類別**](cbasereferenceclock.md)。

**預設參考時鐘**

篩選 Graph 管理員會在圖形執行時自動選取參考時鐘。 它會使用下列演算法來選取時鐘：

-   如果應用程式已選取時鐘 (請參閱下面的) ，請使用該時鐘。
-   如果圖形包含支援 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)的即時來源篩選器，請使用該篩選準則。 如需即時來源的定義，請參閱 [即時來源](live-sources.md)。
-   如果圖表不包含任何即時來源篩選，請使用圖形中支援 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)的任何篩選，從轉譯器開始，然後工作上游。 偏好未連接的篩選準則的連接篩選。  (如果圖形正在轉譯音訊串流，則演算法中的這個步驟通常會選取音訊轉譯器篩選器。 ) 
-   如果沒有任何篩選準則提供適當的時鐘，請使用 [系統參考時鐘](system-reference-clock.md)（以系統時間為基礎）。

**設定參考時鐘**

應用程式可以在篩選 Graph 管理員上呼叫 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)方法，以選取時鐘。 只有當您有特殊原因想要使用另一個時鐘時，才應該這麼做。

您可以使用值 **Null** 來呼叫 [**SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) ，以指示篩選 Graph 管理員不要使用參考時鐘。 例如，您可能會盡可能快速地處理範例。 若要還原預設的參考時鐘，請在篩選 Graph 管理員上呼叫 [**IFilterGraph：： SetDefaultSyncSource**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource)方法。

每當參考時鐘變更時，Filter Graph Manager 就會呼叫其 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)方法來通知每個篩選準則。 應用程式永遠不應該在篩選器上呼叫這個方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 Graph 時鐘](setting-the-graph-clock.md)
</dt> <dt>

[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



