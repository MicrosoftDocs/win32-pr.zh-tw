---
title: 'ActiveBasicDevice IsSetNextSourceSupported 屬性 (PlayToDevice .h) '
description: 取得值，這個值會指出是否支援設定下一個來源。
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- IsSetNextSourceSupported 屬性媒體串流 API
- IsSetNextSourceSupported 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，IsSetNextSourceSupported 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b84190336678e677ad3f0436d7233a49d4587574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995584"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a>ActiveBasicDevice：： IsSetNextSourceSupported 屬性

取得值，這個值會指出是否支援設定下一個來源。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>屬性值

指出是否支援設定下一個來源的 **布林值** 指標。

如果支援設定下一個來源，則為 **true** ;否則 **為 false**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>PlayToDevice。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

