---
description: 執行緒順序服務會控制一個或多個用戶端執行緒的執行。 它可確保每個用戶端執行緒在指定的期間內以及相對循序執行一次。
ms.assetid: 5c37873a-ced4-447e-a6e1-55cfa8ab24b4
title: 執行緒順序服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b3cd12b26124b47d506585425388a4542a70df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974271"
---
# <a name="thread-ordering-service"></a>執行緒順序服務

*執行緒順序服務* 會控制一個或多個用戶端執行緒的執行。 它可確保每個用戶端執行緒在指定的期間內以及相對循序執行一次。

**Windows Server 2003 和 WINDOWS XP：** 從 Windows Vista 和 Windows Server 2008 開始，可以使用「執行緒順序」服務。

依預設，執行緒順序服務為關閉，且必須由使用者啟動。 當執行緒排序服務正在執行時，會每隔5秒啟動一次，以檢查是否有新的要求，即使系統處於閒置狀態也一樣。 這可防止系統睡眠超過5秒，導致系統耗用更多電源。 如果能源效率對應用程式而言是很重要的，最好不要使用「執行緒順序」服務，而是讓系統排程器管理執行緒的執行。

每個用戶端執行緒都屬於 *執行緒順序群組*。 *父執行緒* 藉由呼叫 [**AvRtCreateThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup)函式來建立一或多個執行緒排序群組。 父執行緒會使用這個函數來指定執行緒順序群組的期間和逾時間隔。

其他用戶端執行緒會呼叫 [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup) 函式來聯結現有的執行緒排序群組。 這些執行緒會指出其是否為執行順序中父執行緒的前置或後置。 每個用戶端執行緒預期每個期間都會完成特定數量的處理。 群組內的所有線程都應該在期間加上逾時間隔來完成其執行。

執行緒順序群組的執行緒會將其處理常式代碼括在 [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) 函式所控制的迴圈中。 首先，前置執行緒會依照其加入群組的順序，一次執行一個執行緒，而父和後續的執行緒則會在呼叫 **AvRtWaitOnThreadOrderingGroup** 時遭到封鎖。 當每個前置執行緒完成處理時，控制權會回到其處理迴圈的最上方，然後執行緒會再次呼叫 **AvRtWaitOnThreadOrderingGroup** 來封鎖，直到下一個回合為止。 在所有前置執行緒都呼叫這個函式之後，執行緒順序服務就可以排程父執行緒。 最後，當父執行緒完成其處理，並再次呼叫 **AvRtWaitOnThreadOrderingGroup** 時，執行緒順序服務可以依其加入群組的順序，一次排程一個後續執行緒。 如果所有線程在一段時間結束之前完成其執行，則所有線程都會等到句號的其餘部分經過一段時間後才會再次執行。

當用戶端不再以執行緒排列群組的一部分執行時，它會呼叫 [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup) 函式，以從群組中移除本身。 請注意，父執行緒不應從執行緒排序群組中移除本身。 如果執行緒未在期間加上逾時間隔之前完成其執行，則會從群組中刪除。

父執行緒會呼叫 [**AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup) 函數來刪除線程排序群組。 如果父執行緒未在期間加上逾時間隔之前完成其執行，則也會終結執行緒順序群組。 當執行緒排序群組終結時，從該群組之執行緒 [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) 的任何呼叫都會失敗或超時。

 

 



