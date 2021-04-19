---
description: 取得 KeyType 方法會抓取索引 \_ 鍵的類型。
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'IDxtKey：： get_KeyType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998606"
---
# <a name="idxtkeyget_keytype-method"></a>IDxtKey：：取得 \_ KeyType 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取索引 `get_KeyType` 鍵的類型。

## <a name="syntax"></a>語法


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[退出，retval\]
</dt> <dd>

接收下列其中一個列舉值。



| 值             | 描述                                           |
|-------------------|-------------------------------------------------------|
| DXTKEY \_ RGB       | 色度鍵。  (RGB 值的索引鍵。 )                        |
| DXTKEY \_ NONRED    | Nonred 鍵。  (使藍和綠區域透明。 )  |
| DXTKEY \_ 亮度 | 亮度索引鍵。                                        |
| DXTKEY \_ ALPHA     | 依字母值的索引鍵。                                   |
| DXTKEY \_ 色調       | 按鍵（依色調）。                                           |



 

</dd> </dl>

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

[**IDxtKey 介面**](idxtkey.md)
</dt> </dl>

 

 




