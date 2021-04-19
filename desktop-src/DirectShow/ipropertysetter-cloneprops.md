---
description: CloneProps 方法會從這個屬性 setter 複製一組屬性，並將其加入至新的屬性 setter。
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'IPropertySetter：： CloneProps 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998386"
---
# <a name="ipropertysettercloneprops-method"></a>IPropertySetter：： CloneProps 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`CloneProps`方法會從這個屬性 setter 複製一組屬性，並將其加入至新的屬性 setter。

## <a name="syntax"></a>語法


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppSetter* \[擴展\]
</dt> <dd>

接收新屬性 setter 之 **IPropertySetter** 介面的指標。

</dd> <dt>

*rtStart* \[在\]
</dt> <dd>

要複製之值範圍的開始時間，以 100-毫微秒單位表示。

</dd> <dt>

*rtStop* \[在\]
</dt> <dd>

保留的。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

只會複製在指定開始時間之後的值。 然後，會根據開始時間調整複製值的時間。 例如，如果 *rtStart* 為 20000000 (2 秒) ，則時間 30000000 (3) 秒的值會以時間 10000000 (1 秒) 進行複製。 最後，每個複製的屬性都會有一個初始值，其初始值等於開始時間的原始屬性值 (正確地插入（如有必要）) 。 實際上，屬性資料會在指定的開始時間進行分割。

如果方法成功，則傳回的 [**IPropertySetter**](ipropertysetter.md) 介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

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

 

 




