---
description: Windows 並存元件是由資訊清單描述。
ms.assetid: 501BBFFE-5927-4656-8EEE-1F6ECFAFEF5E
title: 關於並存元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e190e6428f2e366af45a4f0961ad6ea6fb3561fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944142"
---
# <a name="about-side-by-side-assemblies"></a><span data-ttu-id="4da0b-103">關於並存元件</span><span class="sxs-lookup"><span data-stu-id="4da0b-103">About Side-by-Side Assemblies</span></span>

<span data-ttu-id="4da0b-104">Windows 並存元件是由 [資訊清單](manifests.md)描述。</span><span class="sxs-lookup"><span data-stu-id="4da0b-104">A Windows side-by-side assembly is described by [manifests](manifests.md).</span></span> <span data-ttu-id="4da0b-105">並存元件包含一組資源（一組 Dll、Windows 類別、COM 伺服器、類型程式庫或介面）的集合，這些資源一律會同時提供給應用程式。</span><span class="sxs-lookup"><span data-stu-id="4da0b-105">A side-by-side assembly contains a collection of resources—a group of DLLs, Windows classes, COM servers, type libraries, or interfaces—that are always provided to applications together.</span></span> <span data-ttu-id="4da0b-106">這些會在組件資訊清單中描述。</span><span class="sxs-lookup"><span data-stu-id="4da0b-106">These are described in the assembly manifest.</span></span>

