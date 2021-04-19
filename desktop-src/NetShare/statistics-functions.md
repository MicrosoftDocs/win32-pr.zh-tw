---
description: Windows 作業系統會從工作站或伺服器服務啟動時，累積工作站和伺服器的一組操作統計資料。
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Statistics 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979959"
---
# <a name="statistics-functions"></a>Statistics 函數

Windows 作業系統會從工作站或伺服器服務啟動時，累積工作站和伺服器的一組操作統計資料。 若要取得這些統計資料，您可以呼叫下列網路管理統計資料函數。



| 函式                                     | 描述                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**NetStatisticsGet**](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | 捕獲服務的作業統計資料;支援工作站和伺服器服務。 |



 

要求工作站統計資料時， **NetStatisticsGet** 函式會傳回 [**stat \_ 工作站 \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) 結構; 當要求伺服器統計資料時，此函數會傳回 [**stat \_ server \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) 結構。

 

 



