---
description: 尋找 localhost 的所有 IP 位址。
ms.assetid: 47f7d03e-c1a1-4395-9889-01891208fe0f
title: myIPAddressEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5db6107c061c845113e91590dab405bdd84cb4741f766abfeef6a1344652f115
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744160"
---
# <a name="myipaddressex-function"></a>myIPAddressEx 函式

尋找 localhost 的所有 IP 位址。

## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

以分號分隔的字串，其中包含 localhost (IPv6 和（或） IPv4) 的所有 IP 位址，如果無法將 localhost 解析為 IP 位址，則為空字串。

## <a name="remarks"></a>備註

FindProxyforURLEx 實作者應該將會將以分號分隔的 IP 位址字串分隔成不同位址的程式碼。

## <a name="examples"></a>範例

``` syntax
myIpAddressEx();
    would return the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71:f5b9:a3b5" 
    if you were running on that host.
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[IPv6 感知 Proxy Helper API 定義](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[瀏覽器自動設定檔案格式的 IPv6 擴充功能](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



