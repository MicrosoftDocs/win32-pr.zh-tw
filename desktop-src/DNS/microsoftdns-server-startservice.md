---
title: MicrosoftDNS_Server 類別的 StartService 方法
description: StartService 方法會啟動 DNS 伺服器。
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- StartService 方法 DNS
- StartService 方法 DNS，MicrosoftDNS_Server 類別
- MicrosoftDNS_Server 類別 DNS，StartService 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e74de96ad24ff16ea2c2effaef78003011f5d6bd5d421336084ac5c7701f79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432638"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a>MicrosoftDNS 伺服器類別的 StartService 方法 \_

**StartService** 方法會啟動 DNS 伺服器。

## <a name="syntax"></a>語法


```mof
uint32 StartService();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

錯誤 \_ 成功表示服務已順利啟動。 任何其他值都是錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 命名空間<br/>                | 根 \\ MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MicrosoftDNS \_ 伺服器**](microsoftdns-server.md)
</dt> <dt>

[**MicrosoftDNS 伺服器類別的 StopService 方法 \_**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**MicrosoftDNS 伺服器類別的 StartScavenging 方法 \_**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**MicrosoftDNS 伺服器類別的 GetDistinguishedName 方法 \_**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





