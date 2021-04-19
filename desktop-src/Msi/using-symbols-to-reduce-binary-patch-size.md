---
description: 針對您的目標和升級映射二進位檔使用公用符號，可減少大約一半的二進位修補程式大小。
ms.assetid: 83351a1b-ba70-4f0b-bacf-71ad7993a5aa
title: 使用符號來減少二進位修補程式大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5ccf33dbf3ffefbee909d99bd0204ea2f49aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973095"
---
# <a name="using-symbols-to-reduce-binary-patch-size"></a><span data-ttu-id="404ab-103">使用符號來減少二進位修補程式大小</span><span class="sxs-lookup"><span data-stu-id="404ab-103">Using Symbols to Reduce Binary Patch Size</span></span>

<span data-ttu-id="404ab-104">針對您的目標和升級映射二進位檔使用公用符號，可減少大約一半的二進位修補程式大小。</span><span class="sxs-lookup"><span data-stu-id="404ab-104">Using public symbols for your target and upgrade image binaries can reduce binary patch sizes by approximately one half.</span></span> <span data-ttu-id="404ab-105">實際的縮減取決於所使用的符號。</span><span class="sxs-lookup"><span data-stu-id="404ab-105">The actual reduction depends upon the symbols used.</span></span> <span data-ttu-id="404ab-106">請注意，使用符號可能會導致修補程式建立速度變慢，因為處理符號檔需要較長的時間。</span><span class="sxs-lookup"><span data-stu-id="404ab-106">Note that using symbols can result in slower patch creation times because it takes longer to process the symbol files.</span></span>

<span data-ttu-id="404ab-107">若要使用符號來縮減二進位修補程式的大小，您必須為目標和升級映射二進位檔提供符號。</span><span class="sxs-lookup"><span data-stu-id="404ab-107">To reduce the size of a binary patch using symbols, you must provide symbols for both the target and upgrade image binaries.</span></span> <span data-ttu-id="404ab-108">在 [TargetImages](targetimages-table-patchwiz-dll-.md) 資料表的 SymbolPaths 資料行和 [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) 資料表的 SymbolPaths 資料行中指定符號。</span><span class="sxs-lookup"><span data-stu-id="404ab-108">Specify the symbols in the SymbolPaths column of the [TargetImages](targetimages-table-patchwiz-dll-.md) table and the SymbolPaths column of the [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) table.</span></span> <span data-ttu-id="404ab-109">您必須使用 Visual C++ 在程式資料庫 (PDB) 檔案格式產生符號。</span><span class="sxs-lookup"><span data-stu-id="404ab-109">You must use Visual C++ to generate symbols in the program database (PDB) file format.</span></span> <span data-ttu-id="404ab-110">較新版本的 Visual C++ 會提供 PDB 檔案中的所有必要資訊。</span><span class="sxs-lookup"><span data-stu-id="404ab-110">Newer versions of Visual C++ provide all of the necessary information in the PDB file.</span></span> <span data-ttu-id="404ab-111">較舊版本的 Visual C++ 也會產生 debug (DBG) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="404ab-111">Older versions of Visual C++ also generate the debug (DBG) file format.</span></span> <span data-ttu-id="404ab-112">在此情況下，SymbolsPaths 值應該指定 PDB 和 DBG 檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="404ab-112">In this case, the SymbolsPaths value should specify the location of both the PDB and DBG files.</span></span>

<span data-ttu-id="404ab-113">例如，修補程式的 TargetImage 可能是隨附于 Windows 2000 的安裝套件，而且會安裝1.1.1029.0 版本的 MSI.DLL。</span><span class="sxs-lookup"><span data-stu-id="404ab-113">For example, the TargetImage for a patch might be the installation package that shipped with Windows 2000 and that installs the 1.1.1029.0 version of MSI.DLL.</span></span> <span data-ttu-id="404ab-114">UpgradedImage 可能是隨附于 Windows 2000 Service Pack 1 (SP1) 的更新版安裝套件，而且會安裝 MSI.DLL 的1.11.1314.0 版本。</span><span class="sxs-lookup"><span data-stu-id="404ab-114">The UpgradedImage might be the updated installation package that shipped with Windows 2000 with Service Pack 1 (SP1) and that installs the 1.11.1314.0 version of MSI.DLL.</span></span> <span data-ttu-id="404ab-115">您必須建立兩個 Patch 建立屬性 (PCP) 檔案，其中一個檔案的 [TargetImages](targetimages-table-patchwiz-dll-.md) 和 [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) 資料表的 SymbolPaths 資料行都是 Null (空白) ，另一個則是 SymbolPaths 和 TargetImages 資料表的 UpgradedImages 資料行，並以二進位檔的符號位置填入。</span><span class="sxs-lookup"><span data-stu-id="404ab-115">Two Patch Creation Properties (PCP) files would then have to be created, one with the SymbolPaths column of both the [TargetImages](targetimages-table-patchwiz-dll-.md) and [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) tables left NULL (blank) and the other with the SymbolPaths column of both the TargetImages and UpgradedImages tables populated with the location of the symbols for the binaries.</span></span> <span data-ttu-id="404ab-116">在此情況下，不使用符號所產生的修補程式大小，大約是使用符號產生之修補程式大小的三倍。</span><span class="sxs-lookup"><span data-stu-id="404ab-116">In this case, the size of the patch generated without using symbols can be approximately three times the size of the patch generated using symbols.</span></span>

<span data-ttu-id="404ab-117">Mpatch.exe 公用程式可以用來測試單一檔案的二進位修補程式產生，以及檢查符號是否有效。</span><span class="sxs-lookup"><span data-stu-id="404ab-117">The Mpatch.exe utility can be used to test the generation of binary patches for a single file and to check whether or not the symbols are valid.</span></span> <span data-ttu-id="404ab-118">Mpatch.exe 公用程式包含在 [Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中。</span><span class="sxs-lookup"><span data-stu-id="404ab-118">The Mpatch.exe utility is included in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="404ab-119">Mpatch.exe 的輸出會指出符號是否不相符。</span><span class="sxs-lookup"><span data-stu-id="404ab-119">The output of Mpatch.exe will indicate if the symbols do not match.</span></span>

<span data-ttu-id="404ab-120">例如，輸入下列命令列來檢查符號是否有效。</span><span class="sxs-lookup"><span data-stu-id="404ab-120">For example, enter the following command line to check whether or not the symbols are valid.</span></span>

<span data-ttu-id="404ab-121">**mpatch.exe-NEWSYMPATH： d： \\ update-OLDSYMPATH： d： \\ target d： \\ target \\example.dll d： \\ update \\example.dll 範例 .pat**</span><span class="sxs-lookup"><span data-stu-id="404ab-121">**mpatch.exe -NEWSYMPATH:d:\\update -OLDSYMPATH:d:\\target d:\\target\\example.dll d:\\update\\example.dll example.pat**</span></span>

<span data-ttu-id="404ab-122">如果符號不在正確的位置，Mpatch.exe 的輸出可能會包含下列警告。</span><span class="sxs-lookup"><span data-stu-id="404ab-122">If the symbols are not in the correct location, the output of Mpatch.exe may include the following warning.</span></span>

``` syntax
WARNING: no debug symbols for d:\update\example.dll
```

 

 



