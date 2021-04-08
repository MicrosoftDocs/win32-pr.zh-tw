---
title: 資源記錄
description: 資源記錄（通常稱為 RR）是 DNS 區域檔案中的資訊專案單位。Rr 是主機名稱和 IP 資訊的基本組建區塊，可用來解析所有 DNS 查詢。
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05b667b95a8ede32018e1aad7de375e77a890487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674732"
---
# <a name="resource-records"></a>資源記錄

資源記錄（通常稱為 RR）是 DNS 區域檔案中的資訊專案單位。Rr 是主機名稱和 IP 資訊的基本組建區塊，可用來解析所有 DNS 查詢。 資源記錄有許多類型，可提供延伸的名稱解析服務。

不同類型的 Rr 具有不同的格式，因為它們包含不同的資料。 不過，一般而言，許多 Rr 共用通用格式，如下列位址資源記錄範例所示。 下列虛構範例說明在資源記錄中找到的欄位：

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   第一個 (microsoft.com 的欄位) 代表擁有者。
-   第二個欄位 (600) 是存留時間 (TTL) 參數（以秒為單位）。
-   ) 中的第三個欄位 (是代表通訊協定系列的類別欄位，此欄位幾乎都是針對網際網路類別。
-   第四個欄位 () 是 RR 所代表的資源類型。
-   第五個欄位 (150.150.150.1) 為資源資料或 .RDATA。 此欄位是提供資源類型相關資訊的變數類型;在此情況下，它是32位的 IP 位址。

DNS 中通常會使用下列資源記錄類型：

-    (SOA) 的授權單位啟動
-    (NS) 的名稱伺服器
-   [*指標記錄*](p-gly.md) (PTR) 
-    () 的位址
-   IPv6 位址 (AAAA) 
-   郵件交換 (MX) 
-   [*標準名稱*](c-gly.md) (CNAME) 
-   Windows Internet 命名服務 (WINS) 
-   WINS 反向查閱 (WINSR) 

DNS 中有許多其他資源記錄類型。 如需詳細資訊，請參閱 [DNS WMI 提供者參考](dns-wmi-provider-reference.md)。

 

 




