---
description: 說明應用程式或服務提供者可以使用智慧卡子系統連接到智慧卡的方式。
ms.assetid: 27f8f25f-1883-4070-94a4-0d3c51032378
title: 存取智慧卡
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b155d467c9de28b1e02dea01511ea1e71d574eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987575"
---
# <a name="accessing-a-smart-card"></a>存取智慧卡

[*智慧卡*](/windows/desktop/SecGloss/s-gly)子系統提供數種方法，讓應用程式或 [*服務提供者*](/windows/desktop/SecGloss/c-gly)連接到智慧卡：

-   應用程式可以呼叫 [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) ，以連接到位於指定讀取器中的卡片。 這是與智慧卡建立通訊的最簡單方式。
-   應用程式可以在指定的讀者群組內搜尋特定的智慧卡。 應用程式會依其顯示名稱來識別卡片，並指定卡片可能出現的讀取器清單。 [*資源管理員*](/windows/desktop/SecGloss/r-gly)會在讀取器清單中搜尋 [*ATR 字串*](/windows/desktop/SecGloss/a-gly)符合命名卡，並將狀態資訊傳回給應用程式的所有卡片。 [*智慧卡子系統*](/windows/desktop/SecGloss/s-gly)絕對不會在取得 ATR 字串的情況下，使用 GUI 或與卡片互動。 但是，它會提供足夠的資訊給應用程式或通用控制項，讓使用者能夠透過尋找所需的卡片或卡片類型來引導使用者。 這會導致將要求對應至特定讀取器，以進一步的 i/o 導向。
-   應用程式可以要求支援一組指定智慧卡介面的卡片清單。 然後，應用程式可以使用先前案例中的清單。 這可讓應用程式根據其功能連接到卡片，而不考慮其名稱。

當應用程式尋找卡片時，它會提供要在其中查看的讀者名稱陣列。 資源管理員會針對陣列中的每個讀取器元素提供下列資訊：

-   此應用程式是否可使用讀取器。
-   是否有卡片插入此讀取器，如果有的話，它的 ATR 字串是什麼。
-   卡片的 ATR 字串是否符合任何要求的卡片 ATR 字串。

應用程式會使用傳回的資訊，將進一步的篩選套用到卡片，或提示使用者選取所需的卡片。 請注意，可能會開啟一或多個已傳回的讀取器清單，供其他應用程式使用，因此不保證無法存取這份讀取器清單。

 

 
