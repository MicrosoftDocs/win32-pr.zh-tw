---
description: 這個類別會為輸入和輸出的釘選 IAMStreamControl 介面。
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: 'CBaseStreamControl 類別 (Strmctl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978669"
---
# <a name="cbasestreamcontrol-class"></a>CBaseStreamControl 類別

![cbasestreamcontrol 類別階層](images/strmctl1.png)

這個類別會為輸入和輸出的釘選 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) 介面。 它可讓您控制在篩選器上啟動及停止個別的 pin。 支援 **IAMStreamControl** 的 pin 應該繼承自這個基類。 以下是輸入 pin 的一般宣告：

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

務必覆寫 **NonDelegatingQueryInteface** 以公開 **IAMStreamControl**。 如需詳細資訊，請參閱 [如何執行 IUnknown](how-to-implement-iunknown.md)。



| 公用方法                                                        | Description                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**CBaseStreamControl**](cbasestreamcontrol-cbasestreamcontrol.md)   | 函式方法。                                                                                  |
| [**~ CBaseStreamControl**](cbasestreamcontrol--cbasestreamcontrol.md) | 函式方法。                                                                                   |
| [**CheckStreamState**](cbasestreamcontrol-checkstreamstate.md)       | 決定是否應該傳遞或捨棄媒體範例。                                  |
| [**沖洗**](cbasestreamcontrol-flushing.md)                       | 通知基類： pin 已啟動或停止排清。                                |
| [**NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md)     | 當篩選準則的狀態變更時，通知 pin。                                                    |
| [**SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md)           | 指定資料流程控制事件的事件接收器。                                                  |
| [**SetSyncSource**](cbasestreamcontrol-setsyncsource.md)             | 通知目前參考時鐘的基類。                                              |
| IAMStreamControl 方法                                              | Description                                                                                          |
| [**GetInfo**](cbasestreamcontrol-getinfo.md)                         | 抓取目前資料流程控制設定的相關資訊，包括開始和停止時間。 |
| [**StartAt**](cbasestreamcontrol-startat.md)                         | 通知 pin 何時開始傳遞資料。                                                       |
| [**StopAt**](cbasestreamcontrol-stopat.md)                           | 通知 pin 何時停止傳遞資料。                                                        |



 

## <a name="remarks"></a>備註

此類別需要 pin 和擁有篩選準則，以在發生各種事件時通知類別，例如加入圖形或接收新的參考時鐘的篩選準則。 您應該呼叫下列類別方法：

-   在篩選的 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) 方法中，呼叫 [**CBaseStreamControl：： SetSyncSource**](cbasestreamcontrol-setsyncsource.md) 方法。 這個方法會通知目前參考時鐘的類別。
-   在篩選的 [**CBaseFilter：： JoinFilterGraph**](cbasefilter-joinfiltergraph.md) 方法中，呼叫 [**CBaseStreamControl：： SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) 方法。 這個方法會為類別提供篩選圖形管理員的指標，讓類別可以傳送正確的資料流程控制事件。
-   每當篩選變更狀態 (為 [執行中]、[已暫停] 或 [已停止]) 時，請呼叫 [**CBaseStreamControl：： NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) 方法。
-   在釘選的 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 和 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法中，呼叫 [**CBaseStreamControl：：**](cbasestreamcontrol-flushing.md) 排清方法。

`CBaseStreamControl`類別會使用篩選圖形的參考時鐘來決定要傳遞的範例，以及應捨棄的範例。 在您的 pin [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法中，以連入媒體範例的指標呼叫 [**CBaseStreamControl：： CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) 方法。 如果方法傳回資料流程 \_ 流動值，請傳遞範例下游。 否則，請捨棄它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Strmctl (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




