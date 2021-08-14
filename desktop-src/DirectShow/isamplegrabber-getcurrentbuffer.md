---
description: GetCurrentBuffer 方法會抓取與最新樣本相關聯的緩衝區複本。
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'ISampleGrabber：： GetCurrentBuffer 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 88af9469a1470a02be62b7684a66990c5622820e370518ed53267bd87d981879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818047"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a>ISampleGrabber：： GetCurrentBuffer 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

**GetCurrentBuffer** 方法會抓取與最新樣本相關聯的緩衝區複本。

## <a name="syntax"></a>語法


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBufferSize* \[in、out\]
</dt> <dd>

緩衝區大小的指標。 如果 *pBuffer* 為 **Null**，則此參數會收到所需的緩衝區大小（以位元組為單位）。 如果 *pBuffer* 不是 **Null**，請將此參數設定為等於緩衝區的大小（以位元組為單位）。 在輸出上，參數會接收復制到緩衝區的位元組數目。 這個值可能小於緩衝區的大小。

</dd> <dt>

*pBuffer* \[擴展\]
</dt> <dd>

*PBufferSize* 大小位元組陣列的指標，或 **為 Null**。 如果這個參數不是 **Null**，則會將目前的緩衝區複製到陣列中。 如果此參數為 **Null**，則 *pBufferSize* 參數會收到所需的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值。



| 傳回碼                                                                                           | Description                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | 未緩衝處理範例。 呼叫 [**ISampleGrabber：： SetBufferSamples**](isamplegrabber-setbuffersamples.md)。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | 指定的緩衝區不夠大。<br/>                                                                         |
| <dl> <dt>**E \_ 指標**</dt> </dl>             | **Null** 指標引數。<br/>                                                                                        |
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                                                                                                          |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 篩選未連接。<br/>                                                                                      |
| <dl> <dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt> </dl>   | 篩選尚未收到任何範例。 若要傳遞範例，請執行或暫停圖形。<br/>                         |



 

## <a name="remarks"></a>備註

若要啟用緩衝處理，請呼叫 [**ISampleGrabber：： SetBufferSamples**](isamplegrabber-setbuffersamples.md) ，並將值 **設為 TRUE**。

呼叫這個方法兩次。 在第一次呼叫時，將 *pBuffer* 設定為 **Null**。 緩衝區的大小會在 *pBufferSize* 中傳回。 然後配置陣列，並再次呼叫方法。 在第二個呼叫中，傳遞 *pBufferSize* 中的陣列大小，然後在 *pBuffer* 中傳遞陣列的位址。 如果陣列不夠大，則方法會傳回 E \_ OUTOFMEMORY。

*PBuffer* 參數的類型為 **long** 指標，但緩衝區的內容會根據資料的格式而定。 呼叫 [**ISampleGrabber：： GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) 來取得格式的媒體類型。

當篩選圖形正在執行時，請勿呼叫這個方法。 當篩選圖形正在執行時，範例捕獲篩選器會在每次收到新的範例時覆寫緩衝區的內容。 使用這個方法的最佳方式是使用「一次模式」，這會在收到第一個樣本之後停止圖形。 若要設定一次模式，請呼叫 [**ISampleGrabber：： SetOneShot**](isamplegrabber-setoneshot.md)。

篩選不會緩衝預先執行的範例，或者 [**am \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構的 **dwStreamId** 成員是串流媒體以外的任何其他範例 \_ \_ 。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用範例捕獲](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber 介面**](isamplegrabber.md)
</dt> </dl>

 

 




