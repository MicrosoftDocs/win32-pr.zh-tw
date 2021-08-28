---
title: In-Process 伺服器執行緒問題
description: In-Process 伺服器執行緒問題
ms.assetid: 7bd6f62f-8c91-44bd-9a7f-d47988180eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50239af2c0e254f8ccead8065573df2e3ece39540bbdf8e5a205fe33dfe4f956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567858"
---
# <a name="in-process-server-threading-issues"></a>In-Process 伺服器執行緒問題

同進程伺服器不會呼叫 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize)、 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)或 [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) 來標記其執行緒模型。 針對執行緒感知 DLL 型或同進程物件，您必須在登錄中設定執行緒模型。 當您未指定執行緒模型時，預設模型為單一執行緒的每個進程。 若要指定模型，請將 **>threadingmodel** 值新增至登錄中的 [InprocServer32](inprocserver32.md) 索引鍵。

支援類別物件具現化的 Dll 必須執行和匯出函式 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 和 [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)。 當用戶端想要 DLL 支援的類別實例時，直接呼叫 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (或透過呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) 會呼叫 **DllGetClassObject** ，在 DLL 中實作為物件的類別物件時取得指標。 因此， **DllGetClassObject** 應該可以提供多個類別物件或單一安全線程物件 (基本上只是 [](/windows/win32/api/winnt/nf-winnt-interlockedincrement) / 在其內部參考計數) 上使用 InterlockedIncrement [**InterlockedDecrement**](/windows/desktop/api/winbase/nf-winbase-interlockeddecrement) 。

顧名思義，會呼叫 [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow) 來判斷執行它的 DLL 是否正在使用中，如果不是，則可讓呼叫者安全地卸載它。 從任何執行緒呼叫 [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) 一律會路由到主要的單元執行緒，以呼叫 **DllCanUnloadNow**。

就像其他伺服器一樣，同進程伺服器也可以是單一執行緒、跨執行緒或無限制執行緒。 無論該用戶端使用的執行緒模型為何，這些伺服器都可以由任何 OLE 用戶端使用。

用戶端與同進程物件之間允許所有線程模型互通性的組合。 用戶端與使用不同執行緒模型的同進程物件之間的互動，與用戶端與跨進程伺服器之間的互動完全一樣。 針對同進程伺服器，當用戶端和同進程伺服器的執行緒模型不同時，COM 必須在用戶端與物件之間 interpose 本身。

當用戶端的多個執行緒同時呼叫支援單一執行緒模型的同進程物件時，COM 無法允許用戶端執行緒直接存取物件的 interfaceâ€「物件不是針對這類存取而設計。 相反地，COM 必須確保呼叫會進行同步處理，而且只由建立物件的用戶端執行緒進行。 因此，COM 會在用戶端的主單元中建立物件，並要求所有其他用戶端單元使用 proxy 來存取該物件。

當在用戶端中) 的自由執行緒單元 (多執行緒單元模型時，會在用戶端中建立一個執行緒的單元模型「主機」執行緒。 這個主控制項執行緒會建立物件，並將介面指標封送處理回用戶端的自由執行緒單元。 同樣地，當單元模型用戶端中的單一執行緒單元建立無限制執行緒的同進程伺服器時，COM 會將自由執行緒的主執行緒 (在建立物件的多執行緒單元上，然後再封送處理回用戶端單一執行緒的單元) 。

> [!Note]  
> 一般而言，如果您在同進程伺服器上設計自訂介面，您也應該為它提供封送處理常式代碼，讓 COM 可以封送處理用戶端單元之間的介面。

 

COM 會要求從其建立所在的相同用戶端單元存取，以協助保護對單一執行緒 DLL 所提供物件的存取。 此外，所有的 DLL 進入點 (例如 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 和 [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)) ，而全域資料應該一律由相同的單元存取。 COM 會在用戶端的主要單元中建立這類物件，讓主單元直接存取物件的指標。 來自其他單元的呼叫會使用 interthread 封送處理，從 proxy 移至主要單元中的存根，然後到物件。 這可讓 COM 同步處理對物件的呼叫。 Interthread 呼叫的速度很慢，因此建議您重新撰寫這些伺服器，以支援多個單元。

就像單一執行緒的同進程伺服器一樣，由單元模型 DLL 所提供的物件，必須由其建立所在的相同用戶端單元來存取。 不過，此伺服器提供的物件可以在用戶端的多個單元中建立，因此伺服器必須執行其進入點 (例如 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 和 [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)) ，以便進行多執行緒的使用。 例如，如果用戶端的兩個單元嘗試同時建立同進程物件的兩個實例，則這兩個單元都可以同時呼叫 **DllGetClassObject** 。 必須撰寫 **DllCanUnloadNow** ，以便在程式碼仍在 dll 中執行時，dll 不會卸載。

如果 DLL 只提供一個 class factory 實例來建立所有物件，則類別 factory 的執行也必須設計為多執行緒使用，因為它將會由多個用戶端單元存取。 如果 DLL 在每次呼叫 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 時，都會建立 class factory 的新實例，則 class factory 不需要是安全線程。

Class factory 所建立的物件不需要是安全線程。 一旦執行緒建立之後，一律會透過該執行緒存取物件，並由 COM 來同步處理對物件的所有呼叫。 建立此物件之用戶端的單元模型單元將會取得物件的直接指標。 不同于建立物件之單元的用戶端單元必須透過 proxy 存取物件。 當用戶端在其單元之間封送處理介面時，就會建立這些 proxy。

當同進程 DLL **>threadingmodel** 值設定為 "Both" 時，就可以在單一執行緒或多執行緒用戶端單元中，直接建立並使用這個 DLL 提供的物件 (而不需要 proxy) 。 不過，它只能在建立它的單元內直接使用。 若要將物件提供給任何其他的單元，必須封送處理物件。 DLL 物件必須執行它自己的同步處理，而且可以同時由多個用戶端單元存取。

為了加速可自由執行緒存取同進程 DLL 物件的效能，COM 提供 [**CoCreateFreeThreadedMarshaler**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) 函數。 這個函式會建立一個無限制執行緒封送處理物件，此物件可以使用同進程伺服器物件進行匯總。 當同一進程中的用戶端需要存取另一個單元中的物件時，匯總無限制執行緒封送處理器會提供用戶端直接指標給用戶端，而不是 proxy，當用戶端將物件的介面封送處理至不同的單元時。 用戶端不需要執行任何同步處理。 這僅適用于相同的進程;標準封送處理是用於傳送至另一個進程之物件的參考。

僅支援無線程執行緒的同進程 DLL 所提供的物件是無限制執行緒的物件。 它會執行它自己的同步處理，並可同時由多個用戶端執行緒存取。 此伺服器不會線上程之間封送處理介面，因此可以直接建立和使用此伺服器 (而不需要 proxy) 用戶端中的多執行緒單元。 建立它的單一執行緒單元會透過 proxy 來存取它。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[跨單元存取介面](accessing-interfaces-across-apartments.md)
</dt> <dt>

[選擇執行緒模型](choosing-the-threading-model.md)
</dt> <dt>

[多執行緒單元](multithreaded-apartments.md)
</dt> <dt>

[進程、執行緒和單元](processes--threads--and-apartments.md)
</dt> <dt>

[單一執行緒和多執行緒通訊](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[單一執行緒單元](single-threaded-apartments.md)
</dt> </dl>

 

 