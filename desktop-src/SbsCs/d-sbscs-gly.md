---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3A4C5579-7543-4E0B-921D-BED42C2583D9
title: 'D (隔離的應用程式和並存元件) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c8912f24478f79be8aa00c963dc27cb46ec756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026874"
---
# <a name="d-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="1d562-103">D (隔離的應用程式和並存元件) </span><span class="sxs-lookup"><span data-stu-id="1d562-103">D (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="1d562-104">[B C](a-sbscs-gly.md) D E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T W X Y Z</span><span class="sxs-lookup"><span data-stu-id="1d562-104">[A](a-sbscs-gly.md) B C D E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="1d562-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**DEF-coNtext assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="1d562-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**DEF-context assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="1d562-106">**AssemblyIdentity** 子項目，定義資訊清單所描述的並存元件。</span><span class="sxs-lookup"><span data-stu-id="1d562-106">An **assemblyIdentity** subelement defining the side-by-side assembly described by the manifest.</span></span> <span data-ttu-id="1d562-107">DEF 內容 **assemblyIdentity** 子項目一律是 **元件** 專案的第一個子項目。</span><span class="sxs-lookup"><span data-stu-id="1d562-107">A DEF-context **assemblyIdentity** subelement is always the first subelement of an **assembly** element.</span></span>

</dd> <dt>

<span data-ttu-id="1d562-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**DLL 版本控制衝突**</span><span class="sxs-lookup"><span data-stu-id="1d562-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**DLL versioning conflict**</span></span>
</dt> <dd>

<span data-ttu-id="1d562-109">相容性問題。</span><span class="sxs-lookup"><span data-stu-id="1d562-109">Compatibility problem.</span></span> <span data-ttu-id="1d562-110">當應用程式安裝的共用元件版本與先前安裝的版本不相容時，就會發生元件共用問題。</span><span class="sxs-lookup"><span data-stu-id="1d562-110">Assembly sharing problems occur when an application installs a version of a shared assembly that is not backward compatible with the previously installed version.</span></span> <span data-ttu-id="1d562-111">DLL 版本控制衝突的解決方案是使用並存元件共用和隔離的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1d562-111">A solution to DLL versioning conflicts is to use side-by-side assembly sharing and isolated applications.</span></span> <span data-ttu-id="1d562-112">使用並存元件共用時，可以同時執行相同 Windows 元件的多個版本。</span><span class="sxs-lookup"><span data-stu-id="1d562-112">With side-by-side assembly sharing, multiple versions of the same Windows assembly can run simultaneously.</span></span> <span data-ttu-id="1d562-113">開發人員可以選擇要使用哪個並存元件。</span><span class="sxs-lookup"><span data-stu-id="1d562-113">Developers can choose which side-by-side assembly to use.</span></span>

</dd> </dl>

 

 



