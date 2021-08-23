---
description: IPv6 連結-本機和網站-本機位址稱為範圍位址。
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: IPv6 連結-本機和網站-本機位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22220adb2c1b0338462f7ed87b3937a97c3d0b8a8b0aa2d9858d5c5efc8b4f54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794778"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a>IPv6 連結-本機和網站-本機位址

IPv6 連結-本機和網站-本機位址稱為範圍位址。 Windows 通訊端 (Winsock) API 支援 [**sockaddr \_ in6**](sockaddr-2.md)結構中的 **sin6 \_ 範圍 \_ 識別碼** 成員，以搭配範圍位址使用。 針對 IPv6 連結-本機位址 (fe80：：/10 首碼) ， **sockaddr \_ in6** 結構中的 **sin6 \_ 範圍 \_ 識別碼** 成員是介面編號。 針對 IPv6 網站-本機位址 (fec0：：/10 首碼) ， **sockaddr \_ in6** 結構中的 **sin6 \_ 範圍 \_ 識別碼** 成員是網站識別碼。

介面5上的連結-本機 IPv6 位址範例 \# 如下：

``` syntax
fe80::208:74ff:feda:625c%5
```

下列命令適用于 Windows XP Service Pack 1 (SP1) 和更新版本，可在本機電腦上查詢和設定 IPv6：

-   [Netsh.exe](netsh-exe.md)

使用 Netsh.exe 命令所做的設定變更是永久性的，而且在重新開機電腦或 IPv6 通訊協定時不會遺失。

在 Windows XP Service Pack 1 (SP1) 之前，IPv6 設定和管理使用了數個舊版命令列工具 (Net.exe、Ipv6.exe 和 Ipsec6.exe) 來設定和管理 ipv6。 使用這些較舊的工具，IPv6 變更不是永久性的，而且會在電腦或 IPv6 通訊協定重新開機時遺失。 這些舊版的命令列工具僅在 Windows XP 上受到支援。

在 Windows XP SP1 上，下列命令會在本機電腦上顯示 IPv6 介面的清單，包括介面索引、介面名稱和各種其他介面屬性。

**netsh interface ipv6 show 介面**

在 Windows XP SP1 上，下列命令會變更與介面索引相關聯的網站識別碼。

**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid = value**

在 Windows XP 上，下列舊版的命令也會將與網站-本機位址相關聯的網站識別碼變更為3。

**ipv6 rtu fec0：：/10 3**

如果您要傳送或連接至範圍位址，則 [**sockaddr \_ in6**](sockaddr-2.md)結構中的 **sin6 \_ 範圍 \_ 識別碼** 成員可以保留未指定 (零) 代表不明確的範圍位址。 例如，下列連結-本機位址是不明確的：

``` syntax
fe80::10
```

如果您要系結至有範圍的位址，則 [**sockaddr \_ in6**](sockaddr-2.md)結構中的 **sin6 \_ 範圍 \_ 識別碼** 成員必須包含非零值，以指定連結-本機位址的有效介面編號，或網站-本機位址的網站識別碼。

## <a name="ambiguous-scoped-addresses"></a>不明確的範圍位址

如果您要傳送或連接至範圍內的位址，而且尚未在 [**sockaddr \_ in6**](sockaddr-2.md)結構中指定 **sin6 \_ 範圍 \_ 識別碼** 成員，則範圍位址不明確。 若要解決此問題，IPv6 通訊協定會先判斷您是否已將通訊端系結至來源位址。 如果是，系結來源位址會藉由提供介面編號或網站識別碼來解析不明確的情況。

如果您要傳送或連接至範圍位址，但未指定 **sin6 \_ 範圍 \_ 識別碼** 成員或系結來源位址，則 IPv6 通訊協定會檢查路由表。 例如，下列命令會在本機電腦上顯示 IPv6 路由表：

**netsh interface ipv6 show route**

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

這表示預設會將連結-本機位址視為介面 \# 13 和14的連結 \# 。

當本機電腦有多張網路介面卡時，會發生混淆。 例如，上述的 **netsh** 命令表示有兩個網路介面 (區域網路連線，而無線網路連線) 。 當應用程式指定目的地連結-本機位址 (fe80：：10時（例如) 不含範圍識別碼），並不會清除要用來傳送封包的介面卡。 只有連結-本機單播 (fe80：：/64) 或連結範圍多播 (ff00：：/8) IPv6 目的地位址在傳送封包時，不會有範圍識別碼。

## <a name="neighbor-discovery"></a>鄰居搜索

如果您尚未在 [**sockaddr \_ in6**](sockaddr-2.md)結構中指定 **sin6 \_ 範圍 \_ 識別碼** 成員、未系結來源位址，而且尚未指定連結-本機位址的路由，則 IPv6 通訊協定會嘗試使用鄰居探索來解析目的地連結-本機位址。 針對正在傳送的指定封包，會嘗試一個介面。 第一個嘗試的介面視為最慣用的介面。 如果鄰居探索無法解析介面上的連結-本機位址，則會捨棄要傳送的封包，而系統會記得目的地連結-本機位址無法透過該介面連線。 在下一個要在所有相同條件下傳送的封包上，會嘗試使用不同的介面來進行鄰居探索。 此程式會繼續執行每個新封包的本機電腦上的每個介面，直到鄰近探索回應目的地連結-本機位址，或已嘗試和失敗所有可能的介面為止。 每次嘗試解決鄰近的問題時，就會刪除該鄰居的一個介面。

如果目的地連結-本機位址解析，則會使用該介面來傳送目前的封包。 此介面也會用於傳送至相同連結-本機目的地位址的任何後續不明確範圍封包。

如果鄰居探索無法解析所有介面上的目的地連結-本機位址，系統就會嘗試在最慣用的介面上傳送封包， (第一個介面嘗試) 。 網路堆疊會持續嘗試解析最慣用介面上的目的地連結-本機位址。 在所有介面上的鄰近探索失敗之後的一段時間之後，網路堆疊會再次重新開機進程，並嘗試解析所有介面上的目的地連結-本機位址。 目前，當鄰近探索在所有介面上再次嘗試時，此時間間隔為60秒。 不過，此時間間隔可能會在 Windows 版本上變更，因此應用程式不應該採用此時間間隔。

> [!Note]  
> 如果應用程式在鄰居探索解析出連結-本機位址之後，將相同的連結-本機位址系結至不同的介面，則不會覆寫鄰居探索所傳回之連結-本機目的地位址的介面。

 

如需有關 IP 第6版之鄰居探索的詳細資訊，請參閱 IETF 發佈的 [RFC4861](https://tools.ietf.org/html/rfc4861) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IPv6 網站首碼](site-prefixes-2.md)
</dt> <dt>

[Ipv6.exe](ipv6-exe-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> <dt>

[使用 IPv6](using-ipv6-2.md)
</dt> </dl>

 

 



