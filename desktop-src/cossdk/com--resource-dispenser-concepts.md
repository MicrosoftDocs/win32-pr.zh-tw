---
description: 應用程式元件使用 COM + 資源配置器來存取和管理共用的非持久性狀態資訊，例如元件之間的連接，以及指定的資源管理員。
ms.assetid: 252c7180-61b1-485d-883d-36bf77357a29
title: COM + 資源配置器概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0fcf281d6d7b8ed0e087b6d77e4d686e28e1fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688711"
---
# <a name="com-resource-dispenser-concepts"></a>COM + 資源配置器概念

應用程式元件使用 COM + 資源配置器來存取和管理共用的非持久性狀態資訊，例如元件之間的連接，以及指定的資源管理員。 在執行時間，資源配置器可使用動態資源集區，例如資料庫連接、網路連接、佇列、執行緒、物件和記憶體區塊的連接。 應用程式進程會使用最少的常用資源數目來達到高效能。 資源配置器也可以自動執行交易和回收。  (如需此功能的詳細資訊，請參閱 [自動資源回收](automatic-resource-reclamation.md) 。 ) 

> [!Note]  
> 資源是資源配置器所建立的任何 *資源* 。 例如，資源管理員的連接是常見的資源。 資源位於資源配置器的記憶體中，而且永遠不會複製到分配器管理員。 只有 (**RESID**) 的不透明控制碼知道資源，且不一定能夠執行交易。 雖然受管理的資源通常可能會連接到管理持久狀態的元件，但連線本身並不是永久性的。 資源配置器通常會使用相關的資源管理員來保留持久狀態。

 

就架構而言，COM + 資源配置器系統包含資源機和分配器管理員。 資源機是使用者提供的元件，可為應用程式提供簡單的共用資源介面。 分配器管理員是 COM + 所提供的元件，可協調各種資源機的活動。

資源配置器是動態連結程式庫 (DLL) 元件，可提供至少兩個介面。 第一個 [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)會為分配器管理員提供有關如何建立、終結和登錄所管理資源的基本資訊。 第二個是公開給應用程式，可以是 COM 介面或一組介面，也可以是應用程式設計介面， (API) 透過匯入程式庫連結元件。 應用程式可以呼叫任何資源配置器，進而將任何 API 提供給應用程式。 如果資源配置器是自動化元件，則可以從 Microsoft Visual Basic 存取。 當應用程式元件參考資源配置器時，會將它具現化。

COM + 所提供的分配器管理員會追蹤資源機和它們之間的座標。 它會執行兩個介面： [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) 和 [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)。 資源機會使用 **IDispenserManager** 介面自行註冊。 然後，分配器管理員會為其提供 **IHolder** 的指標，以用來通知其活動的分配器管理員。

交易式資源配置器必須登錄分散式交易協調器的 (DTC) 交易。 這表示使用內部或外部 (與與 OLE 交易相容的資源配置) 資源管理員。

> [!Note]  
> COM + 程式設計模型包含 *宣告式交易*，可協助保護應用程式物件在其存留期間所執行的工作。 當應用程式物件使用 COM + 資源配置器時，它所執行的工作會自動進行交易;也就是說，元件不需要明確宣告交易。 這些交易是在 OLE 交易規格中定義、由 DTC 所執行，並由 COM + 代表應用程式物件起始。 如需詳細資訊，請參閱 DTC 開發指南。

 

資源不需要交易。 將非交易式資源集區的資源配置器，仍然可以藉由讓應用程式物件存取這些資源的共用集區，來達到高效能。 這種類型的資源配置器 \_ 會從 [**IDispenserDriver：： EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) 方法傳回 S FALSE，這表示資源配置器未登錄資源，因為資源不是交易式。

資源配置器也可以獨立于 COM + 運作，只提供資源分享功能。 例如，如果資源配置器公開 API (例如 ODBC) ，則資源配置器可能是透過匯入程式庫（ (）或使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數) 所存取的 DLL。 資源配置器也可能是應用程式透過呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)來存取的 COM 元件。 如果沒有 COM +，就永遠無法呼叫資源配置器的 [**EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) 方法，因為分配器管理員不知道目前的元件交易。

在啟動時，資源配置程式 DLL 必須向分配器管理員註冊本身。 分配器管理員是控制管理和卸載資源機、提供 COM + 內容，以及控制清查統計資料管理員的控制主管。  (需詳細資訊，請參閱 [Com + 分配管理員](com--dispenser-manager.md)。 ) 資源配置器會先呼叫 [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) 函式，然後呼叫 [**IDispenserManager：： RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser) 方法，傳遞資源配置器所執行的 [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) 指標。 此呼叫會傳回 [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)的參考。

為了關閉，資源配置器會呼叫 [**IHolder：： Close**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-close)。 為了確保乾淨的封裝關機，資源配置器必須能夠處理在 COM + 要求系統關閉之後，從商務物件呼叫繼續抵達的情況。

本節中的下列主題提供 COM + 資源配置器服務的詳細資訊：

-   [COM + 分配管理員](com--dispenser-manager.md)
-   [COM + 資源配置器執行緒類型](com--resource-dispenser-thread-types.md)
-   [適用于 COM + 資源配置器的共用資源狀態](pooled-resource-states-available-to-com--resource-dispenser.md)
-   [在交易中登記資源](enlisting-a-resource-in-a-transaction.md)
-   [資源配置器資源配置進程](resource-dispenser-resource-allocation-process.md)
-   [追蹤未配置的資源](tracking-non-allocated-resources.md)
-   [自動資源回收](automatic-resource-reclamation.md)
-   [COM + 資源配置器介面中使用的類型](types-used-in-com--resource-dispenser-interfaces.md)
-   [COM + 資源配置器介面](com--resource-dispenser-interfaces.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 資源配置器工作](com--resource-dispenser-tasks.md)
</dt> </dl>

 

 
