---
description: Put \_ 倒轉方法會指定是否反轉索引鍵作業。 這個屬性會套用至 DXTKEY ALPHA 以外的所有索引鍵類型 \_ 。
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: 'IDxtKey：:p ut_Invert 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed1ed445e7a6f5f1f07eff74ac739934f2c9ca1358affe3e0cd699b7a101f0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819435"
---
# <a name="idxtkeyput_invert-method"></a>IDxtKey：:p 的 ui \_ 反轉方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`put_Invert`方法會指定金鑰作業是否反轉。 這個屬性會套用至 DXTKEY ALPHA 以外的所有索引鍵類型 \_ 。

## <a name="syntax"></a>語法


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* \[在\]
</dt> <dd>

指定布林值。 若 **為 TRUE**，則會根據預設作業反轉過量影像中的圖元。 如果 **為 FALSE**，則會以預設方式將上層影像中的圖元變成透明。

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

 

 




