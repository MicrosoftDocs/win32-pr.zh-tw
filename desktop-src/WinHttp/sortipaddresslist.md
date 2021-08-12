---
description: 排序 IP 位址清單。
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: sortIpAddressList 函式
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
ms.openlocfilehash: 3144ecf044f832a49dd6aa4d9fabf76ce8e81c79c195ec101d294c432a8081e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562445"
---
# <a name="sortipaddresslist-function"></a>sortIpAddressList 函式

排序 IP 位址清單。

## <a name="parameters"></a>參數

<dl> <dt>

*IpAddressList* 
</dt> <dd>

以分號分隔的字串，其中包含 IP 位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

已排序之分號分隔 IP 位址的清單，如果無法排序 IP 位址清單，則為空字串。

## <a name="remarks"></a>備註

FindProxyforURLEx 實作者應該將會將以分號分隔的 IP 位址字串分隔成不同位址的程式碼。

## <a name="examples"></a>範例

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[IPv6 感知 Proxy Helper API 定義](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[瀏覽器自動設定檔案格式的 IPv6 擴充功能](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



