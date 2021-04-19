---
description: Windows Installer 可以安裝、移除及更新由 Microsoft .NET Framework 的 common language runtime 所使用的 Win32 元件和元件。
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: 組件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981538"
---
# <a name="assemblies"></a><span data-ttu-id="a54a8-103">組件</span><span class="sxs-lookup"><span data-stu-id="a54a8-103">Assemblies</span></span>

<span data-ttu-id="a54a8-104">Windows Installer 可以安裝、移除及更新由 Microsoft .NET Framework 的 common language runtime 所使用的 Win32 元件和元件。</span><span class="sxs-lookup"><span data-stu-id="a54a8-104">Windows Installer can install, remove, and update Win32 assemblies and assemblies used by the common language runtime of the Microsoft .NET Framework.</span></span> <span data-ttu-id="a54a8-105">元件是以單一安裝程式元件的 Windows Installer 來處理。</span><span class="sxs-lookup"><span data-stu-id="a54a8-105">An assembly is handled by the Windows Installer as a single installer component.</span></span> <span data-ttu-id="a54a8-106">構成元件的所有檔案都必須包含在 [元件](component-table.md) 資料表中所列的單一安裝程式元件中。</span><span class="sxs-lookup"><span data-stu-id="a54a8-106">All of the files that constitute an assembly must be contained by a single installer component that is listed in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="a54a8-107">在 Windows Vista 和 Windows XP 上執行的 Windows Installer 可以安裝並存元件。</span><span class="sxs-lookup"><span data-stu-id="a54a8-107">Windows Installer running on Windows Vista and Windows XP can install side-by-side assemblies.</span></span> <span data-ttu-id="a54a8-108">並存元件可以安全地在多個應用程式之間共用元件，並可抵消元件共用的負面影響，例如 DLL 衝突。</span><span class="sxs-lookup"><span data-stu-id="a54a8-108">Side-by-side assemblies can safely share assemblies among multiple applications and can offset the negative effects of assembly sharing, such as DLL conflicts.</span></span> <span data-ttu-id="a54a8-109">除了會假設與所有應用程式回溯相容的單一版本元件之外，並存元件共用也可讓多個版本的 COM 或 Win32 元件在系統上同時執行。</span><span class="sxs-lookup"><span data-stu-id="a54a8-109">Instead of a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a COM or Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="a54a8-110">這項增強功能可隔離應用程式是 Microsoft .NET Framework 的重要部分。</span><span class="sxs-lookup"><span data-stu-id="a54a8-110">This improved capability to isolate applications is an important part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="a54a8-111">如需詳細資訊，請參閱 [隔離的應用程式和並存元件](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)。</span><span class="sxs-lookup"><span data-stu-id="a54a8-111">For more information, see [Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span></span>

<span data-ttu-id="a54a8-112">下列各節描述如何搭配使用元件與 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="a54a8-112">The following sections describe the use of assemblies with the Windows Installer.</span></span>

-   [<span data-ttu-id="a54a8-113">將元件加入封裝中</span><span class="sxs-lookup"><span data-stu-id="a54a8-113">Adding Assemblies to a Package</span></span>](adding-assemblies-to-a-package.md)
-   [<span data-ttu-id="a54a8-114">安裝和移除元件</span><span class="sxs-lookup"><span data-stu-id="a54a8-114">Installing and Removing Assemblies</span></span>](installing-and-removing-assemblies.md)
-   [<span data-ttu-id="a54a8-115">更新組件</span><span class="sxs-lookup"><span data-stu-id="a54a8-115">Updating Assemblies</span></span>](updating-assemblies.md)
-   [<span data-ttu-id="a54a8-116">Common Language Runtime 元件的重新安裝模式</span><span class="sxs-lookup"><span data-stu-id="a54a8-116">Reinstallation Modes of Common Language Runtime Assemblies</span></span>](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [<span data-ttu-id="a54a8-117">Windows Installer 所寫入的元件登錄機碼</span><span class="sxs-lookup"><span data-stu-id="a54a8-117">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)

<span data-ttu-id="a54a8-118">如需安裝 COM 和 COM + 1.0 應用程式的詳細資訊，請參閱 [安裝具有 Windows Installer 的 COM + 應用程式](installing-a-com--application-with-the-windows-installer.md)、將 [com 元件安裝至私用位置](installing-a-com-component-to-a-private-location.md)，以及 [將 com 元件設為私用的現有封裝](make-a-com-component-in-an-existing-package-private.md)。</span><span class="sxs-lookup"><span data-stu-id="a54a8-118">For information about installing COM and COM+ 1.0 applications, see [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md), [Installing a COM Component to a Private Location](installing-a-com-component-to-a-private-location.md), and [Make a COM Component in an Existing Package Private](make-a-com-component-in-an-existing-package-private.md).</span></span>

 

 
