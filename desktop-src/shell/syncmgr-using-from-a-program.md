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
# <a name="using-synchronization-manager-from-a-program"></a><span data-ttu-id="42daa-103">從程式使用同步處理管理員</span><span class="sxs-lookup"><span data-stu-id="42daa-103">Using Synchronization Manager from a Program</span></span>

<span data-ttu-id="42daa-104">若要讓您的應用程式使用同步處理管理員，您必須將元件物件模型 (COM) 物件，以處理從 SyncMgr 接收的同步處理通知。</span><span class="sxs-lookup"><span data-stu-id="42daa-104">To enable your application to work with the Synchronization Manager you must implement a Component Object Model (COM) object to handle synchronization notifications that you receive from SyncMgr.</span></span> <span data-ttu-id="42daa-105">您應用程式的處理常式會針對您處理的專案執行同步處理。</span><span class="sxs-lookup"><span data-stu-id="42daa-105">Your application's handler performs the synchronization for the items that you handle.</span></span> <span data-ttu-id="42daa-106">包含在您的處理常式中，您必須執行 [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) 介面。</span><span class="sxs-lookup"><span data-stu-id="42daa-106">Included in your handler, you must implement the [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) interface.</span></span> <span data-ttu-id="42daa-107">此外，您必須提供列舉值物件，並 [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) 您的應用程式可以同步處理的任何個別專案。</span><span class="sxs-lookup"><span data-stu-id="42daa-107">Also, you must provide an enumerator object and [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) for any separate items that your application can synchronize.</span></span>

<span data-ttu-id="42daa-108">SyncMgr 會實行 [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) 和 [**ISyncMgrSynchronizeInvoke**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke)。</span><span class="sxs-lookup"><span data-stu-id="42daa-108">SyncMgr implements [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) and [**ISyncMgrSynchronizeInvoke**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke).</span></span>

<span data-ttu-id="42daa-109">SyncMgr 會在您的 [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) 中呼叫方法，以取得應用程式所處理專案的相關資訊，以及您提供來同步處理這些專案之處理常式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42daa-109">The SyncMgr calls methods in your [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) to get information on the items that your application handles and information on the handler that you provide for synchronizing these items.</span></span>

<span data-ttu-id="42daa-110">在執行時間，同步處理常式會遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="42daa-110">At runtime, the synchronization process follows these steps.</span></span>

1.  <span data-ttu-id="42daa-111">SyncMgr 會通知您的應用程式，它是指您的應用程式透過呼叫 [**ISyncMgrSynchronize：： Initialize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize) 方法所處理的其中一個專案進行同步處理的時間。</span><span class="sxs-lookup"><span data-stu-id="42daa-111">SyncMgr notifies your application that it is time for synchronization to occur for one of the items that your application handles by calling your [**ISyncMgrSynchronize::Initialize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize) method.</span></span>
2.  <span data-ttu-id="42daa-112">SyncMgr 會呼叫 [**ISyncMgrSynchronize：： EnumSyncMgrItems**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) ，以取得應用程式所處理專案的 [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) 介面。</span><span class="sxs-lookup"><span data-stu-id="42daa-112">SyncMgr calls [**ISyncMgrSynchronize::EnumSyncMgrItems**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) to obtain the [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) interface for the items handled by your application.</span></span>
3.  <span data-ttu-id="42daa-113">SyncMgr 會呼叫 [**ISyncMgrSynchronize：： SetProgressCallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) ，為您的處理常式提供 [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) 介面的介面指標。</span><span class="sxs-lookup"><span data-stu-id="42daa-113">SyncMgr calls [**ISyncMgrSynchronize::SetProgressCallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) to provide your handler with the interface pointer for the [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) interface.</span></span> <span data-ttu-id="42daa-114">在同步處理期間，您的處理常式會使用這個介面回呼 SyncMgr。</span><span class="sxs-lookup"><span data-stu-id="42daa-114">Your handler uses this interface to call back to the SyncMgr during synchronization.</span></span>
4.  <span data-ttu-id="42daa-115">接著，SyncMgr 會呼叫您的 [**ISyncMgrSynchronize：:P repareforsync**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) 方法，讓您的處理常式有機會顯示在開始同步處理之前所需的任何使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="42daa-115">SyncMgr then calls your [**ISyncMgrSynchronize::PrepareForSync**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) method to give your handler a chance to display any user interface element that is necessary before synchronization begins.</span></span> <span data-ttu-id="42daa-116">例如，電子郵件應用程式可能會顯示使用者登入對話方塊。</span><span class="sxs-lookup"><span data-stu-id="42daa-116">For example, an email application may display a user logon dialog.</span></span>
5.  <span data-ttu-id="42daa-117">在顯示任何使用者介面元素之前和之後，您的處理常式會呼叫 [**ISyncMgrSynchronizeCallback：： EnableModeless**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) 。</span><span class="sxs-lookup"><span data-stu-id="42daa-117">Your handler calls [**ISyncMgrSynchronizeCallback::EnableModeless**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) before and after displaying any user interface elements.</span></span> <span data-ttu-id="42daa-118">當您完成時，您的處理常式會呼叫 [**ISyncMgrSynchronizeCallback：:P repareforsynccompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted) 。</span><span class="sxs-lookup"><span data-stu-id="42daa-118">Your handler calls [**ISyncMgrSynchronizeCallback::PrepareForSyncCompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted) when you are done.</span></span>
6.  <span data-ttu-id="42daa-119">SyncMgr 會呼叫您的 [**ISyncMgrSynchronize：： Synchronize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) 方法來開始同步處理。</span><span class="sxs-lookup"><span data-stu-id="42daa-119">SyncMgr calls your [**ISyncMgrSynchronize::Synchronize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) method to start the synchronization.</span></span>

<span data-ttu-id="42daa-120">在同步處理常式期間，SyncMgr 會繼續呼叫 [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) 介面中的方法。</span><span class="sxs-lookup"><span data-stu-id="42daa-120">During the synchronization process, SyncMgr continues to call methods in your [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) interface.</span></span> <span data-ttu-id="42daa-121">它可以傳送處理常式錯誤、進度和通知。</span><span class="sxs-lookup"><span data-stu-id="42daa-121">It can send your handler errors, progress, and notifications.</span></span> <span data-ttu-id="42daa-122">它也可以列舉應用程式所處理的專案，或允許您的應用程式顯示專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="42daa-122">It can also enumerate through the items that your application handles or allow your application to show properties for the items.</span></span>

<span data-ttu-id="42daa-123">您的處理常式會在 [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) 中呼叫方法，以判斷是否應該略過專案、記錄錯誤，以及在同步處理期間張貼進度資訊。</span><span class="sxs-lookup"><span data-stu-id="42daa-123">Your handler calls methods in [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) to determine if an item should be skipped, to log errors, and to post progress information during the synchronization process.</span></span>

<span data-ttu-id="42daa-124">如需詳細資訊，請參閱相關介面的相關參考頁面。</span><span class="sxs-lookup"><span data-stu-id="42daa-124">For further information, see the related reference pages for the interfaces involved.</span></span>

<span data-ttu-id="42daa-125">當同步處理完成時，您的處理常式會呼叫 [**ISyncMgrSynchronizeCallback：： SynchronizeCompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted)。</span><span class="sxs-lookup"><span data-stu-id="42daa-125">When the synchronization is completed, your handler calls [**ISyncMgrSynchronizeCallback::SynchronizeCompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted).</span></span>

 

 



