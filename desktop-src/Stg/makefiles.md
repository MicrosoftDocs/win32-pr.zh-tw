---
title: 生成
description: 此系列中每個程式碼範例的 makefile 都是一般 Microsoft Win32 makefile，而且是要從命令提示字元視窗建立。
ms.assetid: f9944069-b536-4ae2-8411-f02c3a78978c
keywords:
- Makefile 結構化儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15fef5818c28986232e8c2a648f43bdc096832f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311582"
---
# <a name="makefiles"></a><span data-ttu-id="447c9-104">生成</span><span class="sxs-lookup"><span data-stu-id="447c9-104">Makefiles</span></span>

<span data-ttu-id="447c9-105">此系列中每個程式碼範例的 makefile 都是一般 Microsoft Win32 makefile，而且是要從命令提示字元視窗建立。</span><span class="sxs-lookup"><span data-stu-id="447c9-105">The makefiles for each of the code samples in this series are generic Microsoft Win32 makefiles and are meant to be built from the Command Prompt window.</span></span> <span data-ttu-id="447c9-106">它們會假設 Microsoft 編譯器和連結器工具，而且可能需要進行一些修改才能與其他工具搭配使用。</span><span class="sxs-lookup"><span data-stu-id="447c9-106">They assume Microsoft compiler and linker tools and will probably require some modification to work with other tools.</span></span> <span data-ttu-id="447c9-107">大部分的編譯器/連結器命令列參數都是由 Win32 中定義的宏指定，也就是平臺軟體發展工具組 (SDK) 隨附的檔案。</span><span class="sxs-lookup"><span data-stu-id="447c9-107">Most compiler/linker command line switches are specified by macros defined in the Win32.mak makefile include file included with the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="447c9-108">Makeall.bat 檔案，以及每個個別的程式碼範例 makefile，都支援下表所列的常見選項，以便從 [命令提示字元] 視窗用來控制組建的本質。</span><span class="sxs-lookup"><span data-stu-id="447c9-108">The Makeall.bat file, and each respective code sample makefile, support common options, listed in the following table, for invocation from the Command Prompt window to control the nature of the build.</span></span>



| <span data-ttu-id="447c9-109">Nmake 調用</span><span class="sxs-lookup"><span data-stu-id="447c9-109">Nmake invocation</span></span>        | <span data-ttu-id="447c9-110">Makeall 調用</span><span class="sxs-lookup"><span data-stu-id="447c9-110">Makeall invocation</span></span>          | <span data-ttu-id="447c9-111">效果</span><span class="sxs-lookup"><span data-stu-id="447c9-111">Effect</span></span>                       |
|-------------------------|-----------------------------|------------------------------|
| <span data-ttu-id="447c9-112">**Nmake**</span><span class="sxs-lookup"><span data-stu-id="447c9-112">**nmake**</span></span>               | <span data-ttu-id="447c9-113">**makeall**</span><span class="sxs-lookup"><span data-stu-id="447c9-113">**makeall**</span></span>                 | <span data-ttu-id="447c9-114">使用 debug 資訊編譯。</span><span class="sxs-lookup"><span data-stu-id="447c9-114">Compile with debug info.</span></span>     |
| <span data-ttu-id="447c9-115">**nmake** **nodebug = 1**</span><span class="sxs-lookup"><span data-stu-id="447c9-115">**nmake** **nodebug=1**</span></span> | <span data-ttu-id="447c9-116">**makeall** **"nodebug = 1"**</span><span class="sxs-lookup"><span data-stu-id="447c9-116">**makeall** **"nodebug=1"**</span></span> | <span data-ttu-id="447c9-117">編譯而不含 debug 資訊。</span><span class="sxs-lookup"><span data-stu-id="447c9-117">Compile without debug info.</span></span>  |
| <span data-ttu-id="447c9-118">**nmake** **設定檔 = 1**</span><span class="sxs-lookup"><span data-stu-id="447c9-118">**nmake** **profile=1**</span></span> | <span data-ttu-id="447c9-119">**makeall** **"profile = 1"**</span><span class="sxs-lookup"><span data-stu-id="447c9-119">**makeall** **"profile=1"**</span></span> | <span data-ttu-id="447c9-120">使用程式碼剖析資訊進行編譯。</span><span class="sxs-lookup"><span data-stu-id="447c9-120">Compile with profiling info.</span></span> |
| <span data-ttu-id="447c9-121">**nmake** **微調 = 1**</span><span class="sxs-lookup"><span data-stu-id="447c9-121">**nmake** **tune=1**</span></span>    | <span data-ttu-id="447c9-122">**makeall** **"微調 = 1"**</span><span class="sxs-lookup"><span data-stu-id="447c9-122">**makeall** **"tune=1"**</span></span>    | <span data-ttu-id="447c9-123">使用工作集調諧器資訊。</span><span class="sxs-lookup"><span data-stu-id="447c9-123">With working set tuner info.</span></span> |
| <span data-ttu-id="447c9-124">**nmake** **unicode = 1**</span><span class="sxs-lookup"><span data-stu-id="447c9-124">**nmake** **unicode=1**</span></span> | <span data-ttu-id="447c9-125">**makeall** **"unicode = 1"**</span><span class="sxs-lookup"><span data-stu-id="447c9-125">**makeall** **"unicode=1"**</span></span> | <span data-ttu-id="447c9-126">針對 Unicode 編譯。</span><span class="sxs-lookup"><span data-stu-id="447c9-126">Compile for Unicode.</span></span>         |
| <span data-ttu-id="447c9-127">**nmake** **清除**</span><span class="sxs-lookup"><span data-stu-id="447c9-127">**nmake** **clean**</span></span>     | <span data-ttu-id="447c9-128">**makeall** **clean**</span><span class="sxs-lookup"><span data-stu-id="447c9-128">**makeall** **clean**</span></span>       | <span data-ttu-id="447c9-129">刪除暫存二進位檔。</span><span class="sxs-lookup"><span data-stu-id="447c9-129">Delete temporary binaries.</span></span>   |
| <span data-ttu-id="447c9-130">**nmake** **cleanall**</span><span class="sxs-lookup"><span data-stu-id="447c9-130">**nmake** **cleanall**</span></span>  | <span data-ttu-id="447c9-131">**makeall** **cleanall**</span><span class="sxs-lookup"><span data-stu-id="447c9-131">**makeall** **cleanall**</span></span>    | <span data-ttu-id="447c9-132">刪除所有產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="447c9-132">Delete all generated files.</span></span>  |



 

