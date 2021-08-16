---
description: CPullPin 類別可支援透過 IAsyncReader 介面提取資料的輸入圖釘。
ms.assetid: 33a6c342-3896-41f8-b32d-01db3eed003e
title: 'CPullPin 類別 (Pullpin) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d70217fa60afdae3f588f98ecbe61a728ace6ec0b0d78859f55cd241cbc00e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330841"
---
# <a name="cpullpin-class"></a>CPullPin 類別

![cpullpin 類別階層](images/pulpin01.png)

`CPullPin`類別可支援透過 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)介面提取資料的輸入圖釘。 如果您正在執行使用提取模型來要求上游篩選器資料的篩選，請使用這個類別。 如需詳細資訊，請參閱篩選 Graph 和提取模型中的資料 Flow。

這個類別不會衍生自 **CBasePin** 或實作為 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面，而某些方法名稱會與 **IPin** 衝突，因此最適合用來做為 pin 內的 helper 物件。 若要使用此類別，請執行下列動作：

1.  從衍生一個 helper 類別 `CPullPin` ，並從 **CBasePin** 衍生一個輸入圖釘類別。 將物件的實例宣告 `CPullPin` 為釘選類別的成員變數。
2.  覆寫 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md)方法，以呼叫 [**CPullPin：：連線**](cpullpin-connect.md)。 這個方法會查詢另一個 pin 以進行 **IAsyncReader**。
3.  覆寫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法以呼叫 [**CPullPin：:D isconnect**](cpullpin-disconnect.md)。
4.  覆寫 [**CBasePin：： active**](cbasepin-active.md) 方法以呼叫 [**CPullPin：： active**](cpullpin-active.md)。 這個方法會啟動從上游篩選器提取樣本的背景工作執行緒。 當釘選連線時，您可以指定是否要讓工作者執行緒建立異步或同步讀取要求。
5.  覆寫 [**CBasePin：：非**](cbasepin-inactive.md) 使用中方法，以呼叫 [**CPullPin：：非**](cpullpin-inactive.md)使用中。 這個方法會關閉背景工作執行緒。
6.  執行純虛擬 [**CPullPin：： Receive**](cpullpin-receive.md) 方法來處理傳入範例，並將其傳遞至下游。
7.  若要設定停止和開始位置，或要搜尋資料流程，請呼叫 [**CPullPin：： seek**](cpullpin-seek.md) 方法。 這個方法會暫停背景工作執行緒，並清除篩選圖形。
8.  依照這些方法的備註所述，執行純虛擬 [**CPullPin：： EndOfStream**](cpullpin-endofstream.md)、 [**CPullPin：： BeginFlush**](cpullpin-beginflush.md)和 [**CPullPin：： EndFlush**](cpullpin-endflush.md) 方法。
9.  執行純虛擬 [**CPullPin：： OnError**](cpullpin-onerror.md) 方法來處理串流錯誤。



| Public 成員變數                             | 描述                                                                           |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [**m \_ pAlloc**](cpullpin-m-palloc.md)              | 記憶體配置器之 **IMemAllocator** 介面的指標。                   |
| 公用方法                                      | 描述                                                                           |
| [**使用中**](cpullpin-active.md)                   | 建立從輸出釘選提取資料的背景工作執行緒。                          |
| [**AlignDown**](cpullpin-aligndown.md)             | 將值截斷為指定的對齊界限。                                  |
| [**AlignUp**](cpullpin-alignup.md)                 | 將值四捨五入到指定的對齊界限。                                  |
| [**連線**](cpullpin-connect.md)                 | 完成輸出釘選的連接。                                             |
| [**CPullPin**](cpullpin-cpullpin.md)               | 函式方法。                                                                   |
| [**~ CPullPin**](cpullpin--cpullpin.md)             | 函式方法。 虛擬。                                                           |
| [**DecideAllocator**](cpullpin-decideallocator.md) | 使用輸出圖釘協調配置器。 虛擬。                                 |
| [**中斷連線**](cpullpin-disconnect.md)           | 使用輸出圖釘 Beaks 連接。                                             |
| [**持續時間**](cpullpin-duration.md)               | 捕獲資料流程的持續時間。                                                 |
| [**System.diagnostics.symbolstore.isymbolbinder1.getreader**](cpullpin-getreader.md)             | 傳回輸出釘選 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面的指標。 |
| [**非使用中**](cpullpin-inactive.md)               | 關閉從輸出圖釘提取資料的背景工作執行緒。                     |
| [**Seek**](cpullpin-seek.md)                       | 設定資料流程的開始和停止位置。                                      |
| 純虛擬方法                                | 描述                                                                           |
| [**BeginFlush**](cpullpin-beginflush.md)           | 通知擁有篩選以排清下游篩選。                            |
| [**EndFlush**](cpullpin-endflush.md)               | 通知擁有篩選結束清除作業。                                   |
| [**EndOfStream**](cpullpin-endofstream.md)         | 在物件傳遞最後一個範例之後呼叫。                                     |
| [**OnError**](cpullpin-onerror.md)                 | 在串流處理期間發生錯誤時呼叫。                                           |
| [**收到**](cpullpin-receive.md)                 | 當物件從輸出圖釘接收媒體範例時呼叫。                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




