---
description: GetPropertySetter 方法會抓取物件的屬性 setter。 當物件呈現時，屬性 setter 中包含的屬性資訊會套用至物件。
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'IAMTimelineObj：： GetPropertySetter 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4410a0b63a0228d9e8e403ef1f0403d1968ad639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990949"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a>IAMTimelineObj：： GetPropertySetter 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetPropertySetter` 物件的屬性 setter。 當物件呈現時，屬性 setter 中包含的屬性資訊會套用至物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[退出，retval\]
</dt> <dd>

接收屬性 setter [**IPropertySetter**](ipropertysetter.md) 介面的指標。 如果物件沒有屬性 setter，此值會設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果 *pVal* 中傳回的值不是 **Null**，則 **IPropertySetter** 介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

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

[**IAMTimelineObj 介面**](iamtimelineobj.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




