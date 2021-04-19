---
title: 'ActiveBasicDevice IsVideoSupported 屬性 (PlayToDevice .h) '
description: 取得值，這個值會指出裝置是否支援影片。
ms.assetid: E8D33A04-748D-42F8-878F-35D973A6B559
keywords:
- IsVideoSupported 屬性媒體串流 API
- IsVideoSupported 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，IsVideoSupported 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsVideoSupported
- ActiveBasicDevice.get_IsVideoSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be369b34355b199cd47518065724242b9a422e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980293"
---
# <a name="activebasicdeviceisvideosupported-property"></a>ActiveBasicDevice：： IsVideoSupported 屬性

取得值，這個值會指出裝置是否支援影片。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_IsVideoSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>屬性值

**布林值** 的指標，指出裝置是否支援影片。

如果裝置支援影片，則 **為 true** ;否則 **為 false**。

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

 

