---
description: Put \_ Alpha 方法會指定整個影像的 Alpha 值。
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: 'IDxtAlphaSetter：:p ut_Alpha 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994359"
---
# <a name="idxtalphasetterput_alpha-method"></a>IDxtAlphaSetter：:p 的 ui \_ Alpha 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`put_Alpha`方法會指定整個影像的 Alpha 值。

## <a name="syntax"></a>語法


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Alpha* \[在\]
</dt> <dd>

Alpha 值。 此值將會套用至整個目標映射。 若要停用此屬性，請設定負數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果您將這個屬性設定為非負數值，您也必須藉由呼叫 **put \_ AlphaRamp** 與負數值，來停用 Alpha 曲線的屬性。 否則效果將不會正確呈現。

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

[**IDxtAlphaSetter 介面**](idxtalphasetter.md)
</dt> <dt>

[**IDxtAlphaSetter：:p 的 \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 




