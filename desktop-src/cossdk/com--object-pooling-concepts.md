---
description: 物件共用是 COM + 所提供的自動服務，可讓您設定元件，使其本身的實例在集區中保持作用中狀態，以供任何要求元件的用戶端使用。
ms.assetid: 74a45220-449a-4d89-a979-a206e5e3d3ad
title: COM + 物件共用概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb2aa6481b2493371801d0d274420d356b0a32e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385902"
---
# <a name="com-object-pooling-concepts"></a><span data-ttu-id="97736-103">COM + 物件共用概念</span><span class="sxs-lookup"><span data-stu-id="97736-103">COM+ Object Pooling Concepts</span></span>

<span data-ttu-id="97736-104">物件共用是 COM + 所提供的自動服務，可讓您設定元件，使其本身的實例在集區中保持作用中狀態，以供任何要求元件的用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="97736-104">Object pooling is an automatic service provided by COM+ that enables you to configure a component to have instances of itself kept active in a pool, ready to be used by any client that requests the component.</span></span> <span data-ttu-id="97736-105">您可以針對指定的元件進行系統管理設定和監視集區，並指定集區大小和建立要求超時值等特性。</span><span class="sxs-lookup"><span data-stu-id="97736-105">You can administratively configure and monitor the pool maintained for a given component, specifying characteristics such as pool size and creation request time-out values.</span></span> <span data-ttu-id="97736-106">當應用程式正在執行時，COM + 會為您管理集區，並根據您指定的準則來處理物件啟用和重複使用的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="97736-106">When the application is running, COM+ manages the pool for you, handling the details of object activation and reuse according to the criteria you have specified.</span></span>

<span data-ttu-id="97736-107">您可以用這種方式重複使用物件，以達到非常顯著的效能和調整優點，特別是當它們被撰寫以充分利用重複使用時。</span><span class="sxs-lookup"><span data-stu-id="97736-107">You can achieve very significant performance and scaling benefits by reusing objects in this manner, particularly when they are written to take full advantage of reuse.</span></span> <span data-ttu-id="97736-108">使用物件共用時，您可以獲得下列優點：</span><span class="sxs-lookup"><span data-stu-id="97736-108">With object pooling, you gain the following benefits:</span></span>

-   <span data-ttu-id="97736-109">您可以加快每個用戶端的物件使用時間，並從物件針對用戶端執行的實際工作中，分解出耗時的初始化和資源取得。</span><span class="sxs-lookup"><span data-stu-id="97736-109">You can speed object use time for each client, factoring out time-consuming initialization and resource acquisition from the actual work that the object performs for clients.</span></span>
-   <span data-ttu-id="97736-110">您可以分享在所有用戶端上取得昂貴資源的成本。</span><span class="sxs-lookup"><span data-stu-id="97736-110">You can share the cost of acquiring expensive resources across all clients.</span></span>
-   <span data-ttu-id="97736-111">您可以在應用程式啟動時預先設定物件，然後再傳入任何用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="97736-111">You can pre-allocate objects when the application starts, before any client requests come in.</span></span>
-   <span data-ttu-id="97736-112">您可以使用系統管理集區管理來管理資源的使用方式，例如，藉由設定適當的最大集區層級，您可以只開啟與您擁有授權一樣多的資料庫連接。</span><span class="sxs-lookup"><span data-stu-id="97736-112">You can govern resource use with administrative pool management for example, by setting an appropriate maximum pool level, you can keep open only as many database connections as you have a license for.</span></span>
-   <span data-ttu-id="97736-113">您可以系統管理員設定共用以充分利用可用的硬體資源，您可以在可用的硬體資源變更時輕鬆地調整集區設定。</span><span class="sxs-lookup"><span data-stu-id="97736-113">You can administratively configure pooling to take best advantage of available hardware resources you can easily adjust the pool configuration as available hardware resources change.</span></span>
-   <span data-ttu-id="97736-114">您可以加快使用即時 [ (JIT) 啟用](com--just-in-time-activation.md)之物件的重新開機時間，同時刻意控制如何將資源專用給用戶端。</span><span class="sxs-lookup"><span data-stu-id="97736-114">You can speed reactivation time for objects that use [just-in-time (JIT) activation](com--just-in-time-activation.md), while deliberately controlling how resources are dedicated to clients.</span></span>

## <a name="writing-poolable-objects"></a><span data-ttu-id="97736-115">寫入共用物件</span><span class="sxs-lookup"><span data-stu-id="97736-115">Writing Poolable Objects</span></span>

