---
description: 下圖顯示專家和剖析器應用程式之間的關聯性，以及網路監視器架構的其他元件之間的關聯性。
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: 專家和剖析器架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112245"
---
# <a name="expert-and-parser-architecture"></a>專家和剖析器架構

下圖顯示 [專家](experts.md) 和剖析器應用程式之間的關聯 [性，以及](parsers.md) 網路監視器架構的其他元件之間的關聯性。

![專家和剖析器應用程式之間的關聯性](images/nm-arch1.png)

從 NDIS 驅動程式收集網路流量，作為個別的畫面。 網路監視器驅動程式 (Nmnt.sys) 接著將框架路由傳送到網路封包提供者 (NPP) ，這會捕捉資料並將其放在一或多個 capture 檔案中。 NPP 是用來捕捉資料的 COM 介面集合。 在此情況下， [**IDelaydC**](idelaydc.md) 介面會用來執行延遲的捕獲。

> [!Note]  
> NPP 用於延遲和即時的捕獲。 若為即時捕捉，則會使用 [**IRTC**](irtc.md) 介面。

 

當網路框架儲存在 capture 檔中，而且檔案可供存取時，專家和剖析器可以使用網路監視器 UI 和 Nmapi.dll 中提供的網路監視器函數來分析資料。 在 capture 完成之前，無法存取 capture 檔。

 

 



