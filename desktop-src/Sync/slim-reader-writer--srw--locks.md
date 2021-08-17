---
description: 超薄的讀取器/寫入器 (SRW) 鎖定可讓單一進程的執行緒存取共用資源;它們已針對速度進行優化，且佔用極少的記憶體。
ms.assetid: 2d439b21-291f-4ff0-910a-c1c27e800019
title: 超薄的讀取器/寫入器 (SRW) 鎖定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc478d5f9bbfec1268f65b3e4a7f562b9bdca3d2df21f4570a52782eec9f028
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959978"
---
# <a name="slim-readerwriter-srw-locks"></a>超薄的讀取器/寫入器 (SRW) 鎖定

超薄的讀取器/寫入器 (SRW) 鎖定可讓單一進程的執行緒存取共用資源;它們已針對速度進行優化，且佔用極少的記憶體。 超薄讀取器-寫入器鎖定無法跨進程共用。

讀取器執行緒會從共用資源讀取資料，而寫入器執行緒會將資料寫入至共用資源。 使用共用資源讀取和寫入多個執行緒時，如果讀取器執行緒持續執行，但很罕見的寫入作業，則專有鎖定（例如重要區段或 mutex）可能會成為瓶頸。

SRW 鎖定提供兩種模式，可讓執行緒存取共用資源：

-   **共用模式**，可授與對多個讀取器執行緒的共用唯讀存取權，讓他們能夠同時從共用資源讀取資料。 如果讀取作業超過寫入作業，則相較于重要區段，此平行存取會增加效能和輸送量。
    > [!NOTE]
    > 共用模式 SRW 鎖定不應以遞迴方式取得，因為這可能會在結合獨佔取得時導致鎖死。

-   **獨佔模式**，一次將讀取/寫入存取權授與一個寫入器執行緒。 在獨佔模式中取得鎖定時，在寫入器釋放鎖定之前，沒有其他執行緒可以存取共用資源。
    > [!NOTE]
    > 獨佔模式 SRW 鎖定無法以遞迴方式取得。 如果執行緒嘗試取得已保存的鎖定，則在 [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)的 [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)) 或鎖死 (的嘗試將會失敗 () 

可以在任一模式中取得單一 SRW 鎖定;讀取器執行緒可以在共用模式中取得，而寫入器執行緒可以在獨佔模式中取得它。 不保證要求擁有權的執行緒會被授與擁有權的順序;SRW 鎖定既不公平也不是 FIFO。

SRW 鎖定是指標的大小。 優點是更新鎖定狀態的速度很快。 缺點是可以儲存非常少的狀態資訊，因此 SRW 鎖定不會在共用模式中偵測到不正確的遞迴用途。 此外，在共用模式中擁有 SRW 鎖定的執行緒無法將鎖定的擁有權升級為獨佔模式。

呼叫端必須配置 SRWLOCK 結構，並將它初始化，方法是呼叫 [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock) (，以動態方式初始化結構) 或將常數 **SRWLOCK \_ INIT** 指派給結構變數 (以靜態方式初始化結構) 。

您可以使用 [應用程式驗證器](/windows-hardware/drivers/devtest/application-verifier) 來尋找遞迴 (可重新進入的) 使用 SRW 鎖定。

以下是 SRW 鎖定函數。

| SRW lock 函數                                                | 描述                                                                                                                                       |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)       | 取得獨佔模式的 SRW 鎖定。                                                                                                           |
| [**AcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockshared)             | 取得共用模式中的 SRW 鎖定。                                                                                                              |
| [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock)                   | 初始化 SRW 鎖定。                                                                                                                           |
| [**ReleaseSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockexclusive)       | 釋放以獨佔模式開啟的 SRW 鎖定。                                                                                           |
| [**ReleaseSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockshared)             | 釋放以共用模式開啟的 SRW 鎖定。                                                                                              |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)   | 在指定的條件變數上進入睡眠狀態，並以不可部分完成的作業形式釋放指定的鎖定。                                                |
| [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive) | 嘗試取得超薄的讀取器/寫入器 (在獨佔模式中 SRW) 鎖定。 如果呼叫成功，呼叫的執行緒就會取得鎖定的擁有權。 |
| [**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)       | 嘗試取得輕巧的讀取器/寫入器 (在共用模式中 SRW) 鎖定。 如果呼叫成功，呼叫的執行緒就會取得鎖定的擁有權。    |

 