<span data-ttu-id="447c9-133">針對 Makeall.bat 調用，您必須擁有引號，如下所示。</span><span class="sxs-lookup"><span data-stu-id="447c9-133">For the Makeall.bat invocations you must have the quotes as shown.</span></span> <span data-ttu-id="447c9-134">**Nodebug**、**設定檔** 和 **微調** 選項都是互斥的：您只能針對指定的編譯/連結，使用其中一個（或無）。</span><span class="sxs-lookup"><span data-stu-id="447c9-134">The **nodebug**, **profile**, and **tune** options are mutually exclusive: you may use only one of them, or none, for a given compilation/link.</span></span> <span data-ttu-id="447c9-135">若要編譯範例以使用 Unicode 字串執行，請使用 **"Unicode = 1"** 選項。</span><span class="sxs-lookup"><span data-stu-id="447c9-135">To compile the samples to run with Unicode strings, use the **"unicode=1"** option.</span></span> <span data-ttu-id="447c9-136">預設值是針對傳統的 ANSI 字串支援進行編譯，因為您接著可以在任何32位的 Windows 作業系統上執行。</span><span class="sxs-lookup"><span data-stu-id="447c9-136">The default is to compile for the traditional ANSI string support, because you can then run on any 32-bit Windows operating system.</span></span> <span data-ttu-id="447c9-137">您可以在 Windows Server 2003 和更新版本以及 Windows 2000 和更新版本上，自由編譯和執行，或不使用 Unicode。</span><span class="sxs-lookup"><span data-stu-id="447c9-137">You can freely compile and run with or without Unicode on Windows Server 2003 and later, and Windows 2000 and later.</span></span> <span data-ttu-id="447c9-138">請注意，APPUTIL 一律會使用與其他程式碼範例相同的選項進行編譯，您可能會另外進行編譯。</span><span class="sxs-lookup"><span data-stu-id="447c9-138">Be aware that APPUTIL is always compiled with the same options as the other code samples you may be separately compiling.</span></span> <span data-ttu-id="447c9-139">這對 **"unicode = 1"** 選項而言更是如此。</span><span class="sxs-lookup"><span data-stu-id="447c9-139">This is especially true for the **"unicode=1"** option.</span></span>

<span data-ttu-id="447c9-140">您可以使用已安裝的32位 c + + 整合式開發環境 (IDE) 使用提供的一般 makefile 來建立範例。</span><span class="sxs-lookup"><span data-stu-id="447c9-140">You may use an installed 32-bit C++ integrated development environment (IDE) to build the samples using the generic makefiles provided.</span></span> <span data-ttu-id="447c9-141">若要這樣做，您必須在 IDE 中，將一般 makefile 處理為「外部」 makefile。</span><span class="sxs-lookup"><span data-stu-id="447c9-141">To do so requires that within your IDE you handle the generic makefiles as 'external' makefiles.</span></span> <span data-ttu-id="447c9-142">提供的 makefile 需要 Microsoft NMAKE 相容的建立公用程式。</span><span class="sxs-lookup"><span data-stu-id="447c9-142">The makefiles provided require a Microsoft NMAKE-compatible make utility.</span></span>

<span data-ttu-id="447c9-143">大部分的 c + + Ide 可以將這些 makefile 辨識為外部，但仍提供許多 IDE 的編輯-組建-debug 的優點。</span><span class="sxs-lookup"><span data-stu-id="447c9-143">Most C++ IDEs can recognize these makefiles as external and yet still provide many edit-build-debug benefits of the IDE.</span></span> <span data-ttu-id="447c9-144">例如，在 Microsoft Visual Studio 97 或更新版本中，您可以使用 [檔案] 功能表 [開啟工作區] 選項來產生工作區，方法是開啟適當命名的複製 (例如程式碼範例 Win32 makefile 的 Exeskel. mak) 。</span><span class="sxs-lookup"><span data-stu-id="447c9-144">For example, in Microsoft Visual Studio 97 or later, you can use the File menu Open Workspace choice to produce a workspace by opening an appropriately named copy (for example, Exeskel.mak) of the code sample Win32 makefile.</span></span>

 

 




