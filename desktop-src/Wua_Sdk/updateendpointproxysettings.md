---
description: UpdateEndpointProxySettings 結構會定義要求權杖時所使用的 proxy 設定。
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: 'UpdateEndpointProxySettings 結構 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026269"
---
# <a name="updateendpointproxysettings-structure"></a>UpdateEndpointProxySettings 結構

**UpdateEndpointProxySettings** 結構會定義要求權杖時所使用的 proxy 設定。

## <a name="syntax"></a>語法


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a>成員

<dl> <dt>

**szProxyAddr**
</dt> <dd>

要使用 (proxy 伺服器的 DNS 名稱或 IP 位址，例如 "proxy.somecorp.com" 或 "192.168.0.4" ) ，如果未使用 proxy，則為空字串。

</dd> <dt>

**szBypassList**
</dt> <dd>

應略過 proxy 伺服器的主機位址清單; 如果所有主機位址都應該使用 proxy 伺服器，則為空字串。

如果 **szProxyAddr** 是空的，則 WUA 不會使用此資料。

</dd> <dt>

**szUserName**
</dt> <dd>

用來向 proxy 伺服器進行驗證的使用者名稱，如果不需要驗證，則為空字串。

如果 **szProxyAddr** 是空的，則 WUA 不會使用此資料。

</dd> <dt>

**szPassword**
</dt> <dd>

用來向 proxy 伺服器進行驗證的密碼，如果不需要驗證，則為空字串。

如果 **szProxyAddr** 是空的，則 WUA 不會使用此資料。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                              |
| 標頭<br/>                   | <dl> <dt>UpdateEndpointAuth。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




