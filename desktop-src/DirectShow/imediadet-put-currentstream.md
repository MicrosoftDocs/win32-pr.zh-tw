---
description: Put \_ CurrentStream 方法會指定要使用之媒體偵測器的串流號碼。
ms.assetid: 01fb7ccf-9b45-434c-b574-f3027d85ea8a
title: 'IMediaDet：:p ut_CurrentStream 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ba8b9cfe7cf898e9645d0f1caf8ef789bb45967bfc268f08555a5bdea53c4127
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952597"
---
# <a name="imediadetput_currentstream-method"></a>IMediaDet：:p 的 \_ CurrentStream 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`put_CurrentStream`方法會指定要使用之媒體偵測器的串流號碼。

## <a name="syntax"></a>語法


```C++
HRESULT put_CurrentStream(
  [in] long newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* \[在\]
</dt> <dd>

資料流程號碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p 的 \_**](imediadet-put-filename.md) 檔案名稱，以設定檔案名。 呼叫 [**IMediaDet：： get \_ OutputStreams**](imediadet-get-outputstreams.md) ，以判斷原始程式檔中包含的資料流程數目。

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

 

 




