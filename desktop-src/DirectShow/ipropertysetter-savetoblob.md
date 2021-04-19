---
description: SaveToBlob 方法會將屬性資料儲存至保存格式。
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'IPropertySetter：： SaveToBlob 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989868"
---
# <a name="ipropertysettersavetoblob-method"></a>IPropertySetter：： SaveToBlob 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會將 `SaveToBlob` 屬性資料儲存至保存格式。

## <a name="syntax"></a>語法


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcSize* \[擴展\]
</dt> <dd>

接收資料的大小（以位元組為單位）。

</dd> <dt>

*ppb* \[擴展\]
</dt> <dd>

接收接收資料之位元組陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

方法會配置位元組陣列的記憶體。 呼叫端必須使用 **CoTaskMemFree** 函數釋放它。

所有屬性名稱和值的長度都會截斷為40個字元。 基於這個理由，XML 是慣用的持續性格式。 請參閱 [**IXml2Dex 介面**](ixml2dex.md)。

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

 

 




