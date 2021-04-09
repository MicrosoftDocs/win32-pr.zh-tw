---
title: 多播群組管理員用戶端
description: 用戶端是呼叫 MGM 函數的實體，例如路由通訊協定或系統管理應用程式。
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675576"
---
# <a name="multicast-group-manager-client"></a>多播群組管理員用戶端

用戶端是呼叫 MGM 函數的實體，例如路由通訊協定或系統管理應用程式。

MGM API 主要是由多播路由通訊協定使用。 多播路由通訊協定的開發人員會使用 MGM API 來：

-   維護群組成員資格
-   控制介面擁有權
-   從多播群組管理員接收有關多播資料的其他多播路由通訊協定要求的通知

必須監視多播轉送專案的特定系統管理應用程式 (MFEs) 可以這麼做，而不需要新增或移除群組成員資格。 系統管理應用程式開發人員會使用特定的 MGM 函式來檢查 MFEs 中的資訊。

> [!Note]  
> 多播路由通訊協定也會存取 MFEs。

 

MFE 是「多播群組管理員」依據群組成員資格建立的轉送資訊。 從多播群組管理員中取出的 MFEs 可以提供統計資訊。 系統管理應用程式接著可以使用此資訊來判斷適當的動作。 例如，系統管理應用程式可以根據特定介面上的封包量來執行動作。

 

 




