---
description: 有些應用程式的設計方式是防止在電腦上安裝多個應用程式實例。
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: 應用程式設計限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992390"
---
# <a name="application-design-restrictions"></a><span data-ttu-id="0757b-103">應用程式設計限制</span><span class="sxs-lookup"><span data-stu-id="0757b-103">Application Design Restrictions</span></span>

<span data-ttu-id="0757b-104">有些應用程式的設計方式是防止在電腦上安裝多個應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="0757b-104">Some applications are designed in a way that prevents multiple instances of the application from being installed on a computer.</span></span> <span data-ttu-id="0757b-105">有了這樣的限制，應用程式就無法使用分割區功能。</span><span class="sxs-lookup"><span data-stu-id="0757b-105">With such a limitation, an application cannot make use of the partitions feature.</span></span> <span data-ttu-id="0757b-106">您可能需要先修改下列應用程式設計功能，然後才能將資料分割用於該應用程式。</span><span class="sxs-lookup"><span data-stu-id="0757b-106">The following application design features might need to be modified before partitions can be used for that application.</span></span>

## <a name="tables-and-arrays"></a><span data-ttu-id="0757b-107">資料表和陣列</span><span class="sxs-lookup"><span data-stu-id="0757b-107">Tables and Arrays</span></span>

<span data-ttu-id="0757b-108">有些應用程式會建立資料庫資料表、記憶體內部資料表或使用 CLSID 作為唯一登錄機碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="0757b-108">Some applications create database tables, in-memory tables, or arrays that use a CLSID as a unique registry key.</span></span> <span data-ttu-id="0757b-109">在沒有磁碟分割的電腦上，此登錄機碼通常是每台電腦)  (一個 CLSID 的電腦/CLSID。</span><span class="sxs-lookup"><span data-stu-id="0757b-109">On a computer without partitions, this registry key is typically computer/CLSID (one CLSID per computer).</span></span>

<span data-ttu-id="0757b-110">相反地，在具有磁碟分割的電腦上，此登錄機碼是電腦/磁碟分割識別碼/應用程式識別碼/CLSID (每一部電腦) 的多重 CLSID 實例。</span><span class="sxs-lookup"><span data-stu-id="0757b-110">Conversely, on a computer with partitions, this registry key is computer/partition ID/application ID/CLSID (multiple instances of a CLSID per computer).</span></span> <span data-ttu-id="0757b-111">因為分割區功能可讓 CLSID 的多個實例存在於電腦上，所以包含每一部電腦需要唯一 CLSID 之設計項目的應用程式可能會受到負面影響。</span><span class="sxs-lookup"><span data-stu-id="0757b-111">Because the partitions feature allows multiple instances of a CLSID to exist on a computer, applications that contain design elements that require a unique CLSID per computer might be adversely affected.</span></span>

## <a name="global-resources"></a><span data-ttu-id="0757b-112">全域資源</span><span class="sxs-lookup"><span data-stu-id="0757b-112">Global Resources</span></span>

<span data-ttu-id="0757b-113">有些應用程式會使用全域資源，例如共用記憶體、資料檔案和登錄專案。</span><span class="sxs-lookup"><span data-stu-id="0757b-113">Some applications use global resources such as shared memory, data files, and registry entries.</span></span> <span data-ttu-id="0757b-114">如果這類應用程式的多個實例同時執行，這可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="0757b-114">This could cause problems if multiple instances of such an application are executing simultaneously.</span></span>

<span data-ttu-id="0757b-115">例如，如果元件使用共用記憶體來與其他元件互動，則必須修改元件，讓元件的每個實例都配置它自己的共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="0757b-115">For example, if a component uses shared memory for interacting with other components, the component will need to be modified so that each instance of the component allocates its own shared memory.</span></span>

## <a name="type-libraries"></a><span data-ttu-id="0757b-116">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0757b-116">Type Libraries</span></span>

<span data-ttu-id="0757b-117">類型程式庫提供元件介面和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0757b-117">Type libraries provide information about a component's interfaces and methods.</span></span> <span data-ttu-id="0757b-118">這項資訊可用於數個用途，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="0757b-118">This information is used for several purposes, including the following:</span></span>

-   <span data-ttu-id="0757b-119">進行函式呼叫時，封送處理元件之間的資料</span><span class="sxs-lookup"><span data-stu-id="0757b-119">Marshaling data between components when function calls are made</span></span>
-   <span data-ttu-id="0757b-120">協助 COM + 佇列元件和 COM + 事件服務</span><span class="sxs-lookup"><span data-stu-id="0757b-120">Helping the COM+ Queued Components and COM+ Events services</span></span>
-   <span data-ttu-id="0757b-121">在 Microsoft Visual Basic 編輯器中提供正確的資訊</span><span class="sxs-lookup"><span data-stu-id="0757b-121">Providing the correct information within a Microsoft Visual Basic editor</span></span>

<span data-ttu-id="0757b-122">類型程式庫的參考會安裝在電腦的登錄中。</span><span class="sxs-lookup"><span data-stu-id="0757b-122">References to a type library are installed in the registry of a computer.</span></span> <span data-ttu-id="0757b-123">開發從磁碟分割中叫用的應用程式時，將最新版本的類型程式庫安裝在登錄中是很重要的。</span><span class="sxs-lookup"><span data-stu-id="0757b-123">When developing applications that will be invoked from within partitions, it is important that the latest version of a type library is installed in the registry.</span></span> <span data-ttu-id="0757b-124">這可確保所使用的 Visual Basic 編輯器將取得該元件可用方法的精確資訊。</span><span class="sxs-lookup"><span data-stu-id="0757b-124">This ensures that the Visual Basic editor being used will get accurate information about the methods available for that component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0757b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="0757b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0757b-126">COM + 佇列元件和分割區</span><span class="sxs-lookup"><span data-stu-id="0757b-126">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="0757b-127">分割區執行</span><span class="sxs-lookup"><span data-stu-id="0757b-127">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="0757b-128">在分割區中註冊和啟用元件</span><span class="sxs-lookup"><span data-stu-id="0757b-128">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="0757b-129">什麼是 COM + 磁碟分割？</span><span class="sxs-lookup"><span data-stu-id="0757b-129">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



