---
description: LoadXML 方法會載入可延伸標記語言 (XML)  (XML) 中表示的屬性資料。
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'IPropertySetter：： LoadXML 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991562"
---
# <a name="ipropertysetterloadxml-method"></a>IPropertySetter：： LoadXML 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`LoadXML`方法會載入以可延伸標記語言 (XML)  (XML) 表示的屬性資料。

## <a name="syntax"></a>語法


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.pxml* \[在\]
</dt> <dd>

Microsoft XML 剖析器所建立之 XML 元素的 **IUnknown** 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                                  | Description                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | 沒有屬性資料。<br/>    |
| <dl> <dt>**S \_ 確定**</dt> </dl>                         | 成功。<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                | 記憶體不足。<br/> |
| <dl> <dt>**VFW \_ E \_ 不正確 \_ 檔 \_ 格式**</dt> </dl> | 格式無效。<br/>      |



 

## <a name="remarks"></a>備註

一般來說，應用程式不需要使用這個方法。 DES 在內部使用它從 XTL 檔案載入屬性。

若要使用此方法，請建立 **IXMLDocument** 物件，並使用它來剖析 XML 檔案。 然後使用 **IXMLDocument** 物件來取出 **IXMLElement** 物件。 如果物件有屬性，您可以將 **IXMLElement** 指標傳遞給 **LoadXML** 方法。 方法會將屬性載入至屬性 setter。

> [!Note]  
> **IXMLDocument** 和 **IXMLElement** 介面是在 Microsoft XML Core Services (msxml) 1.0 版中執行，但不會在較新版本的 msxml 中執行。

 

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

 

 




