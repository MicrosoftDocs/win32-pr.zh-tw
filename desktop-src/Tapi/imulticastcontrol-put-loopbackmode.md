---
description: Put \_ LoopbackMode 會設定多播回送模式。
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: 'IMulticastControl：:p ut_LoopbackMode 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5b5e51b3814b380cc06d9c960db1a4e4b9ecb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993610"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a>IMulticastControl：:p 的 \_ LoopbackMode 方法

\[**put \_LoopbackMode** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**Put \_ LoopbackMode** 會設定多播回送模式。

## <a name="syntax"></a>語法


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*模式* \[在\]
</dt> <dd>

[**多播 \_新 \_**](multicast-loopback-mode.md) 回送模式的回送模式描述項。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                  | Description                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 方法成功。<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *模式* 參數無效。<br/> |



 

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

 

 




