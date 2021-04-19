---
description: Put \_ AlphaRamp 方法會指定 Alpha 曲線的屬性。 Alpha 斜接是調整原始影像中 Alpha 值的百分比。 例如，如果 Alpha 的斜坡為0.5，則影像中的 Alpha 值會降低50%。
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: 'IDxtAlphaSetter：:p ut_AlphaRamp 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994902"
---
# <a name="idxtalphasetterput_alpharamp-method"></a>IDxtAlphaSetter：:p 的 \_ AlphaRamp 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`put_AlphaRamp`方法會指定 Alpha 曲線的屬性。 Alpha 斜接是調整原始影像中 Alpha 值的百分比。 例如，如果 Alpha 的斜坡為0.5，則影像中的 Alpha 值會降低50%。

## <a name="syntax"></a>語法


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Alpha* \[在\]
</dt> <dd>

以百分比表示的 Alpha 斜坡。 例如，1.0 是100%。 若要停用此屬性，請設定負數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果您將這個屬性設定為非負數值，您也必須使用負數值來呼叫 **put \_ Alpha** ，以停用 Alpha 屬性。 否則效果將不會正確呈現。

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

[**IDxtAlphaSetter：:p ui \_ Alpha**](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




