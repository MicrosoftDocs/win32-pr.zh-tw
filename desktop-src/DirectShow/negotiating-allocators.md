---
description: 協商配置器
ms.assetid: fe13477c-1a7b-4098-9d0f-c54783102bc9
title: 協商配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2faa393ba9fcd8585d68947cec172d4cfca6decf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970068"
---
# <a name="negotiating-allocators"></a>協商配置器

當兩個 pin 連線時，他們需要一種機制來交換媒體資料。 這項機制稱為「 *傳輸*」。 一般而言，DirectShow 架構與傳輸無關。 有兩個篩選器可以使用兩個支援的傳輸來同意連接。

最常見的傳輸是 *本機記憶體* 傳輸，其中的媒體資料位於主儲存體中。 本機記憶體傳輸有兩種： *推送模型* 和 *提取模型*。 在推送模型中，來源篩選器會使用下游篩選器輸入 pin 上的 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面，將資料推送至下游篩選器。 在提取模型中，下游篩選器會使用來源篩選器輸出釘選上的 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面，要求來源篩選的資料。 如需這兩種資料流程模型的詳細資訊，請參閱 [篩選圖形中的](data-flow-in-the-filter-graph.md)資料流程。

在本機記憶體傳輸中，負責配置記憶體 *緩衝區的物件* 稱為配置器。 配置器支援 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面。 這兩個 pin 都會共用單一配置器。 這兩種 pin 都可提供配置器，但輸出 pin 會選取要使用的配置器。

輸出釘選也會設定配置器屬性，以判斷配置器所建立的緩衝區數目、每個緩衝區的大小，以及記憶體的對齊方式。 輸出釘選可能會延後到緩衝區需求的輸入 pin。

在 **IMemInputPin** 連接中，配置器協商的運作方式如下：

1.  （選擇性）輸出圖釘會呼叫 [**IMemInputPin：： GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements)。 這個方法會抓取輸入釘選的緩衝區需求，例如記憶體對齊。 一般而言，輸出 pin 應接受輸入 pin 的要求，除非有很好的理由。
2.  （選擇性）輸出圖釘會呼叫 [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)。 這個方法會從輸入 pin 要求配置器。 輸入 pin 碼會提供一個，或傳回錯誤碼。
3.  輸出釘選會選取配置器。 它可以使用輸入 pin 所提供的一個，或建立自己的 pin。
4.  輸出圖釘會呼叫 [**IMemAllocator：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) 來設定配置器屬性。 不過，配置器可能無法接受要求的屬性。  (例如，如果輸入 pin 提供配置器，就會發生這種情況。 ) 配置器會以 **SetProperties** 方法中的輸出參數傳回實際的屬性。
5.  Outpin 會呼叫 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) 來通知選取專案的輸入 pin。
6.  輸入 pin 應呼叫 [**IMemAllocator：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) ，以確認是否可接受配置器屬性。
7.  輸出針腳負責認可和 decommitting 配置器。 當串流開始和停止時，就會發生這種情況。

在 **IAsyncReader** 連接中，配置器協商的運作方式如下：

1.  輸入 pin 會在輸出釘選上呼叫 [**IAsyncReader：： RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) 。 輸入 pin 會指定其緩衝區需求，並選擇性地提供配置器。
2.  輸出釘選會選取配置器。 它可以使用輸入 pin 所提供的埠（如果有的話），或建立自己的 pin。
3.  輸出圖釘會以 **RequestAllocator** 方法中的外寄參數傳回配置器。 輸入的 pin 應檢查配置器屬性。
4.  輸入 pin 負責認可和 decommitting 配置器。
5.  在配置器協商程式進行期間，任何一種 pin 都可能會使連接失敗。
6.  如果輸出釘選使用輸入釘選器，它只能使用該配置器將範例傳遞給該輸入 pin。 擁有篩選不得使用配置器將範例傳遞給其他 pin。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[提供自訂配置器](providing-a-custom-allocator.md)
</dt> </dl>

 

 



