---
description: ClearProps 方法會清除屬性 setter 中的所有屬性資料。 應用程式可以在呼叫這個函數之後設定新的屬性資料。
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: 'IPropertySetter：： ClearProps 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 62bb30b69ba0e4ba795b0d39af72a156b63cac11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995635"
---
# <a name="ipropertysetterclearprops-method"></a>IPropertySetter：： ClearProps 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`ClearProps`方法會清除屬性 setter 中的所有屬性資料。 應用程式可以在呼叫這個函數之後設定新的屬性資料。

清除屬性資料並不會將物件的屬性還原為其原始值。 它只會防止 DirectShow 套用任何進一步的變更。 當專案呈現時，會在執行時間套用屬性值。

## <a name="syntax"></a>語法


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

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

[**IPropertySetter 介面**](ipropertysetter.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