<span data-ttu-id="4da0b-107">通常，並存元件是單一 DLL。</span><span class="sxs-lookup"><span data-stu-id="4da0b-107">Typically, a side-by-side assembly is a single DLL.</span></span> <span data-ttu-id="4da0b-108">例如，Microsoft COMCTL32.DLL 元件是具有資訊清單的單一 DLL，而 Microsoft Visual C++ 開發系統執行時間程式庫元件包含多個檔案。</span><span class="sxs-lookup"><span data-stu-id="4da0b-108">For example, the Microsoft COMCTL32 assembly is a single DLL with a manifest whereas the Microsoft Visual C++ development system run-time libraries assembly contains multiple files.</span></span> <span data-ttu-id="4da0b-109">資訊清單包含描述並存元件和並存元件相依性的 [*中繼資料*](m-sbscs-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="4da0b-109">Manifests contain [*metadata*](m-sbscs-gly.md) that describes side-by-side assemblies and side-by-side assembly dependencies.</span></span>

<span data-ttu-id="4da0b-110">作業系統會使用並存元件做為命名、系結、版本控制、部署和設定的基礎單位。</span><span class="sxs-lookup"><span data-stu-id="4da0b-110">Side-by-side assemblies are used by the operating system as fundamental units of naming, binding, versioning, deployment, and configuration.</span></span> <span data-ttu-id="4da0b-111">每個並存元件都有唯一的身分識別。</span><span class="sxs-lookup"><span data-stu-id="4da0b-111">Every side-by-side assembly has a unique identity.</span></span> <span data-ttu-id="4da0b-112">元件身分識別的其中一個屬性是其版本。</span><span class="sxs-lookup"><span data-stu-id="4da0b-112">One of the attributes of the assembly identity is its version.</span></span> <span data-ttu-id="4da0b-113">如需詳細資訊，請參閱 [元件版本](assembly-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="4da0b-113">For more information, see [Assembly Versions](assembly-versions.md).</span></span>

<span data-ttu-id="4da0b-114">從 Windows XP 開始，同時執行的應用程式可以使用多個並存元件版本。</span><span class="sxs-lookup"><span data-stu-id="4da0b-114">Starting with Windows XP, multiple versions of side-by-side assemblies can be used by applications running at the same time.</span></span> <span data-ttu-id="4da0b-115">資訊清單和元件版本號碼會由載入器用來判斷正確的元件版本系結至應用程式。</span><span class="sxs-lookup"><span data-stu-id="4da0b-115">Manifests, and the assembly version number, are used by the loader to determine the correct binding of assembly versions to applications.</span></span> <span data-ttu-id="4da0b-116">並存元件和資訊清單可與應用程式和並存管理員一起運作，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="4da0b-116">Side-by-side assemblies and manifests work with applications and the side-by-side manager as illustrated in the following figure.</span></span>

![一般並存元件的標記法](images/sxsman.png)

<span data-ttu-id="4da0b-118">在上述範例中，Comctl32.DLL 6.0 版和 Comctl32.DLL 5.0 版都位於並存的組件快取中，而且可供應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="4da0b-118">In the preceding example, both Comctl32.DLL version 6.0 and Comctl32.DLL version 5.0 are in the side-by-side assembly cache and available to applications.</span></span> <span data-ttu-id="4da0b-119">當應用程式呼叫載入 DLL 時，並存管理員會決定應用程式是否具有資訊清單中所述的版本相依性。</span><span class="sxs-lookup"><span data-stu-id="4da0b-119">When an application calls to load the DLL, the side-by-side manager determines whether the application has a version dependence described in a manifest.</span></span> <span data-ttu-id="4da0b-120">如果沒有相關的資訊清單，系統會載入元件的預設版本。</span><span class="sxs-lookup"><span data-stu-id="4da0b-120">If there is no relevant manifest, the system loads the default version of the assembly.</span></span> <span data-ttu-id="4da0b-121">若為 Windows XP，Comctl32.DLL 的5.0 版是系統預設值。</span><span class="sxs-lookup"><span data-stu-id="4da0b-121">For Windows XP, version 5.0 of Comctl32.DLL is the system default.</span></span> <span data-ttu-id="4da0b-122">如果並存管理員找到資訊清單中所述版本6.0 的相依性，則該版本會載入以與應用程式一起執行。</span><span class="sxs-lookup"><span data-stu-id="4da0b-122">If the side-by-side manager finds a dependence on version 6.0 stated in a manifest, that version is loaded to run with the application.</span></span>

<span data-ttu-id="4da0b-123">Microsoft 提供數個重要的系統元件，做為並存元件。</span><span class="sxs-lookup"><span data-stu-id="4da0b-123">Several key system assemblies are being made available from Microsoft as side-by-side assemblies.</span></span> <span data-ttu-id="4da0b-124">如需詳細資訊，請參閱 [支援的 Microsoft 並存元件](supported-microsoft-side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="4da0b-124">For more information, see [Supported Microsoft Side-by-side Assemblies](supported-microsoft-side-by-side-assemblies.md).</span></span> <span data-ttu-id="4da0b-125">應用程式開發人員也可以建立自己的並存元件。</span><span class="sxs-lookup"><span data-stu-id="4da0b-125">Application developers can also create their own side-by-side assemblies.</span></span> <span data-ttu-id="4da0b-126">如需詳細資訊，請參閱 [建立並存元件的指導方針](guidelines-for-creating-side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="4da0b-126">For more information, see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span> <span data-ttu-id="4da0b-127">在許多情況下，您可以將現有的應用程式更新為使用並存元件，而不需要變更應用程式程式碼。</span><span class="sxs-lookup"><span data-stu-id="4da0b-127">In many cases it is possible to update existing applications to use side-by-side assemblies without having to change the application code.</span></span>

<span data-ttu-id="4da0b-128">我們鼓勵開發人員使用並存元件來建立 [隔離的應用程式](isolated-applications.md)，並將現有的應用程式更新為隔離的應用程式，原因如下：</span><span class="sxs-lookup"><span data-stu-id="4da0b-128">Developers are encouraged to use side-by-side assemblies to create [isolated applications](isolated-applications.md), and to update existing applications into isolated applications for the following reasons:</span></span>

-   <span data-ttu-id="4da0b-129">並存元件可以減少 DLL 版本衝突的可能性。</span><span class="sxs-lookup"><span data-stu-id="4da0b-129">Side-by-side assemblies reduce the possibility of DLL version conflicts.</span></span>
-   <span data-ttu-id="4da0b-130">並存元件共用可讓多個 COM 或 Windows 元件版本同時執行。</span><span class="sxs-lookup"><span data-stu-id="4da0b-130">Side-by-side assembly sharing enables multiple versions of COM or Windows assemblies to run at the same time.</span></span>
-   <span data-ttu-id="4da0b-131">應用程式和系統管理員可以在部署之後，以 [全域](publisher-configuration.md) 或個別 [應用程式](per-application-configuration.md) 的設定來更新元件設定。</span><span class="sxs-lookup"><span data-stu-id="4da0b-131">Applications and administrators can update assembly configuration on either a [global](publisher-configuration.md) or [per-application configuration](per-application-configuration.md) basis after deployment.</span></span> <span data-ttu-id="4da0b-132">例如，您可以將應用程式更新為使用並存元件（包含更新），而不需要重新安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="4da0b-132">For example, an application can be updated to use a side-by-side assembly that includes an update without having to reinstall the application.</span></span>

 

 



