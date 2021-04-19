---
description: 您的應用程式可以使用排程的計時器或裝置事件，將處於睡眠狀態的電腦還原到工作狀態。
ms.assetid: b7326b09-0829-4e76-80d0-e4ecdf7f556e
title: 系統喚醒事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13332305ef023d932f2912f7299aa12cd402733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977906"
---
# <a name="system-wake-up-events"></a>系統喚醒事件

下列資訊適用于從 [睡眠 (S3) 和休眠 (S4) ](/windows-hardware/drivers/kernel/system-sleeping-states)喚醒。 若要從新式待命喚醒 (S0 低功率閒置) ，請參閱 [從閒置轉換為使用中的轉換](/windows-hardware/design/device-experiences/transition-from-idle-to-active)。

您的應用程式可以使用排程的計時器或裝置事件，將處於睡眠狀態的電腦還原到工作狀態。 這就是所謂的 *喚醒事件*。 使用 [可等候計時器物件](/windows/desktop/Sync/waitable-timer-objects) 來指定系統應該喚醒的時間。 若要建立物件，請使用 [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) 函數。 若要設定計時器，請使用 [**SetWaitableTimer**](/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer) 函數。 *PDueTime* 參數會指定何時將計時器發出信號。 若要指定系統應該在計時器收到信號時喚醒，請將 *fResume* 參數設定為 **TRUE**。

當系統自動喚醒時，因為 (電源交換器或使用者活動) 以外的事件，系統會自動將自動閒置計時器設定為至少2分鐘。 此計時器讓應用程式有足夠的時間呼叫 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 函式，以指出它們正在忙碌中。 這段時間可讓系統在不再需要電腦之後，快速返回睡眠狀態。 下列準則會判斷系統是否返回睡眠狀態：

-   如果系統自動喚醒 (也就是沒有任何使用者活動存在) ，它會在自動閒置計時器過期時立即關閉，假設沒有任何應用程式已呼叫 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 來表示系統是必要的。
-   以裝置為基礎的喚醒預設會觸發自動閒置計時器，除非設備磁碟機表示使用者存在。 如果驅動程式指出使用者狀態，則會使用系統閒置計時器。
-   如果系統自動喚醒，但使用者在處理事件時提供新的輸入，系統就不會根據自動閒置計時器自動返回睡眠狀態。 相反地，系統會根據系統閒置計時器返回睡眠狀態。
-   如果系統因為使用者活動而喚醒，系統不會根據自動閒置計時器自動返回睡眠狀態。 相反地，系統會根據系統閒置計時器返回睡眠狀態。

當系統自動喚醒時，會將 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 事件廣播至所有應用程式。 由於使用者不存在，大部分的應用程式都不應該執行任何動作。 事件處理應用程式（例如傳真伺服器）應該處理其事件。 若要判斷系統是否處於此狀態，請呼叫 [**IsSystemResumeAutomatic**](/windows/desktop/api/Winbase/nf-winbase-issystemresumeautomatic) 函數。 當系統自動喚醒時，不會自動開啟顯示器。

如果系統因為使用者活動而喚醒，系統會先廣播 [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) 事件，後面接著 [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) 事件。 此外，系統也會開啟顯示器。 您的應用程式應該在系統進入睡眠狀態時重新開啟已關閉的檔案，並為使用者輸入做好準備。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於電源管理](about-power-management.md)
</dt> <dt>

[系統睡眠準則](system-sleep-criteria.md)
</dt> </dl>

 

 
