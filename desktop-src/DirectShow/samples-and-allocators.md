---
description: 範例和配置器
ms.assetid: 1fbea741-f29a-4815-9885-94ca9cf4bb95
title: 範例和配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d196adeb9b5d5bd1220c9d71d74e2c0b23769c20bcad8daf80385aaee3920e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952000"
---
# <a name="samples-and-allocators"></a>範例和配置器

當 pin 將媒體資料傳遞給另一個 pin 時，不會將直接指標傳遞至記憶體緩衝區。 相反地，它會將指標傳遞至管理記憶體的 COM 物件。 這個物件稱為 *媒體範例*，會公開 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面。 接收的 pin 會藉由呼叫 **IMediaSample** 方法（例如 [**IMediaSample：： GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer)、 [**IMediaSample：： GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize)和 [**IMediaSample：： GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength)）來存取記憶體緩衝區。

範例一律會從輸出釘選到輸入 pin，以下游傳送。 在推送模型中，輸出 pin 會在輸入 pin 上呼叫 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 來傳遞範例。 輸入 pin 將會同步處理資料 (也就是完全在 **Receive** 方法) 內，或是在工作者執行緒上以非同步方式處理。 如果需要等候資源，就可以在 **Receive** 方法內封鎖輸入 pin。

另一個 COM 物件稱為配置 *器，負責* 建立和管理媒體範例。 配置器會公開 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面。 每當篩選準則需要具有空緩衝區的媒體範例時，它會呼叫 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法，以傳回範例的指標。 每個 pin 連接都會共用一個配置器。 當兩個 pin 連線時，它們會決定要提供配置器的篩選器。 釘選也會在配置器上設定屬性，例如緩衝區數目和每個緩衝區的大小。  (需詳細資訊，請參閱[篩選連線](how-filters-connect.md)和[協商配置器](negotiating-allocators.md)。 ) 

下圖顯示配置器、媒體範例和篩選器之間的關聯性。

![媒體範例和配置器](images/mediasamples.png)

**媒體範例參考計數**

配置器會建立有限的範例集區。 在任何時候，有些範例可能會在使用中，而其他範例則適用于 **GetBuffer** 呼叫。 配置器會使用參考計數來追蹤範例。 **GetBuffer** 方法會傳回參考計數為1的範例。 如果參考計數變成零，此範例會回到配置器的集區，以便在下一個 **GetBuffer** 呼叫中使用。 只要參考計數維持在零的上方，就無法使用 **GetBuffer** 的範例。 如果正在使用屬於配置器的每個範例， **GetBuffer** 方法會封鎖，直到範例變成可用為止。

例如，假設輸入 pin 會收到範例。 如果它是以同步方式處理範例，則在 **Receive** 方法內，它不會遞增參考計數。 在 **接收** 傳回之後，輸出圖釘會釋出範例，參考計數會變成零，而範例則會返回配置器的集區。 另一方面，如果輸入 pin 在背景工作執行緒上處理此範例，則會在離開 **Receive** 方法之前遞增參考計數。 參考計數現在是2。 當輸出針腳釋出範例時，計數會變成 1;此範例尚未返回集區。 使用範例完成背景工作執行緒之後，它會呼叫 **Release** 來釋放範例。 現在，此範例會回到集區。

當 pin 收到範例時，它可以將資料複製到另一個範例，也可以修改原始範例，並將該範例傳遞給下一個篩選準則。 範例可能會移動整個圖形的長度，每個篩選器會依序呼叫 **AddRef** 和 **放開** 。 因此，在呼叫 **Receive** 之後，輸出 pin 絕對不能重複使用範例，因為下游篩選可能會使用此範例。 輸出 pin 必須一律呼叫 **GetBuffer** 以取得新的範例。

這項機制可減少記憶體配置的數量，因為篩選器會重複使用相同的緩衝區。 它也會防止篩選不小心寫入尚未處理的資料，因為配置器會維護可用範例的清單。

篩選可以針對輸入和輸出使用不同的配置器。 如果展開輸入資料 (例如，將其解壓縮) ，它可能會這麼做。 如果輸出不大於輸入，篩選器可能會就地處理資料，而不會將它複製到新的範例。 在此情況下，兩個或多個 pin 連線可以共用一個配置器。

**認可和 Decommitting 配置器**

當篩選器第一次建立配置器時，配置器尚未保留任何記憶體緩衝區。 此時，對 **GetBuffer** 方法的任何呼叫都將會失敗。 串流處理開始時，輸出圖釘會呼叫 [**IMemAllocator：： Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)，它會認可配置器，使其配置記憶體。 Pin 現在可呼叫 **GetBuffer**。

當串流停止時，pin 會呼叫 [**IMemAllocator：:D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)，以解除配置器。 對 **GetBuffer** 的所有後續呼叫都會失敗，直到重新認可配置器為止。 此外，如果對 **GetBuffer** 的任何呼叫目前封鎖等候範例，則會立即傳回失敗碼。 **取消認可** 方法不一定會釋出記憶體，視執行而定。 例如， [**CMemAllocator**](cmemallocator.md) 類別會等待其「函式」方法釋放記憶體。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選 Graph 中的資料 Flow](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 
