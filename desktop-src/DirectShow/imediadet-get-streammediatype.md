---
description: Get \_ StreamMediaType 方法會抓取目前資料流程的媒體類型。 所有的影片串流都會轉換成 VIDEOINFOHEADER 類型，而所有音訊串流都會轉換成 WAVEFORMATEX 類型。
ms.assetid: 7fc15cb3-af77-42c1-b5eb-d1d88bf9cd1d
title: 'IMediaDet：： get_StreamMediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e62f7c7d5a6881647280e17d7ae21c442ae57c21a0c48470e255434007c5db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154180"
---
# <a name="imediadetget_streammediatype-method"></a>IMediaDet：： get \_ StreamMediaType 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `get_StreamMediaType` 目前資料流程的媒體類型。 所有的影片串流都會轉換成 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 類型，而所有音訊串流都會轉換成 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 類型。

## <a name="syntax"></a>語法


```C++
HRESULT get_StreamMediaType(
  [out, retval] AM_MEDIA_TYPE *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[退出，retval\]
</dt> <dd>

以媒體類型填滿的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)

如果媒體偵測器處於點陣圖抓取模式，這個方法會傳回 E \_ INVALIDARG。 如需詳細資訊，請參閱 [**IMediaDet：： EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)。

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

[**IMediaDet 介面**](imediadet.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 
