---
description: 處理 SQL-DMO 中的資料
ms.assetid: 715482d9-23f4-40d0-9c09-7a81e148c543
title: 處理 SQL-DMO 中的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9f5d5d820dc1467c25f9d411d46a9c66935e8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846424"
---
# <a name="processing-data-in-a-dmo"></a>處理 SQL-DMO 中的資料

本節說明如何使用 SQL-DMO 處理資料串流。 此區段中所列的步驟是預設行為;所有 DMOs 都必須支援此處所述的方法。 這些方法會針對輸入和輸出使用不同的緩衝區。 有些 DMOs 也支援使用單一緩衝區進行就地處理。 如需就地處理的詳細資訊，請參閱就地 [處理](in-place-processing.md)。

**配置緩衝區**

用戶端負責所有的緩衝區配置。 在您設定了一組媒體類型之後，請查詢每個資料流程的緩衝區需求。 這些可能會根據媒體類型而變更。 針對每個資料流程，呼叫 [**IMediaObject：： GetInputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo) 或 [**IMediaObject：： GetOutputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo) 方法。 這些方法會傳回下列資訊：

-   緩衝區大小下限（以位元組為單位）。
-   對齊需求（如果有的話）。 如果起始位址是某個特定整數的倍數，就會對齊緩衝區。
-   用來進行先行查看的資料量上限。 此數位只適用于輸入資料流程。 針對某些類型的資料 (例如，) 的 MPEG 編碼方式，可能需要在資料流程中向前查看。 右值會指出在產生輸出之前，需要有多少輸入資料。

用戶端必須配置符合這些需求的緩衝區。 此外，SQL-DMO 可能會要求用戶端如何封裝輸入資料。 例如，每個緩衝區可能會要求每個緩衝區只包含一個樣本 (或影片畫面格) 。 若要判斷這些需求，請呼叫 [**IMediaObject：： GetInputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo) 方法。 [**IMediaObject：： GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo)方法會傳回類似輸出資料流程的資訊。

在預設的串流模型中，用戶端不會將原始的緩衝區指標傳遞至 相反地，它會使用公開 [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) 介面的輕量 COM 物件。 **IMediaBuffer** 介面會作為記憶體區塊的 COM 包裝函式。 由於它是 COM 物件，它支援參考計數，可協助確保在仍在使用時不會釋放緩衝區。

> [!Note]  
> **IMediaBuffer** 介面的功能類似于 DirectShow 中的 **IMediaSample** 介面。

 

用戶端必須執行 **IMediaBuffer** 物件。 如需詳細資訊，請參閱 [執行 IMediaBuffer](implementing-imediabuffer.md)。

**處理資料**

若要處理資料，請執行下列動作：

1.  針對每個輸入資料流程，以輸入資料填滿緩衝區。
2.  呼叫 [**IMediaObject：:P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput) 傳遞每個緩衝區。
3.  呼叫 [**IMediaObject：:P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) 來處理資料。 這個方法會採用緩衝區的陣列，每個輸出資料流程各一個。
4.  重複直到沒有其他輸入資料為止。

**ProcessInput** 方法會一次接受一個資料流程的輸入。 通常方法會立即傳回，而] 則是在 **IMediaBuffer** 物件上保存參考計數。 它會在處理緩衝區中的所有資料之後，或當應用程式清除該物件時，釋放物件。 除非在一放開緩衝區，否則請不要重複使用緩衝區。 若要判斷輸入資料流程是否可以接受更多資料，請呼叫 [**IMediaObject：： GetInputStatus**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstatus) 方法。 \_ \_ \_ \_ 如果資料流程可以接受更多輸入，這個方法會傳回 Sql-dmo 輸入 STATUSF 接受資料旗標。

**ProcessOutput** 方法會一次產生所有輸出資料流程的輸出。 應用程式會傳入 [**Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) 結構的陣列，每個輸出資料流程各一個。 陣列中的每個結構都有指向 **IMediaBuffer** 物件的指標。 當您盡可能將輸出資料寫入緩衝區時，就會將其寫入。 它也會設定各種旗標來報告作業的狀態。 [SQL-DMO \_ 輸出 \_ 資料 \_ BUFFERF \_ 未完成] 旗標表示 sql-dmo 可以產生更多來自現有輸入的輸出。 在這種情況下，用戶端可以再次呼叫 **ProcessOutput** 。 否則，它應該以更多輸入資料來呼叫 **ProcessInput** 。 在輸入緩衝區中的資料絕對不會修改;它只會寫入輸出緩衝區。

將所有資料傳送至輸入資料流程之後，請呼叫 [**IMediaObject：:D iscontinuity**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-discontinuity) 方法。 除非您處理其餘的輸出 (或排清) ，否則，

串流開始之後的任何時間點都可以接收輸入或產生輸出，或兩者皆可。 因此， **GetInputStatus** 會傳回 Sql-dmo \_ 輸入 \_ STATUSF \_ ACCEPT \_ 資料，否則 **ProcessOutput** 會傳回 sql-dmo \_ 輸出 \_ 資料 \_ BUFFERF \_ 未完成。 應用程式會藉由測試這些旗標，並據以呼叫 **ProcessInput** 或 **ProcessOutput** ，以保持資料流程動。 若要中斷資料流程，請呼叫 [**IMediaObject：： Flush**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-flush) 方法。 這個方法會讓 SQL-DMO 捨棄它在內部保留的任何緩衝區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[直接裝載](directly-hosting-a-dmo.md)
</dt> <dt>

[就地處理](in-place-processing.md)
</dt> </dl>

 

 



