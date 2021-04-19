---
description: EnterBitmapGrabMode 方法會將媒體偵測器切換為點陣圖抓取模式，並搜尋篩選圖形到指定的時間。
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'IMediaDet：： EnterBitmapGrabMode 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983050"
---
# <a name="imediadetenterbitmapgrabmode-method"></a>IMediaDet：： EnterBitmapGrabMode 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會將 `EnterBitmapGrabMode` 媒體偵測器切換為點陣圖抓取模式，並搜尋篩選圖形到指定的時間。

## <a name="syntax"></a>語法


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StreamTime* 
</dt> <dd>

圖表搜尋的時間（以秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下：



| 傳回碼                                                                                             | Description                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 成功。<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | 無效引數。<br/>                             |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | 來源檔案沒有影片串流。<br/> |
| <dl> <dt>**VFW \_ 電子 \_ 時間已 \_ 過期**</dt> </dl>    | 搜尋命令逾時。<br/>                       |



 

## <a name="remarks"></a>備註

在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)

這個方法會將 [**範例捕獲**](sample-grabber-filter.md) 篩選器插入至篩選圖形。 然後，您可以呼叫 [**IMediaDet：： GetSampleGrabber**](imediadet-getsamplegrabber.md) 來取得 [**ISampleGrabber**](isamplegrabber.md) 介面的指標。 一旦媒體偵測器進入點陣圖抓取模式， **IMediaDet** 中的各種資訊方法就無法運作。

[**IMediaDet：： GetBitmapBits**](imediadet-getbitmapbits.md)或 [**IMediaDet：： WriteBitmapBits**](imediadet-writebitmapbits.md)方法也會將媒體偵測器放入點陣圖抓取模式。

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

[**IMediaDet 介面**](imediadet.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




