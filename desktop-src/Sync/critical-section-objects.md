---
description: 重要區段物件提供的同步處理與 mutex 物件所提供的類似，不同之處在于，只有單一進程的執行緒可以使用重要區段。
ms.assetid: 2ec11a42-3d12-4d60-9dd7-dc38926d56e1
title: 重要區段物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcada1f2ddbc6d370445f36a3dbd51c5c9f54bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980407"
---
# <a name="critical-section-objects"></a>重要區段物件

*重要區段物件* 提供的同步處理與 mutex 物件所提供的類似，不同之處在于，只有單一進程的執行緒可以使用重要區段。 不可跨進程共用重要區段物件。

事件、mutex 和信號物件也可以在單一進程應用程式中使用，但重要區段物件可提供稍微更快、更有效率的機制來進行相互排除的同步處理 (處理器特定的測試和設定指令) 。 就像 mutex 物件一樣，一次只能有一個執行緒擁有一個重要區段物件，這有助於保護共用的資源，使其不會同時存取。 與 mutex 物件不同的是，沒有任何方法可分辨是否已放棄重要區段。

從 Windows Server 2003 （含 Service Pack 1） (SP1) 開始，在重要區段上等候的執行緒，並不會以先進先出的基礎來取得重要區段。 這種變更可大幅提高大部分程式碼的效能。 不過，有些應用程式相依于先進先出 (FIFO) 順序，而且可能會在目前的 (Windows 版本上執行效能不佳的情況，例如，已使用重要區段作為速率限制器) 的應用程式。 為了確保您的程式碼能繼續正常運作，您可能需要新增額外的同步處理層級。 例如，假設您有一個生產者執行緒和一個取用者執行緒，其使用重要區段物件來同步處理其工作。 建立兩個事件物件，每個執行緒都有一個，用來表示它已準備好讓其他執行緒繼續執行。 取用者執行緒會等待產生者在進入重要區段之前發出其事件的信號，而生產者執行緒會等待取用者執行緒在進入重要區段之前，先對其事件發出信號。 在每個執行緒離開重要區段之後，它會通知其事件釋放另一個執行緒。

**Windows Server 2003 和 WINDOWS XP：** 等候重要區段的執行緒會新增至等候佇列;它們是喚醒的，而且通常會依新增至佇列的順序取得重要區段。 但是，如果以速度夠快的速度將執行緒新增至此佇列，效能可能會因為將每個等候執行緒所需的時間而下降。

此處理程式負責配置重要區段所使用的記憶體。 一般來說，只要宣告類型 **重要 \_ 區段** 的變數就可以完成這項工作。 在進程的執行緒可以使用它之前，請先使用 [**InitializeCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsection) 或 [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) 函數來初始化重要區段。

執行緒使用 [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) 或 [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) 函數來要求重要區段的擁有權。 它會使用 [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) 函式來釋放重要區段的擁有權。 如果重要區段物件目前是由另一個執行緒所擁有， **EnterCriticalSection** 會無限期等候擁有權。 相反地，當 mutex 物件用於相互排除時， [等候](wait-functions.md) 函式會接受指定的逾時間隔。 **TryEnterCriticalSection** 函式會嘗試進入重要區段，而不會封鎖呼叫執行緒。

當執行緒擁有重要區段時，它可以對 [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) 或 [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) 進行額外的呼叫，而不會封鎖它的執行。 這可防止在等候已擁有的重要區段時，死結本身的執行緒。 若要釋放其擁有權，執行緒必須在每次進入重要區段時呼叫 [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) 一次。 等待中的執行緒取得重要區段擁有權的順序並不會有任何保證。

執行緒使用 [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) 或 [**SetCriticalSectionSpinCount**](/windows/win32/api/synchapi/nf-synchapi-setcriticalsectionspincount) 函數來指定重要區段物件的微調計數。 旋轉表示當執行緒嘗試取得已鎖定的重要區段時，執行緒會進入迴圈、檢查鎖定是否已釋放，如果未釋放鎖定，執行緒就會進入睡眠狀態。 在單處理器系統上，會忽略微調計數，並將關鍵區段微調計數設為 0 (零) 。 在多處理器系統上，如果重要區段無法使用，呼叫執行緒會在與重要區段相關聯的信號上執行等候作業之前，先旋轉 *dwSpinCount* 時間。 如果重要區段在微調作業期間變成可用，則呼叫執行緒會避免等候作業。

進程的任何執行緒都可以使用 [**DeleteCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection) 函式來釋放在初始化重要區段物件時所配置的系統資源。 呼叫此函式之後，無法使用重要區段物件進行同步處理。

當重要區段物件擁有時，唯一受影響的其他執行緒是在 [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection)呼叫中等候擁有權的執行緒。 未等候的執行緒可以繼續執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Mutex 物件](mutex-objects.md)
</dt> <dt>

[使用重要區段物件](using-critical-section-objects.md)
</dt> </dl>

 

 
