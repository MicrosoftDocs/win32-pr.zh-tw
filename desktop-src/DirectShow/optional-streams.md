---
description: 選用資料流程
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: 選用資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940be49196396aa2d1fa71502213b0d4fbacb5ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972925"
---
# <a name="optional-streams"></a>選用資料流程

SQL-DMO 可以將部分輸出資料流程指定為選擇性。 選擇性的資料流程會產生應用程式可以捨棄的資料，無論是完全或偶爾的範例。 例如，選擇性資料流程可能包含有關主要資料流程的其他資訊。

若要查詢資料流程是否為選擇性，請呼叫 [**IMediaObject：： GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) 方法，並檢查 *pdwFlags* 參數。 選擇性資料流程會傳回 SQL-DMO \_ output \_ STREAMF \_ DISCARDABLE 旗標或 Sql-dmo \_ output \_ STREAMF \_ 選擇性旗標。 這些旗標表示幾乎相同的內容;稍後將會說明其中的一個小差異。

如果資料流程是選擇性的，用戶端可以指示當該資料流程處理輸出時，從該資料流程捨棄資料。 若要這樣做，請呼叫 [**IMediaObject：:P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) 方法，並將每個要捨棄的資料流程的輸出緩衝區設定為 **Null** 。  (在 [**Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer)的 **pBuffer** 成員中指定輸出緩衝區。 ) \_ \_ \_ \_ \_ \_ 在 *DWFLAGS* 參數中沒有任何緩衝區旗標時，也請設定 [sql-dmo 進程輸出捨棄]。

針對 *pBuffer* 指標為 **Null** 的每個資料流程，每個資料流程都會嘗試捨棄資料。 如果資料流程是選擇性的，則會保證會捨棄資料。 如果資料流程不是選擇性的，則會盡可能捨棄資料，但不保證會這樣做。 如果它無法捨棄資料，它會設定 [SQL-DMO \_ 輸出 \_ 資料 \_ BUFFERF \_ 不完整] 旗標。 如果您將 *pBuffer* 指標設定為 **Null** ，但未設定 [ \_ \_ \_ \_ 當無緩衝區旗標時]，則會捨棄 []，而不 \_ \_ 會捨棄資料。 在這種情況下，會在內部緩衝輸出，或只是 **ProcessOutput** 呼叫失敗。

SQL-DMO \_ 輸出 \_ STREAMF \_ 選用旗標和 Sql-dmo \_ output \_ STREAMF \_ DISCARDABLE 旗標之間唯一的功能差異如下：

-   [SQL-DMO \_ 輸出 \_ STREAMF] \_ 選擇性旗標表示用戶端不需要在該資料流程上設定媒體類型。 但是，如果用戶端在沒有設定該資料流程的媒體類型的情況下開始處理資料，則它必須在串流的整個持續期間捨棄該資料流程中的資料。 如果您想要選擇性地捨棄樣本，則必須設定媒體類型。
-   [SQL-DMO \_ OUTPUT \_ STREAMF \_ DISCARDABLE] 旗標表示雖然資料流程是選擇性的，但它一律需要媒體類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[直接裝載](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



