---
description: 隨附于 COM + 系統管理介面的 MTS 管理程式庫會提供與 MTS 2.0 管理程式庫的回溯相容性。
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: MTS 管理程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510546"
---
# <a name="mts-administration-library"></a><span data-ttu-id="15eb4-103">MTS 管理程式庫</span><span class="sxs-lookup"><span data-stu-id="15eb4-103">MTS Administration Library</span></span>

<span data-ttu-id="15eb4-104">隨附于 COM + 系統管理介面的 MTS 管理程式庫會提供與 MTS 2.0 管理程式庫的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="15eb4-104">The MTS Administration Library shipped with the COM+ Administration interfaces provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="15eb4-105">大部分現有的 MTS 2.0 管理程式碼仍可與提供的 MTSAdmin 程式庫搭配使用;不過，某些功能已變更。</span><span class="sxs-lookup"><span data-stu-id="15eb4-105">Most existing MTS 2.0 administration code will still work with the MTSAdmin Library that is provided; however, some functionality has changed.</span></span>

<span data-ttu-id="15eb4-106">若要利用新功能或第一次撰寫管理程式碼，您應該使用 COMAdmin 程式庫。</span><span class="sxs-lookup"><span data-stu-id="15eb4-106">To take advantage of new functionality or if you are writing administration code for the first time, you should use the COMAdmin Library.</span></span>

<span data-ttu-id="15eb4-107">目前的 MTS 管理程式庫中的下列元素會從 MTS 2.0 管理程式庫變更：</span><span class="sxs-lookup"><span data-stu-id="15eb4-107">The following elements in the current MTS Administration Library are changed from the MTS 2.0 Administration Library:</span></span>

-   <span data-ttu-id="15eb4-108">**IRemoteComponentUtil** 介面無法再使用。</span><span class="sxs-lookup"><span data-stu-id="15eb4-108">The **IRemoteComponentUtil** interface is no longer available.</span></span>
-   <span data-ttu-id="15eb4-109">無法再使用 **RemoteComponents** 集合。</span><span class="sxs-lookup"><span data-stu-id="15eb4-109">The **RemoteComponents** collection is no longer available.</span></span>
-   <span data-ttu-id="15eb4-110">RoleID 屬性已無法再使用，角色名稱現在會做為此的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="15eb4-110">The RoleID property is no longer available, the Role Name is now used as the key for this.</span></span>
-   <span data-ttu-id="15eb4-111">**ExportPackage** 方法不再匯出 client.exe。</span><span class="sxs-lookup"><span data-stu-id="15eb4-111">The **ExportPackage** method no longer exports a client.exe.</span></span>
-   <span data-ttu-id="15eb4-112">RemoteComponentInstallPath 屬性不再于 [**LocalComputer**](localcomputer.md) 集合公開。</span><span class="sxs-lookup"><span data-stu-id="15eb4-112">The RemoteComponentInstallPath property is no longer exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="15eb4-113">ApplicationInstallPath 屬性將不再于 [**LocalComputer**](localcomputer.md) 集合公開。</span><span class="sxs-lookup"><span data-stu-id="15eb4-113">The ApplicationInstallPath property will no longer be exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="15eb4-114">系統封裝現在已命名為 [系統應用程式]。</span><span class="sxs-lookup"><span data-stu-id="15eb4-114">The System package is now named System Application.</span></span>
-   <span data-ttu-id="15eb4-115">公用程式套件現在已命名為 COM + 公用程式。</span><span class="sxs-lookup"><span data-stu-id="15eb4-115">The Utilities package is now named COM+ Utilities.</span></span>
-   <span data-ttu-id="15eb4-116">IsSystem 屬性存在於 MTSAdmin 中的 [**元件**](components.md) 集合中，但會在核取時傳回 ">notimpl"，如果設定，將不會儲存。</span><span class="sxs-lookup"><span data-stu-id="15eb4-116">The IsSystem property exists in the [**Components**](components.md) collection in MTSAdmin but will return "NotImpl" when checked and will not be saved if set.</span></span>
-   <span data-ttu-id="15eb4-117">[**元件**](components.md)集合已不再支援 PackageName 屬性。</span><span class="sxs-lookup"><span data-stu-id="15eb4-117">The PackageName property is no longer supported by the [**Components**](components.md) collection.</span></span> <span data-ttu-id="15eb4-118">若要找出套件的名稱，您現在需要取得 PackageID，然後在封裝集合中尋找相符的封裝。</span><span class="sxs-lookup"><span data-stu-id="15eb4-118">To figure out the package's name, you will now need to get the PackageID and then find the matching package in the Packages collection.</span></span>
-   <span data-ttu-id="15eb4-119">下列屬性已不再存在於 [**InterfacesForComponent**](interfacesforcomponent.md) 集合上：</span><span class="sxs-lookup"><span data-stu-id="15eb4-119">The following properties no longer exist on the [**InterfacesForComponent**](interfacesforcomponent.md) collection:</span></span>
    -   <span data-ttu-id="15eb4-120">**ProxyCLSID**</span><span class="sxs-lookup"><span data-stu-id="15eb4-120">**ProxyCLSID**</span></span>
    -   <span data-ttu-id="15eb4-121">**ProxyDLL**</span><span class="sxs-lookup"><span data-stu-id="15eb4-121">**ProxyDLL**</span></span>
    -   <span data-ttu-id="15eb4-122">**ProxyThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="15eb4-122">**ProxyThreadingModel**</span></span>
    -   <span data-ttu-id="15eb4-123">**TypeLibFile**</span><span class="sxs-lookup"><span data-stu-id="15eb4-123">**TypeLibFile**</span></span>
    -   <span data-ttu-id="15eb4-124">**TypeLibID**</span><span class="sxs-lookup"><span data-stu-id="15eb4-124">**TypeLibID**</span></span>
    -   <span data-ttu-id="15eb4-125">**TypeLibLangID**</span><span class="sxs-lookup"><span data-stu-id="15eb4-125">**TypeLibLangID**</span></span>
    -   <span data-ttu-id="15eb4-126">**TypeLibPlatform**</span><span class="sxs-lookup"><span data-stu-id="15eb4-126">**TypeLibPlatform**</span></span>
    -   <span data-ttu-id="15eb4-127">**TypeLibVersion**</span><span class="sxs-lookup"><span data-stu-id="15eb4-127">**TypeLibVersion**</span></span>

## <a name="related-topics"></a><span data-ttu-id="15eb4-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="15eb4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15eb4-129">從 MTS 自動轉換</span><span class="sxs-lookup"><span data-stu-id="15eb4-129">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="15eb4-130">COM + 轉換結果和問題</span><span class="sxs-lookup"><span data-stu-id="15eb4-130">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="15eb4-131">從 MTS 手動轉換</span><span class="sxs-lookup"><span data-stu-id="15eb4-131">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> </dl>

 

 



