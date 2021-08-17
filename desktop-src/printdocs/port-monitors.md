---
description: 設備磁碟機將整個日誌檔案轉換成原始裝置命令之後，已轉換命令的檔案會傳回至多工緩衝處理器。
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: 埠監視器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8334da48fb147a41924be2cf090f55d7955cb1d7913c43b302a312fd4447602f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470928"
---
# <a name="port-monitors"></a>埠監視器

設備磁碟機將整個日誌檔案轉換成原始裝置命令之後，已轉換命令的檔案會傳回至多工緩衝處理器。 多工緩衝處理器會將這些低層級的命令傳送至監視器。 埠監視器是一種 .dll，可透過網路、透過平行埠，或透過序列埠傳送至印表機裝置來傳遞原始裝置命令。 您可以安裝自訂埠監視，以支援透過其他通訊埠傳遞裝置資料。

使用下列功能來處理埠監視器。



| 函式                               | 描述                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**AddMonitor**](addmonitor.md)       | 安裝本機埠監視器，並連結設定、資料和監視檔案。 |
| [**DeleteMonitor**](deletemonitor.md) | 移除 [**AddMonitor**](addmonitor.md) 函式所新增的埠監視器。      |
| [**EnumMonitors**](enummonitors.md)   | 列舉安裝在指定伺服器上的埠監視器。                       |



 

 

 



