---
description: Get 方法會抓取指定音訊設定屬性的值。
ms.assetid: 5ad9a4e8-c5b0-43e9-bf75-6460fd23501a
title: 'ITAudioSettings：： Get 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2773bf0f1a26978321ed0d02c3c30d8a96fef1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996016"
---
# <a name="itaudiosettingsget-method"></a>ITAudioSettings：： Get 方法

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。 RTC 用戶端 API 提供類似的功能。\]

**Get** 方法會抓取指定 [**音訊設定屬性**](audiosettingsproperty.md)的值。

## <a name="syntax"></a>語法


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

[**AudioSettingsProperty**](audiosettingsproperty.md)列舉的成員。

</dd> <dt>

*plValue* \[擴展\]
</dt> <dd>

輸入 *屬性* 的值。

</dd> <dt>

*plFlags* \[擴展\]
</dt> <dd>

[**TAPIControlFlags**](tapicontrolflags.md)列舉的值，指出 *屬性* 值的控制方式。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
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

 

 




