---
description: 將主機字串解析為其 IP 位址
ms.assetid: 32d70f10-803b-484d-a9e0-d4c61a8d897f
title: dnsResolveEx 函式
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
ms.openlocfilehash: 1c63ba3e20653c41864394d9c563c851f2aab5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985684"
---
# <a name="dnsresolveex-function"></a>dnsResolveEx 函式

將主機字串解析為其 IP 位址

## <a name="parameters"></a>參數

<dl> <dt>

*主機* 
</dt> <dd>

字串，其中包含提供給 FindProxyForUrl 的 HTTP 主控制項。

</dd> </dl>

## <a name="return-value"></a>傳回值

以分號分隔的字串，包含 IPv6 和 IPv4 位址，如果無法解析主機，則為空字串。

## <a name="remarks"></a>備註

FindProxyforURLEx 實作者應該將會將以分號分隔的 IP 位址字串分隔成不同位址的程式碼。

## <a name="examples"></a>範例

``` syntax
dnsResolveEx("testmachine1");
    returns the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[IPv6 感知 Proxy Helper API 定義](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[瀏覽器自動設定檔案格式的 IPv6 擴充功能](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



