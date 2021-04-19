---
description: 時間戳記
ms.assetid: 445fe6b9-9d5b-45fd-9c9e-8c632c5228ae
title: 時間戳記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855d2c472d7964ccad6ec8bbc87efd39b1c4cdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000337"
---
# <a name="time-stamps"></a>時間戳記

*時間戳記* 會定義媒體範例的開始和完成時間，以資料流程時間來測量。 時間戳記有時稱為 *呈現時間*。 閱讀本文的其餘部分時，請務必記住，並非所有格式都會以相同的方式使用時間戳。 例如，並非所有 MPEG 範例都會加上時間戳記。 在 MPEG 篩選圖形中，時間戳記不會套用至每個框架，直到它們從解碼器輸出為止。

當轉譯器篩選器收到範例時，它會根據時間戳記排定轉譯。 如果範例遲到或沒有時間戳記，則篩選會立即轉譯範例。 否則，篩選準則會等到範例的開始時間轉譯樣本為止。  (它會藉由呼叫 [**IReferenceClock：： AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) 方法來等候開始時間。 ) 

來源篩選器和剖析器篩選器負責在其處理的範例上設定正確的時間戳記。 使用下列指導方針。

-   檔案播放：第一個範例是以零為起始時間的時間戳記。 後續的時間戳記取決於樣本長度和播放速率，也就是由檔案格式決定。 剖析檔案的篩選準則負責計算正確的時間戳記 (例如， [AVI 分隔器](avi-splitter-filter.md)) 。
-   影片和音訊捕獲：每個範例都是時間戳記，其開始時間等於捕捉的資料流程時間，但有下列注意事項：
    -   預覽 pin 的影片框架 (與捕捉 pin) 不會加上時間戳記。 由於圖表的延遲，以拍攝時間加上戳記的影片畫面，將一律在影片轉譯器遲到。 這可能會導致轉譯器卸載框架，以嘗試品質控制。 如需品質控制的詳細資訊，請參閱 [品質控制管理](quality-control-management.md)。
    -   音訊捕獲：音訊捕獲篩選器會使用自己的緩衝區集，這些緩衝區與音訊驅動程式所使用的不同。 音訊驅動程式會以固定的間隔填入捕獲篩選器的緩衝區。 間隔取決於驅動程式，但通常不會超過10毫秒。 音訊樣本上的時間戳記會反映驅動程式填滿音訊捕獲篩選器緩衝區的時間。 這些時間可能稍微不正確，特別是當應用程式使用極小的緩衝區大小時。 不過，媒體時間會精確地反映緩衝區中的數位音訊樣本。
-   Mux 篩選器：根據輸出格式，mux 篩選可能需要產生時間戳記，否則可能不會。 例如，AVI 檔案格式所使用的固定畫面播放速率沒有時間戳記，因此 [AVI Mux](avi-mux-filter.md) 篩選器會假設樣本抵達的時間大約是正確的時間。 但是，如果傳入的時間戳記顯示大於一框架的間隙，則 AVI Mux 會寫入大小為零的索引項目目，以表示已卸載的框架。 在檔案播放時，會在執行時間產生新的時間戳記，如先前所述。

若要設定範例的時間戳記，請呼叫 [**IMediaSample：： SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) 方法。

**媒體時間**

篩選也可以選擇性地指定範例的 *媒體時間* 。 在影片串流中，媒體時間代表畫面格編號。 在音訊串流中，媒體時間代表封包中的範例數目。 例如，如果每個封包都包含44.1 千赫茲 (kHz) 音訊的1秒，則第一個封包的媒體開始時間為零，而媒體停止時間為44100。 在可搜尋的資料流程中，媒體時間一律相對於資料流程的開始時間。 例如，假設您從 15 fps video 串流的開頭到2秒。 搜尋之後的第一個媒體範例的時間戳記為零，而媒體時間為30。

轉譯器和 mux 篩選器可以透過檢查間距，以使用媒體時間來判斷是否已卸載框架或樣本。 但是，不需要篩選來設定媒體時間。 若要設定範例的媒體時間，請呼叫 [**IMediaSample：： SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



