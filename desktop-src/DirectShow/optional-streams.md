---
description: 選用資料流程
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: 選用資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d7c30f783a8c13b00020c2dac62cd11e2a79d6f2ea66af01f715c3cb389853
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830968"
---
# <a name="optional-streams"></a>選用資料流程

DMO 可以將部分輸出資料流程指定為選擇性。 選擇性的資料流程會產生應用程式可以捨棄的資料，無論是完全或偶爾的範例。 例如，選擇性資料流程可能包含有關主要資料流程的其他資訊。

若要查詢資料流程是否為選擇性，請呼叫 [**IMediaObject：： GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) 方法，並檢查 *pdwFlags* 參數。 選擇性資料流程會傳回 DMO \_ output \_ STREAMF \_ DISCARDABLE 旗標或 DMO \_ OUTPUT \_ STREAMF \_ 選擇性旗標。 這些旗標表示幾乎相同的內容;稍後將會說明其中的一個小差異。

如果資料流程是選擇性的，用戶端可以指示 DMO 在處理輸出時捨棄該資料流程中的資料。 若要這樣做，請呼叫 [**IMediaObject：:P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) 方法，並將每個要捨棄的資料流程的輸出緩衝區設定為 **Null** 。  (在 [**DMO \_ 輸出 \_ 資料 \_ 緩衝區**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer)的 **pBuffer** 成員中指定輸出緩衝區。 ) 也會在 \_ \_ \_ \_ \_ \_ *dwFlags* 參數中沒有緩衝區旗標時，設定 DMO 流程輸出捨棄。

針對 *pBuffer* 指標為 **Null** 的每個資料流程，DMO 將會嘗試捨棄資料。 如果資料流程是選擇性的，則會保證 DMO 捨棄資料。 如果資料流程不是選擇性的，DMO 會捨棄資料（可能的話），但不保證這麼做。 如果它無法捨棄資料，它會設定 DMO \_ OUTPUT \_ data \_ BUFFERF \_ 不完整旗標。 如果您將 *pBuffer* 指標設定為 **Null** ，但未將 DMO \_ 進程輸出捨棄設定為 \_ \_ \_ \_ 沒有 \_ 緩衝區旗標，則 DMO 不會捨棄資料。 在這種情況下，DMO 會在內部緩衝輸出，或只是因為 **ProcessOutput** 呼叫失敗。

DMO \_ 輸出 \_ STREAMF \_ 選用旗標和 DMO \_ output \_ STREAMF \_ DISCARDABLE 旗標之間唯一的功能差異如下：

-   DMO \_ OUTPUT \_ STREAMF \_ OPTIONAL 旗標表示用戶端不需要在該資料流程上設定媒體類型。 但是，如果用戶端在沒有設定該資料流程的媒體類型的情況下開始處理資料，則它必須在串流的整個持續期間捨棄該資料流程中的資料。 如果您想要選擇性地捨棄樣本，則必須設定媒體類型。
-   DMO \_ OUTPUT \_ STREAMF \_ DISCARDABLE 旗標指出，雖然資料流程是選擇性的，但它一律需要媒體類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[直接裝載 DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



