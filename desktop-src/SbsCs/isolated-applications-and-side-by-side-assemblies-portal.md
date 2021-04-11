---
description: 從程式管理系統並存元件存放區中的元件共用和 DLL 版本控制。 撰寫組件資訊清單和自我描述元件共用和重新導向 Dll 的應用程式。
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: 隔離應用程式和並存組件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112705"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="e7e42-104">隔離應用程式和並存組件</span><span class="sxs-lookup"><span data-stu-id="e7e42-104">Isolated Applications and Side-by-side Assemblies</span></span>

## <a name="purpose"></a><span data-ttu-id="e7e42-105">目的</span><span class="sxs-lookup"><span data-stu-id="e7e42-105">Purpose</span></span>

<span data-ttu-id="e7e42-106">隔離應用程式和並存元件是 Microsoft Windows 解決方案，可減少 Windows 用戶端應用程式中的版本控制衝突。</span><span class="sxs-lookup"><span data-stu-id="e7e42-106">Isolated Applications and Side-by-side Assemblies is a Microsoft Windows solution that reduces versioning conflicts in Windows-client applications.</span></span> <span data-ttu-id="e7e42-107">在 Windows 中，應用程式開發人員可以建立隔離的應用程式，這些應用程式是由登錄、其他應用程式或系統上執行之其他版本元件的變更，完全自我描述且不受影響。</span><span class="sxs-lookup"><span data-stu-id="e7e42-107">With Windows, application developers can build isolated applications that are fully self-describing and unaffected by changes to the registry, other applications, or other versions of assemblies running on the system.</span></span> <span data-ttu-id="e7e42-108">應用程式作者和系統管理員可以使用資訊清單，在部署于全球或每個應用程式之後，管理並存元件的共用。</span><span class="sxs-lookup"><span data-stu-id="e7e42-108">Application authors and administrators can use manifests to manage the sharing of side-by-side assemblies after deployment on either a global or per-application basis.</span></span> <span data-ttu-id="e7e42-109">客戶可受益于更穩定且更可靠地更新的隔離應用程式。</span><span class="sxs-lookup"><span data-stu-id="e7e42-109">Customers benefit from isolated applications that are more stable and more reliably updated.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e7e42-110">適用時</span><span class="sxs-lookup"><span data-stu-id="e7e42-110">Where applicable</span></span>

<span data-ttu-id="e7e42-111">隔離應用程式和並存元件共用可以用來開發安全地共用作業系統元件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e7e42-111">Isolated applications and side-by-side assembly sharing can be used to develop applications that safely share operating system assemblies.</span></span> <span data-ttu-id="e7e42-112">開發人員可以使用這項技術來修正由不相容的共用元件版本所造成的 DLL 版本控制衝突。</span><span class="sxs-lookup"><span data-stu-id="e7e42-112">Developers can use this technology to correct DLL versioning conflicts caused by an incompatible version of a shared assembly.</span></span>

<span data-ttu-id="e7e42-113">如果您的應用程式必須一致地取得您已測試的元件版本，您可以將應用程式隔離，讓應用程式一律會在使用者電腦上以測試過的元件版本執行。</span><span class="sxs-lookup"><span data-stu-id="e7e42-113">If your application must consistently get the version of a component you have tested, it is possible to isolate your application so that it will always be run with the tested version of the component on the user's computer.</span></span>

<span data-ttu-id="e7e42-114">隔離應用程式和並存元件適用于桌面樣式應用程式的開發。</span><span class="sxs-lookup"><span data-stu-id="e7e42-114">Isolated Applications and Side-by-side Assemblies is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e7e42-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="e7e42-115">Developer audience</span></span>

<span data-ttu-id="e7e42-116">本檔主要適用于軟體發展人員、應用程式開發人員和網路系統管理員：</span><span class="sxs-lookup"><span data-stu-id="e7e42-116">This documentation is primarily intended for software developers, application developers, and network administrators:</span></span>

-   <span data-ttu-id="e7e42-117">想要建立隔離應用程式的軟體發展人員，這些應用程式會使用 Microsoft 和其他並存元件發行者所提供的並存元件。</span><span class="sxs-lookup"><span data-stu-id="e7e42-117">Software developers who want to create isolated applications that will use the side-by-side assemblies made available by Microsoft and other side-by-side assembly publishers.</span></span>
-   <span data-ttu-id="e7e42-118">有興趣建立自己並存元件以隔離其應用程式的應用程式開發人員。</span><span class="sxs-lookup"><span data-stu-id="e7e42-118">Application developers who are interested in creating their own side-by-side assemblies to isolate their applications.</span></span>
-   <span data-ttu-id="e7e42-119">需要有關隔離應用程式之詳細資訊的網路系統管理員。</span><span class="sxs-lookup"><span data-stu-id="e7e42-119">Network administrators who want more information about isolated applications.</span></span>

<span data-ttu-id="e7e42-120">作為並存元件共用和隔離應用程式的主要參考，本檔提供有關撰寫資訊清單和並存元件、安裝隔離的應用程式和並存元件，以及使用啟用內容 API 的一般背景資訊。</span><span class="sxs-lookup"><span data-stu-id="e7e42-120">As the primary reference for side-by-side assembly sharing and isolated applications, this documentation provides general background information about authoring manifests and side-by-side assemblies, installing isolated applications and side-by-side assemblies, and using the Activation Context API.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e7e42-121">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="e7e42-121">Run-time requirements</span></span>

<span data-ttu-id="e7e42-122">需要 windows Server 2003 和更新版本或 Windows XP 及更新版本，才能使用並存元件和資訊清單來隔離應用程式，並使用啟用內容 API。</span><span class="sxs-lookup"><span data-stu-id="e7e42-122">Windows Server 2003 and later or Windows XP and later is required to use side-by-side assemblies and manifests to isolate applications and to use the Activation Context API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e7e42-123">本節內容</span><span class="sxs-lookup"><span data-stu-id="e7e42-123">In this section</span></span>



| <span data-ttu-id="e7e42-124">主題</span><span class="sxs-lookup"><span data-stu-id="e7e42-124">Topic</span></span>                                                         | <span data-ttu-id="e7e42-125">描述</span><span class="sxs-lookup"><span data-stu-id="e7e42-125">Description</span></span>                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="e7e42-126">參考</span><span class="sxs-lookup"><span data-stu-id="e7e42-126">Reference</span></span>](side-by-side-assemblies-reference.md)<br/> | <span data-ttu-id="e7e42-127">隔離應用程式和並存元件的檔。</span><span class="sxs-lookup"><span data-stu-id="e7e42-127">Documentation of Isolated Applications and Side-by-side Assemblies.</span></span><br/> |



 

 

 




