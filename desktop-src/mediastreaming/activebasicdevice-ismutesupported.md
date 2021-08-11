---
title: 'ActiveBasicDevice IsMuteSupported 屬性 (PlayToDevice .h) '
description: 取得值，這個值會指出裝置是否支援將音訊靜音。
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- IsMuteSupported 屬性媒體串流 API
- IsMuteSupported 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，IsMuteSupported 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fad8352504a6c950bb76206f05c77c5baa9f3baed2f1144a1d6c165e380a4b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236646"
---
# <a name="activebasicdeviceismutesupported-property"></a>ActiveBasicDevice：： IsMuteSupported 屬性

取得值，這個值會指出裝置是否支援將音訊靜音。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>屬性值

**布林值** 的指標，指出裝置是否支援將音訊靜音。

如果裝置支援音訊靜音，則 **為 true** ;否則 **為 false**。

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

 

