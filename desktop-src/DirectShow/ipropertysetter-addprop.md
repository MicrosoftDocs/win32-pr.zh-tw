---
description: AddProp 方法會將屬性加入至屬性 setter，以及定義時間範圍內屬性值的時間值配對陣列。
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'IPropertySetter：： AddProp 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977437"
---
# <a name="ipropertysetteraddprop-method"></a>IPropertySetter：： AddProp 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`AddProp`方法會將屬性加入至屬性 setter，以及定義時間範圍內屬性值的時間值配對陣列。

## <a name="syntax"></a>語法


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param* \[在\]
</dt> <dd>

[**DEXTER \_**](dexter-param.md)指定屬性的 PARAM 結構。 結構 **的值成員必須** 等於 *paValue* 參數中指定的陣列大小。

</dd> <dt>

*paValue* \[在\]
</dt> <dd>

[**DEXTER \_ 值**](dexter-value.md)結構的陣列的指標，其中包含時間值的配對。 陣列必須是遞增的時間順序。 時間相對於效果或轉換的開始時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

第一個 [**DEXTER \_ 值**](dexter-value.md) 結構必須指定零的參考時間和插補旗標 (**dwInterp**) 的 **DEXTERF \_ 跳躍**，否則方法會傳回錯誤。

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

 

 




