---
title: 多執行緒單元
description: 多執行緒單元
ms.assetid: d3e6acd9-cd5c-4a2c-8526-4f43db3b606b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2594f9341fc662b068fb7e007e538282a31273
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106968937"
---
# <a name="multithreaded-apartments"></a>多執行緒單元

在多執行緒單元模型中，進程中已初始化為自由執行緒的所有線程都位於單一單元中。 因此，不需要線上程之間進行封送處理。 執行緒不需要取得和分派訊息，因為 COM 不會在此模型中使用視窗訊息。

呼叫多執行緒單元中的物件方法時，可以在該單元中的任何執行緒上執行。 沒有呼叫的序列化;許多呼叫可能會同時對相同的方法或相同物件進行。 在多執行緒單元中建立的物件必須能夠隨時從其他執行緒其方法的呼叫。

由於呼叫物件不會以任何方式序列化，因此多執行緒物件並行可提供最高的效能，並充分利用跨執行緒、跨進程和跨電腦呼叫的多處理器硬體。 不過，這表示物件的程式碼必須在其介面實現中提供同步處理，通常是透過使用同步處理原始物件（例如事件物件、重要區段、mutex 或信號），這會在本節稍後說明。 此外，因為物件不會控制正在存取之執行緒的存留期，所以執行緒區域儲存區) 中的物件 (不能儲存任何執行緒特定的狀態。

以下是有關多執行緒單元同步處理的一些重要考慮：

-   COM 僅提供單一執行緒單元的呼叫同步處理。
-   多執行緒單元在) 的相同執行緒上呼叫 (時，不會接收呼叫。
-   多執行緒單元無法進行輸入同步處理呼叫。
-   非同步呼叫會轉換成多執行緒單元中的同步呼叫。
-   不會針對多執行緒單元中的任何執行緒呼叫訊息篩選器。

若要將執行緒初始化為無限制執行緒，請呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)，並指定 COINIT \_ 多執行緒。 如需同進程伺服器執行緒的詳細資訊，請參閱同 [進程伺服器執行緒問題](in-process-server-threading-issues.md)。

多個用戶端可以同時從不同的執行緒呼叫支援無限制執行緒的物件。 在可自由執行緒的跨進程伺服器（COM）中，透過 RPC 子系統建立的執行緒集區會在伺服器進程中建立執行緒集區，而用戶端呼叫 (或多個用戶端呼叫，) 可以在任何時間由這些執行緒傳遞。 跨進程伺服器也必須在其 class factory 中執行同步處理。 無限制執行緒的同進程物件可以接收來自用戶端多個執行緒的直接呼叫。

用戶端可以在多個執行緒中執行 COM 工作。 所有線程都屬於相同的多執行緒單元。 介面指標會直接從執行緒傳遞至多執行緒單元內的執行緒，因此介面指標不會在其執行緒之間進行封送處理。 Imessagefilter.prefiltermessage) 的訊息篩選器 (的[](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) ，不會用於多執行緒單元。 用戶端執行緒會在對跨單元物件進行 COM 呼叫時暫停，而且會在呼叫傳回時繼續。 進程之間的呼叫仍會由 RPC 處理。

以自由執行緒模型初始化的執行緒必須執行自己的同步處理。 如本節稍早所述，Windows 會透過下列同步處理原始物件來啟用此執行：

-   事件物件提供一種方式，讓一個或多個執行緒發生事件。 進程內的任何執行緒都可以建立事件物件。 事件建立函式會傳回事件的控制碼， [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)。 一旦建立事件物件之後，具有物件控制碼的執行緒就可以等候它，然後再繼續執行。
-   重要區段適用于需要對某些共用資料進行獨佔存取才能執行的程式碼區段，而且只有在單一進程內的執行緒才能使用。 重要區段就像是一次只有一個執行緒可以通過的門，如下所示：
    -   為了確保一次不會有一個以上的執行緒存取共用資料，進程的主要執行緒會配置全域關鍵 \_ 區段資料結構，並初始化其成員。 進入重要區段的執行緒會呼叫 [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) 函數，並修改資料結構的成員。
    -   嘗試進入重要區段的執行緒會呼叫 [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) ，以查看重要 \_ 區段資料結構是否已修改。 如果是，則另一個執行緒目前位於重要區段中，後續的執行緒則會進入睡眠狀態。 離開重要區段的執行緒會呼叫 [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection)，以重設資料結構。 當執行緒離開重要區段時，系統會將其中一個休眠執行緒喚醒，然後進入重要區段。
-   Mutex 執行的功能與重要區段相同，不同之處在于在不同進程中執行的執行緒可以存取 mutex。 擁有 mutex 物件就像是在爭論的樓層。 進程會藉由呼叫 [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) 函式來建立 mutex 物件，該函式會傳回控制碼。 要求 mutex 物件的第一個執行緒取得其擁有權。 當執行緒已完成 mutex 時，擁有權會先以先服務的方式傳遞給其他執行緒。
-   信號是用來維護一些可用資源的參考計數。 執行緒會藉由呼叫 [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea) 函式並傳遞資源指標、初始資源計數和資源計數上限，來建立資源的信號。 此函數會傳回控制碼。 要求資源的執行緒會在 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) 函式的呼叫中傳遞其信號控制碼。 信號物件會輪詢資源，以判斷它是否可用。 如果是，則信號會遞減資源計數，並喚醒等候中的執行緒。 如果計數為零，則執行緒會保持睡眠，直到另一個執行緒釋出資源，導致信號將計數遞增一。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[跨單元存取介面](accessing-interfaces-across-apartments.md)
</dt> <dt>

[選擇執行緒模型](choosing-the-threading-model.md)
</dt> <dt>

[同進程伺服器執行緒問題](in-process-server-threading-issues.md)
</dt> <dt>

[進程、執行緒和單元](processes--threads--and-apartments.md)
</dt> <dt>

[單一執行緒和多執行緒通訊](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[單一執行緒單元](single-threaded-apartments.md)
</dt> </dl>

 

 