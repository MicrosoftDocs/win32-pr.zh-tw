---
description: 監視器是動態連結程式庫 (DLL) ，可檢查網路流量的即時捕獲。
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: 監視器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943512"
---
# <a name="monitors"></a>監視器

監視器是動態連結程式庫 (DLL) ，可檢查網路流量的即時捕獲。 它會搜尋預先定義的條件，然後在偵測到這些狀況時產生事件。 例如，當嘗試網路中斷時、惡意工作站正在處理 IP 位址，或路由器故障時，就會引發事件。

> [!Note]  
> 如果您需要對需要後續捕獲分析的網路資料執行詳細分析，您必須使用 [*專家*](e.md)[*和剖析*](p.md)器應用程式。

 

[*監視器控制服務*](m.md) (MCSVC) 提供管理監視的架構。 它提供的函式可將監視器 Dll 和通訊介面載入至監視器控制工具，讓您可以建立、設定、啟動、停止和停用監視的多個實例。

監視會在兩個執行執行緒中執行。 MCSVC 會提供第一個執行緒，以提供監視的直接控制。 第二個執行緒是由 [*網路封包提供者*](n.md) 所提供 (NPP) ，它提供一種方式，可將捕獲的網路資料、統計資料和 NPP 的狀態從傳回給監視器。

每個用來捕捉資料的執行時間 NPP 介面都可以有多個相同監視的實例。

 

 



