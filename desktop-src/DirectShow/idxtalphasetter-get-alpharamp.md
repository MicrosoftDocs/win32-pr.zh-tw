---
description: Get \_ AlphaRamp 方法會抓取 Alpha 曲線的屬性。 Alpha 斜接是調整原始影像中 Alpha 值的百分比。 例如，如果 Alpha 的斜坡為0.5，則影像中的 Alpha 值會降低50%。
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'IDxtAlphaSetter：： get_AlphaRamp 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9768ed96f0b40e074fd44de04ca44a8cc17d9de7ce4b75af948975e26b5e3077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952737"
---
# <a name="idxtalphasetterget_alpharamp-method"></a>IDxtAlphaSetter：： get \_ AlphaRamp 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `get_AlphaRamp` Alpha 曲線的屬性。 Alpha 斜接是調整原始影像中 Alpha 值的百分比。 例如，如果 Alpha 的斜坡為0.5，則影像中的 Alpha 值會降低50%。

## <a name="syntax"></a>語法


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAlpha* \[退出，retval\]
</dt> <dd>

接收 Alpha 斜坡。 負數值表示未設定 Alpha 斜坡。

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

 

 




