---
description: SetCallback 方法會指定要對傳入範例呼叫的回呼方法。
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'ISampleGrabber：： SetCallback 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993524"
---
# <a name="isamplegrabbersetcallback-method"></a>ISampleGrabber：： SetCallback 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

**SetCallback** 方法會指定要對傳入範例呼叫的回呼方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCallback* 
</dt> <dd>

包含回呼方法之 [**ISampleGrabberCB**](isamplegrabbercb.md) 介面的指標，或為 **Null** 以取消回呼。

</dd> <dt>

*WhichMethodToCallback* 
</dt> <dd>

指定回呼方法的索引。 必須是下列其中一個值。



| 值 | 描述                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 範例捕獲篩選準則會呼叫 [**ISampleGrabberCB：： SampleCB**](isamplegrabbercb-samplecb.md) 方法。 這個方法會接收 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 指標。               |
| 1     | 範例捕獲篩選準則會呼叫 [**ISampleGrabberCB：： BufferCB**](isamplegrabbercb-buffercb.md) 方法。 這個方法會接收包含在媒體範例中的緩衝區指標。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

資料處理執行緒會封鎖，直到回呼方法傳回為止。 如果回呼不會快速傳回，它可能會干擾播放。

此篩選不會叫用預算範例的回呼函式，或針對 [**am \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構的 **dwStreamId** 成員是串流媒體以外的任何範例 \_ \_ 。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

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

 

 




