---
title: 遠端資料服務已移除
description: 遠端資料服務伺服器元件已在 Windows 8 中移除
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- RDS 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "103933681"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a>遠端資料服務伺服器元件已在 Windows 8 中移除

## <a name="platforms"></a>平台

 **客戶** 端-Windows 8  
**伺服器** -Windows Server 2012  



## <a name="description"></a>Description

Windows 8 中無法使用 (RDS) server 的遠端資料服務：

-   會移除裝載預設「商務物件」 RDSServer 的檔案 msadcf.dll，並移除其相關聯的檔案 (msadcfr.dll、msadcfr.dll mui、處理 .reg 和 handsafe .reg) 
-   檔案 msdfmap.dll （這是預設處理常式）已移除，並移除檔案 msdfmap.ini
-   檔案 msadcs.dll （ISAPI）已移除

## <a name="manifestation"></a>表現

客戶無法在 Windows 8 上裝載 RDS 伺服器。

## <a name="mitigation"></a>降低

客戶可以將 RDS 伺服器保留在 Windows 7 或其他舊版作業系統的電腦上。

## <a name="solution"></a>解決方法

客戶可以將 RDS 伺服器保留在 Windows 7 或其他舊版作業系統的電腦上。

## <a name="resources"></a>資源

[資料存取技術藍圖](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 