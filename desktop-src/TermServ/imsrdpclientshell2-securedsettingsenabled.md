---
title: IMsRdpClientShell2 SecuredSettingsEnabled 屬性
description: 抓取值，指出目前的網頁是否位於信任的 Internet Explorer URL 安全性區域中。
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- SecuredSettingsEnabled 屬性遠端桌面服務
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsRdpClientShell2 介面
- IMsRdpClientShell2 介面遠端桌面服務，SecuredSettingsEnabled 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d418df76de38313d681f9f01a4dea33ba0803ad67e42d92d90d2ba5a354a8eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870878"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a>IMsRdpClientShell2：： SecuredSettingsEnabled 屬性

抓取值，指出目前的網頁是否位於信任的 Internet Explorer URL 安全性區域中。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>屬性值

布林值的指標，指出目前網頁是否位於信任的 Internet Explorer URL 安全性區域中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

 





