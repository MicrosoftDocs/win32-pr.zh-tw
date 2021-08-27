---
title: 使用 RPC over HTTP 的遠端程序呼叫
description: 網際網路瀏覽器程式通常會使用超文字傳輸通訊協定 (HTTP) 作為流覽全球 Web 的主要方式。
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- 使用 RPC/HTTP 的遠端程序呼叫 RPC、工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fedeb1700d798a616d3441b356f6f31867eed0399f412ed1f82923bcc4ac5f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101658"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a>使用 RPC over HTTP 的遠端程序呼叫

網際網路瀏覽器程式通常會使用超文字傳輸通訊協定 (HTTP) 作為流覽全球 Web 的主要方式。 因此，HTTP 現在會在大部分的電腦上看到廣泛的使用量。 Microsoft 已將其 Internet Information Server 的功能延伸 (IIS) ，以提供使用 HTTP 的遠端程序呼叫服務。

Microsoft RPC over HTTP 的 (RPC over HTTP) 可讓 RPC 用戶端安全且有效率地透過網際網路連接到 RPC 伺服器程式，並執行遠端程序呼叫。 這是透過稱為 RPC over HTTP Proxy 的媒介，或單純的 RPC Proxy 來完成。

RPC Proxy 會在 IIS 電腦上執行。 它會接受來自網際網路的 RPC 要求、對這些要求執行驗證、驗證和存取檢查，如果要求通過所有測試，RPC Proxy 就會將要求轉送到執行實際處理的 RPC 伺服器。 使用 RPC over HTTP 時，RPC 用戶端和伺服器不會直接通訊;相反地，它們會使用 RPC Proxy 作為媒介。 因為許多原因而選擇這個模型。 如需詳細資訊，請參閱 [RPC OVER HTTP 安全性](rpc-over-http-security.md)。

本節提供下列主題中 RPC over HTTP 的總覽：

-   [使用 HTTP 做為 RPC 傳輸](using-http-as-an-rpc-transport.md)
-   [RPC over HTTP 安全性](rpc-over-http-security.md)
-   [RPC over HTTP 的系統需求和互通性](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [設定 RPC over HTTP 的電腦](configuring-computers-for-rpc-over-http.md)
-   [RPC over HTTP 部署建議](rpc-over-http-deployment-recommendations.md)

如需有關高容量 RPC over HTTP 案例的詳細資訊，請參閱 [MICROSOFT RPC 負載平衡](rpc-load-balancing.md)。

 

 




