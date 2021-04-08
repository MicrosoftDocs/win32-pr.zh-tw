---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: ODJ_POLICY_DNS_DOMAIN_INFO IDL 定義
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "103684205"
---
# <a name="odj_policy_dns_domain_info-structure"></a>ODJ_POLICY_DNS_DOMAIN_INFO 結構

包含用戶端應加入之網域和樹系的相關資訊。

## <a name="syntax"></a>語法

```C++
typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
{
    ODJ_UNICODE_STRING Name;
    ODJ_UNICODE_STRING DnsDomainName;
    ODJ_UNICODE_STRING DnsForestName;
    GUID DomainGuid;
    PODJ_SID Sid;
} ODJ_POLICY_DNS_DOMAIN_INFO;
```

## <a name="members"></a>成員

### <a name="name"></a>Name

必須設定為 Netbios 功能變數名稱。

### <a name="dnsdomainname"></a>DnsDomainName

必須設定為 DNS 格式的功能變數名稱。

### <a name="dnsforestname"></a>DnsForestName

必須設定為 DNS 格式的樹系名稱。

### <a name="domainguid"></a>DomainGuid

必須設定為網域 guid。

### <a name="sid"></a>Sid

必須設定為網域 sid。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**ODJ \_ UNICODE \_ 字串**](odj-odj_unicode_string.md)

[**ODJ \_ SID**](odj-odj_sid.md)
