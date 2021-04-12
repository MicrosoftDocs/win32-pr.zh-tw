---
description: 開發人員會產生修補程式建立檔案，並使用 Msimsp.exe 在 Patchwiz.dll 中呼叫 UiCreatePatchPackageEx 函式，藉以建立修補程式套件。
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: 建立修補程式套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193123"
---
# <a name="creating-a-patch-package"></a><span data-ttu-id="141d9-103">建立修補程式套件</span><span class="sxs-lookup"><span data-stu-id="141d9-103">Creating a Patch Package</span></span>

<span data-ttu-id="141d9-104">開發人員會產生修補程式建立檔案，並使用[Msimsp.exe](msimsp-exe.md)在[Patchwiz.dll](patchwiz-dll.md)中呼叫[UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md)函式，藉以建立修補程式套件。</span><span class="sxs-lookup"><span data-stu-id="141d9-104">Developers create a patch package by generating a patch creation file and using [Msimsp.exe](msimsp-exe.md) to call the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="141d9-105">Windows Installer SDK 中提供 Msimsp.exe 和 Patchwiz.dll。</span><span class="sxs-lookup"><span data-stu-id="141d9-105">Msimsp.exe and Patchwiz.dll are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="141d9-106">如需詳細資訊，請參閱 [小型更新修補範例](a-small-update-patching-example.md)。</span><span class="sxs-lookup"><span data-stu-id="141d9-106">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="141d9-107">由於 Windows Installer 套件的修補程式會導致使用新的 .msi 檔案安裝原始來源，因此新的 .msi 檔案必須與原始來源的配置保持相容。</span><span class="sxs-lookup"><span data-stu-id="141d9-107">Because the application of a patch to a Windows Installer package results in the installation of the original sources using a new .msi file, the new .msi file must remain compatible with the layout of the original source.</span></span>

<span data-ttu-id="141d9-108">當您撰寫修補程式套件時，您必須使用未壓縮的安裝映射來建立修補程式，例如，系統管理映射或從 CD-ROM 的未壓縮安裝映射。</span><span class="sxs-lookup"><span data-stu-id="141d9-108">When you author a patch package you must use an uncompressed setup image to create a patch, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="141d9-109">您也必須遵守下列限制：</span><span class="sxs-lookup"><span data-stu-id="141d9-109">You must also adhere to the following restrictions:</span></span>

-   <span data-ttu-id="141d9-110">請勿將檔案從某個資料夾移至另一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="141d9-110">Do not move files from one folder to another.</span></span>
-   <span data-ttu-id="141d9-111">請勿將檔案從一個封包移至另一個。</span><span class="sxs-lookup"><span data-stu-id="141d9-111">Do not move files from one cabinet to another.</span></span>
-   <span data-ttu-id="141d9-112">請勿變更封包中的檔案順序。</span><span class="sxs-lookup"><span data-stu-id="141d9-112">Do not change the order of files in a cabinet.</span></span>
-   <span data-ttu-id="141d9-113">請勿變更現有檔案的序號。</span><span class="sxs-lookup"><span data-stu-id="141d9-113">Do not change the sequence number of existing files.</span></span> <span data-ttu-id="141d9-114">序號是在 [File 資料表](file-table.md)的 sequence 資料行中指定的值。</span><span class="sxs-lookup"><span data-stu-id="141d9-114">The sequence number is the value specified in the Sequence column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="141d9-115">修補程式所加入的任何新檔案都必須放在現有檔案順序的結尾。</span><span class="sxs-lookup"><span data-stu-id="141d9-115">Any new files that are added by the patch must be placed at the end of the existing file sequence.</span></span> <span data-ttu-id="141d9-116">升級映射中任何新檔案的序號都必須大於目標映射中現有檔案的最大序號。</span><span class="sxs-lookup"><span data-stu-id="141d9-116">The sequence number of any new file in the upgraded image must be greater than the largest sequence number of existing files in the target image.</span></span>
-   <span data-ttu-id="141d9-117">請勿在原始和新的 .msi 檔案版本之間變更檔案 [資料表](file-table.md) 中的主鍵。</span><span class="sxs-lookup"><span data-stu-id="141d9-117">Do not change the primary keys in the [File Table](file-table.md) between the original and new .msi file versions.</span></span>
    > [!Note]  
    > <span data-ttu-id="141d9-118">檔案在目標映射和更新的映射的檔案 [資料表](file-table.md) 中必須有相同的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="141d9-118">The file must have the same key in the [File Table](file-table.md) of both the target image and the updated image.</span></span> <span data-ttu-id="141d9-119">這兩個數據表的 File 資料行中的字串值必須相同，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="141d9-119">The string values in the File column of both tables must be identical, including the case.</span></span>

     

-   <span data-ttu-id="141d9-120">請勿使用只有大小寫不同的檔案 [資料表](file-table.md) 索引鍵來撰寫套件，例如，避免使用下表範例。</span><span class="sxs-lookup"><span data-stu-id="141d9-120">Do not author a package with [File Table](file-table.md) keys that differ only in case, for example, avoid the following table example.</span></span>

    

    | <span data-ttu-id="141d9-121">檔案</span><span class="sxs-lookup"><span data-stu-id="141d9-121">File</span></span>       | <span data-ttu-id="141d9-122">元件\_</span><span class="sxs-lookup"><span data-stu-id="141d9-122">Component\_</span></span> | <span data-ttu-id="141d9-123">FileName</span><span class="sxs-lookup"><span data-stu-id="141d9-123">FileName</span></span>   |
    |------------|-------------|------------|
    | <span data-ttu-id="141d9-124">readme.txt</span><span class="sxs-lookup"><span data-stu-id="141d9-124">readme.txt</span></span> | <span data-ttu-id="141d9-125">Comp1</span><span class="sxs-lookup"><span data-stu-id="141d9-125">Comp1</span></span>       | <span data-ttu-id="141d9-126">readme.txt</span><span class="sxs-lookup"><span data-stu-id="141d9-126">readme.txt</span></span> |
    | <span data-ttu-id="141d9-127">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="141d9-127">ReadMe.txt</span></span> | <span data-ttu-id="141d9-128">Comp2</span><span class="sxs-lookup"><span data-stu-id="141d9-128">Comp2</span></span>       | <span data-ttu-id="141d9-129">readme.txt</span><span class="sxs-lookup"><span data-stu-id="141d9-129">readme.txt</span></span> |

    

     

    <span data-ttu-id="141d9-130">當 Comp1 和 Comp2 安裝在不同的目錄，但您無法使用 [Msimsp.exe](msimsp-exe.md) 或 [Patchwiz.dll](patchwiz-dll.md) 產生封裝的修補程式時，Windows Installer 可以允許上一個資料表範例。</span><span class="sxs-lookup"><span data-stu-id="141d9-130">The Windows Installer can allow the previous table example when Comp1 and Comp2 are installed on different directories, but then you cannot use [Msimsp.exe](msimsp-exe.md) or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package.</span></span> <span data-ttu-id="141d9-131">Msimsp.exe 和 Patchwiz.dll 呼叫 Makecab.exe，不區分大小寫且失敗。</span><span class="sxs-lookup"><span data-stu-id="141d9-131">Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive and fails.</span></span>

    <span data-ttu-id="141d9-132">在安裝程式中使用合併模組時，請確定檔案序號和配置符合上述指導方針。</span><span class="sxs-lookup"><span data-stu-id="141d9-132">When using merge modules in the setup, ensure that file sequence numbers and layout adhere to the above guidelines.</span></span>

 

 



