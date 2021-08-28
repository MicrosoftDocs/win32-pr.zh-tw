---
description: CBasePin 類別是一個抽象類別，可實作為泛型的釘選。
ms.assetid: 23b9a0e2-24fe-4ff9-b2bb-97630c237de9
title: 'CBasePin 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55f697d6ff1a2bd3ebac77a77d8ba98321f29d09a75181b52e8ef08b03eed682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056191"
---
# <a name="cbasepin-class"></a>CBasePin 類別

![cbasepin 類別階層](images/filter02.png)

`CBasePin`類別是抽象類別，可實作為泛型的釘選。

下列主題描述如何使用這個類別：

-   [CBasePin 連接進程](cbasepin-connection-process.md)
-   [通知 CBasePin 篩選狀態變更](notifying-cbasepin-of-filter-state-changes.md)
-   [衍生自 CBasePin](deriving-from-cbasepin.md)



| 受保護的成員變數                                               | 描述                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**m \_ pName**](cbasepin-m-pname.md)                                     | Pin 名稱。                                                                                                  |
| [**m \_ 已連線**](cbasepin-m-connected.md)                             | 連接至此釘選的釘選指標。                                                          |
| [**m \_ dir**](cbasepin-m-dir.md)                                         | Pin 的方向。                                                                                      |
| [**m \_ pLock**](cbasepin-m-plock.md)                                     | 重要區段物件的指標。                                                                      |
| [**m \_ bRunTimeError**](cbasepin-m-bruntimeerror.md)                     | 指出執行階段錯誤是否發生的旗標。                                                 |
| [**m \_ bCanReconnectWhenActive**](cbasepin-m-bcanreconnectwhenactive.md) | 指出 pin 是否支援動態重新連接的旗標。                                         |
| [**m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md)               | 旗標，指出 pin 是否先嘗試其慣用的媒體類型，再接收 pin。 |
| [**m \_ pFilter**](cbasepin-m-pfilter.md)                                 | 建立釘選之篩選準則的指標。                                                                |
| [**m \_ pQSink**](cbasepin-m-pqsink.md)                                   | 處理品質訊息之物件的指標。                                                       |
| [**m \_ TypeVersion**](cbasepin-m-typeversion.md)                         | 慣用媒體類型集合的最新版本。                                                       |
| [**m \_ mt**](cbasepin-m-mt.md)                                           | 目前連接的媒體類型。                                                                 |
| [**m \_ tStart**](cbasepin-m-tstart.md)                                   | 區段開始時間。                                                                                        |
| [**m \_ tStop**](cbasepin-m-tstop.md)                                     | 區段停止時間。                                                                                         |
| [**m \_ dRate**](cbasepin-m-drate.md)                                     | 區段速率。                                                                                              |
| 保護方法                                                        | 描述                                                                                                |
| [**DisplayPinInfo**](cbasepin-displaypininfo.md)                        | 在調試過程中追蹤 pin 連接。                                                                  |
| [**DisplayTypeInfo**](cbasepin-displaytypeinfo.md)                      | 在調試過程中顯示媒體類型資訊。                                                          |
| [**AttemptConnection**](cbasepin-attemptconnection.md)                  | 使用指定的媒體類型連接到另一個 pin。                                                      |
| [**TryMediaTypes**](cbasepin-trymediatypes.md)                          | 指定媒體類型的清單之後，會嘗試使用這些類型的其中一種來完成連接。                      |
| [**AgreeMediaType**](cbasepin-agreemediatype.md)                        | 搜尋媒體類型以建立 pin 連接。                                                        |
| [**DisconnectInternal**](cbasepin-disconnectinternal.md)                | 中斷目前的 pin 連接。                                                                         |
| 公用方法                                                           | 描述                                                                                                |
| [**CBasePin**](cbasepin-cbasepin.md)                                    | 函式方法。                                                                                        |
| [**~ CBasePin**](cbasepin--cbasepin.md)                                 | 函式方法。 虛擬。                                                                                |
| [**IsConnected**](cbasepin-isconnected.md)                              | 判斷 pin 是否已連接到另一個 pin。                                                    |
| [**GetConnected**](cbasepin-getconnected.md)                            | 抓取連接至此釘選的釘選。                                                           |
| [**IsStopped**](cbasepin-isstopped.md)                                  | 判斷包含此 pin 的篩選是否已停止。                                              |
| [**GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)              | 抓取一組慣用媒體類型的版本號碼。 虛擬。                                  |
| [**IncrementTypeVersion**](cbasepin-incrementtypeversion.md)            | 遞增一組慣用媒體類型的版本號碼。                                         |
| [**使用中**](cbasepin-active.md)                                        | 通知釘選篩選現在已啟用。 虛擬。                                                   |
| [**非使用中**](cbasepin-inactive.md)                                    | 通知 pin 此篩選已不再有效。 虛擬。                                             |
| [**執行**](cbasepin-run.md)                                              | 通知釘選篩選現在正在執行。 虛擬。                                                  |
| [**SetMediaType**](cbasepin-setmediatype.md)                            | 設定連接的媒體類型。 虛擬。                                                           |
| [**CheckConnect**](cbasepin-checkconnect.md)                            | 判斷 pin 連接是否合適。 虛擬。                                                  |
| [**BreakConnect**](cbasepin-breakconnect.md)                            | 釋放連接的 pin。 虛擬。                                                               |
| [**CompleteConnect**](cbasepin-completeconnect.md)                      | 完成與另一個 pin 的連接。 虛擬。                                                            |
| [**GetMediaType**](cbasepin-getmediatype.md)                            | 依索引值抓取慣用的媒體類型。 虛擬。                                                 |
| [**CurrentStopTime**](cbasepin-currentstoptime.md)                      | 捕獲區段停止時間。                                                                           |
| [**CurrentStartTime**](cbasepin-currentstarttime.md)                    | 捕獲區段開始時間。                                                                          |
| [**CurrentRate**](cbasepin-currentrate.md)                              | 捕獲區段速率。                                                                                |
| [**名稱**](cbasepin-name.md)                                            | 抓取 pin 識別碼。                                                                              |
| [**SetReconnectWhenActive**](cbasepin-setreconnectwhenactive.md)        | 指定 pin 是否支援動態重新連接。                                                  |
| [**CanReconnectWhenActive**](cbasepin-canreconnectwhenactive.md)        | 查詢 pin 是否支援動態重新連接。                                                    |
| 純虛擬方法                                                     | 描述                                                                                                |
| [**CheckMediaType**](cbasepin-checkmediatype.md)                        | 判斷 pin 是否接受特定的媒體類型。                                                       |
| IPin 方法                                                             | 描述                                                                                                |
| [**連線**](cbasepin-connect.md)                                      | 將 pin 連接到另一個 pin。                                                                           |
| [**ReceiveConnection**](cbasepin-receiveconnection.md)                  | 接受來自另一個 pin 的連接。                                                                     |
| [**中斷連線**](cbasepin-disconnect.md)                                | 中斷目前的 pin 連接。                                                                         |
| [**ConnectedTo**](cbasepin-connectedto.md)                              | 抓取連接至此釘選的 pin。                                                                   |
| [**ConnectionMediaType**](cbasepin-connectionmediatype.md)              | 抓取目前 pin 連接的媒體類型（如果有的話）。                                           |
| [**QueryPinInfo**](cbasepin-querypininfo.md)                            | 抓取釘選的相關資訊。                                                                       |
| [**QueryDirection**](cbasepin-querydirection.md)                        | 抓取 pin (輸入或輸出) 的方向。                                                      |
| [**QueryId**](cbasepin-queryid.md)                                      | 抓取 pin 識別碼。                                                                              |
| [**QueryAccept**](cbasepin-queryaccept.md)                              | 判斷 pin 是否接受指定的媒體類型。                                                 |
| [**EnumMediaTypes**](cbasepin-enummediatypes.md)                        | 列舉釘選的慣用媒體類型。                                                                |
| [**QueryInternalConnections**](cbasepin-queryinternalconnections.md)    | 抓取篩選) 內 (在內部連接到此 pin 的釘選。                          |
| [**EndOfStream**](cbasepin-endofstream.md)                              | 通知 pin，不需要額外的資料。                                                      |
| [**NewSegment**](cbasepin-newsegment.md)                                | 通知釘選將此呼叫群組為區段之後所收到的媒體範例。                     |
| IQualityControl 方法                                                  | 描述                                                                                                |
| [**通知**](cbasepin-notify.md)                                        | 通知 pin 已要求品質變更。                                                       |
| [**SetSink**](cbasepin-setsink.md)                                      | 設定外部品質管制員。                                                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




