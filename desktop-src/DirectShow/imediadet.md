---
description: IMediaDet 介面會抓取媒體檔案的相關資訊，例如串流的數目，以及每個資料流程的媒體類型、持續時間和畫面播放速率。
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: 'IMediaDet 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abdf913ab74e6f0f988449a14b84b5be109b9380ebbfb2473edd4a9980f3c577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819030"
---
# <a name="imediadet-interface"></a>IMediaDet 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

介面會抓取媒體檔案的 `IMediaDet` 相關資訊，例如串流的數目，以及每個資料流程的媒體類型、持續時間和畫面播放速率。 它也包含從影片串流中取出個別畫面格的方法。 媒體偵測器 [ (MediaDet) ](media-detector--mediadet.md) 物件會公開這個介面。

若要使用此介面取得檔案的相關資訊，請執行下列步驟：

1.  藉由呼叫 **CoCreateInstance** 來建立 MediaDet 物件的實例。 類別識別碼是 CLSID \_ MediaDet。
2.  呼叫 [**IMediaDet：:p 的 \_**](imediadet-put-filename.md) 檔案名稱，以指定原始程式檔的名稱。
3.  呼叫 [**IMediaDet：： get \_ OutputStreams**](imediadet-get-outputstreams.md) 取得來源中的輸出資料流程數目。
4.  呼叫 [**IMediaDet：:p 工作 \_ CurrentStream**](imediadet-put-currentstream.md) ]，以指定特定的資料流程。
5.  呼叫下列任一方法：
    -   [**IMediaDet：：取得 \_ 幀率**](imediadet-get-framerate.md)
    -   [**IMediaDet：： get \_ StreamLength**](imediadet-get-streamlength.md)
    -   [**IMediaDet：： get \_ StreamMediaType**](imediadet-get-streammediatype.md)
    -   [**IMediaDet：： get \_ StreamType**](imediadet-get-streamtype.md)

若要取出影片框架，請呼叫 [**IMediaDet：： GetBitmapBits**](imediadet-getbitmapbits.md) 或 [**IMediaDet：： WriteBitmapBits**](imediadet-writebitmapbits.md)。 傳回的框架一律採用24位 RGB 格式。

> [!Note]  
> 請勿使用與多個檔案相同的 MediaDet 物件。 若要從多個檔案取得資訊或影片框架，請使用個別的 MediaDet 實例。

 

**IMediaDet** 介面不支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)格式，因此您無法使用此介面來取得交錯式欄位或交錯的相關資訊。 此外，如果上游解碼器只支援 **VIDEOINFOHEADER2**，您就無法使用 `IMediaDet` 。 例如，使用 MPEG-2 解碼器時可能會發生這種情況。 此外， `IMediaDet` 介面會忽略檔案中非影片或音訊的任何資料流程。 例如，如果檔案包含音訊串流、資料流程和影片串流， **get \_ OutputStreams** 方法將只會報告兩個串流 (音訊和影片) 。

## <a name="members"></a>成員

**IMediaDet** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IMediaDet** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMediaDet** 介面具有這些方法。



| 方法                                                        | 描述                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)  | 將媒體偵測器切換為點陣圖抓取模式，並搜尋篩選圖形到指定的時間。<br/> |
| [**取得 \_ CurrentStream**](imediadet-get-currentstream.md)     | 抓取媒體偵測器目前使用的資料流程號碼。<br/>                               |
| [**取得 \_ 檔案名**](imediadet-get-filename.md)               | 抓取媒體偵測器目前所使用的原始程式檔名稱。<br/>                     |
| [**取得 \_ 篩選**](imediadet-get-filter.md)                   | 抓取媒體偵測器目前使用的來源篩選指標。<br/>                  |
| [**取得 \_ 畫面播放速率**](imediadet-get-framerate.md)             | 抓取目前資料流程的畫面播放速率。<br/>                                                 |
| [**取得 \_ OutputStreams**](imediadet-get-outputstreams.md)     | 抓取媒體來源中包含的音訊和影片資料流程數目。<br/>                  |
| [**取得 \_ StreamLength**](imediadet-get-streamlength.md)       | 捕獲目前資料流程的持續時間。<br/>                                                   |
| [**取得 \_ StreamMediaType**](imediadet-get-streammediatype.md) | 抓取目前資料流程的媒體類型。<br/>                                                 |
| [**取得 \_ StreamType**](imediadet-get-streamtype.md)           | 針對目前資料流程的媒體類型，抓取全域唯一識別碼 (GUID) 。<br/>       |
| [**取得 \_ StreamTypeB**](imediadet-get-streamtypeb.md)         | 抓取字串，表示目前資料流程之媒體類型的 GUID。<br/>              |
| [**GetBitmapBits**](imediadet-getbitmapbits.md)              | 抓取指定媒體時間的影片畫面。<br/>                                            |
| [**GetSampleGrabber**](imediadet-getsamplegrabber.md)        | 捕獲 [**ISampleGrabber**](isamplegrabber.md) 介面的指標。<br/>                  |
| [**put \_ CurrentStream**](imediadet-put-currentstream.md)     | 指定要使用之媒體偵測器的串流號碼。<br/>                                      |
| [**放置 \_ 檔案名**](imediadet-put-filename.md)               | 指定媒體偵測器要使用的原始程式檔名稱。<br/>                            |
| [**put \_ 篩選**](imediadet-put-filter.md)                   | 指定媒體偵測器要使用的來源篩選器。<br/>                                        |
| [**WriteBitmapBits**](imediadet-writebitmapbits.md)          | 在指定的媒體時間抓取影片畫面格，並將其寫入檔案。<br/>                    |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
