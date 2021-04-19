---
description: 判斷指定的主機字串是否可解析為 IP 位址。
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: isResolvableEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1172aaed93a9fc6cede5ae5393c5dd430613a466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980626"
---
# <a name="isresolvableex-function"></a>isResolvableEx 函式

判斷指定的主機字串是否可解析為 IP 位址。

## <a name="parameters"></a>參數

<dl> <dt>

*主機* 
</dt> <dd>

字串，其中包含提供給 FindProxyForUrl 的 HTTP 主控制項。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果主機可解析為 IPv4 或 IPv6 位址，則為 TRUE;否則為 FALSE。

## <a name="examples"></a>範例

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[IPv6 感知 Proxy Helper API 定義](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[瀏覽器自動設定檔案格式的 IPv6 擴充功能](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



