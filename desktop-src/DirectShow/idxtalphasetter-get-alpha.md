---
description: Get \_ Alpha 方法會抓取整個影像的 Alpha 值。
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'IDxtAlphaSetter：： get_Alpha 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 054e2a1745f96dc4d6ea846bed0448948fae8407dd6ab44d2796742e405f2e1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051968"
---
# <a name="idxtalphasetterget_alpha-method"></a>IDxtAlphaSetter：： get \_ Alpha 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `get_Alpha` 整個影像的 Alpha 值。

## <a name="syntax"></a>語法


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAlpha* \[退出，retval\]
</dt> <dd>

接收 Alpha 值。 此 Alpha 值會套用至整個目標影像。 負數值表示未設定 Alpha 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                               | 描述                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標引數<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>      | Success<br/>                   |



 

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

[**IDxtAlphaSetter 介面**](idxtalphasetter.md)
</dt> </dl>

 

 




