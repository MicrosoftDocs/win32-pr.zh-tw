---
description: 並行安裝（也稱為嵌套安裝）是 Windows Installer 的已淘汰功能。
ms.assetid: 579ae4ee-47a0-440e-81ca-ea8bf60c5349
title: 並行安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09264df8c47c08f7d1512b46d65572d3572d5190f960254c8ed13182dd668657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144405"
---
# <a name="concurrent-installations"></a>並行安裝

並行安裝（也稱為嵌套安裝）是 Windows Installer 的已淘汰功能。 隨著並行安裝安裝的應用程式最後可能會失敗，因為客戶很難正確地服務。 請勿使用並行安裝來安裝要發行至公用的產品。 當使用安裝的應用程式不適合公開發行時，並行安裝在受控制的公司環境中可能會有有限的適用性。 並行安裝檔是針對想要將並行安裝與非公開發布的應用程式一起使用的封裝作者提供的。

同時安裝動作會在目前執行的安裝期間安裝另一個 Windows Installer 套件。 同時安裝會新增至封裝，方法是在 [CustomAction 資料表](customaction-table.md) 中撰寫並行安裝動作，並將此自訂動作排程到順序資料表中。 CustomAction 資料表的目標欄位包含並行安裝所使用的公用屬性設定字串。 CustomAction 資料表的來源欄位會識別並行套件。 同時安裝動作只能重新安裝或移除目前應用程式安裝套件已安裝的應用程式。

並行安裝動作的類型是在 CustomAction 資料表的 [類型] 欄位中指定。 根據自訂動作類型而定，並行應用程式的封裝可以位於主要套件的 substorage 中，做為檔案在屬性指定位置的檔案，或作為使用者電腦上的公告應用程式。 下列自訂動作類型會執行並行安裝。



| 自訂動作類型                                 | 描述                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------|
| [自訂動作類型7](custom-action-type-7.md)   | 產品的並行安裝，位於安裝套件中。      |
| [自訂動作類型23](custom-action-type-23.md) | 在目前的來源樹狀結構中同時安裝安裝程式套件。 |
| [自訂動作類型39](custom-action-type-39.md) | 同時安裝已公告的安裝程式套件。                     |



 

並行安裝會共用與主要安裝相同的使用者介面和記錄設定。

並行安裝動作應放置在主要安裝動作順序的 [InstallInitialize 動作](installinitialize-action.md) 和 [InstallFinalize 動作](installfinalize-action.md) 之間。 復原主要安裝之後，安裝程式也會復原並行安裝。 因為安裝程式結合並行和主要安裝的復原資訊，所以不需要使用 [順延強制](deferred-execution-custom-actions.md) 搭配並行安裝動作。 復原安裝時，所有變更都會反轉。

並行安裝動作的傳回值與其他自訂動作的值相同。 請參閱 [自訂動作傳回值](custom-action-return-values.md)。

指定自動重新開機系統，或要求使用者重新開機的標準或自訂動作，也可以從並行安裝內執行重新開機或要求。

一旦安裝程式開始並行安裝，它就會鎖定所有其他安裝，直到並行安裝完成，然後再繼續主要安裝。 安裝程式只能以同步的自訂動作來執行並行安裝。 查看 [同步和非同步自訂動作](synchronous-and-asynchronous-custom-actions.md)。 [自訂動作傳回處理選項](custom-action-return-processing-options.md)中所述的選項旗標必須設定為 none (+ 0) 或 **msidbCustomActionTypeContinue** (+ 64) 。

並行安裝動作可以安裝要在本機執行的應用程式、從來源執行、重新安裝，或是以使用 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) 進行一般安裝時的相同方式來移除。 若要指定安裝類型，請將 [ [**ADDLOCAL**](addlocal.md)]、[ [**ADDSOURCE**](addsource.md)]、[ [**重新安裝**](reinstall.md)] 或 [ [**移除**](remove.md) ] 屬性傳遞至 [並行安裝] 動作。

並行安裝動作可以成對撰寫，一個用於安裝的動作，還有另一個用來移除並行安裝的動作。 [自訂動作類型 7](custom-action-type-7.md)或[自訂動作類型 23](custom-action-type-23.md)通常用來安裝。 [自訂動作類型 39](custom-action-type-39.md)通常用來在卸載父產品時移除並行安裝。 [CustomAction 資料表](customaction-table.md)中移除自訂動作的記錄，在來源欄位中可以有產品代碼 GUID，而在目標欄位中可以有「移除 = 全部」。 您必須在具有互斥條件的動作順序資料表中撰寫兩個自訂動作。 例如，安裝產品的自訂動作在其條件欄位中可能會有「未安裝」，而自訂動作會移除其條件欄位中的並行安裝可以有 REMOVE = "ALL"。

沒有任何方法可查詢套件的成本。 這使得並行安裝的成本變得很困難。 您必須將資料列加入至 [ReserveCost 資料表](reservecost-table.md) ，以指出與並行安裝相關聯之元件的資料夾與最差案例成本。

並行安裝動作唯一可用的 [自訂動作傳回處理選項](custom-action-return-processing-options.md) 為 none (+ 0) 或 **msidbCustomActionTypeContinue** (+ 64) 。

請注意，父安裝無法呼叫其本身的套件作為並行安裝動作。

請注意，如果個別電腦安裝嘗試執行個別使用者的並行安裝，則安裝程式預設會將父安裝註冊為每位使用者。 這可能會導致安裝程式不正確地移除應用程式，因為安裝程式會在實際註冊為每位使用者的情況下，每一部電腦卸載應用程式。 若要強制並行安裝的狀態追蹤其父安裝的狀態，請 \[ \] 在 [CustomAction 資料表](customaction-table.md)的目標資料行中輸入 ALLUSERS = "allusers"。 在此情況下，如果父代為每部電腦，則並行安裝為每部電腦，如果父系為每位使用者，則並行安裝為每位使用者。

開發人員在撰寫並行安裝時，應該注意下列警告。

-   並行安裝無法共用元件。
-   系統管理安裝也不能包含並行安裝。
-   修補和升級可能無法搭配並行安裝使用。
-   安裝程式可能不會正確地產生並行安裝的成本。
-   整合式 ProgressBars 無法搭配並行安裝使用。
-   並行安裝無法安裝要公告的資源。
-   執行應用程式並行安裝的封裝，也應該在父產品卸載時卸載並行應用程式。

若要防止封裝安裝為並行安裝，請將下列其中一個條件陳述式加入至 [LaunchCondition](launchcondition-table.md) 資料表。 這可防止另一個安裝執行的並行安裝動作來安裝套件。 這不會防止 [RemoveExistingProducts](removeexistingproducts-action.md) 動作移除套件。 另請參閱 [**ParentOriginalDatabase**](parentoriginaldatabase.md) 屬性和 [**ParentProductCode**](parentproductcode.md) 屬性。

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

 

 



