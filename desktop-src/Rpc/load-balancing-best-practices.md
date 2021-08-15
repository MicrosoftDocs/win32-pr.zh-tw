---
title: 負載平衡的最佳作法
description: 負載平衡的最佳作法
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fe4af9dffe758c89d1a494d4cc2597e057c563ca8c85db87d789ae91b89698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928593"
---
# <a name="load-balancing-best-practices"></a>負載平衡的最佳作法

設定和設定 RPC 負載平衡時，應該遵循幾個最佳作法。

首先，安全性應該設定在傳入和傳出的磅通話上。 這表示兩個選用的 [NoSecurity](configuring-load-balancing.md) 登錄機碼應該不存在，或應該設定為零。

第二，請注意必須支付與 RPC 負載平衡解決方案搭配使用的前端負載平衡解決方案。 例如，如果前端負載平衡器使用簡單的迴圈配置資源負載平衡，伺服器陣列中應該會有奇數部伺服器。 這是為了降低所有連接的可能性，因此可以由同一部伺服器或伺服器來提供服務。

基於安全性，通常最好讓防火牆控制 RPC Proxy 伺服器的存取權。 如果採用以埠為基礎的防火牆解決方案，RPC 端點必須是靜態的，才能限制在防火牆中開啟的埠數目。 在 Windows Server 2008 和更新版本的 Windows 中，RPC 會提供一個機制，將靜態埠指派給動態端點。 這是透過 RPC netsh firewall 命令來達成。 將磅介面設定為靜態埠3010的範例命令集為：

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

您可以使用 RPC netsh 命令，為任何動態或靜態介面設定靜態端點。 當您限制對執行埠型防火牆解決方案的電腦進行存取時，這會很有用。 如果使用 Windows 防火牆解決方案，則可以封鎖或啟用 RPC 介面，而不需要將它指派給特定埠。 如需詳細資訊，請參閱 [RPC netsh firewall 命令參考](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10))。

 

 