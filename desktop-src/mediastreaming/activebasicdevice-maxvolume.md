---
title: 'ActiveBasicDevice MaxVolume 屬性 (PlayToDevice .h) '
description: 取得裝置支援的最大數量。
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- MaxVolume 屬性媒體串流 API
- MaxVolume 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，MaxVolume 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 803e2e66306bce0d6fd308501edece61668d5f2e0d8041273d508b662f6cd66f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736194"
---
# <a name="activebasicdevicemaxvolume-property"></a>ActiveBasicDevice：： MaxVolume 屬性

取得裝置支援的最大數量。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a>屬性值

**UINT32** 的指標，指定裝置支援的最大數量。

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

 

