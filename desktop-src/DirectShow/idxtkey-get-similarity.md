---
description: 取得 \_ 相似性方法會抓取變成透明的色彩資料範圍。 在較高的值中，較大範圍的相似色彩是透明的。 只有當索引鍵類型是 DXTKEY \_ RGB 或 DXTKEY NONRED 時，才會套用此屬性 \_ 。
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'IDxtKey：： get_Similarity 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dda31145fe28f0b428189eafd3105ae56120fbc19e0c611ad0df8d9f511130a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399138"
---
# <a name="idxtkeyget_similarity-method"></a>IDxtKey：：取得 \_ 相似性方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`get_Similarity`方法會抓取變成透明的色彩資料範圍。 在較高的值中，較大範圍的相似色彩是透明的。 只有當索引鍵類型是 DXTKEY \_ RGB 或 DXTKEY NONRED 時，才會套用此屬性 \_ 。

## <a name="syntax"></a>語法


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[退出，retval\]
</dt> <dd>

接收相似性值。

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

[**IDxtKey：：取得 \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




