---
title: 'ActiveBasicDevice IsImageSupported 屬性 (PlayToDevice .h) '
description: 取得值，這個值會指出裝置是否支援影像。
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- IsImageSupported 屬性媒體串流 API
- IsImageSupported 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，IsImageSupported 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a147c5156f07c6cc6461cafcf8dc778013a7eb3048d1428f854b844d24f5642a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236709"
---
# <a name="activebasicdeviceisimagesupported-property"></a>ActiveBasicDevice：： IsImageSupported 屬性

取得值，這個值會指出裝置是否支援影像。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>屬性值

**布林值** 的指標，指出裝置是否支援影像。

如果裝置支援影像，則 **為 true** ;否則 **為 false**。

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

 

