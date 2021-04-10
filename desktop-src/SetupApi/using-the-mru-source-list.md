---
description: SetupSetSourceList 函數會開啟或建立使用者系統上的來源清單。
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: 使用 MRU 來源清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbecb9e32a554d1818661b1fd7f6e782744c16e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943920"
---
# <a name="using-the-mru-source-list"></a>使用 MRU 來源清單

[**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista)函式會開啟或建立使用者系統上的來源清單。 您可以指定將使用者清單、系統清單、使用者和系統清單的組合，或暫時清單設定為 MRU 來源清單。 如果使用暫存清單，則在呼叫 [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) 之前，它將是唯一可用來安裝應用程式的清單，或第二次呼叫 **SetupSetSourceList** 。

設定清單之後，您可以使用 [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) 來查詢來源清單，以取得來源路徑的陣列。 當不再需要來源清單陣列時，您必須呼叫 [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) 函式來釋放 [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista)所配置的資源。

若要將路徑新增至來源清單，也就是在使用者系統上的任何一個路徑或臨時清單中，請呼叫 [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista)。 如果指定的來源清單不是暫時性的，則該來源將會保留在使用者的系統上，並且可供後續安裝存取。

若要從來源路徑移除路徑，請呼叫 [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) 函數。

 

 



