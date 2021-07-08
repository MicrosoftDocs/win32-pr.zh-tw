---
description: 本文說明如何註冊和散發屬性處理常式，以便與 Windows 屬性系統搭配使用。
ms.assetid: E6E81E04-9CC1-4df5-9A87-DE0CBD177356
title: 註冊和散發屬性處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce53f0805c4db5efe38e77ba4e7d1ab5b331c83f
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481923"
---
# <a name="registering-and-distributing-property-handlers"></a>註冊和散發屬性處理常式

本主題說明如何建立和註冊屬性處理常式，以便與 Windows 的屬性系統搭配使用。

本主題的組織方式如下：

-   [註冊和散發屬性處理常式](#registering-and-distributing-property-handlers)
-   [屬性處理常式的效能和可靠性考慮](#performance-and-reliability-considerations-for-property-handlers)
    -   [效能和可靠性的指導方針](#guidelines-for-performance-and-reliability)
-   [相關主題](#related-topics)

## <a name="registering-and-distributing-property-handlers"></a>註冊和散發屬性處理常式

在執行屬性處理常式之後，它必須註冊，而且其副檔名必須與處理常式相關聯。 下列使用配方副檔名的範例說明所需的登錄專案。

```
HKEY_CLASSES_ROOT
   CLSID
      {50d9450f-2a80-4f08-93b9-2eb526477d1a}
         (Default) = Recipe Property Handler
         ManualSafeSave [REG_DWORD] = 00000001
         InProcServer32
            (Default) = C:\\SDK\\PropertyHandlerSample\\bin\\RecipeHandlers.dll
            ThreadingModel = Apartment
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     .recipe
                        (Default) = {50d9450f-2a80-4f08-93b9-2eb526477d1a}
```

特定檔案類型的屬性處理常式通常會與應用程式 () ，以建立或操作該類型的檔案。 不過，您也應該考慮讓您的屬性處理常式可獨立于這些應用程式中使用，以支援在伺服器案例中，索引子會使用屬性處理常式來編制檔案類型的索引，但不需要這些應用程式的隨附應用程式。 如果您為屬性處理常式建立獨立的安裝套件，請確定它包含下列各項：

-   在 [註冊和散發屬性處理常式]()的主題中指定的屬性處理常式註冊詳細資料。
-   註冊您的檔案類型以及任何必須安裝的架構檔案，以便讓用戶端存取屬性處理常式的所有功能。

## <a name="performance-and-reliability-considerations-for-property-handlers"></a>屬性處理常式的效能和可靠性考慮

系統會針對特定電腦上的每個檔案叫用屬性處理常式。 通常會在下列情況下呼叫它們：

-   在編制檔案的索引期間。 這是跨進程完成，在具有限制許可權的隔離進程中。
-   在 Windows 檔案總管中存取檔案的目的是為了讀取和寫入屬性值。 這是在同進程中完成。

### <a name="guidelines-for-performance-and-reliability"></a>效能和可靠性的指導方針

使用者在任何時候都可能有數十個特定類型的檔案 (包括您在電腦上) ，而且隨時都可以存取或修改任何或所有檔案。 因為通常會叫用屬性處理常式來支援這些存取和修改作業，所以您的屬性處理常式的效能和可靠性特性在忙碌中，高度並行的環境相當重要。

當您開發和測試屬性處理常式時，請記住下列指導方針。

-   **屬性列舉**

    在列舉屬性時，屬性處理常式應該會有非常快速的回應時間。 應避免對屬性值、網路查閱或搜尋資源以外的資源進行記憶體密集的計算，以確保回應時間快速。

-   **就地寫入屬性**

    如果可能的話，處理中型或大型檔案 (數百 KB 或更大的) 時，應排列檔案格式，以便讀取或寫入屬性值，而不需要從磁片讀取整個檔案。 即使需要搜尋檔案，也不應該將它完整讀入記憶體，因為這樣會還更膨脹 Windows 檔案總管的工作集或 Windows Search 索引子，因為它們會嘗試存取或為這些檔案編制索引。 如需詳細資訊，請參閱 [初始化屬性處理常式](./building-property-handlers-property-handlers.md)。

    完成這項工作的一項實用技巧是以額外的空間填補檔案的標頭，如此一來，下次需要寫入屬性值時，就可以就地寫入該值，而不需要重寫整個檔案。 這需要 ManualSafeSave 功能。 這種方法需要額外的風險，因為寫入進行中時可能會中斷檔案寫入作業 (因為) 的系統損毀或電源中斷，但由於屬性大小通常很小，因此這類中斷的機率也相當小，而且可透過就地屬性寫入來實現的效能提升，會被視為足以證明這項額外的風險。 即便如此，您也應該小心測試您的實作，以確保在寫入作業期間發生失敗時，您的檔案不會損毀。

    最後，當您執行以 ManualSafeSave 撰寫的就地屬性時，有時無法就地執行作業，而且必須改為重寫整個資料流程。 為了方便重寫，處理常式初始化期間提供的資料流程支援 [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) 介面。 **IDestinationStreamFactory** 介面讓處理常式得以取得要寫入的暫存資料流程;當所有寫入都已完成並呼叫 [**IDestinationStreamFactory：： GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream)方法時，此資料流程會用來完全取代原始檔案資料流程。 使用目的資料流程時，原始檔案資料流程應視為唯讀，因為它會在呼叫 **IDestinationStreamFactory：： GetDestinationStream** 方法之後，由目的地資料流程取代。

-   **選擇您的 COM 執行緒模型**

    若要最大化您的屬性處理常式效率，您應該指定它使用 COM 執行緒模型 `Both` 。 這可讓您直接從 STA 公寓 (Windows 檔案總管存取，例如) 和郵件傳輸代理程式 (MTA) 單元 (Windows Search 中的 SearchProtocolHost 程式，例如) ，避免在這些環境中進行封送處理的額外負荷。 若要達成執行緒模型的完整優點 `Both` ，您的處理常式所相依的任何服務都應該也指定為， `Both` 以避免呼叫這些元件時進行任何封送處理。 請查看這些特定服務的檔，確認它們是否使用此執行緒模型。

-   **屬性處理常式並行**

    屬性處理常式和 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面是針對序列而非平行存取所設計。 WindowsExplorer、Windows Search 索引子和 Windows 程式碼基底中的所有其他屬性處理常式叫用都能保證此使用方式。 協力廠商不應該同時使用屬性處理常式，但無法保證此行為。 此外，即使呼叫模式必須是序列，呼叫也可能會在不同的執行緒 (例如，當透過 COM RPC 從遠端呼叫物件時，會發生在索引子) 中。 因此，屬性處理常式的執行必須支援在不同的執行緒上呼叫，而在此情況下，如果同時呼叫，則應該不會影響任何不良的效果 因為預定的呼叫模式是序列，所以使用重要區段的簡單執行應該足以滿足大部分情況下的這些需求。 您可以使用 [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) 函式偵測和失敗並行呼叫，以避免封鎖並行呼叫。

-   **檔案並行**

    屬性處理常式通常用於多個應用程式同時存取檔案的案例中。 因此，處理常式和應用程式需要在開啟檔案時指定適當的共用模式來管理並行。 他們也必須留意其他應用程式所指定的存取權，以及管理不允許存取的情況。 如果所有取用者都指定了適當的共用模式，讓其他人能夠同時存取該檔案，但在這麼做時，必須管理一致性問題。 若要使用最適當的共用模式，必須在存取檔案的應用程式之應用程式的內容中進行決策。

    檔案系統可讓應用程式以一種方式開啟檔案，讓它們能夠控制其他應用程式是否可以開啟檔案。 共用模式可啟用讀取、寫入和刪除存取。 屬性系統支援這些共用模式的子集，如下表所述。

    

    | 存取模式                     | 共用模式                             |
    |---------------------------------|------------------------------------------|
    | 寫入                           | 拒絕其他讀者和寫入器           |
    | 撰寫 (EnableShareDenyWrite)     | 啟用其他讀取器，拒絕其他寫入器 |
    | 唯讀 (預設)              | 啟用其他讀取器，拒絕其他寫入器 |
    | 唯讀 (EnableShareDenyNone)  | 啟用其他讀取器和寫入器         |

    

     

    開啟以供 **寫入** (GPS READWRITE 的屬性處理常式 \_) 將會拒絕其他讀取器和寫入器。 處理常式可以選擇允許讀取器，方法是指定 `EnableShareDenyWrite` 旗標 (表示在其註冊中啟用讀取) 。

    屬性處理常式會開啟以供 **讀取** (GPS \_ 預設) ，預設會啟用其他讀取器，但拒絕其他寫入器。 處理常式可以選擇啟用其他寫入器，方法是 `EnableShareDenyNone` 在其註冊中指定旗標。 這表示處理常式可以成功處理在處理常式讀取檔案時，檔案內容變更的情況。

    如需旗標定義，請參閱 [**GETPROPERTYSTOREFLAGS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[瞭解屬性處理常式](./building-property-handlers-properties.md)
</dt> <dt>

[使用種類名稱](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[使用屬性清單](./building-property-handlers-property-lists.md)
</dt> <dt>

[初始化屬性處理常式](./building-property-handlers-property-handlers.md)
</dt> <dt>

[屬性處理常式的最佳作法和常見問題](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
