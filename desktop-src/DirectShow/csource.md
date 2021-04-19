---
description: CSource 類別是用來執行來源篩選準則的基類。 衍生自 CSource 的篩選包含一或多個衍生自 CSourceStream 類別的輸出圖釘。 每個輸出釘選都會建立會將媒體範例推送至下游的背景工作執行緒。
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: 'CSource 類別 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989660"
---
# <a name="csource-class"></a>CSource 類別

![csource 類別階層](images/source01.png)

**CSource** 類別是用來執行來源篩選準則的基類。 衍生自 **CSource** 的篩選包含一或多個衍生自 [**CSourceStream**](csourcestream.md) 類別的輸出圖釘。 每個輸出釘選都會建立會將媒體範例推送至下游的背景工作執行緒。

> [!Note]  
> **CSource** 類別是設計來支援資料流程的推送模型。 此類別不建議用來建立檔案讀取器篩選。 檔案讀取器應該透過 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面支援提取模型。 如需詳細資訊，請參閱 [篩選開發人員的](data-flow-for-filter-developers.md)資料流程。

 



| 受保護的成員變數                     | Description                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**m \_ iPins**](csource-m-ipins.md)            | 篩選器上的釘選數目。                                |
| [**m \_ paStreams**](csource-m-pastreams.md)    | Pin 的陣列。                                               |
| [**m \_ cStateLock**](csource-m-cstatelock.md)  | 保護篩選狀態的重要區段物件。      |
| 公用方法                                 | Description                                                  |
| [**CSource**](csource-csource.md)             | 函式方法。                                          |
| [**~ CSource**](csource--csource.md)           | 函式方法。                                           |
| [**GetPinCount**](csource-getpincount.md)     | 抓取篩選上的釘選數目。                  |
| [**GetPin**](csource-getpin.md)               | 捕獲 pin。                                             |
| [**pStateLock**](csource--pstatelock.md)      | 抓取篩選準則的重要區段物件的指標。 |
| [**AddPin**](csource-addpin.md)               | 將新的輸出圖釘新增至篩選準則。                         |
| [**RemovePin**](csource-removepin.md)         | 從篩選中移除指定的 pin。                     |
| [**FindPinNumber**](csource-findpinnumber.md) | 抓取篩選上指定之圖釘的數目。       |
| IBaseFilter 方法                            | Description                                                  |
| [**FindPin**](csource-findpin.md)             | 使用指定的識別碼抓取 pin。             |



 

## <a name="remarks"></a>備註

若要執行輸出釘選，請執行下列動作：

-   從 [**CSourceStream**](csourcestream.md)衍生類別。
-   覆寫 [**CSourceStream：： GetMediaType**](csourcestream-getmediatype.md) 方法，可能是 [**CSourceStream：： CheckMediaType**](csourcestream-checkmediatype.md) 方法，它會驗證 pin 的媒體類型。
-   執行 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) 方法，這會傳回 pin 的緩衝區需求。
-   執行 [**CSourceStream：： FillBuffer**](csourcestream-fillbuffer.md) 方法，以資料填入媒體範例緩衝區。

若要執行篩選準則，請執行下列動作：

-   從 **CSource** 衍生類別。
-   在此函式中，建立一個或多個衍生自 [**CSourceStream**](csourcestream.md)的輸出圖釘。 Pin 會在其函式方法中自動將自己新增至篩選器，並在其函式方法中移除本身。

若要同步處理多個執行緒之間的篩選狀態，請呼叫 [**CSource：:P statelock**](csource--pstatelock.md) 方法。 這個方法會將指標傳回至篩選狀態重要區段。 使用 [**CAutoLock**](cautolock.md) 類別來保存重要區段。 從 pin，您可以從釘選的 [**CBasePin：： m \_ pFilter**](cbasepin-m-pfilter.md)成員變數存取 **pStateLock** ，如下所示：


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[寫入來源篩選](writing-source-filters.md)
</dt> </dl>

 

 




