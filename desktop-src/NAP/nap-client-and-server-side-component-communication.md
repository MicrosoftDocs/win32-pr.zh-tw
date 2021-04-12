---
title: NAP 用戶端和伺服器端元件通訊
description: NAP 用戶端和伺服器端元件通訊
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372538"
---
# <a name="nap-client-and-server-side-component-communication"></a>NAP 用戶端和伺服器端元件通訊

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

NAP 代理程式元件可以透過下列程式與 NAP 管理伺服器元件通訊：

1.  NAP 代理程式會將 SSoH 傳遞至 NAP EC。
2.  NAP EC 會將 SSoH 傳遞給 NAP ES。
3.  NAP ES 會將 SSoH 傳遞至網路原則伺服器 (NPS) 服務。
4.  NPS 服務會將 SSoH 傳遞給 NAP 管理伺服器。

SHA 可透過下列進程與其對應的 SHV 通訊：

1.  SHA 會將其 SoH 傳遞給 NAP 代理程式。
2.  NAP 代理程式會將包含在 SSoH 內的 SoH 傳遞至 NAP EC。
3.  NAP EC 會將 SoH 傳遞給 NAP ES。
4.  NAP ES 將 SoH 傳遞給 NAP 管理伺服器。
5.  NAP 管理伺服器會將 SoH 傳遞給 SHV。

下圖顯示 NAP 用戶端元件與 NAP 伺服器端元件之間的通訊流程。

![nap 平臺中用戶端對伺服器通訊的架構](images/nap-client-to-server-comm.png)

NAP 管理伺服器可以透過下列程式與 NAP 代理程式通訊：

1.  NAP 管理伺服器會將 Sohr 傳遞給 NPS 服務。
2.  NPS 服務會將 SSoHR 傳遞至 NAP ES。
3.  NAP ES 會將 SSoHR 傳遞給 NAP EC。
4.  NAP EC 將 SSoHR 傳遞給 NAP 代理程式。

SHV 可透過下列進程與其對應的 SHA 通訊：

1.  SHV 會將其 SoHR 傳遞給 NAP 管理伺服器。
2.  NAP 管理伺服器會將 SoHR 傳遞給 NPS 服務。
3.  NPS 服務會將包含在 SSoHR 中的 SoHR 傳遞至 NAP ES。
4.  NAP ES 會將 SoHR 傳遞給 NAP EC。
5.  NAP EC 將 SoHR 傳遞給 NAP 代理程式。
6.  NAP 代理程式會將 SoHR 傳遞給 SHA。

下圖顯示從 NAP 伺服器端元件到 NAP 用戶端元件的通訊流程。

![nap 平臺中伺服器對用戶端通訊的架構](images/nap-server-to-client-comm.png)

 

 




