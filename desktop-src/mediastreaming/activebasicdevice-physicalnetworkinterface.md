---
title: 'ActiveBasicDevice PhysicalNetworkInterface 屬性 (PlayToDevice .h) '
description: 取得實體網路介面的識別碼。
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- PhysicalNetworkInterface 屬性媒體串流 API
- PhysicalNetworkInterface 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，PhysicalNetworkInterface 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd9eb004607d93b92d502d22b253258bf39e501969e6b3952a58b0a03a1eec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736204"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a>ActiveBasicDevice：:P hysicalNetworkInterface 屬性

取得實體網路介面的識別碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>屬性值

**GUID** 的指標，可指定實體網路介面的識別碼。

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

 

