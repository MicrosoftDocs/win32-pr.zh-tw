---
title: Single-Threaded 單元
description: Single-Threaded 單元
ms.assetid: 2f345ae2-8314-4067-a6d6-5a0275941ed4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f9b969a48fd83ac82307c42bf4e801168bcf97f83536045fc078b19e3eb77d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129820"
---
# <a name="single-threaded-apartments"></a>Single-Threaded 單元

使用單一執行緒的單元 (單元模型進程) 提供以訊息為基礎的範例，可處理多個同時執行的物件。 它可讓您藉由允許執行緒來撰寫更有效率的程式碼，同時等待一些耗時的作業完成，以允許執行另一個執行緒。

進程中的每個執行緒都會初始化為「單元模型」處理常式，並可抓取和分派視窗訊息，是單一執行緒的單元執行緒。 每個執行緒都存在於自己的單元中。 在一個單元中，介面指標可在不封送處理的情況下傳遞，因此一個單一執行緒的單元執行緒中的所有物件都會直接進行通訊。

所有在相同執行緒上執行，因此必須有同步執行的相關物件的邏輯群組，可以存留在相同的單一執行緒的單元執行緒上。 但是，一個單元模型物件不能位於一個以上的執行緒上。 呼叫其他執行緒中的物件時，必須在主控執行緒的內容中進行，讓分散式 COM 在您于 proxy 上呼叫時，自動為您切換執行緒。

進程間和 interthread 模型很類似。 當您需要將介面指標傳遞至另一個執行緒上另一個執行緒中的物件時，) 在相同進程中的另一個執行緒上 (，您會使用不同進程中的物件用來跨進程界限傳遞指標的相同封送處理模型。 藉由取得標準封送處理物件的指標，您可以在各) 單元之間的執行緒界限之間進行介面指標的封送處理 (的方式，與處理常式之間的方式相同。 在單元之間傳遞時，必須封送處理 (介面指標。 ) 

單一執行緒單元的規則很簡單，但請務必小心遵循：

-   每個物件都應該只存留于單一執行緒的單元) 內的一個執行緒 (。
-   初始化每個執行緒的 COM 程式庫。
-   在單元之間傳遞物件的所有指標封送處理。
-   每個單一執行緒的單元都必須有訊息迴圈，才能處理來自相同進程中其他進程和單元的呼叫。 沒有物件的單一執行緒單元 (用戶端僅) 也需要訊息迴圈，以分派某些應用程式所使用的廣播訊息。
-   以 DLL 為基礎或同進程物件不會呼叫 COM 初始化函數;相反地，他們會在登錄中的 [InprocServer32](inprocserver32.md)機碼下，使用 **>threadingmodel** 的名稱-value 來註冊其執行緒模型。 可感知單元的物件也必須小心地寫入 DLL 進入點。 有一些特殊考慮適用于執行緒內含式伺服器。 如需詳細資訊，請參閱同 [進程伺服器執行緒問題](in-process-server-threading-issues.md)。

雖然多個物件可以存留在單一線程上，但是沒有任何單元模型物件可以存留在一個以上的執行緒上。

用戶端進程或跨進程伺服器的每個執行緒都必須呼叫 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize)，或呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 並指定 \_ *dwCoInit* 參數的 COINIT APARTMENTTHREADED。 主單元是先呼叫 **CoInitializeEx** 的執行緒。 如需同進程伺服器的資訊，請參閱同 [進程伺服器執行緒問題](in-process-server-threading-issues.md)。

對物件的所有呼叫都必須在其) 的執行緒 (中進行。 禁止直接從另一個執行緒呼叫物件;以這種無線程方式使用物件，可能會導致應用程式發生問題。 這項規則的含意是，物件的所有指標都必須在單元之間傳遞時進行封送處理。 COM 針對此目的提供下列兩個函數：

-   [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) 會將介面封送處理至傳回給呼叫端的資料流程物件。
-   [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) 會從資料流程物件拆收介面指標，並加以釋放。

這些函式會將呼叫包裝至 [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) 和 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) 函式，這需要使用 MSHCTX \_ INPROC 旗標。

一般而言，封送處理是由 COM 自動完成。 例如，當將介面指標做為方法呼叫中的參數傳遞至另一個單元中的物件時，或在呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)時，COM 會自動進行封送處理。 不過，在某些特殊情況下，如果應用程式寫入器在不同的單元之間傳遞介面指標，而不使用一般的 COM 機制，則寫入器必須手動處理封送處理。

如果一個處理常式中的一個單元 (的) 有介面指標，而另一個單元 (的單元 2) 需要使用，則必須呼叫 [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) 來封送處理介面。 此函式所建立的資料流程為安全線程，而且必須儲存在可由單元2存取的變數中。 單元2必須將此資料流程傳遞至 [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) 以 unmarshal 介面，並且會取得 proxy 的指標，讓它可以存取介面。 主要的單元必須保持運作，直到用戶端完成所有的 COM 工作 (，因為部分內含式物件會載入到主單元中，如) 的 [進程伺服器執行緒問題](in-process-server-threading-issues.md) 中所述。 以這種方式線上程之間傳遞一個物件之後，就很容易將介面指標當作參數傳遞。 如此一來，分散式 COM 會對應用程式進行封送處理和執行緒切換。

若要處理相同進程中其他進程和單元的呼叫，每個單一執行緒的單元都必須有訊息迴圈。 這表示執行緒的工作函式必須有 GetMessage/DispatchMessage 迴圈。 如果有其他同步處理原始物件是用來線上程之間進行通訊， [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) 函數可以用來等候訊息和執行緒同步處理事件。 此函式的檔有這類組合迴圈的範例。

COM 會使用每個單一執行緒單元中的 Windows 類別 "OleMainThreadWndClass" 來建立隱藏視窗。 對物件的呼叫會以視窗訊息的形式接收到此隱藏視窗。 當物件的單元抓取並分派訊息時，隱藏的視窗就會收到訊息。 視窗程式接著會呼叫物件的對應介面方法。

當有多個用戶端呼叫物件時，呼叫會排入訊息佇列中，而物件會在每次其單元抓取和分派訊息時接收呼叫。 由於呼叫是由 COM 進行同步處理，而且呼叫一律由屬於物件之單元的執行緒傳遞，所以物件的介面執行不需要提供同步處理。 單一執行緒單元可以執行 [**imessagefilter.prefiltermessage**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) ，以允許它們在必要時取消呼叫或接收視窗訊息。

如果物件的其中一個介面方法實重新輸入抓取並分派訊息，或對另一個執行緒進行 ORPC 呼叫，而導致相同的單元) 將另一個呼叫傳遞給物件 (，則物件可以是的。 OLE 不會防止在相同執行緒上重新進入，但有助於提供執行緒安全性。 這與視窗程式在處理訊息時，可以重新輸入並分派訊息的方式相同。 但是，呼叫跨進程的單一執行緒單元伺服器（呼叫另一個單一執行緒的單元伺服器）將允許重新輸入第一部伺服器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[跨單元存取介面](accessing-interfaces-across-apartments.md)
</dt> <dt>

[選擇執行緒模型](choosing-the-threading-model.md)
</dt> <dt>

[多執行緒單元](multithreaded-apartments.md)
</dt> <dt>

[同進程伺服器執行緒問題](in-process-server-threading-issues.md)
</dt> <dt>

[進程、執行緒和單元](processes--threads--and-apartments.md)
</dt> <dt>

[單一執行緒和多執行緒通訊](single-threaded-and-multithreaded-communication.md)
</dt> </dl>

 

 