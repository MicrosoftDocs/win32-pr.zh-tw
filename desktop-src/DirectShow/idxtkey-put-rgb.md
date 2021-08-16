---
description: Put \_ RGB 方法會指定要做為索引鍵的 rgb 色彩。 只有當索引鍵類型是 DXTKEY RGB 時，才會套用此屬性 \_ 。
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: 'IDxtKey：:p ut_RGB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f53cb5d856377b611c5ea90d3b9c1f7fa522d892e6c79aa50d350883497398a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819391"
---
# <a name="idxtkeyput_rgb-method"></a>IDxtKey：:p ui \_ RGB 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`put_RGB`方法會指定要做為索引鍵的 RGB 色彩。 只有當索引鍵類型是 DXTKEY RGB 時，才會套用此屬性 \_ 。

## <a name="syntax"></a>語法


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* \[在\]
</dt> <dd>

使用0xRRGGBB 格式將色彩指定為十六進位數位，其中 RR 是紅色值、GG 為綠色值，而 BB 為藍色值。

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

 

 




