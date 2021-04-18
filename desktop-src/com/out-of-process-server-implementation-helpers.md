---
title: 跨進程伺服器執行協助程式
description: 跨進程伺服器執行協助程式
ms.assetid: 18641a84-56f8-4d27-9ddb-fa64011ac8ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 264d3f26b179b3ecb659ef93785c8c223b6c524e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382974"
---
# <a name="out-of-process-server-implementation-helpers"></a>跨進程伺服器執行協助程式

有四個可由跨進程伺服器呼叫的 helper 函式，可簡化撰寫伺服器程式碼的作業。 COM 用戶端和 COM 同進程伺服器通常不會呼叫它們。 這些函式的設計目的是在伺服器有多個單元或多個類別物件時，協助防止伺服器啟用中的競爭條件。 不過，它們也可以輕易用於單一執行緒和單一類別的物件服務器。 這些函數如下所示：

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess)
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)
-   [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects)
-   [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects)

若要正常關閉，COM 伺服器必須追蹤它已具現化的物件實例數目，以及已呼叫 [**IClassFactory：： LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) 方法的次數。 只有在這兩個計數都達到零時，伺服器才會關閉。 在單一執行緒的 COM 伺服器中，要關閉的決策是與由訊息佇列所序列化的傳入啟用要求協調。 伺服器在收到最後一個物件實例上的版本，並決定關閉時，會先撤銷其類別物件，再分派任何更多的啟用要求。 如果在此時間點之後發生啟用要求，COM 會辨識出類別物件已遭撤銷，而且會將錯誤傳回至服務控制管理員 (SCM) ，這樣會導致執行新的本機伺服器進程實例。

不過，在有不同類別物件在不同的單元上註冊的單元模型伺服器中，以及所有無限制執行緒的伺服器中，這項關閉決策必須與跨多個執行緒的啟動要求協調，如此一來，當伺服器的另一部執行緒忙於處理類別物件或物件實例時，伺服器的一個執行緒就不會決定要關閉。 解決這個情況的一個傳統但繁瑣的方法，就是讓伺服器在它撤銷其類別物件之後，重新檢查其實例計數並保持運作，直到所有實例都已釋放為止。

為了讓伺服器寫入器更容易處理這些類型的競爭情形，COM 提供兩個參考計數函數：

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) 會遞增全域每一進程的參考計數。
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) 會遞減全域每一進程的參考計數。

當全域每一進程的參考計數達到零時，COM 會自動呼叫 [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects)，以防止任何新的啟用要求進入。 然後伺服器就可以在休閒的不同執行緒中取消註冊其各種類別物件，而不需要擔心有可能出現另一個啟用要求。 所有新的啟用要求都是由 SCM 處理的因而需要，會啟動本機伺服器進程的新實例。

若要讓本機伺服器應用程式使用這些函式，最簡單的方式就是在每個實例物件的函式中呼叫 [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) ，並在 *FLock* 參數為 **TRUE** 時，于其每個 [**IClassFactory：： LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver)方法中呼叫。 當 *fLock* 參數為 **FALSE** 時，伺服器應用程式也應該在其每一個實例物件和其每個 IClassFactory：：**LockServer** 方法的函式中呼叫 [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) 。

最後，伺服器應用程式應該注意來自 [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)的傳回碼，如果它傳回0，則伺服器應用程式應該起始其清除，這對於具有多個執行緒的伺服器而言，通常表示它應該指示其各種執行緒結束其訊息迴圈，並呼叫 [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) 和 [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)。 如果使用伺服器進程存留期管理函式，則必須在物件實例和 [**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) 方法中使用這些函數;否則，可能會提前關閉伺服器應用程式。

提出 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 要求時，COM 會與伺服器連線、封送處理類別物件的 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面、傳回用戶端進程、拆收 **IClassFactory** 介面，然後將其傳回給用戶端。 此時，用戶端通常會以 **TRUE** 呼叫 [**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) ，以防止伺服器進程關機。 不過，在封送處理類別物件時，以及當用戶端呼叫 **LockServer** 時，如果另一個用戶端可以連接到同一部伺服器、取得實例，然後釋放該實例，則會導致伺服器關機，並讓第一個用戶端保持在中斷連線的 **IClassFactory** 指標上。 為了避免發生這種競爭情形，COM 會將對 **LockServer** 的隱含呼叫加入至類別物件（當它封 **送處理** **IClassFactory** 介面時），並在用戶端釋出 **IClassFactory** 介面時，將 **LockServer** 的隱含呼叫設為 **FALSE** 。 因此，不需要對伺服器進行遠端 **LockServer** 回呼，而 **LockServer** 的 proxy 只會在 \_ 沒有實際遠端呼叫的情況下傳回 S。

初始化跨進程伺服器進程時，有另一個啟用相關的競爭情形。 註冊多個類別的 COM 伺服器，通常[](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) \_ \_ 會針對它所支援的每個 CLSID 呼叫 CoRegisterClassObject with REGCLS 本機伺服器。 針對所有類別完成此操作之後，伺服器會進入其訊息迴圈。 針對單一執行緒的 COM 伺服器，所有啟動要求都會遭到封鎖，直到伺服器進入訊息迴圈為止。 但是，如果是在不同的單元中註冊不同類別物件的部門模型伺服器，以及所有無限制執行緒的伺服器，則啟動要求可能會比這個更早抵達。 在公寓模型伺服器的案例中，只要有任何一個執行緒進入其訊息迴圈，就可以立即到達啟用要求。 在無限制執行緒伺服器的情況下，啟用要求會在第一個類別物件註冊之後立即抵達。 由於啟動可能會提早發生，因此最終版本也可能會發生 (，因此在伺服器的其餘部分有機會完成初始化之前，伺服器會開始關機) 。

若要排除這些競爭情形並簡化伺服器寫入器的工作，任何想要向 COM 註冊多個類別物件的伺服器，都應該呼叫 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) ，並 \_ \_ \| \_ 針對伺服器支援的每個不同 CLSID 來呼叫 REGCLS 本機伺服器 REGCLS。 在所有類別都註冊完成，而且伺服器進程準備好接受傳入的啟用要求之後，伺服器應該呼叫 [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects)。 此函式會告知 COM 將所有已註冊的類別告知 SCM，並開始讓啟動要求進入伺服器進程。 使用這些函數可提供下列優點：

-   無論有多少個 Clsid 註冊，都只會對 SCM 進行一次呼叫，藉此減少整體的註冊時間 (以及伺服器應用程式) 的啟動時間。
-   如果伺服器有多個公寓和不同的 Clsid 在不同的單元中註冊，或如果伺服器是無限制執行緒的伺服器，則在伺服器呼叫 [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects)之前，將不會出現任何啟動要求，讓伺服器有機會註冊其所有 clsid，並在必須處理啟動要求和可能關機要求之前，先進行適當的設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 伺服器責任](com-server-responsibilities.md)
</dt> </dl>

 

 