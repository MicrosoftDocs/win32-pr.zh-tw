---
description: 下圖顯示監視器與網路監視器架構的其他元件之間的關聯性。
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: 監視架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9cd0a099fc1474255b36f1f04d28899b25a527fee19ba1d29434b4692615ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677121"
---
# <a name="monitor-architecture"></a>監視架構

下圖顯示 [*監視器*](m.md) 與網路監視器架構的其他元件之間的關聯性。

![監視器與網路監視器的其他元件之間的關聯性](images/nmarch2.png)

從 NDIS 驅動程式) 的個別畫面格 (收集網路流量。 網路監視器驅動程式 (Nmnt.sys) 接著將框架路由傳送到網路封包提供者 (NPP) ，進而在即時模式中捕獲資料。 NPP 是用來捕捉資料的 COM 介面集合。 在此情況下， [**IRTC**](irtc.md) 介面會用來執行即時捕捉。

> [!Note]  
> NPP 用於延遲和即時的捕獲。 若為專家和剖析器所使用的延遲捕捉，則會使用 [**IDelaydC**](idelaydc.md) 介面。

 

然後，監視器會以即時模式檢查捕捉的資料、偵測特定的網路狀況，並視需要產生事件。

監視器應用程式會使用其他三個元件：監視器控制工具、監視器控制服務 (MCSVC) 和事件檢視器：

-   監視器控制工具是用來管理您的監視器應用程式。 這包括設定和執行所有的監視器應用程式。
-   監視器控制服務 (MCSVC) 引發事件、提供 WMI 的通訊連結以進行事件的查看，以及協調監視作業的處理。
-   事件檢視器會顯示監視器控制服務所引發的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMonitor**](imonitor.md)
</dt> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> </dl>

 

 



