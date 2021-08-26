---
description: WriteXML 方法會將時間軸轉譯為 XML 字串。
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'IXml2Dex：： WriteXML 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a5285faad36f83dbab693c63a0c96ca2b1d2b6a25220bb601a9527aac9dc5ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051288"
---
# <a name="ixml2dexwritexml-method"></a>IXml2Dex：： WriteXML 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會將 `WriteXML` 時間軸轉譯為 XML 字串。

## <a name="syntax"></a>語法


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTimeline* 
</dt> <dd>

時間軸物件的 **IUnknown** 介面指標。

</dd> <dt>

*pbstrXML* 
</dt> <dd>

BSTR 類型變數的指標，此變數會接收描述時間軸的 XML 字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK。 如果沒有足夠的記憶體可進行轉換，則會傳回 E \_ OUTOFMEMORY。 否則，會傳回另一個錯誤碼。

## <a name="remarks"></a>備註

方法會配置字串的記憶體。 應用程式必須呼叫 **SysFreeString** 來釋放記憶體。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Internet Explorer 4.0 或更新版本<br/>                                               |
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IXml2Dex 介面**](ixml2dex.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




