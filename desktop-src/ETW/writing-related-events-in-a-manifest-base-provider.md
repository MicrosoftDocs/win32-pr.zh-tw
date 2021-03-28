---
description: 當有數個元件希望在端對端追蹤案例中建立其事件的關聯時，請使用 EventWriteTransfer 函數。
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: 在以資訊清單為基礎的提供者中撰寫相關的事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512181"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a>在以資訊清單為基礎的提供者中撰寫相關的事件

當有數個元件希望在端對端追蹤案例中建立其事件的關聯時，請使用 [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) 函數。 例如，元件 A、B 和 C 會針對相關活動執行工作，而且想要連結與該活動相關的所有事件。

ETW 使用執行緒區域儲存區，將上一個元件的活動識別碼提供給下一個元件。 元件會從本機儲存體取出先前元件的識別碼，並將相關的活動識別碼設定為它。 然後，取用者可以使用相關的活動識別碼，將來自某個元件的事件鏈引導至下一個元件。

 

 



