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
# <a name="using-the-mru-source-list"></a><span data-ttu-id="df23c-103">使用 MRU 來源清單</span><span class="sxs-lookup"><span data-stu-id="df23c-103">Using the MRU Source List</span></span>

<span data-ttu-id="df23c-104">[**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista)函式會開啟或建立使用者系統上的來源清單。</span><span class="sxs-lookup"><span data-stu-id="df23c-104">The [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) function will open or create a source list on the user's system.</span></span> <span data-ttu-id="df23c-105">您可以指定將使用者清單、系統清單、使用者和系統清單的組合，或暫時清單設定為 MRU 來源清單。</span><span class="sxs-lookup"><span data-stu-id="df23c-105">You can specify to set the user list, the system list, a combination of the user and system lists, or a temporary list as the MRU source list.</span></span> <span data-ttu-id="df23c-106">如果使用暫存清單，則在呼叫 [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) 之前，它將是唯一可用來安裝應用程式的清單，或第二次呼叫 **SetupSetSourceList** 。</span><span class="sxs-lookup"><span data-stu-id="df23c-106">If a temporary list is used, it will be the only list available to the setup application until [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) is called, or **SetupSetSourceList** is called a second time.</span></span>

<span data-ttu-id="df23c-107">設定清單之後，您可以使用 [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) 來查詢來源清單，以取得來源路徑的陣列。</span><span class="sxs-lookup"><span data-stu-id="df23c-107">After a list is set, you can query the source list by using [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) to obtain an array of the source paths.</span></span> <span data-ttu-id="df23c-108">當不再需要來源清單陣列時，您必須呼叫 [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) 函式來釋放 [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista)所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="df23c-108">When the source list array is no longer needed, you must call the [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) function to free the resources allocated by [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span></span>

<span data-ttu-id="df23c-109">若要將路徑新增至來源清單，也就是在使用者系統上的任何一個路徑或臨時清單中，請呼叫 [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista)。</span><span class="sxs-lookup"><span data-stu-id="df23c-109">To add a path to a source list, either one that is resident on the user's system, or a temporary list, call [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span></span> <span data-ttu-id="df23c-110">如果指定的來源清單不是暫時性的，則該來源將會保留在使用者的系統上，並且可供後續安裝存取。</span><span class="sxs-lookup"><span data-stu-id="df23c-110">If the source list specified is not temporary, that source will remain on the user's system and is accessible to subsequent installations.</span></span>

<span data-ttu-id="df23c-111">若要從來源路徑移除路徑，請呼叫 [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) 函數。</span><span class="sxs-lookup"><span data-stu-id="df23c-111">To remove a path from the source path, call the [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) function.</span></span>

 

 



