---
description: Get \_ StreamType 方法會針對目前資料流程的媒體類型，抓取 (GUID) 的全域唯一識別碼。
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'IMediaDet：： get_StreamType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984826"
---
# <a name="imediadetget_streamtype-method"></a>IMediaDet：： get \_ StreamType 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`get_StreamType`方法會針對目前資料流程的媒體類型，抓取 (GUID) 的全域唯一識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[退出，retval\]
</dt> <dd>

接收媒體類型的主要類型 GUID。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法會抓取 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的 **majortype** 成員。 **AM \_ 媒體 \_ 類型** 結構描述資料流程的格式，而 **majortype** 成員是指出一般類別的 GUID，例如音訊或影片。 若為影片串流，GUID 為媒體媒體 \_ 。 若是音訊，則是媒體媒體 \_ 。 若要取出整個 **AM \_ 媒體 \_ 類型** 結構，請呼叫 [**IMediaDet：： get \_ StreamMediaType**](imediadet-get-streammediatype.md) 方法。

在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)

如果媒體偵測器處於點陣圖抓取模式，這個方法會傳回 E \_ INVALIDARG。 如需詳細資訊，請參閱 [**IMediaDet：： EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)。

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

 

 




