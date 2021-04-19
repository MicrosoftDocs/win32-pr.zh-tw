---
description: 產生修補程式套件的建議方法是使用修補程式建立工具，例如 Msimsp.exe 和 Patchwiz.dll。 Msimsp.exe 工具僅適用于 Windows Installer 開發人員 Windows SDK 元件。
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106976641"
---
# <a name="msimspexe"></a><span data-ttu-id="19e95-104">Msimsp.exe</span><span class="sxs-lookup"><span data-stu-id="19e95-104">Msimsp.exe</span></span>

<span data-ttu-id="19e95-105">產生修補程式套件的建議方法是使用修補程式建立工具，例如 Msimsp.exe 和 [Patchwiz.dll](patchwiz-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="19e95-105">The recommended method for generating a patch package is to use patch creation tools such as Msimsp.exe and [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="19e95-106">Msimsp.exe 工具僅適用于 [Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="19e95-106">The Msimsp.exe tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="19e95-107">Msimsp.exe 是呼叫 [Patchwiz.dll](patchwiz-dll.md)的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="19e95-107">Msimsp.exe is a executable file that calls [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="19e95-108">此工具可用來建立修補程式套件，方法是將路徑傳遞至 patch 建立屬性檔 ( pcp 檔案) ，以及要建立之修補程式套件的路徑。</span><span class="sxs-lookup"><span data-stu-id="19e95-108">The tool can be used to create a patch package by passing in the path to a patch creation properties file (.pcp file) and the path to the patch package that is being created.</span></span> <span data-ttu-id="19e95-109">Msimsp 也可以用來建立記錄檔，並指定暫存資料夾，以儲存用來建立修補程式套件的轉換、封包和檔案。</span><span class="sxs-lookup"><span data-stu-id="19e95-109">Msimsp.ex can also be used to create a log file and to specify a temporary folder in which the transforms, cabinets, and files that are used to create the patch package are saved.</span></span>

<span data-ttu-id="19e95-110">Msimsp.exe 的命令列語法為：</span><span class="sxs-lookup"><span data-stu-id="19e95-110">The command-line syntax for Msimsp.exe is:</span></span>

<span data-ttu-id="19e95-111">*\[ Pcp \]* 檔案的 **Msimsp.exe s** 路徑- *\[ .msp \]* 檔案 **的 p** 路徑 **{options}**</span><span class="sxs-lookup"><span data-stu-id="19e95-111">**Msimsp.exe -s** *\[path to .pcp file\]* **-p** *\[path to .msp file\]* **{options}**</span></span>

<span data-ttu-id="19e95-112">命令列選項不區分大小寫，而且可以使用斜線分隔符號，而不是虛線。</span><span class="sxs-lookup"><span data-stu-id="19e95-112">The command-line options are not case-sensitive, and slash delimiters can be used instead of a dash.</span></span> <span data-ttu-id="19e95-113">如果未指定任何選項，Msimsp.exe 會顯示摘要資訊屬性目前的值。</span><span class="sxs-lookup"><span data-stu-id="19e95-113">If no options are specified, Msimsp.exe displays the current values of the summary Information properties.</span></span>

<dl> <dt>

<span data-ttu-id="19e95-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s 的**_\[ \] pcp 檔案路徑_</span><span class="sxs-lookup"><span data-stu-id="19e95-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[path to .pcp file\]_</span></span>
</dt> <dd>

<span data-ttu-id="19e95-115">這是必要的，其後必須接著修補程式建立屬性檔的路徑 ( pcp 副檔名) 。</span><span class="sxs-lookup"><span data-stu-id="19e95-115">This is required and must be followed by the path to the patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="19e95-116">如需詳細資訊，請參閱 [PatchWiz.dll](patchwiz-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="19e95-116">For more information, see [PatchWiz.dll](patchwiz-dll.md).</span></span>

</dd> <dt>

<span data-ttu-id="19e95-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-**_指向 .msp_ 檔案的 p 路徑</span><span class="sxs-lookup"><span data-stu-id="19e95-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_path to .msp file_</span></span>
</dt> <dd>

<span data-ttu-id="19e95-118">這是必要的，且後面接著 ( .msp 延伸模組) 所建立修補套件的路徑。</span><span class="sxs-lookup"><span data-stu-id="19e95-118">This is required and followed by the path to patch package that is being created (.msp extension).</span></span>

</dd> <dt>

<span data-ttu-id="19e95-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-**_暫存資料夾_ 的 f 路徑</span><span class="sxs-lookup"><span data-stu-id="19e95-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_path to temporary folder_</span></span>
</dt> <dd>

<span data-ttu-id="19e95-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="19e95-120">Optional.</span></span> <span data-ttu-id="19e95-121">後面接著暫存資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="19e95-121">Followed by path to temporary folder.</span></span> <span data-ttu-id="19e95-122">預設位置為% TMP% \\ ~ pcw \_ tmp \\ .。</span><span class="sxs-lookup"><span data-stu-id="19e95-122">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="19e95-123"><span id="-k"></span><span id="-K"></span>**-k**</span><span class="sxs-lookup"><span data-stu-id="19e95-123"><span id="-k"></span><span id="-K"></span>**-k**</span></span>
</dt> <dd>

<span data-ttu-id="19e95-124">選擇性。</span><span class="sxs-lookup"><span data-stu-id="19e95-124">Optional.</span></span> <span data-ttu-id="19e95-125">如果暫存資料夾已存在，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="19e95-125">Fail if the temporary folder already exists.</span></span>

</dd> <dt>

<span data-ttu-id="19e95-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_記錄_ 檔的路徑</span><span class="sxs-lookup"><span data-stu-id="19e95-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_path to log file_</span></span>
</dt> <dd>

<span data-ttu-id="19e95-127">選擇性。</span><span class="sxs-lookup"><span data-stu-id="19e95-127">Optional.</span></span> <span data-ttu-id="19e95-128">後面接著記錄檔的路徑，說明修補程式建立程式和錯誤。</span><span class="sxs-lookup"><span data-stu-id="19e95-128">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="19e95-129">如需詳細資訊，請參閱 UiCreatePatchPackage 的傳回 [值](return-values-for-uicreatepatchpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="19e95-129">For more information, see [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="19e95-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-**_具有效能資料之記錄_ 檔的 lp 路徑</span><span class="sxs-lookup"><span data-stu-id="19e95-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-lp**_path to log file with performance data_</span></span>
</dt> <dd>

<span data-ttu-id="19e95-131">選擇性。</span><span class="sxs-lookup"><span data-stu-id="19e95-131">Optional.</span></span> <span data-ttu-id="19e95-132">後面接著記錄檔的路徑，說明修補程式建立程式和錯誤。</span><span class="sxs-lookup"><span data-stu-id="19e95-132">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="19e95-133">此選項會將效能資料寫入至記錄檔。</span><span class="sxs-lookup"><span data-stu-id="19e95-133">This option writes performance data to log file.</span></span> <span data-ttu-id="19e95-134">此選項需要4.0 版的 Patchwiz.dll。</span><span class="sxs-lookup"><span data-stu-id="19e95-134">This option requires version 4.0 of Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="19e95-135"><span id="-d"></span><span id="-D"></span>**-d.ddd...e**</span><span class="sxs-lookup"><span data-stu-id="19e95-135"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="19e95-136">選擇性。</span><span class="sxs-lookup"><span data-stu-id="19e95-136">Optional.</span></span> <span data-ttu-id="19e95-137">如果修補程式建立順利完成，則會顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="19e95-137">Displays a dialog if the patch creation completes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="19e95-138"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="19e95-138"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="19e95-139">顯示命令列說明。</span><span class="sxs-lookup"><span data-stu-id="19e95-139">Displays command-line help.</span></span>

</dd> </dl>

> [!Note]
> <span data-ttu-id="19e95-140">如果安裝 [套件的檔案](file-table.md) 資料行中有值只有大小寫不同，Msimsp.exe 可能會在呼叫 Makecab.exe 時失敗。</span><span class="sxs-lookup"><span data-stu-id="19e95-140">Msimsp.exe can fail when it calls Makecab.exe if there are values in the File column of the [File table](file-table.md) of the installation package that differ only by case.</span></span> <span data-ttu-id="19e95-141">Windows Installer 會區分大小寫，而且只有在 Comp1 和 Comp2 安裝到不同的目錄時，才允許安裝套件，例如下表中的。</span><span class="sxs-lookup"><span data-stu-id="19e95-141">Windows Installer is case-sensitive and allows an installation package such as in the table below only when Comp1 and Comp2 are installed into different directories.</span></span> <span data-ttu-id="19e95-142">不過，在此案例中，您無法使用 Msimsp.exe 或 [Patchwiz.dll](patchwiz-dll.md) 來產生封裝的修補程式，因為 Msimsp.exe 和 Patchwiz.dll 呼叫不區分大小寫的 Makecab.exe。</span><span class="sxs-lookup"><span data-stu-id="19e95-142">However, in this scenario you cannot use Msimsp.exe or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package, because Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive.</span></span>
> 
> <span data-ttu-id="19e95-143">避免撰寫安裝套件，例如下列部分檔案 [資料表](file-table.md)。</span><span class="sxs-lookup"><span data-stu-id="19e95-143">Avoid authoring an installation package such as the following partial [File table](file-table.md).</span></span>
> 
> | <span data-ttu-id="19e95-144">檔案</span><span class="sxs-lookup"><span data-stu-id="19e95-144">File</span></span>       | <span data-ttu-id="19e95-145">元件\_</span><span class="sxs-lookup"><span data-stu-id="19e95-145">Component\_</span></span> | <span data-ttu-id="19e95-146">FileName</span><span class="sxs-lookup"><span data-stu-id="19e95-146">FileName</span></span>   |
> |------------|-------------|------------|
> | <span data-ttu-id="19e95-147">readme.txt</span><span class="sxs-lookup"><span data-stu-id="19e95-147">readme.txt</span></span> | <span data-ttu-id="19e95-148">Comp1</span><span class="sxs-lookup"><span data-stu-id="19e95-148">Comp1</span></span>       | <span data-ttu-id="19e95-149">readme.txt</span><span class="sxs-lookup"><span data-stu-id="19e95-149">readme.txt</span></span> |
> | <span data-ttu-id="19e95-150">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="19e95-150">ReadMe.txt</span></span> | <span data-ttu-id="19e95-151">Comp2</span><span class="sxs-lookup"><span data-stu-id="19e95-151">Comp2</span></span>       | <span data-ttu-id="19e95-152">readme.txt</span><span class="sxs-lookup"><span data-stu-id="19e95-152">readme.txt</span></span> |


## <a name="related-topics"></a><span data-ttu-id="19e95-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="19e95-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19e95-154">建立修補程式套件</span><span class="sxs-lookup"><span data-stu-id="19e95-154">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="19e95-155">小型更新修補範例</span><span class="sxs-lookup"><span data-stu-id="19e95-155">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)
</dt> <dt>

[<span data-ttu-id="19e95-156">Windows Installer 開發工具</span><span class="sxs-lookup"><span data-stu-id="19e95-156">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="19e95-157">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="19e95-157">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