<span data-ttu-id="97736-116">共用物件必須符合特定需求，才能讓多個用戶端使用單一物件實例。</span><span class="sxs-lookup"><span data-stu-id="97736-116">Poolable objects must meet certain requirements to enable a single object instance to be used by multiple clients.</span></span> <span data-ttu-id="97736-117">例如，它們無法保存用戶端狀態或具有任何執行緒親和性。</span><span class="sxs-lookup"><span data-stu-id="97736-117">For example, they can't hold client state or have any thread affinity.</span></span> <span data-ttu-id="97736-118">交易對象也有特定需求，因為集區物件所持有的 managed 資源必須手動登錄于交易中。</span><span class="sxs-lookup"><span data-stu-id="97736-118">Transactional objects also have particular requirements, in that managed resources held by a pooled object must be manually enlisted in a transaction.</span></span>

<span data-ttu-id="97736-119">集區物件可以執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) 來控制如何重複使用它們。</span><span class="sxs-lookup"><span data-stu-id="97736-119">Pooled objects can implement [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) to control how they are reused.</span></span> <span data-ttu-id="97736-120">這可讓他們在指定的內容中啟動時，執行初始化，以清除停用的任何用戶端狀態，並指出它們處於無法重複使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="97736-120">This enables them to perform initialization when activated in a given context, to clean up any client state on deactivation, and to indicate when they are in a non-reusable state.</span></span>

<span data-ttu-id="97736-121">通常，以稍微泛用的方式撰寫共用物件，以便系統管理員以函式字串進行自訂，會很有用。</span><span class="sxs-lookup"><span data-stu-id="97736-121">Often, it useful to write poolable objects in a somewhat generic fashion so that they can be administratively customized with a constructor string.</span></span> <span data-ttu-id="97736-122">例如，可能會撰寫物件來保存泛型 ODBC 連接，並以系統管理員的方式在函式字串中指定特定的 DSN。</span><span class="sxs-lookup"><span data-stu-id="97736-122">For example, an object might be written to hold a generic ODBC connection, with a particular DSN administratively specified in a constructor string.</span></span>

<span data-ttu-id="97736-123">下表所述，本節中的主題提供有關物件共用如何在 COM + 中運作的資訊，以及如何撰寫、設定和執行共用物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97736-123">The topics in this section, described in the following table, provide information about how object pooling works in COM+, as well as information about how to write, configure, and implement poolable objects.</span></span>



| <span data-ttu-id="97736-124">主題</span><span class="sxs-lookup"><span data-stu-id="97736-124">Topic</span></span>                                                                                                 | <span data-ttu-id="97736-125">描述</span><span class="sxs-lookup"><span data-stu-id="97736-125">Description</span></span>                                                                                              |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97736-126">物件共用的運作方式</span><span class="sxs-lookup"><span data-stu-id="97736-126">How Object Pooling Works</span></span>](how-object-pooling-works.md)<br/>                                   | <span data-ttu-id="97736-127">提供基本概念。</span><span class="sxs-lookup"><span data-stu-id="97736-127">Presents basic concepts.</span></span><br/>                                                                      |
| [<span data-ttu-id="97736-128">使用物件共用改善效能</span><span class="sxs-lookup"><span data-stu-id="97736-128">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)<br/> | <span data-ttu-id="97736-129">提供有關如何以最有效率的方式使用物件共用的特定詳細資料。</span><span class="sxs-lookup"><span data-stu-id="97736-129">Provides specific details on how you can use object pooling most effectively.</span></span><br/>                 |
| [<span data-ttu-id="97736-130">共用物件的需求</span><span class="sxs-lookup"><span data-stu-id="97736-130">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)<br/>                 | <span data-ttu-id="97736-131">提供如何撰寫要共用之物件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="97736-131">Provides details on how to write an object that is to be pooled.</span></span><br/>                              |
| [<span data-ttu-id="97736-132">共用交易對象</span><span class="sxs-lookup"><span data-stu-id="97736-132">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)<br/>                         | <span data-ttu-id="97736-133">提供適用于共用交易對象之特殊需求的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="97736-133">Provides details about the special requirements that apply to poolable transactional objects.</span></span><br/> |
| [<span data-ttu-id="97736-134">控制物件存留期和狀態</span><span class="sxs-lookup"><span data-stu-id="97736-134">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)<br/>         | <span data-ttu-id="97736-135">描述如何執行集區物件，以控制如何重複使用這些物件。</span><span class="sxs-lookup"><span data-stu-id="97736-135">Describes how pooled objects can be implemented to control how they are reused.</span></span><br/>               |



 

## <a name="related-topics"></a><span data-ttu-id="97736-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="97736-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97736-137">COM + 物件共用工作</span><span class="sxs-lookup"><span data-stu-id="97736-137">COM+ Object Pooling Tasks</span></span>](com--object-pooling-tasks.md)
</dt> </dl>

 

 




