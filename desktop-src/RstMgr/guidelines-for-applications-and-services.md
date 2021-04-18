---
title: 應用程式和服務的指導方針
description: 若要減少在 Windows Vista 或 Windows Server 2008 上安裝和處理應用程式時系統重新開機的次數，您應該觀察下列指導方針，讓您的應用程式或服務能夠完全關閉並重新啟動。
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969034"
---
# <a name="guidelines-for-applications-and-services"></a>應用程式和服務的指導方針

若要減少在 Windows Vista 或 Windows Server 2008 上安裝和處理應用程式時系統重新開機的次數，您應該觀察下列指導方針，讓您的應用程式或服務能夠完全關閉並重新啟動。

-   當需要安裝更新時，您的應用程式和服務應該準備好讓系統關機並重新啟動。 一般來說，安裝更新時，應用程式或服務需要關閉，因為它目前持有受影響的檔案。 在更新期間，所有可保存所使用檔案的應用程式或服務都應該準備好完全關閉。
-   在重新開機之後，您的應用程式應該會儲存所需的使用者資料和狀態資訊，而且應遵守 [應用程式指南](guidelines-for-applications.md)中所述的指導方針。
-   您的服務應遵守 [服務指導方針](guidelines-for-services.md)中所述的指導方針。
-   重新開機管理員不會關閉 [重要的系統服務](critical-system-services.md);因此，這些服務應該會限制它們所依賴的 Dll 數目。

 

 




