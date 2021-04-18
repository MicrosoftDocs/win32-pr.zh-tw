---
title: 建立公事包 Reconcilers
description: 公事包調整器提供公事包協調檔不同版本的方法。
ms.assetid: 86d66291-96ae-40ea-98ef-ef263f25aa82
keywords:
- 公事包 reconcilers
- 和解
- IReconcilableObject
- IReconcileInitiator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b925e7055e15f6c7a49408aa28d147fb2eef5a7e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375001"
---
# <a name="creating-briefcase-reconcilers"></a>建立公事包 Reconcilers

公事包調整器提供公事包協調檔不同版本的方法。

-   [關於公事包 Reconcilers](#about-briefcase-reconcilers)
    -   [和解](#reconciliation)
    -   [建立公事包調整器](#creating-a-briefcase-reconciler)
    -   [對帳中的使用者互動](#user-interaction-in-reconciliation)
    -   [協調内嵌物件](#reconciling-embedded-objects)
    -   [殘留](#residues)
-   [公事包調整器參考](#briefcase-reconciler-reference)
    -   [公事包調整器介面和方法](#briefcase-reconciler-interfaces-and-methods)

## <a name="about-briefcase-reconcilers"></a>關於公事包 Reconcilers

公事包調整器會結合檔的不同輸入版本，以產生單一、新的檔輸出版本。 您可能需要建立公事包調整器，以支援您的檔案類型。 本總覽說明 [公事包] reconcilers，並說明如何建立它們。

我們將討論下列主題：

-   [和解](#reconciliation)
-   [建立公事包調整器](#creating-a-briefcase-reconciler)
-   [對帳中的使用者互動](#user-interaction-in-reconciliation)
-   [協調内嵌物件](#reconciling-embedded-objects)
-   [殘留](#residues)

### <a name="reconciliation"></a>和解

檔是可複製及變更的資訊集合。 如果檔的至少兩份複本的內容不同，則檔會有不同的版本。 對帳會從兩個或更多的初始版本產生單一版本的檔。 一般來說，已協調的版本是一組初始版本的資訊組合，其中包含最新或最有用的資訊。

當「公事包」判斷相同檔的兩個或多個副本不同時，即會起始對帳。 公事包（作為此內容中的起始者）會尋找並啟動與指定檔案類型相關聯的公事包調整器。 調整器會比較檔並決定要保留的檔部分。 某些 reconcilers 可能需要使用者互動才能完成對帳。 其他人可能會在沒有使用者互動的情況下完成對帳。 調整器可以包含在應用程式內，也可以是實作為 DLL 的延伸模組。

某些公事包 reconcilers 可能會建立 residues。 Residue 檔通常與初始檔具有相同的檔案類型，其中包含未儲存在合併版本中的資訊。 Residues 通常用來讓作者能夠快速判斷原始檔案中的哪些資訊不在最終的合併版本中。 如果調整器支援 residues，則會為檔的每個原始版本建立一個 residue。 除非起始端要求，否則不會建立 Residues。

有些 [公事包] reconcilers 與 [公事包] 搭配使用，讓使用者可以終止對帳。 這對可能決定不應繼續進行對等的使用者而言，是一項重要的功能。 當對帳需要使用者互動，而且可能很長時，重新調整器通常會提供終止物件。 在某些環境中，重新調整器可能會允許部分的對帳，讓使用者可以暫時暫停對帳，之後再繼續。 不過，[公事包] 目前不支援部分對帳。

### <a name="creating-a-briefcase-reconciler"></a>建立公事包調整器

您可以藉由執行對帳介面來建立公事包調整器。 調整器至少會執行 [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 介面和 [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) 或 [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面。 作為起始端，「公事包」會判斷何時需要進行調整，並呼叫 [**IReconcilableObject：：調解**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) 方法來起始對帳。

雖然 [**IReconcilableObject：：調解**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) 提供廣泛的一組對帳功能，但「公事包」重新調整器只會在大部分情況下執行最少量的調整。 尤其是，「公事包」不需要調整器就能支援 residue 產生或支援終止物件。 此外，重新調整器會執行單一的由上而下的對帳，且不能傳回 REC \_ E \_ NOTCOMPLETE 值，也就是說，它不應該嘗試部分的對帳。

[公事包] 提供 [**IReconcileInitiator**](ireconcileinitiator.md) 介面。 公事包調整器可以使用 [**IReconcileInitiator：： SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback) 方法來設定終止物件。 「公事包」不會使用版本識別碼，因此，如果調整器要求在 **IReconcileInitiator** 中使用對應的方法，則提供舊版的檔。

公事包會傳遞至 [**IReconcilableObject：：調解**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) 檔案的名字，代表要進行協調的檔版本。 公事包調整器會使用 [IMoniker：： BindToObject](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) 或 [IMoniker：： BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) 方法，取得版本的存取權。 後者通常更快，建議您這樣做。 調整器必須釋放它所系結的任何物件或儲存體。

當「公事包調整器」使用 [IMoniker：： BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage)時，它會系結至) 或 OLE 定義結構化儲存體 (資料流程的儲存體。 如果調整器需要一般儲存體，則應該使用 IMoniker：： BindToStorage 來要求 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 介面。 如果調整器預期結構化儲存體，則應該要求 [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) 介面。 在這兩種情況下，它應該要求唯讀直接 (非交易) 存取儲存體;可能無法使用讀取/寫入存取權。

最基本的公事包調整器通常會直接查看其他版本的儲存體，並以非常基本的方式處理内嵌物件，例如在輸出版本中包含這兩個版本來合併兩個版本的物件。

啟動器會使用 [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile) 函式所執行的邏輯子集來判斷指定檔案的類型，然後在登錄中尋找與指定檔案類型相關聯的重新調整器類別，以找出適當的公事包調整器。 [公事包] 和 [其他 Shell 元件] 一樣，只會以副檔名來決定檔案的類型。 檔案的副檔名必須有 [公事包] 的註冊檔案類型，才能叫用此檔案的調整程式。 安裝您的調整器時，您必須設定下列表單的登錄專案。

```
CLSID
   {the file CLSID}
      Roles
         Reconciler
            (Default) = {the reconciler-classid}
```

類別必須是快速載入、必須指定為 \_ MULTIPLEUSE，而且除非提供對等式介面的封送處理器，否則必須是 DLL) 中所包含的同進程伺服器 (，而不是在 .exe 檔) 中實作為本機伺服器 (。

### <a name="user-interaction-in-reconciliation"></a>對帳中的使用者互動

「公事包」重新調整器應該會嘗試在沒有使用者互動的情況下執行對帳。 重新調整的自動化越好，使用者對流程的認知就越好。

在某些情況下，使用者介入可能很重要。 例如，檔案系統可能會要求使用者在接受合併版本的檔之前，先檢查變更，或者可能需要使用者提出批註來說明已進行的變更。 在這些情況下，起始端（而不是公事包調整器）負責查詢使用者並執行使用者的指示。

在其他情況下，可能需要使用者介入，例如，以不相容的方式編輯兩個版本時。 在這種情況下，啟動器或公事包調整器必須查詢使用者，以取得如何解決衝突的指示。 一般情況下，沒有任何啟動者可以依賴在不需要某些使用者互動的情況下完成對帳。 另一方面，Reconcilers 可以選擇與使用者互動，以解決衝突或要求啟動器這樣做。

### <a name="reconciling-embedded-objects"></a>協調内嵌物件

當協調檔時，如果它發現無法協調之類型的内嵌物件，則公事包自動調整器本身可以成為起始端。 在此情況下，調整器必須以遞迴方式協調每個内嵌物件，並假設啟動器的所有責任。

為了執行遞迴，公事包調整器會載入物件，並查詢適當的介面。 物件的處理常式必須支援介面。 如果介面的任何方法傳回 OLE \_ E \_ NOTRUNNING 值，則調整器必須執行物件，才能執行作業。 因為内嵌物件的程式碼並非永遠可用，所以調整器必須提供此條件的解決方案。 例如，調整器可能會在已協調的版本中包含舊的和新的内嵌物件版本。 調整器不能嘗試跨連結進行協調。

啟動器會儲存正在合併的檔版本。 在許多情況下，起始端可以存取每個版本的儲存體，並使用類似的儲存體來儲存對帳的結果。 不過，有時候啟動者可能會有無法使用任何持續性版本的記憶體內建物件。 當包含開啟的内嵌物件的檔必須在儲存之前進行協調時，就會發生這種情況。 在這種情況下，啟動器會將對帳的結果儲存在記憶體中找到的版本。

啟動器會使用 [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) 介面來系結合並版本 (載入) 。 如果已建立初始版本，啟動者會使用 [IPersistStorage：： Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) 方法，並針對初始版本使用 [IPersistStorage：： InitNew](/windows/win32/api/objidl/nf-objidl-ipersiststorage-initnew) 方法。 載入合併的版本時，起始端會使用 [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取出 [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 介面的位址。 此介面可讓起始端存取現有 residues 的儲存體，並提供方法來為任何新的 residues 建立儲存體。 然後，起始端會指示介面執行對帳。 啟動器會在 IPersistStorage 之前實際查詢 [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面。 如果調整器支援 IPersistFile，則啟動器會透過 IPersistFile （而不是 IPersistStorage 方法）來操作複本。 這可允許不是儲存為複合檔案的檔案進行調整。

當對帳完成時，起始端可以使用 [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) 或 [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面儲存合併的版本。 在對帳期間，「公事包」重新調整器會視需要建立 residues，並將其持續性位寫入儲存體。 如果合併的版本是資料流程，則傳遞至[IPersistStorage：： Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load)的[IStorage](/windows/win32/api/objidl/nn-objidl-istorage)介面會包含名為 "內容" 的資料流程，並將其儲存狀態設定為 STATEBITS \_ 平坦。  (您可以使用 [IStorage：： Stat](/windows/win32/api/objidl/nf-objidl-istorage-stat) 方法來設定狀態位。在合併之後 ) ，啟動器會以適當的方式寫入資料，以儲存合併的版本。 它應確定 STATEBITS 的一般 \_ 設定是否適用于儲存體。

### <a name="residues"></a>殘留

啟動器會指出它是否想要 residues，方法是在呼叫 [**IReconcilableObject：：調解**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile)方法時，將 *pstgNewResidues* 參數設定為有效的位址。 如果重新調整器不支援建立 residues， \_ \_ 除非 *DwFlags* 參數指定 **RECONCILEF \_ NORESIDUESOK** 值，否則它必須立即傳回 REC E NORESIDUES 值。

公事包調整器會藉由建立新的儲存元素，並將其複製到 *pstgNewResidues* 所指向的陣列，將 residues 傳回給啟動器。 針對結構化儲存體 residues，調整器會複製 [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) 介面，而針對一般儲存體 residues，則會複製 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 或 IStorage 介面與 STATEBITS 一般 \_ 旗標集合。 調整器會使用 IStorage 來建立必要的儲存體，並使用 [IStorage：： CreateStream](/windows/win32/api/objidl/nf-objidl-istorage-createstream) 為 residue 建立一般儲存體（資料流程）和 [IStorage：： CreateStorage](/windows/win32/api/objidl/nf-objidl-istorage-createstorage) 來建立結構化儲存體。

啟動器會準備 *pstgNewResidues* ，讓它不會在 [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) 命名空間的 nonreserved 部分中包含任何元素。 「公事包調整器」會將每個 residue 放在名稱對應至其初始版本順序的元素中。 例如，第一個 residue 包含在 "1" 中，第二個在 "2" 中，依此類推。 如果已協調的物件本身產生 residue，它會在名為 "0" 的元素中找到。

公事包重新調整器會個別認可每個新建立的元素，以確保啟動器可以存取訊號。 但是，調整器不會認可 *pstgNewResidues* 本身。 啟動者負責認可此程式，或處置它。

## <a name="briefcase-reconciler-reference"></a>公事包調整器參考

本節包含對等介面的相關資訊。 處理錯誤時，方法只會傳回明確定義為可能傳回值的錯誤值。 此外，此方法必須在從錯誤傳回之前，設定將其位址作為參數傳遞至 **Null** 的所有變數。

### <a name="briefcase-reconciler-interfaces-and-methods"></a>公事包調整器介面和方法

-   [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 
    -   -   [**IReconcilableObject::GetProgressFeedbackMaxEstimate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-getprogressfeedbackmaxestimate)
        -   [**IReconcilableObject：：調解**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile)

-   [**IReconcileInitiator**](ireconcileinitiator.md) 
    -   -   [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)
        -   [**IReconcileInitiator::SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback)

-   [**INotifyReplica**](/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica) 
    -   -   [**INotifyReplica::YouAreAReplica**](/windows/desktop/api/reconcil/nf-reconcil-inotifyreplica-youareareplica)

 

 