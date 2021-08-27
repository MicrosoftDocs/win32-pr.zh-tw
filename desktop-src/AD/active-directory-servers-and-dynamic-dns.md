---
title: Active Directory 伺服器和動態 DNS
description: Active Directory 伺服器會發佈其位址，讓用戶端可以找到只知道功能變數名稱的名稱。
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- 動態 DNS Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9828a2d6d14d862e98d3c5c4129bbc70f5c411
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880071"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Active Directory 伺服器和動態 DNS

Active Directory 伺服器會發佈其位址，讓用戶端可以找到只知道功能變數名稱的名稱。 Active Directory 的伺服器是使用 DNS 中 (SRV Rr) 的服務資源記錄來發佈。 SRV RR 是用來將服務名稱對應至提供服務之伺服器位址的 DNS 記錄。 SRV RR 的名稱格式如下：


```C++
<service>.<protocol>.<domain>
```



Active Directory 伺服器透過 TCP 通訊協定提供 LDAP 服務，讓發佈的名稱為 "LDAP net.tcp. &lt;網域」 &gt; 。 因此，fabrikam.com 的 SRV RR 為 "ldap.tcp.fabrikam.com"。 SRV RR 的其他相關資料會指出伺服器的優先順序和權數，讓用戶端選擇最適合其需求的伺服器。

安裝 Active Directory 伺服器時，它會使用動態 DNS 來發佈本身。 因為 TCP/IP 位址可能會變更，所以伺服器會定期驗證他們的註冊，以確保它們是正確的，並視需要加以更新。

動態 DNS 是 DNS 標準的最新加入。 動態 DNS 會定義用來動態更新 DNS 伺服器與新資料的通訊協定。 在動態 DNS 之前，系統管理員必須手動設定 DNS 伺服器所儲存的記錄。

 

 




