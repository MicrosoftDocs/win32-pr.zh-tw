---
description: Get \_ 倒轉方法會抓取布林值，指出金鑰作業是否反轉。 這個屬性會套用至 DXTKEY ALPHA 以外的所有索引鍵類型 \_ 。
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'IDxtKey：： get_Invert 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977670"
---
# <a name="idxtkeyget_invert-method"></a>IDxtKey：：取得 \_ 反轉方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`get_Invert`方法會抓取布林值，指出金鑰作業是否反轉。 這個屬性會套用至 DXTKEY ALPHA 以外的所有索引鍵類型 \_ 。

## <a name="syntax"></a>語法


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[退出，retval\]
</dt> <dd>

接收下列其中一個值。



| 值     | 描述                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| **TRUE**  | 相對於預設作業，會反轉過量影像中的圖元。 |
| **FALSE** | 在上層影像中的圖元會以預設的方式變成透明的。         |



 

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

[**IDxtKey：：取得 \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




