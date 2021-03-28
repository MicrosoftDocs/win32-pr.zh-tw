---
description: 若要讓您的應用程式使用同步處理管理員，您必須將元件物件模型 (COM) 物件，以處理從 SyncMgr 接收的同步處理通知。
title: 從程式使用同步處理管理員
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bf18d493-0fe7-46e7-9686-f7ee75b3039b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9bd5abdc382c82c6c1aafcda3a967337384dc807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514112"
---
# <a name="using-synchronization-manager-from-a-program"></a>從程式使用同步處理管理員

若要讓您的應用程式使用同步處理管理員，您必須將元件物件模型 (COM) 物件，以處理從 SyncMgr 接收的同步處理通知。 您應用程式的處理常式會針對您處理的專案執行同步處理。 包含在您的處理常式中，您必須執行 [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) 介面。 此外，您必須提供列舉值物件，並 [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) 您的應用程式可以同步處理的任何個別專案。

SyncMgr 會實行 [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) 和 [**ISyncMgrSynchronizeInvoke**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke)。

SyncMgr 會在您的 [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) 中呼叫方法，以取得應用程式所處理專案的相關資訊，以及您提供來同步處理這些專案之處理常式的相關資訊。

在執行時間，同步處理常式會遵循下列步驟。

1.  SyncMgr 會通知您的應用程式，它是指您的應用程式透過呼叫 [**ISyncMgrSynchronize：： Initialize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize) 方法所處理的其中一個專案進行同步處理的時間。
2.  SyncMgr 會呼叫 [**ISyncMgrSynchronize：： EnumSyncMgrItems**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) ，以取得應用程式所處理專案的 [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) 介面。
3.  SyncMgr 會呼叫 [**ISyncMgrSynchronize：： SetProgressCallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) ，為您的處理常式提供 [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) 介面的介面指標。 在同步處理期間，您的處理常式會使用這個介面回呼 SyncMgr。
4.  接著，SyncMgr 會呼叫您的 [**ISyncMgrSynchronize：:P repareforsync**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) 方法，讓您的處理常式有機會顯示在開始同步處理之前所需的任何使用者介面元素。 例如，電子郵件應用程式可能會顯示使用者登入對話方塊。
5.  在顯示任何使用者介面元素之前和之後，您的處理常式會呼叫 [**ISyncMgrSynchronizeCallback：： EnableModeless**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) 。 當您完成時，您的處理常式會呼叫 [**ISyncMgrSynchronizeCallback：:P repareforsynccompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted) 。
6.  SyncMgr 會呼叫您的 [**ISyncMgrSynchronize：： Synchronize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) 方法來開始同步處理。

在同步處理常式期間，SyncMgr 會繼續呼叫 [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) 介面中的方法。 它可以傳送處理常式錯誤、進度和通知。 它也可以列舉應用程式所處理的專案，或允許您的應用程式顯示專案的屬性。

您的處理常式會在 [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) 中呼叫方法，以判斷是否應該略過專案、記錄錯誤，以及在同步處理期間張貼進度資訊。

如需詳細資訊，請參閱相關介面的相關參考頁面。

當同步處理完成時，您的處理常式會呼叫 [**ISyncMgrSynchronizeCallback：： SynchronizeCompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted)。

 

 



