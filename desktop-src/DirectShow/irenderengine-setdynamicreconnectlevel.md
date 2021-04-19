---
description: SetDynamicReconnectLevel 方法會在轉譯期間設定動態重新連接的層級。
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'IRenderEngine：： SetDynamicReconnectLevel 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001843"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a>IRenderEngine：： SetDynamicReconnectLevel 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會在轉譯 `SetDynamicReconnectLevel` 期間設定動態重新連接的層級。

## <a name="syntax"></a>語法


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Level* 
</dt> <dd>

動態重新 [**連接旗標**](dynamic-reconnection-flags.md)的組合，指定動態重新連接的層級。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                               | Description                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 成功。<br/>         |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl> | 未實作。<br/> |



 

## <a name="remarks"></a>備註

根據預設，基本轉譯引擎會在轉譯專案之前載入每個來源。 這可能會導致很長的啟動時間。 使用動態重新連接時，只有在需要時才會載入來源。 這可以縮短啟動時間，但可能會干擾順暢的播放。 通常，專案所使用的來源剪輯越多，您可能會受益于動態重新連接。

智慧型轉譯引擎不會執行此方法。

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

 

 




