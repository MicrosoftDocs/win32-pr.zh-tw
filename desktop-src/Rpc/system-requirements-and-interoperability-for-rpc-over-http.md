---
title: RPC over HTTP 系統需求，互通性
description: Microsoft RPC 支援 RPC over HTTP，如下表所示。
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc9019789821499168a76d4d2e02ef485529e08b99c5f0759a19bfb4a46f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017308"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>RPC over HTTP 系統需求，互通性

Microsoft RPC 支援 RPC over HTTP，如下表所示。



| 平台                             | 支援                       | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | 用戶端、伺服器和 RPC Proxy | 支援 RPC over HTTP v1 和 RPC over HTTP v2 用戶端和伺服器。 當 IIS 以 IIS 6.0 模式執行時，RPC Proxy 支援 RPC over HTTP v2。 當 IIS 以 IIS 5.0 模式執行時，RPC Proxy 支援 RPC over HTTP v1 和 RPC over HTTP v2。 但是，不建議在 IIS 5.0 模式中執行。 如需詳細資訊，請參閱[RPC over HTTP 部署建議](rpc-over-http-deployment-recommendations.md)。 RPC over HTTP 伺服器和 RPC Proxy 可以位於不同的電腦上。 |
| WindowsXP Service Pack 1 (SP1)  | 用戶端和伺服器            | 支援 RPC over HTTP v1 和 RPC over HTTP v2 用戶端和伺服器。 不支援 RPC Proxy。                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | 用戶端和伺服器            | 僅支援 RPC over HTTP v1 用戶端和伺服器。 不支援 RPC Proxy。                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | 用戶端、伺服器和 RPC Proxy | RPC over HTTP 伺服器程式和 RPC Proxy 可以在不同的電腦上執行。 RPC over HTTP 用戶端、伺服器和 RPC Proxy 僅支援 RPC over HTTP v1。                                                                                                                                                                                                                                                                                                                   |



 

此外，也適用下列需求：

-   Windows 2000 和更新版本需要使用 IIS 4.0 或更新版本。
-   RPC over HTTP proxy 只會在 Windows 伺服器版本上執行。
-   如果 IIS 是在伺服器版本的 Windows 上執行，rpc over HTTP 伺服器程式可以在設定 rpc Proxy 以轉寄流量的任何電腦上執行。 因此，它可以在與 RPC Proxy 相同的電腦上執行，也可以在不同的電腦上執行。

針對要建立的 RPC over HTTP 連線，所有 RPC over HTTP 用戶端、RPC over HTTP 伺服器和 RPC Proxy 都必須同意使用哪個版本的 RPC over HTTP。 如果沒有通用的 RPC over HTTP 版本，這三項支援 (用戶端、伺服器和 RPC Proxy) ，就無法建立 RPC over HTTP 連線。 下表摘要說明不同 RPC over HTTP 版本的這項互通性。



| RPC over HTTP 用戶端 | RPC Proxy      | RPC over HTTP 伺服器 | 工程？                                      | 使用的版本     |
|----------------------|----------------|----------------------|---------------------------------------------|------------------|
| 僅 v1              | 僅 v1        | 僅 v1              | 是，含 v1 限制                    | RPC over HTTP v1 |
| 僅 v1              | 僅 v1        | V1 和 v2       | 是，含 v1 限制                    | RPC over HTTP v1 |
| 僅 v1              | V1 和 v2 | 僅 v1              | 是，含 v1 限制                    | RPC over HTTP v1 |
| 僅 v1              | V1 和 v2 | V1 和 v2       | 是，含 v1 限制                    | RPC over HTTP v1 |
| 僅 v1              | 僅限 v2        | 僅 v1              | No                                          |                  |
| 僅 v1              | 僅限 v2        | V1 和 v2       | No                                          |                  |
| V1 和 v2       | 僅 v1        | 僅 v1              | 是，含 v1 限制                    | RPC over HTTP v1 |
| V1 和 v2       | 僅 v1        | V1 和 v2       | 是，含 v1 限制                    | RPC over HTTP v1 |
| V1 和 v2       | V1 和 v2 | 僅 v1              | 是，含 v1 限制                    | RPC over HTTP v1 |
| V1 和 v2       | V1 和 v2 | V1 和 v2       | Yes                                         | RPC over HTTP v2 |
| V1 和 v2       | 僅限 v2        | 僅 v1              | No                                          |                  |
| V1 和 v2       | 僅限 v2        | V1 和 v2       | 是。 這是建議的設定。 | RPC over HTTP v2 |



 

例如，假設 Windows 2000 用戶端、Windows Server 2003 proxy，且 iis 以 iis 6.0 模式執行，而 Windows server 2003 RPC over HTTP 伺服器。 此參考頁面上的第一個表格顯示 Windows 2000 僅支援 RPC over HTTP v1。 相同的表格顯示，在 iis 6.0 模式中執行的 iis Windows Server 2003 僅支援 rpc over HTTP v2，而且 Windows Server 2003 rpc over HTTP 伺服器支援 rpc over HTTP v1 和 rpc over HTTP v2。 此案例會在此參考頁面上第6列的第6個數據表中說明，其中顯示無法建立 RPC over HTTP 連接。 此外，第二個表格顯示該案例有兩個選擇：

-   如果不考慮安全性和穩定性，IIS 可以切換為 IIS 5.0 模式，同時支援 RPC over HTTP v1 和 RPC over HTTP v2。 這麼做可讓您建立 RPC over HTTP v1 連接。
-   將 Windows 98 用戶端升級至 Windows XP SP1，並取得 RPC over HTTP v2 連接的強大功能、安全性和穩定性。

 

 




