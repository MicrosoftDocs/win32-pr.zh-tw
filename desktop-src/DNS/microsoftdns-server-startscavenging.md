---
title: MicrosoftDNS_Server 類別的 StartScavenging 方法
description: StartScavenging 方法會開始清除要清除之區域中的過時記錄。
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- StartScavenging 方法 DNS
- StartScavenging 方法 DNS，MicrosoftDNS_Server 類別
- MicrosoftDNS_Server 類別 DNS，StartScavenging 方法
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934526"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a>MicrosoftDNS 伺服器類別的 StartScavenging 方法 \_

**StartScavenging** 方法會開始清除要清除之區域中的過時記錄。

## <a name="syntax"></a>語法


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

錯誤 \_ 成功表示清除已順利啟動。 任何其他值都是錯誤碼。

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

[**MicrosoftDNS 伺服器類別的 StartService 方法 \_**](microsoftdns-server-startservice.md)
</dt> <dt>

[**MicrosoftDNS 伺服器類別的 StopService 方法 \_**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**MicrosoftDNS 伺服器類別的 GetDistinguishedName 方法 \_**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





