---
description: GetRange 方法會抓取指定音訊設定屬性的有效值範圍。
ms.assetid: 09ee0c59-6ae6-47eb-a8cf-6b24e759d7fb
title: 'ITAudioSettings：： GetRange 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f08c9eed736725bd4200c79583dcc12abde11399ec272be04805881752b19119
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992008"
---
# <a name="itaudiosettingsgetrange-method"></a>ITAudioSettings：： GetRange 方法

\[此方法無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**GetRange** 方法會抓取指定 [**音訊設定屬性**](audiosettingsproperty.md)的有效值範圍。

## <a name="syntax"></a>語法


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

[**AudioSettingsProperty**](audiosettingsproperty.md)列舉的成員。

</dd> <dt>

*plMin* \[擴展\]
</dt> <dd>

輸入屬性的最小有效值。

</dd> <dt>

*plMax* \[擴展\]
</dt> <dd>

輸入屬性的最大有效值。

</dd> <dt>

*plSteppingDelta* \[擴展\]
</dt> <dd>

可以增加或減少屬性值的遞增量。

</dd> <dt>

*plDefault* \[擴展\]
</dt> <dd>

*Property* 參數的預設值。

</dd> <dt>

*plFlags* \[擴展\]
</dt> <dd>

[**TAPIControlFlags**](tapicontrolflags.md)列舉的值，指出 *屬性* 值的控制方式。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITAudioSettings**](itaudiosettings.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioSettingsProperty**](audiosettingsproperty.md)
</dt> </dl>

 

 




