---
description: SetRenderRange 方法會設定時間軸上要轉譯的時間範圍。 不會轉譯位於指定範圍外的物件，也不會配置資源給它們。
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: 'IRenderEngine：： SetRenderRange 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0255b7806e2e2303bb2ca953fc5e59886480cbf3525d4de1bf1ef2fbd1388caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952517"
---
# <a name="irenderenginesetrenderrange-method"></a>IRenderEngine：： SetRenderRange 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetRenderRange`方法會設定要轉譯的時間軸上的時間範圍。 不會轉譯位於指定範圍外的物件，也不會配置資源給它們。

## <a name="syntax"></a>語法


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*開始* 
</dt> <dd>

開始時間，以 100-毫微秒單位表示。

</dd> <dt>

*停止* 
</dt> <dd>

停止時間，以 100-毫微秒單位表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                            | 描述                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 成功。<br/>                            |
| <dl> <dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt> </dl> | 轉譯引擎無法初始化。<br/> |



 

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

[**IRenderEngine 介面**](irenderengine.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




