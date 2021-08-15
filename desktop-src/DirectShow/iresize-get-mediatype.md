---
description: 取得媒體型別方法會傳回檔整 \_ 器篩選的目前輸出媒體類型。
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: 'IResize：： get_MediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d9e23c78a25f1cda141cb0c3ce55688c12bdf3aab447aca596326e01544b4e8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818229"
---
# <a name="iresizeget_mediatype-method"></a>IResize：： get \_ 媒體方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會傳回檔整 `get_MediaType` 器篩選的目前輸出媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pmt* \[擴展\]
</dt> <dd>

由呼叫端配置的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標。 方法會以媒體類型來填滿此結構。 呼叫端必須釋放格式區塊（如果有的話）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果輸出媒體類型尚未設定，則會傳回預設的媒體類型。 當呼叫 **put \_** 媒體類型或 **put \_ 大小** 方法時，篩選必須更新其輸出媒體類型; 所傳回的媒體類型 `get_MediaType` 必須反映這些變更。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | DirectX 9.0 或更新版本<br/>                                                         |
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> <dt>

[**IResize 介面**](iresize.md)
</dt> </dl>

 

 




