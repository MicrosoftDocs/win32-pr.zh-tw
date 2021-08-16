---
description: Put \_ 色調方法會指定要做為索引鍵的色調值。 這個屬性只適用于索引鍵類型為 DXTKEY 的 \_ 色調。
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: 'IDxtKey：:p ut_Hue 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 063b8be8986a7a8a3fe3c7d14db31c0cb737d537b74366bee0ce3ed3550e3b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819445"
---
# <a name="idxtkeyput_hue-method"></a>IDxtKey：:p 的 ui \_ 色調方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`put_Hue`方法會指定要做為索引鍵的色調值。 這個屬性只適用于索引鍵類型為 DXTKEY 的 \_ 色調。

## <a name="syntax"></a>語法


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* \[在\]
</dt> <dd>

要做為索引鍵的色調值。 有效範圍是從0到360。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

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

[**IDxtKey 介面**](idxtkey.md)
</dt> <dt>

[**IDxtKey：:p 的 ui \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




