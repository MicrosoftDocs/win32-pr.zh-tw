---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 5591218A-3212-46D0-A40F-C0788B459545
title: " (隔離應用程式和並存元件) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9727db4c2db522b0bbb88eccf89481a61a75d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694668"
---
# <a name="s-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="873d5-103"> (隔離應用程式和並存元件) </span><span class="sxs-lookup"><span data-stu-id="873d5-103">S (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="873d5-104">[B C](a-sbscs-gly.md) [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T W X Y Z</span><span class="sxs-lookup"><span data-stu-id="873d5-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="873d5-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**共用並存元件**</span><span class="sxs-lookup"><span data-stu-id="873d5-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**shared side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="873d5-106">共用並存元件可供電腦上的多個應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="873d5-106">A shared side-by-side assembly is available for use by multiple applications on the computer.</span></span> <span data-ttu-id="873d5-107">它會安裝在 Windows 目錄的 Winsxs 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="873d5-107">It is installed in the Winsxs folder of the Windows directory.</span></span> <span data-ttu-id="873d5-108">應用程式和系統管理員可以藉由指定應用程式設定，來管理要使用的共用元件的版本。</span><span class="sxs-lookup"><span data-stu-id="873d5-108">Applications and administrators can manage the version of a shared assembly to be used by specifying the application configuration.</span></span> <span data-ttu-id="873d5-109">並存元件一律會伴隨資訊清單檔案，以提供有關元件的資訊給作業系統。</span><span class="sxs-lookup"><span data-stu-id="873d5-109">Side-by-side assemblies are always accompanied by manifest files that provide information about the assembly to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="873d5-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**並存元件**</span><span class="sxs-lookup"><span data-stu-id="873d5-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="873d5-111">並存元件是一種 Win32 元件，隨附資訊清單。</span><span class="sxs-lookup"><span data-stu-id="873d5-111">A side-by-side assembly is a Win32 assembly accompanied by manifests.</span></span> <span data-ttu-id="873d5-112">並存元件包含一組資源（一組 Dll、windows 類別、COM 伺服器、類型程式庫或介面）的集合，這些資源一律會同時提供給應用程式。</span><span class="sxs-lookup"><span data-stu-id="873d5-112">A side-by-side assembly contains a collection of resources—a group of DLLs, windows classes, COM servers, type libraries, or interfaces—that are always provided to applications together.</span></span>

</dd> <dt>

<span data-ttu-id="873d5-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**並存元件共用**</span><span class="sxs-lookup"><span data-stu-id="873d5-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**side-by-side assembly sharing**</span></span>
</dt> <dd>

<span data-ttu-id="873d5-114">使用並存元件以安全地在多個應用程式之間共用元件，以及抵銷共用的負面影響，例如 DLL 衝突。</span><span class="sxs-lookup"><span data-stu-id="873d5-114">Use of side-by-side assemblies to safely share assemblies among multiple applications and to offset the negative effects of sharing, such as DLL conflicts.</span></span> <span data-ttu-id="873d5-115">並存元件共用會讓多個版本的 Win32 元件在系統上同時執行，而不是擁有單一版本的元件，而該元件會假設與所有應用程式的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="873d5-115">Instead of having a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="873d5-116">並存元件一律會伴隨提供元件資訊清單檔案的組件資訊清單檔，以將元件的相關資訊提供給作業系統。</span><span class="sxs-lookup"><span data-stu-id="873d5-116">Side-by-side assemblies are always accompanied by assembly manifest files that provide information about the assembly to the operating system.</span></span> <span data-ttu-id="873d5-117">應用程式和系統管理員可以在部署之後，藉由以全域或個別應用程式為基礎來更新應用程式設定，以管理並存元件共用。</span><span class="sxs-lookup"><span data-stu-id="873d5-117">Applications and administrators can manage side-by-side assembly sharing after deployment by updating the application configuration on either a global or per-application basis.</span></span>

</dd> </dl>

 

 



