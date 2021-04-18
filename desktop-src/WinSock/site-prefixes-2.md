---
description: 指定連結至介面4的前置詞 \# 。
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: IPv6 網站首碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971207"
---
# <a name="ipv6-site-prefixes"></a>IPv6 網站首碼

Ipv6 rtu 命令可讓您使用網站前置長度來設定已發佈的內部連結首碼。 如果有指定，網站前置長度會放入路由器公告的首碼資訊選項中。 例如：

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

指定連結至介面4的前置詞 \# 。 前置詞已發佈，這表示如果介面 \# 4 是廣告介面，則會將它包含在路由器公告中。 前置詞資訊選項中的存留期為1800秒 (30 分鐘) 。 首碼資訊選項中的網站前置長度為48。

接收指定網站首碼的首碼資訊選項會導致在網站首碼資料表中建立專案，您可以使用 ipv6 spt 命令來顯示專案。 網站首碼資料表是用來移除 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 和相關函式所傳回之不當的網站本機位址。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IPv6 連結-本機和網站-本機位址](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> </dl>

 

 



