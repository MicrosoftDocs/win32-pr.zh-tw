---
description: PrintXML 方法會將屬性資料轉換成 XML 字串。
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: 'IPropertySetter：:P rintXML 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977780"
---
# <a name="ipropertysetterprintxml-method"></a>IPropertySetter：:P rintXML 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`PrintXML`方法會將屬性資料轉換成 XML 字串。

## <a name="syntax"></a>語法


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszXML* \[擴展\]
</dt> <dd>

接收 XML 字串的緩衝區指標。

</dd> <dt>

*cbXML* \[在\]
</dt> <dd>

*PszXML* 所指向的緩衝區大小（以位元組為單位）。

</dd> <dt>

*pcbPrinted* \[擴展\]
</dt> <dd>

接收 XML 字串長度之變數的指標。 可以是 **Null**。

</dd> <dt>

*縮排* \[在\]
</dt> <dd>

最外層標記的縮排層級數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK。 否則，會傳回 **HRESULT** 值，指出錯誤的原因。 如果 XML 字串的長度超過緩衝區，則方法會傳回 E \_ OUTOFMEMORY。

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

 

 




