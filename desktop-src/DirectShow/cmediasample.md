---
description: CMediaSample 類別會定義支援 IMediaSample2 介面的媒體範例。 媒體範例包含記憶體緩衝區的指標，以及儲存為受保護成員變數的各種屬性。
ms.assetid: 1e609c7c-3200-4540-904e-7659976df0da
title: 'CMediaSample 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72cfe0f86ff6b6643f2f7793822899136a5c6454
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995908"
---
# <a name="cmediasample-class"></a>CMediaSample 類別

![cmediasample 類別階層](images/wutil03.png)

`CMediaSample`類別會定義支援 [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2)介面的媒體範例。 媒體範例包含記憶體緩衝區的指標，以及儲存為受保護成員變數的各種屬性。

媒體範例是由配置器所建立，其衍生自 [**CBaseAllocator**](cbaseallocator.md) 類別。 此函式會接收所配置 `CMediaSample` 緩衝區的指標，以及緩衝區的大小。 其他屬性通常是透過 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面方法來設定和取出。

媒體範例的生命週期與大部分 COM 物件的生命週期不同：

-   配置器會保留免費範例的清單。 當篩選準則需要新的範例時，它會呼叫配置器的 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法。 配置器會從它的可用清單中抓取範例、遞增樣本的參考計數，然後將指標傳回範例。
-   使用範例完成篩選之後，它會在範例上呼叫 **IUnknown：： Release** 方法。 與大部分的物件不同的是，此範例不會在其參考計數到達零時刪除本身。 相反地，它會在配置器上呼叫 [**IMemAllocator：： ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) 方法，而配置器會將範例傳回到可用清單。
-   配置器在呼叫 [**IMemAllocator：:D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) 方法之前，不會終結樣本。



| 受保護的成員變數                                           | Description                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**m \_ dwFlags**](cmediasample-m-dwflags.md)                         | 範例屬性旗標。                                                                          |
| [**m \_ dwTypeSpecificFlags**](cmediasample-m-dwtypespecificflags.md) | 特定類型的旗標。                                                                            |
| [**m \_ pBuffer**](cmediasample-m-pbuffer.md)                         | 包含媒體資料之記憶體緩衝區的指標。                                      |
| [**m \_ lActual**](cmediasample-m-lactual.md)                         | 緩衝區中有效資料的長度（以位元組為單位）。                                               |
| [**m \_ cbBuffer**](cmediasample-m-cbbuffer.md)                       | 緩衝區的大小（以位元組為單位）。                                                                   |
| [**m \_ pAllocator**](cmediasample-m-pallocator.md)                   | 建立此範例的配置器指標。                                              |
| [**m \_ pNext**](cmediasample-m-pnext.md)                             | 配置器的範例清單中，下一個範例的指標。                                  |
| [**m \_ 開始**](cmediasample-m-start.md)                             | 範例開始時間。                                                                              |
| [**m \_ 結束**](cmediasample-m-end.md)                                 | 範例結束時間。                                                                                |
| [**m \_ MediaStart**](cmediasample-m-mediastart.md)                   | 媒體開始時間。                                                                               |
| [**m \_ MediaEnd**](cmediasample-m-mediaend.md)                       | 媒體停止時間。                                                                                |
| [**m \_ pMediaType**](cmediasample-m-pmediatype.md)                   | 媒體類型的指標，如果類型已在資料流程中的前一個範例變更。 |
| [**m \_ dwStreamId**](cmediasample-m-dwstreamid.md)                   | 資料流程識別碼。                                                                              |
| Public 成員變數                                              | Description                                                                                     |
| [**m \_ cRef**](cmediasample-m-cref.md)                               | 參考計數。                                                                                |
| 公用方法                                                       | Description                                                                                     |
| [**CMediaSample**](cmediasample-cmediasample.md)                    | 函式方法。                                                                             |
| [**~ CMediaSample**](cmediasample--cmediasample.md)                 | 函式方法。 虛擬。                                                                     |
| [**SetPointer**](cmediasample-setpointer.md)                        | 設定記憶體緩衝區的指標。                                                          |
| IMediaSample 方法                                                 | Description                                                                                     |
| [**GetPointer**](cmediasample-getpointer.md)                        | 擷取緩衝區的讀取/寫入指標。                                                   |
| [**GetSize**](cmediasample-getsize.md)                              | 擷取緩衝區的大小。                                                               |
| [**GetTime**](cmediasample-gettime.md)                              | 抓取此範例應開始及完成的資料流程時間。                        |
| [**SetTime**](cmediasample-settime.md)                              | 設定此範例應開始及完成的資料流程時間。                             |
| [**IsSyncPoint**](cmediasample-issyncpoint.md)                      | 判斷範例的開頭是否為同步處理點。                           |
| [**SetSyncPoint**](cmediasample-setsyncpoint.md)                    | 指定此範例的開頭是否為同步處理點。                      |
| [**IsPreroll**](cmediasample-ispreroll.md)                          | 判斷此範例是否為可提前取樣。                                                  |
| [**SetPreroll**](cmediasample-setpreroll.md)                        | 指定此範例是否為可提前取樣。                                              |
| [**GetActualDataLength**](cmediasample-getactualdatalength.md)      | 擷取緩衝區中有效資料的長度。                                           |
| [**SetActualDataLength**](cmediasample-setactualdatalength.md)      | 設定緩衝區中有效資料的長度。                                                |
| [**GetMediaType**](cmediasample-getmediatype.md)                    | 如果媒體類型與先前的範例不同，則抓取媒體類型。                   |
| [**SetMediaType**](cmediasample-setmediatype.md)                    | 設定範例的媒體類型。                                                             |
| [**IsDiscontinuity**](cmediasample-isdiscontinuity.md)              | 判斷此範例是否表示資料流程中的中斷。                                |
| [**SetDiscontinuity**](cmediasample-setdiscontinuity.md)            | 指定此範例是否表示資料流程中的中斷。                            |
| [**GetMediaTime**](cmediasample-getmediatime.md)                    | 捕獲此範例的媒體時間。                                                      |
| [**SetMediaTime**](cmediasample-setmediatime.md)                    | 設定此範例的媒體時間。                                                           |
| IMediaSample2 方法                                                | Description                                                                                     |
| [**GetProperties**](cmediasample-getproperties.md)                  | 抓取範例的屬性。                                                         |
| [**SetProperties**](cmediasample-setproperties.md)                  | 設定範例的屬性。                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




