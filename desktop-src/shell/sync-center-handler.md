---
description: 本主題提供建立 DLL 檔案的逐步檢查需求，該檔案會執行處理常式以搭配同步中心使用。 這項資訊在 Windows Vista 中是有效的。
title: 開發 Windows 同步中心處理常式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 66b40f81-9515-4190-8ced-44f20bb9df86
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11185aa5976c27b7af95787b081e1eaacd99c8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973272"
---
# <a name="developing-a-windows-sync-center-handler"></a>開發 Windows 同步中心處理常式

本主題提供建立 DLL 檔案的逐步檢查需求，該檔案會執行處理常式以搭配同步中心使用。 這項資訊在 Windows Vista 中是有效的。

-   [Vista 之前的 Windows 同步處理體驗](#the-windows-synchronization-experience-before-vista)
-   [同步中心 Api](#sync-center-apis)
    -   [基本介面](#essential-interfaces)

## <a name="the-windows-synchronization-experience-before-vista"></a>Vista 之前的 Windows 同步處理體驗

Windows XP 提供 [同步處理管理員](syncmgr-start-page.md) (mobsync.exe) 。 許多裝置（例如 mp3 播放機、行動電話和攝影機）也都提供自己的同步處理介面，而不是使用同步處理管理員。 這會導致不一致且 noncentralized 的使用者體驗。

Windows Vista 提供的新同步中心功能比舊版的同步處理管理員多了許多優點。

-   更好的發現能力
-   不需要直接使用者動作
-   不會封鎖其他作業
-   更好的同步處理進度視覺效果
-   更容易瞭解開發模型

## <a name="sync-center-apis"></a>同步中心 Api

同步中心會透過多個元件物件模型 (COM) 介面，與處理常式進行通訊。 並非所有這些介面都需要執行同步中心處理常式。 本主題分為兩個部分。 第一節說明每個處理常式都必須支援的基本 COM 介面，而第二個區段會檢查選用的 COM 介面，並查看處理常式支援這些介面的原因。

-   [基本介面](#essential-interfaces)

### <a name="essential-interfaces"></a>基本介面

所有同步中心處理常式都必須支援下列介面：

-   [**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler)
-   [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo)
-   [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer)
-   [**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems)
-   [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem)
-   [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo)

[**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) 和 [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) 是用來描述與同步中心同步處理相關的單一同步處理專案。 同步處理專案通常代表特定的資料類型 (例如) 的影像或特定位置的資料。

代表不同資料位置的同步處理專案允許進行非常特定的同步處理。 位置的資料細微性是由處理常式作者所撰寫，但請小心設計。 如果)  (位置的同步處理專案太少，則會限制使用者只同步特定資料的能力。 另一方面，太多的資料細微性可能會變得難以管理。

如果處理常式支援一個以上的資料型別或多個資料位置，則需要支援一個以上的同步處理專案物件。 其中一個範例可能是 (PDA) 的個人資料助理，可讓使用者同步處理連絡人、行事曆專案和檔。 這三種資料類型需要以三個唯一的物件來表示，而每個物件會公開 [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) 和 [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) 介面。

[**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems)介面會提供一種機制，以列舉處理常式的同步處理專案。 為了取得此列舉值，同步中心會呼叫處理常式所公開的 [**ISyncMgrSyncItemContainer：： GetSyncItemEnumerator**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator) 方法。 [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer) 也包含兩個其他方法，同步中心可以使用這些方法來取得處理常式同步處理專案的相關資訊：

-   [**GetSyncItem**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem) 會傳回特定的同步處理專案。
-   [**GetSyncItemCount**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount) 會傳回處理常式所支援的同步處理專案數目。

[**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler) 和 [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo) 可用來描述處理常式的屬性，並啟動實際的同步處理。 [**ISyncMgrHandler：： Synchronize：**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandler-synchronize) 處理常式程式碼會執行同步處理，並提供進度的意見反應，以及任何發生的問題。

許多介面方法都不需要完全實作為。 同步中心提供特定數量的預設資訊。 介面可讓處理常式覆寫此資訊，並視需要提供要顯示的自訂資訊。

 

 



