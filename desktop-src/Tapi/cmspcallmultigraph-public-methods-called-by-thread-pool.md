---
description: 下列清單包含執行緒集區所呼叫的 CMSPCallMultiGraph 公用方法。
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: CMSPCallMultiGraph 由執行緒集區呼叫的公用方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971821"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a>CMSPCallMultiGraph 由執行緒集區呼叫的公用方法



| CMSPCallMultiGraph 公用方法                                   | Description                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | 當篩選圖形發出事件信號時呼叫。                                                                                                                                                           |
| [**HandleGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | 由 [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) 靜態方法呼叫。 [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)在主要 MSP 工作者執行緒上的佇列。 |
| [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | 允許 MSP 呼叫物件實例處理篩選圖形事件。                                                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



