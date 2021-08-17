---
description: GetSwapInputs 方法會抓取值，指出是否交換轉換輸入。
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'IAMTimelineTrans：： GetSwapInputs 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 566dbc54b30619c67ffb9d804e4854d51cae86d3688bda0b48eebfeb64cdb749
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316298"
---
# <a name="iamtimelinetransgetswapinputs-method"></a>IAMTimelineTrans：： GetSwapInputs 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetSwapInputs`方法會抓取值，指出是否交換轉換輸入。

根據預設，轉換會從所有較低優先順序層級的複合轉換成轉換所在的圖層。 您可以反轉這項進展，讓轉換從它所在的圖層移回較低優先順序層級的組合。

## <a name="syntax"></a>語法


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* 
</dt> <dd>

接收布林值。 如果值為 **FALSE**，則轉換會從所有較低優先順序層級到轉換圖層的複合。 如果值為 **TRUE**，則轉換會以相反的方向進行。 預設值為 **FALSE**。

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

[**IAMTimelineTrans 介面**](iamtimelinetrans.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




