---
description: Microsoft Internet Explorer 支援使用 IPv6 來連線及存取已啟用 IPv6 的網站 (網頁伺服器和 FTP 伺服器，例如在符合下列情況時) ：執行 Internet Explorer 的主機電腦必須安裝並啟用 IPv6。連接到位於本機子網上的主機時，提供連線的介面必須已指派可路由傳送的 IPv6 位址。連線至 IPv6 回送位址 (：： 1) 或連結-本機目的地時，不需要可路由傳送的 IPv6 位址。如果要求的 URL 包含名稱 (www.contoso.com，例如) ，則網域名稱系統 (DNS) 查詢該名稱必須傳回一或多個 IPv6 位址。如果要求的 URL 包含 IPv6 位址 (：：1（例如) ），則 IPv6 位址必須以方括弧括住 (HTTPs:// \[ ：： 1 \]) 。 範圍識別碼（有時稱為「區域索引」）支援為 IPv6 位址的一部分。 範圍識別碼是用來決定在具有多個網路介面的電腦上傳送要求時，所要使用的網路介面。 在主要 IPv6 位址 (fe80：： 1% 11 之後，使用 '% ' 字元指定範圍識別碼，例如) 。 不過，'% ' 字元必須在與 Internet Explorer 搭配使用的 URL 中進行換用。 例如，使用 Internet Explorer 時，連結-本機位址的範圍識別碼11會指定為 HTTPs:// \[ fe80：： 1% 2511 \] 。 Internet Explorer 7 和更新版本支援在 URL 中使用 IPv6 位址的功能。
ms.assetid: c3a8303a-50d6-4deb-a371-171ac0a7c5a9
title: 使用 Internet Explorer 來存取 IPv6 網站
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48a9f18e80e0e163ad6fe4ccda0aaef43826edd4becb28e294aad5eca7085c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559269"
---
# <a name="using-internet-explorer-to-access-ipv6-websites"></a>使用 Internet Explorer 來存取 IPv6 網站

Microsoft Internet Explorer 支援使用 IPv6 來連接及存取已啟用 IPv6 的網站 (網頁伺服器和 FTP 伺服器，例如在符合下列情況時) ：

-   執行 Internet Explorer 的主機電腦必須安裝並啟用 IPv6。
    -   連接到位於本機子網上的主機時，提供連線的介面必須已指派可路由傳送的 IPv6 位址。
    -   連線至 IPv6 回送位址 (：： 1) 或連結-本機目的地時，不需要可路由傳送的 IPv6 位址。
-   如果要求的 URL 包含名稱 (www.contoso.com，例如) ，則網域名稱系統 (DNS) 查詢該名稱必須傳回一或多個 IPv6 位址。
-   如果要求的 URL 包含 IPv6 位址 (：：1（例如) ），則 IPv6 位址必須以方括弧括住 (HTTPs:// \[ ：： 1 \]) 。 範圍識別碼（有時稱為「區域索引」）支援為 IPv6 位址的一部分。 範圍識別碼是用來決定在具有多個網路介面的電腦上傳送要求時，所要使用的網路介面。 在主要 IPv6 位址 (fe80：： 1% 11 之後，使用 '% ' 字元指定範圍識別碼，例如) 。 不過，'% ' 字元必須在與 Internet Explorer 搭配使用的 URL 中進行換用。 例如，使用 Internet Explorer 時，連結-本機位址的範圍識別碼11會指定為 HTTPs:// \[ fe80：： 1% 2511 \] 。 Internet Explorer 7 和更新版本支援在 URL 中使用 IPv6 位址的功能。

> [!Note]  
> 如果 Internet Explorer 設定為使用 proxy 伺服器，則 proxy 伺服器必須已指派 IPv6 位址，且 proxy 伺服器必須能夠 proxy 處理 IPv6 位址。 Proxy 伺服器將用來連接到使用 IPv6 的外部主機。 通常會略過 IPv6 回送位址和 IPv6 連結-本機位址的 proxy 伺服器。

 

 

 



