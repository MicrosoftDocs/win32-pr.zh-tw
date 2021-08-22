---
description: Get \_ LoopbackMode 方法會取得多播回送模式。
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'IMulticastControl：： get_LoopbackMode 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a3f9a600ea64bacf7cafdc5071df264d79079adfefd4a771eea9569fcbb092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013018"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a>IMulticastControl：： get \_ LoopbackMode 方法

\[**取得 \_LoopbackMode** 無法在 Windows Vista、Windows Server 2008 及後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ LoopbackMode** 方法會取得多播回送模式。

## <a name="syntax"></a>語法


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMode* \[擴展\]
</dt> <dd>

目前回送模式的 [**多播 \_ 回送 \_ 模式**](multicast-loopback-mode.md) 描述元指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 意義                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 方法成功。<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *PMode* 參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMulticastControl**](imulticastcontrol.md)
</dt> </dl>

 

 




