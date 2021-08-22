---
description: SetDefaultEffectB 方法會設定預設效果。 這個方法相當於 IAMTimeline：： SetDefaultEffect，但會採用 BSTR 值，而不是 GUID 的指標。
ms.assetid: ffee9728-f69e-48a4-ac0a-d41347a20deb
title: 'IAMTimeline：： SetDefaultEffectB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 356874574fd0d960350ab991a97bfd9c6e2641d026da836ecf240bb4391c4a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073122"
---
# <a name="iamtimelinesetdefaulteffectb-method"></a>IAMTimeline：： SetDefaultEffectB 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetDefaultEffectB`方法會設定預設效果。 這個方法相當於 [**IAMTimeline：： SetDefaultEffect**](iamtimeline-setdefaulteffect.md)，但會採用 BSTR 值，而不是 GUID 的指標。

## <a name="syntax"></a>語法


```C++
HRESULT SetDefaultEffectB(
   BSTR pGuid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGuid* 
</dt> <dd>

BSTR 值，代表預設效果的 GUID。

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

[**IAMTimeline 介面**](iamtimeline.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




