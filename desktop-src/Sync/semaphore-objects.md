---
description: 信號物件是一種同步處理物件，可維護介於零和指定最大值之間的計數。
ms.assetid: d9da1d98-a306-4e2d-a149-1eef6a724751
title: 信號物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77f36313d76c5d98c786a76f10ad8439965f180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981206"
---
# <a name="semaphore-objects"></a>信號物件

*信號物件* 是一種同步處理物件，可維護介於零和指定最大值之間的計數。 每次執行緒完成信號物件的等候，而且每次執行緒釋放信號時，就會增加計數。 當計數達到零時，就不會有其他執行緒成功等候信號物件狀態變成已發出信號。 旗號的狀態會在其計數大於零時設定為已收到訊號，並在計數為零時設定為未收到訊號。

在控制可支援有限使用者數量的共用資源時，信號物件相當有用。 它會將共用資源的執行緒數目限制為指定的最大數目，作為閘道。 例如，應用程式可能會限制其所建立的視窗數目。 它會使用最大計數等於視窗限制的信號，並在每次建立視窗時遞減計數，並在視窗關閉時遞增。 應用程式會在每個視窗建立之前，指定呼叫其中一個 [等候函數](wait-functions.md) 的信號物件。 當計數為零時（表示已達到視窗限制），等候函式會封鎖視窗建立程式碼的執行。

執行緒使用 [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) 或 [**CreateSemaphoreEx**](/windows/desktop/api/WinBase/nf-winbase-createsemaphoreexa) 函數來建立信號物件。 建立執行緒會指定物件之計數的初始計數和最大值。 初始計數必須小於零，也不能大於最大值。 建立執行緒也可以指定信號物件的名稱。 其他進程中的執行緒可以藉由在 [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew) 函式的呼叫中指定其名稱，來開啟現有信號物件的控制碼。 如需 mutex、事件、信號和計時器物件之名稱的詳細資訊，請參閱 [進程間同步](interprocess-synchronization.md)處理。

如果有一個以上的執行緒正在等候信號，則會選取等候中的執行緒。 請勿採用先進先出 (FIFO) 順序。 外來事件（例如核心模式 Apc）可以變更等候順序。

每次 [等候](wait-functions.md) 函式的其中一個因為信號的狀態設為「已發出信號」而傳回，則信號的計數會減少一。 [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore)函式會以指定的數量來增加信號的計數。 計數絕不能小於零或大於最大值。

信號的初始計數通常會設定為最大值。 然後，會在取用受保護的資源時，從該層級遞減計數。 或者，您可以建立初始計數為零的信號，以在應用程式初始化時封鎖對受保護資源的存取。 初始化之後，您可以使用 [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) 將計數遞增到最大值。

擁有 mutex 物件的執行緒可以針對相同的 mutex 物件重複等候，使其不會被封鎖。 但是，針對相同的信號物件重複等候的執行緒，會在每次等候作業完成時遞減信號的計數;當計數到達零時，會封鎖執行緒。 同樣地，只有擁有 mutex 的執行緒可以成功呼叫 [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) 函式，不過任何執行緒都可以使用 [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) 來增加信號物件的計數。

執行緒可以在對任何 [等候](wait-functions.md)函式的呼叫中重複指定相同的信號物件，藉此遞減信號的計數。 不過，使用包含相同信號之多個控制碼的陣列來呼叫其中一個多物件等候函式，不會導致多個遞減。

當您完成使用信號物件時，請呼叫 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 函數來關閉控制碼。 當最後一個控制碼關閉時，就會終結信號物件。 關閉控制碼並不會影響信號計數;因此，請務必在關閉控制碼之前或進程終止之前呼叫 [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) 。 否則，暫止的等候作業可能會無限期或繼續無限期，視是否已指定超時值而定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用信號物件](using-semaphore-objects.md)
</dt> </dl>

 

 
