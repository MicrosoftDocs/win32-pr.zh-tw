---
title: 網路清單管理員架構
description: 網路清單管理員架構
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567b103cfd5d9944aa33a799c2cc1bc4b983759
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932571"
---
# <a name="network-list-manager-architecture"></a>網路清單管理員架構

網路清單管理員會在 Svchost.exe 內容中以服務的形式執行，並在電腦開機程式期間啟動。 網路清單管理員服務會維護可透過網路清單管理員 API，由應用程式抓取的可用網路和網路屬性資料表。 網路清單管理員提供基本的功能，可篩選及查詢特定網路的網路清單管理員服務，並取得這些網路的屬性。 下圖顯示網路清單管理員架構以及網路清單管理員服務與用戶端應用程式之間的互動。

![網路覺察架構圖表](images/architecture.png)

 

 




