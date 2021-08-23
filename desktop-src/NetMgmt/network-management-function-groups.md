---
title: 網路管理功能群組
description: 網路管理功能可以分成下列群組。
ms.assetid: 4b5d3554-f81a-4ecf-bf31-ee4753509f38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e49a8c45c59031a12653f5cb863fef320a33c93bc60cabdd4cd6fb4aece9dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012506"
---
# <a name="network-management-function-groups"></a>網路管理功能群組

網路管理功能可以分成下列群組：

-   [警示功能](alert-functions.md)
-   [ApiBuffer 函式](apibuffer-functions.md)
-   [目錄服務功能](directory-service-functions.md)
-   [分散式檔案系統 (Dfs) 函式](/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions)
-   [取得函式](get-functions.md)
-   [群組函式](group-functions.md)
-   [本機群組函數](local-group-functions.md)
-   [訊息函數](message-functions.md)
-   [NetFile 函式](netfile-functions.md)
-   [遠端公用程式函式](remote-utility-functions.md)
-   [排程函數](schedule-functions.md)
-   [伺服器函數](server-functions.md)
-   [伺服器和工作站傳輸功能](server-and-workstation-transport-functions.md)
-   [會話函數](session-functions.md)
-   [共用函式](share-functions.md)
-   [Statistics 函數](/windows/desktop/NetShare/statistics-functions)
-   [使用函式](use-functions.md)
-   [使用者函式](user-functions.md)
-   [使用者模式函數](user-modal-functions.md)
-   [工作站和工作站使用者功能](workstation-and-workstation-user-functions.md)

如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定的 ADSI 介面方法，以取得您可以藉由呼叫特定網路管理功能來達成的相同功能。 如需詳細資訊，請參閱 [將 ADSI 介面對應到網路管理功能](mapping-adsi-interfaces-to-the-network-management-functions.md)。

系統也會提供一組與網路無關的網路功能， ([WNet](/windows/desktop/WNet/wnet-functions) 函式) ，可讓網路功能跨不同的網路廠商產品運作。 如果您的應用程式可轉換為使用 WNet 函式，您應該執行轉換。 進行變更的原因如下：

-   WNet 函式與網路無關，而網路管理功能只能在 Microsoft 網路上運作。
-   如果 Microsoft 作業系統的未來版本已被取代，可能不支援某些功能。 除非有對等或更好的功能可供使用，否則 Microsoft 不打算移除特定功能。

 

 