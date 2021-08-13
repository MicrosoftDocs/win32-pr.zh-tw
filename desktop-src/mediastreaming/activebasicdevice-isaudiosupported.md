---
title: 'ActiveBasicDevice IsAudioSupported 屬性 (PlayToDevice .h) '
description: 取得值，這個值會指出裝置是否支援音訊。
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- IsAudioSupported 屬性媒體串流 API
- IsAudioSupported 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，IsAudioSupported 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20125114b6cd134d153ad6425af5af410faf524714a2e505a37fbf57dcda21e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462420"
---
# <a name="activebasicdeviceisaudiosupported-property"></a>ActiveBasicDevice：： IsAudioSupported 屬性

取得值，這個值會指出裝置是否支援音訊。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>屬性值

**布林值** 的指標，指出裝置是否支援音訊。

如果裝置支援音訊，則 **為 true** ;否則 **為 false**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>PlayToDevice。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

