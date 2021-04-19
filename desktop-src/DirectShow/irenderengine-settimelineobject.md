---
description: SetTimelineObject 方法會設定轉譯引擎要使用的時間軸。
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: 'IRenderEngine：： SetTimelineObject 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 954fab15e92e6111439abb66d53d53525a5afdb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995011"
---
# <a name="irenderenginesettimelineobject-method"></a>IRenderEngine：： SetTimelineObject 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetTimelineObject`方法會設定轉譯引擎要使用的時間軸。

## <a name="syntax"></a>語法


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTimeline* 
</dt> <dd>

時間軸物件之 [**IAMTimeline**](iamtimeline.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                            | Description                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 成功。<br/>                            |
| <dl> <dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt> </dl> | 轉譯引擎無法初始化。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | 記憶體不足。<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl>              | 指標無效。<br/>                    |



 

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

[**IRenderEngine 介面**](irenderengine.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




