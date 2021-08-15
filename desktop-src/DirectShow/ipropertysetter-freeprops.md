---
description: FreeProps 方法會釋放 IPropertySetter：： GetProps 方法所配置的資源。 呼叫 GetProps 之後呼叫這個方法，並將 GetProps 傳回的結構傳遞給它。
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'IPropertySetter：： FreeProps 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 34529c7d78ad36a87eb441f624af8daf1167a77148758ff376feacc70250f18e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397549"
---
# <a name="ipropertysetterfreeprops-method"></a>IPropertySetter：： FreeProps 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`FreeProps`方法會釋放 [**IPropertySetter：： GetProps**](ipropertysetter-getprops.md)方法所配置的資源。 呼叫 **GetProps** 之後呼叫這個方法，並將 **GetProps** 傳回的結構傳遞給它。

## <a name="syntax"></a>語法


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cParams* \[在\]
</dt> <dd>

*PaParam* 陣列中的元素數目。

</dd> <dt>

*paParam* \[在\]
</dt> <dd>

[**DEXTER \_ PARAM**](dexter-param.md)結構陣列的指標。

</dd> <dt>

*paValue* \[在\]
</dt> <dd>

[**DEXTER \_ 值**](dexter-value.md)結構陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

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

[**IPropertySetter 介面**](ipropertysetter.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




