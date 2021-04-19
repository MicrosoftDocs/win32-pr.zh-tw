---
description: Put \_ 相似性方法會指定變成透明的色彩資料範圍。 在較高的值中，較大範圍的相似色彩是透明的。 只有當索引鍵類型是 DXTKEY \_ RGB 或 DXTKEY NONRED 時，才會套用此屬性 \_ 。
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: 'IDxtKey：:p ut_Similarity 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994140"
---
# <a name="idxtkeyput_similarity-method"></a>IDxtKey：:p ui \_ 相似性方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`put_Similarity`方法會指定變成透明的色彩資料範圍。 在較高的值中，較大範圍的相似色彩是透明的。 只有當索引鍵類型是 DXTKEY \_ RGB 或 DXTKEY NONRED 時，才會套用此屬性 \_ 。

## <a name="syntax"></a>語法


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* \[在\]
</dt> <dd>

指定相似性值。 有效範圍是從0到100。

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
</dt> <dt>

[**IDxtKey：:p 的 ui \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




