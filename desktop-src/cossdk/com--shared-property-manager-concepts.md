---
description: 在 COM + 中，物件的共用暫時性狀態是使用共用屬性管理員 (SPM) 來管理。 SPM 是一個資源配置器，可讓您用來在伺服器進程內的多個物件之間共用狀態。
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: COM + 共用屬性管理員概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970340"
---
# <a name="com-shared-property-manager-concepts"></a><span data-ttu-id="5986f-104">COM + 共用屬性管理員概念</span><span class="sxs-lookup"><span data-stu-id="5986f-104">COM+ Shared Property Manager Concepts</span></span>

<span data-ttu-id="5986f-105">在 COM + 中，物件的共用暫時性狀態是使用共用屬性管理員 (SPM) 來管理。</span><span class="sxs-lookup"><span data-stu-id="5986f-105">In COM+, shared transient state for objects is managed by using the shared property manager (SPM).</span></span> <span data-ttu-id="5986f-106">SPM 是一個資源配置器，可讓您用來在伺服器進程內的多個物件之間共用狀態。</span><span class="sxs-lookup"><span data-stu-id="5986f-106">The SPM is a resource dispenser that you can use to share state among multiple objects within a server process.</span></span>

<span data-ttu-id="5986f-107">因為並行和名稱衝突的問題，所以您無法在分散式環境中使用全域變數。</span><span class="sxs-lookup"><span data-stu-id="5986f-107">You cannot use global variables in a distributed environment because of concurrency and name collision issues.</span></span> <span data-ttu-id="5986f-108">共用屬性管理員會藉由提供共用屬性群組來消除名稱衝突，而這些群組會為其所包含的共用屬性建立唯一的命名空間。</span><span class="sxs-lookup"><span data-stu-id="5986f-108">The shared property manager eliminates name collisions by providing shared property groups, which establish unique namespaces for the shared properties they contain.</span></span> <span data-ttu-id="5986f-109">SPM 也會執行鎖定和信號，以協助保護共用屬性免于同時存取，這可能會導致更新遺失並讓屬性處於無法預測的狀態。</span><span class="sxs-lookup"><span data-stu-id="5986f-109">The SPM also implements locks and semaphores to help protect shared properties from simultaneous access, which could result in lost updates and leave properties in an unpredictable state.</span></span>

> [!Note]  
> <span data-ttu-id="5986f-110">共用的暫時性狀態是保留在記憶體中的狀態資訊，而這些資訊不會在系統失敗時存活。</span><span class="sxs-lookup"><span data-stu-id="5986f-110">Shared transient state is state information kept in memory that does not survive system failures.</span></span> <span data-ttu-id="5986f-111">這項資訊是設計成跨交易 (的多個物件共用，但不能跨進程) 界限共用。</span><span class="sxs-lookup"><span data-stu-id="5986f-111">The information is designed to be shared by multiple objects across transaction (but not across process) boundaries.</span></span>

 

<span data-ttu-id="5986f-112">儲存在 SPM 中的共用屬性僅適用于在相同進程中執行的物件。</span><span class="sxs-lookup"><span data-stu-id="5986f-112">Shared properties stored in the SPM are available only to objects running in the same process.</span></span> <span data-ttu-id="5986f-113">這表示將使用 SPM 儲存值的物件，以及需要存取這些值的物件，都必須安裝為相同 COM + 應用程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="5986f-113">This means that the objects that will use the SPM for storing values and that will need to have access to these values must be installed as part of the same COM+ application.</span></span> <span data-ttu-id="5986f-114">當您的 COM + 應用程式部署完成後，系統管理員可以將 COM + 類別從一個套件移至另一個套件。</span><span class="sxs-lookup"><span data-stu-id="5986f-114">It is possible for system administrators to move COM+ classes from one package to another after your COM+ application has been deployed.</span></span> <span data-ttu-id="5986f-115">如果您依賴數個透過 SPM 共用屬性的物件，您應該清楚記載必須將它們安裝在相同的 COM + 應用程式中。</span><span class="sxs-lookup"><span data-stu-id="5986f-115">If you rely on several objects sharing properties through the SPM, you should clearly document that they must be installed in the same COM+ application.</span></span>

<span data-ttu-id="5986f-116">共用屬性的元件也必須具有相同的啟用屬性。</span><span class="sxs-lookup"><span data-stu-id="5986f-116">It's also important for components sharing properties to have the same activation attribute.</span></span> <span data-ttu-id="5986f-117">如果相同封裝中的兩個元件有不同的啟用屬性，它們通常無法共用屬性。</span><span class="sxs-lookup"><span data-stu-id="5986f-117">If two components in the same package have different activation attributes, they generally won't be able to share properties.</span></span> <span data-ttu-id="5986f-118">例如，如果某個元件設定為在用戶端進程中執行，而另一個元件設定為在伺服器進程中執行，則它們的物件通常會在不同的進程中執行，即使它們是在相同的封裝中也一樣。</span><span class="sxs-lookup"><span data-stu-id="5986f-118">For example, if one component is configured to run in a client process and the other is configured to run in a server process, their objects will usually run in different processes even though they're in the same package.</span></span>

<span data-ttu-id="5986f-119">您應該一律從 COM + 元件具現化 [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)、 [**SharedPropertyGroup**](sharedpropertygroup.md)和 [**SharedProperty**](sharedproperty.md) 物件，而不是從基底用戶端。</span><span class="sxs-lookup"><span data-stu-id="5986f-119">You should always instantiate the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md), and [**SharedProperty**](sharedproperty.md) objects from COM+ components rather than from a base client.</span></span> <span data-ttu-id="5986f-120">如果基底用戶端建立共用屬性群組和屬性，共用屬性就會在基底用戶端進程內，而不是在伺服器進程中。</span><span class="sxs-lookup"><span data-stu-id="5986f-120">If a base client creates shared property groups and properties, the shared properties are inside the base-client process, not in a server process.</span></span> <span data-ttu-id="5986f-121">這表示，除非物件也在用戶端進程中執行，否則 COM + 物件無法共用屬性 (這通常不是很好的想法) 。</span><span class="sxs-lookup"><span data-stu-id="5986f-121">This means the COM+ objects cannot share the properties unless the objects are also running in the client process (which is generally not a good idea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5986f-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="5986f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5986f-123">COM + 共用屬性管理員</span><span class="sxs-lookup"><span data-stu-id="5986f-123">COM+ Shared Property Manager</span></span>](com--shared-property-manager.md)
</dt> <dt>

[<span data-ttu-id="5986f-124">共用屬性群組</span><span class="sxs-lookup"><span data-stu-id="5986f-124">Shared Property Groups</span></span>](shared-property-groups.md)
</dt> </dl>

 

 



