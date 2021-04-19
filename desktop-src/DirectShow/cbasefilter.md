---
description: CBaseFilter 類別是用來執行篩選的抽象類別。
ms.assetid: 4610c8d6-9d7d-47ca-b1d5-0a867153a5f6
title: 'CBaseFilter 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe032d0614b1067c9351b643d457a718b4917a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993523"
---
# <a name="cbasefilter-class"></a>CBaseFilter 類別

![cbasefilter 類別階層](images/filter01.png)

`CBaseFilter`類別是用來執行篩選的抽象類別。 若要使用這個類別來執行篩選，您必須至少執行下列步驟：

-   從衍生新的類別 `CBaseFilter` 。
-   包含定義篩選準則之圖釘的成員變數。 Pin 必須繼承自 [**CBasePin**](cbasepin.md) 類別。
-   覆寫純虛擬方法 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md)，它會在篩選上抓取圖釘。
-   覆寫單純的虛擬方法 [**CBaseFilter：： GetPinCount**](cbasefilter-getpincount.md)，以抓取釘選數目。
-   提供用來產生、處理或轉譯媒體範例的方法。

有幾個基類衍生自 `CBaseFilter` ，包括 [**CSource**](csource.md)、 [**CBaseRenderer**](cbaserenderer.md)和 [**CTransformFilter**](ctransformfilter.md)。 使用其中一個特製化類別來執行篩選通常會更輕鬆，而不是 `CBaseFilter` 直接使用。



| 受保護的成員變數                                     | Description                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**m \_ 狀態**](cbasefilter-m-state.md)                        | 篩選準則的目前狀態。                                                                       |
| [**m \_ pClock**](cbasefilter-m-pclock.md)                      | 篩選參考時鐘的指標。                                                           |
| [**m \_ tStart**](cbasefilter-m-tstart.md)                      | 對應于資料流程時間0的參考時間。                                                  |
| [**m \_ clsid**](cbasefilter-m-clsid.md)                        | 篩選準則 (CLSID) 的類別識別碼。                                                            |
| [**m \_ pLock**](cbasefilter-m-plock.md)                        | 用來序列化狀態變更的重要區段指標。                             |
| [**m \_ pName**](cbasefilter-m-pname.md)                        | 篩選器名稱。                                                                                       |
| [**m \_ pGraph**](cbasefilter-m-pgraph.md)                      | 篩選圖形管理員的指標。                                                               |
| [**m \_ pSink**](cbasefilter-m-psink.md)                        | 篩選圖形管理員上 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面的指標。   |
| [**m \_ PinVersion**](cbasefilter-m-pinversion.md)              | 此篩選器上的釘選集的目前版本。                                                 |
| 公用方法                                                 | Description                                                                                        |
| [**CBaseFilter**](cbasefilter-cbasefilter.md)                 | 函式方法。                                                                                |
| [**~ CBaseFilter**](cbasefilter--cbasefilter.md)              | 函式方法。                                                                                 |
| [**StreamTime**](cbasefilter-streamtime.md)                   | 抓取目前的資料流程時間。 虛擬。                                                        |
| [**IsActive**](cbasefilter-isactive.md)                       | 判斷篩選目前是否正在使用中 (執行中或已暫停) 。                             |
| [**IsStopped**](cbasefilter-isstopped.md)                     | 判斷篩選目前是否已停止。                                                |
| [**NotifyEvent**](cbasefilter-notifyevent.md)                 | 將事件通知傳送至篩選圖形管理員。                                           |
| [**GetFilterGraph**](cbasefilter-getfiltergraph.md)           | 捕獲篩選圖形管理員的指標。                                                   |
| [**ReconnectPin**](cbasefilter-reconnectpin.md)               | 中斷現有的 pin 連線，並使用指定的媒體類型將它重新連接到相同的 pin。 |
| [**GetPinVersion**](cbasefilter-getpinversion.md)             | 抓取此篩選器集合的版本號碼。 虛擬。                            |
| [**IncrementPinVersion**](cbasefilter-incrementpinversion.md) | 在一組 pin 上遞增版本號碼。                                                  |
| [**GetSetupData**](cbasefilter-getsetupdata.md)               | 捕獲篩選的註冊資料。 虛擬。                                           |
| 純虛擬方法                                           | Description                                                                                        |
| [**GetPinCount**](cbasefilter-getpincount.md)                 | 抓取釘選數目。                                                                      |
| [**GetPin**](cbasefilter-getpin.md)                           | 捕獲 pin。                                                                                   |
| IPersist 方法                                               | Description                                                                                        |
| [**GetClassID**](cbasefilter-getclassid.md)                   | 捕獲類別識別碼。                                                                    |
| IMediaFilter 方法                                           | Description                                                                                        |
| [**GetState**](cbasefilter-getstate.md)                       | 抓取篩選器的狀態 (執行中、已停止或已暫停) 。                                        |
| [**SetSyncSource**](cbasefilter-setsyncsource.md)             | 設定篩選的參考時鐘。                                                             |
| [**GetSyncSource**](cbasefilter-getsyncsource.md)             | 抓取篩選所使用的參考時鐘。                                            |
| [**停止**](cbasefilter-stop.md)                               | 停止篩選。                                                                                  |
| [**暫停**](cbasefilter-pause.md)                             | 暫停篩選。                                                                                 |
| [**執行**](cbasefilter-run.md)                                 | 執行篩選。                                                                                   |
| IBaseFilter 方法                                            | Description                                                                                        |
| [**EnumPins**](cbasefilter-enumpins.md)                       | 列舉此篩選器上的釘選。                                                                |
| [**FindPin**](cbasefilter-findpin.md)                         | 使用指定的識別碼抓取 pin。                                                   |
| [**QueryFilterInfo**](cbasefilter-queryfilterinfo.md)         | 捕獲篩選的相關資訊。                                                            |
| [**JoinFilterGraph**](cbasefilter-joinfiltergraph.md)         | 通知篩選其已加入或離開篩選圖形。                                     |
| [**QueryVendorInfo**](cbasefilter-queryvendorinfo.md)         | 抓取包含廠商資訊的字串。                                                  |
| IAMovieSetup 方法                                           | Description                                                                                        |
| [**註冊**](cbasefilter-register.md)                       | 將篩選新增至登錄。                                                                   |
| [**登出**](cbasefilter-unregister.md)                   | 從登錄中移除篩選。                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




