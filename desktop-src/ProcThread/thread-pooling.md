---
description: 有許多應用程式會建立執行緒，以在睡眠狀態下花費大量時間等待事件發生。
ms.assetid: a5e52080-35d4-47f5-9050-90889e3bf2f8
title: 執行緒共用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c581e416952e6bac14dbf12a8f87202925a5254879b7e220c7cb2d780699f9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081278"
---
# <a name="thread-pooling"></a>執行緒共用

有許多應用程式會建立執行緒，以在睡眠狀態下花費大量時間等待事件發生。 其他執行緒可能只會進入睡眠狀態，才能定期進行喚醒以輪詢變更或更新狀態資訊。 *執行緒* 共用可讓您的應用程式使用由系統管理的背景工作執行緒集區，讓您更有效率地使用執行緒。 至少有一個執行緒會監視佇列到執行緒集區的所有等候作業的狀態。 等候作業完成時，執行緒集區中的背景工作執行緒會執行對應的回呼函數。

本主題說明原始執行緒集區 API。 Windows Vista 中引進的執行緒集區 API 更簡單、更可靠、具有更佳的效能，並為開發人員提供更大的彈性。 如需目前線程集區 API 的詳細資訊，請參閱 [執行緒](thread-pools.md)集區。

您也可以將與等待作業無關的工作專案加入執行緒集區。 若要要求執行緒集區中的執行緒工作專案，請呼叫 [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) 函數。 此函式會將參數提供給從執行緒集區選取的執行緒所呼叫的函式。 在工作專案排入佇列之後，沒有任何方法可以取消。

[計時器-佇列計時器](../sync/timer-queues.md) 和 [已註冊的等候作業](../sync/wait-functions.md) 也會使用執行緒集區。 其回呼函式會排入執行緒集區佇列中。 您也可以使用 [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback) 函式來張貼非同步 i/o 作業。 當 i/o 完成時，回呼會由執行緒集區執行緒執行。

當您第一次呼叫 [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) 或 [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)，或當計時器佇列計時器或已註冊的等候作業將回呼函數排入佇列時，就會建立執行緒集區。 根據預設，可以線上程集區中建立的執行緒數目大約是500。 每個執行緒都會使用預設堆疊大小，並以預設優先權執行。

執行緒集區中有兩種類型的背景工作執行緒： i/o 和非 i/o。 *I/o 工作者執行緒* 是以可提供警示等候狀態等候的執行緒。 工作專案會以非同步程序呼叫的形式排入 i/o 背景工作執行緒， (APC) 。 如果工作專案應該在等待可提供警示狀態的執行緒中執行，您應該將工作專案排入佇列，以將它排入 i/o 工作者執行緒。

*非 i/o 背景工作執行緒* 等候 i/o 完成埠。 使用非 i/o 背景工作執行緒比使用 i/o 背景工作執行緒更有效率。 因此，您應該盡可能使用非 i/o 背景工作執行緒。 如果有暫止的非同步 i/o 要求，i/o 和非 i/o 背景工作執行緒都會結束。 起始非同步 i/o 完成要求的工作專案可使用這兩種類型的執行緒。 但是，如果可能需要很長的時間才能完成，請避免將非同步 i/o 完成要求張貼在非 i/o 工作者執行緒中。

若要使用執行緒共用，工作專案及其呼叫的所有函式都必須是執行緒集區安全的。 Safe 函式不會假設執行它的執行緒是專用或持續性的執行緒。 一般而言，您應該避免使用 [執行緒區域儲存區](thread-local-storage.md) ，或是進行需要持續性執行緒的非同步呼叫，例如 [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) 函式。 不過，您可以在專用的執行緒上呼叫這類函式， (由應用程式建立) 或使用 [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) 搭配 wt. EXECUTEINPERSISTENTTHREAD 選項) 來排入持續性背景工作執行緒 (\_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[可提供警示 i/o](../fileio/alertable-i-o.md)
</dt> <dt>

[非同步程序呼叫](../sync/asynchronous-procedure-calls.md)
</dt> <dt>

[I/o 完成埠](../fileio/i-o-completion-ports.md)
</dt> <dt>

[執行緒集區](thread-pools.md)
</dt> </dl>

 

 
