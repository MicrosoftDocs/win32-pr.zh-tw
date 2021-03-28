---
description: 示範如何在瀏覽器中執行 Shell 命名空間延伸模組，包括內容功能表行為和自訂工作。
title: Explorer 資料提供者範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6bd15cbef62ff69efcccd28fcb625fc1432fdf89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194806"
---
# <a name="explorer-data-provider-sample"></a><span data-ttu-id="67989-103">Explorer 資料提供者範例</span><span class="sxs-lookup"><span data-stu-id="67989-103">Explorer Data Provider Sample</span></span>

<span data-ttu-id="67989-104">示範如何在瀏覽器中執行 Shell 命名空間延伸模組，包括內容功能表行為和自訂工作。</span><span class="sxs-lookup"><span data-stu-id="67989-104">Demonstrates how to implement a Shell namespace extension, including context menu behavior and custom tasks in the browser.</span></span>

<span data-ttu-id="67989-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="67989-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="67989-106">需求</span><span class="sxs-lookup"><span data-stu-id="67989-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="67989-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="67989-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="67989-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="67989-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="67989-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="67989-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="67989-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="67989-110">Requirements</span></span>



| <span data-ttu-id="67989-111">產品</span><span class="sxs-lookup"><span data-stu-id="67989-111">Product</span></span>                                | <span data-ttu-id="67989-112">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="67989-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="67989-113">Windows</span><span class="sxs-lookup"><span data-stu-id="67989-113">Windows</span></span>                                | <span data-ttu-id="67989-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67989-114">Windows Vista</span></span>           |
| <span data-ttu-id="67989-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="67989-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="67989-116">6.1</span><span class="sxs-lookup"><span data-stu-id="67989-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="67989-117">下載範例</span><span class="sxs-lookup"><span data-stu-id="67989-117">Downloading the Sample</span></span>

| <span data-ttu-id="67989-118">Location</span><span class="sxs-lookup"><span data-stu-id="67989-118">Location</span></span>      | <span data-ttu-id="67989-119">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="67989-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67989-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="67989-120">GitHub</span></span>  | [<span data-ttu-id="67989-121">ExplorerDataProvider 範例</span><span class="sxs-lookup"><span data-stu-id="67989-121">ExplorerDataProvider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a><span data-ttu-id="67989-122">建立範例</span><span class="sxs-lookup"><span data-stu-id="67989-122">Building the Sample</span></span>

<span data-ttu-id="67989-123">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="67989-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="67989-124">開啟 [命令提示字元] 視窗，並流覽至 **ExplorerDataProvider** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="67989-124">Open the command prompt window and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="67989-125">輸入 `msbuild ExplorerDataProvider.sln`。</span><span class="sxs-lookup"><span data-stu-id="67989-125">Enter `msbuild ExplorerDataProvider.sln`.</span></span>

<span data-ttu-id="67989-126">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="67989-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="67989-127">開啟 Windows 檔案總管，然後流覽至 **ExplorerDataProvider** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="67989-127">Open Windows Explorer and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="67989-128">按兩下 ExplorerDataProvider .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="67989-128">Double-click the icon for the ExplorerDataProvider.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="67989-129">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="67989-129">From the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="67989-130">DLL 將會建立在預設的 \\ Debug 或 \\ Release 目錄中。</span><span class="sxs-lookup"><span data-stu-id="67989-130">The DLL will be built in the default \\Debug or \\Release directory.</span></span>

> [!Note]  
> <span data-ttu-id="67989-131">在 Windows SDK 中包含的此範例版本中，64位發行組建的設定不會在連結器的 **模組定義** 檔選項中包含 ExplorerDataProvider .def 檔。</span><span class="sxs-lookup"><span data-stu-id="67989-131">In the version of this sample included in the Windows SDK, the configuration for the 64-bit Release build does not include the ExplorerDataProvider.def file in the linker's **Module Definition File** option.</span></span> <span data-ttu-id="67989-132">您必須自行指定該檔案，才能在64位環境中建立。</span><span class="sxs-lookup"><span data-stu-id="67989-132">You must specify that file yourself before building in a 64-bit environment.</span></span> <span data-ttu-id="67989-133">將這一行加入 `ModuleDefinitionFile="ExplorerDataProvider.def"` 至 VCLinkerTool 區段， (從 ExplorerDataProvider vcproj 檔案的行 329) 開始，如下所示：</span><span class="sxs-lookup"><span data-stu-id="67989-133">Add the line `ModuleDefinitionFile="ExplorerDataProvider.def"` to the VCLinkerTool section (begins at line 329) of the ExplorerDataProvider.vcproj file as shown here:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="67989-134">此範例從程式碼庫下載的版本已針對此問題更正，而不需要在您的部分進行任何額外的動作。</span><span class="sxs-lookup"><span data-stu-id="67989-134">The version of this sample downloadable from Code Gallery has been corrected for this issue and no extra action is required on your part.</span></span>
>
>  
>
> ## <a name="running-the-sample"></a><span data-ttu-id="67989-135">執行範例</span><span class="sxs-lookup"><span data-stu-id="67989-135">Running the Sample</span></span>
>
> 1.  <span data-ttu-id="67989-136">使用命令提示字元或 Windows 檔案總管，流覽至包含新 .dll 和 propdesc 檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="67989-136">Navigate to the directory that contains the new .dll and .propdesc file, using the command prompt or Windows Explorer.</span></span>
> 2.  <span data-ttu-id="67989-137">在命令列中，輸入 `regsvr32.exe` 。</span><span class="sxs-lookup"><span data-stu-id="67989-137">At the command line, type `regsvr32.exe`.</span></span>
>     > [!Note]  
>     > <span data-ttu-id="67989-138">如果您是從提高許可權的命令提示字元執行此命令，自我註冊也會自動註冊 propdesc 檔案。</span><span class="sxs-lookup"><span data-stu-id="67989-138">If you run this command from an elevated command prompt, the self-registration will also register the .propdesc file automatically.</span></span> <span data-ttu-id="67989-139">如果是從非提高許可權的命令提示字元執行，則命名空間延伸模組將可運作，但不含自訂屬性功能。</span><span class="sxs-lookup"><span data-stu-id="67989-139">If it is run from a non-elevated command prompt then the namespace extension will work, but without custom property functionality.</span></span>
>
>      
>
> 3.  <span data-ttu-id="67989-140">開啟 **我的電腦** 資料夾，並流覽該處有新的命名空間延伸模組。</span><span class="sxs-lookup"><span data-stu-id="67989-140">Open the **My Computer** folder and browse the new namespace extension present there.</span></span>
>
>  
>
>  
>


