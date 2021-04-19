---
description: Get \_ StreamTypeB 方法會抓取字串，表示目前資料流程的媒體類型 GUID。
ms.assetid: 99ae4b52-4449-4b7c-babf-1a6cba479499
title: 'IMediaDet：： get_StreamTypeB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamTypeB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd1cdf4bbadfa769654f20792cf2fda17dbe2806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993624"
---
# <a name="imediadetget_streamtypeb-method"></a>IMediaDet：： get \_ StreamTypeB 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `get_StreamTypeB` 字串，表示目前資料流程之媒體類型的 GUID。

## <a name="syntax"></a>語法


```C++
HRESULT get_StreamTypeB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[退出，retval\]
</dt> <dd>

接收媒體類型 GUID 的字串表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

傳回的 **BSTR** 格式如下所示： `{73647561-0000-0010-8000-00AA00389B71}`

方法會配置字串的記憶體。 應用程式必須呼叫 **SysFreeString** 來釋放記憶體。

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

 

 




