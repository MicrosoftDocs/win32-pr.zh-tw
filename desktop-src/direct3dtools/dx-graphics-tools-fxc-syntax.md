---
title: Syntax
description: 以下是呼叫 FXC.exe （效果編譯器工具）的語法。 如需範例，請參閱離線編譯。
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- fxc.exe，語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106967502"
---
# <a name="syntax"></a><span data-ttu-id="7c770-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c770-105">Syntax</span></span>

<span data-ttu-id="7c770-106">以下是呼叫 FXC.exe （效果編譯器工具）的語法。</span><span class="sxs-lookup"><span data-stu-id="7c770-106">Here is the syntax for calling FXC.exe, the effect-compiler tool.</span></span> <span data-ttu-id="7c770-107">如需範例，請參閱 [離線編譯](dx-graphics-tools-fxc-using.md)。</span><span class="sxs-lookup"><span data-stu-id="7c770-107">For an example, see [Offline Compiling](dx-graphics-tools-fxc-using.md).</span></span>

-   [<span data-ttu-id="7c770-108">使用量</span><span class="sxs-lookup"><span data-stu-id="7c770-108">Usage</span></span>](#usage)
-   [<span data-ttu-id="7c770-109">引數</span><span class="sxs-lookup"><span data-stu-id="7c770-109">Arguments</span></span>](#arguments)
-   [<span data-ttu-id="7c770-110">備註</span><span class="sxs-lookup"><span data-stu-id="7c770-110">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="7c770-111">設定檔</span><span class="sxs-lookup"><span data-stu-id="7c770-111">Profiles</span></span>](#profiles)
-   [<span data-ttu-id="7c770-112">版本資訊</span><span class="sxs-lookup"><span data-stu-id="7c770-112">Version notes</span></span>](#version-notes)
-   [<span data-ttu-id="7c770-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c770-113">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="7c770-114">使用方式</span><span class="sxs-lookup"><span data-stu-id="7c770-114">Usage</span></span>

<span data-ttu-id="7c770-115">**Fxc.exe** *SwitchOptions* *檔案名*</span><span class="sxs-lookup"><span data-stu-id="7c770-115">**fxc** *SwitchOptions* *Filenames*</span></span>

## <a name="arguments"></a><span data-ttu-id="7c770-116">引數</span><span class="sxs-lookup"><span data-stu-id="7c770-116">Arguments</span></span>
<span data-ttu-id="7c770-117">以空格或冒號分隔每個參數選項。</span><span class="sxs-lookup"><span data-stu-id="7c770-117">Separate each switch option with a space or a colon.</span></span>

### <a name="switchoptions"></a><span data-ttu-id="7c770-118">*SwitchOptions*</span><span class="sxs-lookup"><span data-stu-id="7c770-118">*SwitchOptions*</span></span>
<span data-ttu-id="7c770-119">\[在 [ \] 編譯選項] 中。</span><span class="sxs-lookup"><span data-stu-id="7c770-119">\[in\] Compile options.</span></span> <span data-ttu-id="7c770-120">只有一個必要選項，其他則是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7c770-120">There is just one required option, and many more that are optional.</span></span> <span data-ttu-id="7c770-121">以空格或冒號分隔每一個。</span><span class="sxs-lookup"><span data-stu-id="7c770-121">Separate each with a space or colon.</span></span>

#### <a name="required-option"></a><span data-ttu-id="7c770-122">必要選項</span><span class="sxs-lookup"><span data-stu-id="7c770-122">Required option</span></span>
##### <a name="t-profile"></a><span data-ttu-id="7c770-123">/T <*設定檔*></span><span class="sxs-lookup"><span data-stu-id="7c770-123">/T <*profile*></span></span>
<span data-ttu-id="7c770-124">著色器模型 (查看 [設定檔](#profiles)) 。</span><span class="sxs-lookup"><span data-stu-id="7c770-124">Shader model (see [Profiles](#profiles)).</span></span>

#### <a name="optional-options"></a><span data-ttu-id="7c770-125">選擇性的選項</span><span class="sxs-lookup"><span data-stu-id="7c770-125">Optional options</span></span>
##### <a name="-help"></a><span data-ttu-id="7c770-126">/?、/help</span><span class="sxs-lookup"><span data-stu-id="7c770-126">/?, /help</span></span>
<span data-ttu-id="7c770-127">列印的說明 `FXC.exe` 。</span><span class="sxs-lookup"><span data-stu-id="7c770-127">Print help for `FXC.exe`.</span></span>

##### <a name="commandoptionfile"></a><span data-ttu-id="7c770-128">@<*command. file*></span><span class="sxs-lookup"><span data-stu-id="7c770-128">@<*command.option.file*></span></span>
<span data-ttu-id="7c770-129">包含其他編譯選項的檔案。</span><span class="sxs-lookup"><span data-stu-id="7c770-129">File that contains additional compile options.</span></span> <span data-ttu-id="7c770-130">您可以使用其他命令列編譯選項來混合這個選項。</span><span class="sxs-lookup"><span data-stu-id="7c770-130">This option can be mixed with other command line compile options.</span></span> <span data-ttu-id="7c770-131">*命令*。檔案只能包含每行一個選項。</span><span class="sxs-lookup"><span data-stu-id="7c770-131">The *command.option.file* must contain only one option per line.</span></span> <span data-ttu-id="7c770-132">*命令。* 檔案不能包含任何空白行。</span><span class="sxs-lookup"><span data-stu-id="7c770-132">The *command.option.file* cannot contain any blank lines.</span></span> <span data-ttu-id="7c770-133">檔案中指定的選項不能包含任何開頭或尾端空格。</span><span class="sxs-lookup"><span data-stu-id="7c770-133">Options specified in the file must not contain any leading or trailing spaces.</span></span>

##### <a name="all_resources_bound"></a><span data-ttu-id="7c770-134">/all_resources_bound</span><span class="sxs-lookup"><span data-stu-id="7c770-134">/all_resources_bound</span></span>
<span data-ttu-id="7c770-135">啟用 SM 5.1 + 中的積極壓平合併。</span><span class="sxs-lookup"><span data-stu-id="7c770-135">Enable aggressive flattening in SM5.1+.</span></span> <span data-ttu-id="7c770-136">適用于 Direct3D 12 的新。</span><span class="sxs-lookup"><span data-stu-id="7c770-136">New for Direct3D 12.</span></span>

##### <a name="cc"></a><span data-ttu-id="7c770-137">/Cc</span><span class="sxs-lookup"><span data-stu-id="7c770-137">/Cc</span></span>
<span data-ttu-id="7c770-138">輸出色彩標示的元件。</span><span class="sxs-lookup"><span data-stu-id="7c770-138">Output color-coded assembly.</span></span>

##### <a name="compress"></a><span data-ttu-id="7c770-139">/compress</span><span class="sxs-lookup"><span data-stu-id="7c770-139">/compress</span></span>
<span data-ttu-id="7c770-140">壓縮檔案中的 DX10 著色器位元組檔。</span><span class="sxs-lookup"><span data-stu-id="7c770-140">Compress DX10 shader bytecode from files.</span></span>

##### <a name="d-idtext"></a><span data-ttu-id="7c770-141">/D <*識別碼* >=< *文字*></span><span class="sxs-lookup"><span data-stu-id="7c770-141">/D <*id*>=<*text*></span></span>
<span data-ttu-id="7c770-142">定義宏。</span><span class="sxs-lookup"><span data-stu-id="7c770-142">Define macro.</span></span>

##### <a name="decompress"></a><span data-ttu-id="7c770-143">/decompress</span><span class="sxs-lookup"><span data-stu-id="7c770-143">/decompress</span></span>
<span data-ttu-id="7c770-144">從第一個檔案解壓縮 DX10 著色器位元組碼。</span><span class="sxs-lookup"><span data-stu-id="7c770-144">Decompress DX10 shader bytecode from first file.</span></span> <span data-ttu-id="7c770-145">輸出檔案應該依壓縮期間的順序列出。</span><span class="sxs-lookup"><span data-stu-id="7c770-145">Output files should be listed in the order they were in during compression.</span></span>

##### <a name="dumpbin"></a><span data-ttu-id="7c770-146">/dumpbin</span><span class="sxs-lookup"><span data-stu-id="7c770-146">/dumpbin</span></span>
<span data-ttu-id="7c770-147">載入二進位檔案，而不是編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="7c770-147">Loads a binary file rather than compiling a shader.</span></span>

##### <a name="e-name"></a><span data-ttu-id="7c770-148">/E <name></span><span class="sxs-lookup"><span data-stu-id="7c770-148">/E <name></span></span>
<span data-ttu-id="7c770-149">著色器進入點。</span><span class="sxs-lookup"><span data-stu-id="7c770-149">Shader entry point.</span></span> <span data-ttu-id="7c770-150">如果未指定任何進入點，則會將 **main** 視為著色器專案名稱。</span><span class="sxs-lookup"><span data-stu-id="7c770-150">If no entry point is given, **main** is considered to be the shader entry name.</span></span>

##### <a name="enable_unbounded_descriptor_tables"></a><span data-ttu-id="7c770-151">/enable_unbounded_descriptor_tables</span><span class="sxs-lookup"><span data-stu-id="7c770-151">/enable_unbounded_descriptor_tables</span></span>
<span data-ttu-id="7c770-152">啟用未系結的描述中繼資料表。</span><span class="sxs-lookup"><span data-stu-id="7c770-152">Enables unbounded descriptor tables.</span></span> <span data-ttu-id="7c770-153">適用于 Direct3D 12 的新。</span><span class="sxs-lookup"><span data-stu-id="7c770-153">New for Direct3D 12.</span></span>

##### <a name="extractrootsignature-file"></a><span data-ttu-id="7c770-154">/extractrootsignature <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-154">/extractrootsignature <*file*></span></span>
<span data-ttu-id="7c770-155">從著色器位元組路徑解壓縮根簽章。</span><span class="sxs-lookup"><span data-stu-id="7c770-155">Extract root signature from shader bytecode.</span></span> <span data-ttu-id="7c770-156">適用于 Direct3D 12 的新。</span><span class="sxs-lookup"><span data-stu-id="7c770-156">New for Direct3D 12.</span></span>

##### <a name="fc-file"></a><span data-ttu-id="7c770-157">/Fc <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-157">/Fc <*file*></span></span>
<span data-ttu-id="7c770-158">輸出元件碼清單檔。</span><span class="sxs-lookup"><span data-stu-id="7c770-158">Output assembly code listing file.</span></span>

##### <a name="fd-file"></a><span data-ttu-id="7c770-159">/Fd <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-159">/Fd <*file*></span></span>
<span data-ttu-id="7c770-160">將著色器程式資料庫 (PDB) 資訊中解壓縮，並寫入至指定的檔案。當您編譯著色器時，請使用/Fd 來產生具有著色器調試資訊的 PDB 檔案。</span><span class="sxs-lookup"><span data-stu-id="7c770-160">Extract shader program database (PDB) info and write to the given file.When you compile the shader, use /Fd to generate a PDB file with shader debugging info.</span></span>

##### <a name="fe-file"></a><span data-ttu-id="7c770-161">/Fe <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-161">/Fe <*file*></span></span>
<span data-ttu-id="7c770-162">將警告和錯誤輸出到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="7c770-162">Output warnings and errors to the given file.</span></span>

##### <a name="fh-file"></a><span data-ttu-id="7c770-163">/Fh <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-163">/Fh <*file*></span></span>
<span data-ttu-id="7c770-164">包含物件代碼的輸出標頭檔。</span><span class="sxs-lookup"><span data-stu-id="7c770-164">Output header file containing object code.</span></span>

##### <a name="fl-file"></a><span data-ttu-id="7c770-165">/Fl <*檔案*</span><span class="sxs-lookup"><span data-stu-id="7c770-165">/Fl <*file*</span></span>
<span data-ttu-id="7c770-166">輸出程式庫。</span><span class="sxs-lookup"><span data-stu-id="7c770-166">Output a library.</span></span> <span data-ttu-id="7c770-167">需要 D3dcompiler \_47.dll 或更新版本的 DLL。</span><span class="sxs-lookup"><span data-stu-id="7c770-167">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="fo-file"></a><span data-ttu-id="7c770-168">/Fo <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-168">/Fo <*file*></span></span>
<span data-ttu-id="7c770-169">輸出物件檔案。</span><span class="sxs-lookup"><span data-stu-id="7c770-169">Output object file.</span></span> <span data-ttu-id="7c770-170">通常 &quot; 會提供 fxc.exe &quot; ，不過會使用其他副檔名，例如 &quot; ： o &quot; 、 &quot; .obj &quot; 或 &quot; . dxbc &quot; 。</span><span class="sxs-lookup"><span data-stu-id="7c770-170">Often given the extension &quot;.fxc&quot;, though other extensions are used, such as &quot;.o&quot;, &quot;.obj&quot; or &quot;.dxbc&quot;.</span></span>

##### <a name="fx-file"></a><span data-ttu-id="7c770-171">/Fx <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-171">/Fx <*file*></span></span>
<span data-ttu-id="7c770-172">輸出元件碼和十六進位清單檔。</span><span class="sxs-lookup"><span data-stu-id="7c770-172">Output assembly code and hex listing file.</span></span>

##### <a name="gch"></a><span data-ttu-id="7c770-173">/Gch</span><span class="sxs-lookup"><span data-stu-id="7c770-173">/Gch</span></span>
<span data-ttu-id="7c770-174">編譯為 fx_4_x 設定檔的子效果。</span><span class="sxs-lookup"><span data-stu-id="7c770-174">Compile as a child effect for fx_4_x profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="7c770-175">舊版效果設定檔的支援已淘汰。</span><span class="sxs-lookup"><span data-stu-id="7c770-175">Support for legacy Effects profiles is deprecated.</span></span>

##### <a name="gdp"></a><span data-ttu-id="7c770-176">/Gdp</span><span class="sxs-lookup"><span data-stu-id="7c770-176">/Gdp</span></span>
<span data-ttu-id="7c770-177">停用效果效能模式。</span><span class="sxs-lookup"><span data-stu-id="7c770-177">Disable effect performance mode.</span></span>

##### <a name="gec"></a><span data-ttu-id="7c770-178">/Gec</span><span class="sxs-lookup"><span data-stu-id="7c770-178">/Gec</span></span>
<span data-ttu-id="7c770-179">啟用回溯相容性模式。</span><span class="sxs-lookup"><span data-stu-id="7c770-179">Enable backward compatibility mode.</span></span>

##### <a name="ges"></a><span data-ttu-id="7c770-180">/Ges</span><span class="sxs-lookup"><span data-stu-id="7c770-180">/Ges</span></span>
<span data-ttu-id="7c770-181">啟用 strict 模式。</span><span class="sxs-lookup"><span data-stu-id="7c770-181">Enable strict mode.</span></span>

##### <a name="getprivate-file"></a><span data-ttu-id="7c770-182">/getprivate <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-182">/getprivate <*file*></span></span>
<span data-ttu-id="7c770-183">將著色器 blob (編譯的著色器二進位) 中的私用資料儲存至指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="7c770-183">Save private data from the shader blob (compiled shader binary) to the given file.</span></span> <span data-ttu-id="7c770-184">從著色器 blob 中，解壓縮先前由/setprivate 內嵌的私用資料。</span><span class="sxs-lookup"><span data-stu-id="7c770-184">Extracts private data, previously embedded by /setprivate, from the shader blob.</span></span>

<span data-ttu-id="7c770-185">您必須使用/getprivate. 指定/dumpbin 選項</span><span class="sxs-lookup"><span data-stu-id="7c770-185">You must specify the /dumpbin option with /getprivate.</span></span> <span data-ttu-id="7c770-186">例如：</span><span class="sxs-lookup"><span data-stu-id="7c770-186">For example:</span></span>

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a><span data-ttu-id="7c770-187">/Gfa</span><span class="sxs-lookup"><span data-stu-id="7c770-187">/Gfa</span></span>
<span data-ttu-id="7c770-188">避免流量控制結構。</span><span class="sxs-lookup"><span data-stu-id="7c770-188">Avoid flow control constructs.</span></span>

##### <a name="gfp"></a><span data-ttu-id="7c770-189">/Gfp</span><span class="sxs-lookup"><span data-stu-id="7c770-189">/Gfp</span></span>
<span data-ttu-id="7c770-190">偏好使用流程式控制制結構。</span><span class="sxs-lookup"><span data-stu-id="7c770-190">Prefer flow control constructs.</span></span>

##### <a name="gis"></a><span data-ttu-id="7c770-191">/Gis</span><span class="sxs-lookup"><span data-stu-id="7c770-191">/Gis</span></span>
<span data-ttu-id="7c770-192">強制執行 IEEE 嚴謹度。</span><span class="sxs-lookup"><span data-stu-id="7c770-192">Force IEEE strictness.</span></span>

##### <a name="gpp"></a><span data-ttu-id="7c770-193">/Gpp</span><span class="sxs-lookup"><span data-stu-id="7c770-193">/Gpp</span></span>
<span data-ttu-id="7c770-194">強制部分有效位數。</span><span class="sxs-lookup"><span data-stu-id="7c770-194">Force partial precision.</span></span>
    
##### <a name="i-include"></a><span data-ttu-id="7c770-195">/I <*包含*></span><span class="sxs-lookup"><span data-stu-id="7c770-195">/I <*include*></span></span>
<span data-ttu-id="7c770-196">其他 include 路徑。</span><span class="sxs-lookup"><span data-stu-id="7c770-196">Additional include path.</span></span>

##### <a name="lx"></a><span data-ttu-id="7c770-197">/Lx</span><span class="sxs-lookup"><span data-stu-id="7c770-197">/Lx</span></span>
<span data-ttu-id="7c770-198">輸出十六進位常值。</span><span class="sxs-lookup"><span data-stu-id="7c770-198">Output hexadecimal literals.</span></span> <span data-ttu-id="7c770-199">需要 D3dcompiler \_47.dll 或更新版本的 DLL。</span><span class="sxs-lookup"><span data-stu-id="7c770-199">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="matchuavs"></a><span data-ttu-id="7c770-200">/matchUAVs</span><span class="sxs-lookup"><span data-stu-id="7c770-200">/matchUAVs</span></span>
<span data-ttu-id="7c770-201">符合目前著色器中的範本著色器 UAV 位置配置。</span><span class="sxs-lookup"><span data-stu-id="7c770-201">Match template shader UAV slot allocations in the current shader.</span></span> <span data-ttu-id="7c770-202">如需詳細資訊，請參閱 <a href="#remarks">備註</a>。</span><span class="sxs-lookup"><span data-stu-id="7c770-202">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="mergeuavs"></a><span data-ttu-id="7c770-203">/mergeUAVs</span><span class="sxs-lookup"><span data-stu-id="7c770-203">/mergeUAVs</span></span>
<span data-ttu-id="7c770-204">合併 UAV 位置配置範本著色器和目前的著色器。</span><span class="sxs-lookup"><span data-stu-id="7c770-204">Merge UAV slot allocations of template shader and the current shader.</span></span> <span data-ttu-id="7c770-205">如需詳細資訊，請參閱 <a href=""></a> <a href="#remarks">備註</a>。</span><span class="sxs-lookup"><span data-stu-id="7c770-205">For more info, see <a href=""></a><a href="#remarks">Remarks</a>.</span></span>

##### <a name="ni"></a><span data-ttu-id="7c770-206">/Ni</span><span class="sxs-lookup"><span data-stu-id="7c770-206">/Ni</span></span>
<span data-ttu-id="7c770-207">在元件清單中輸出指令編號。</span><span class="sxs-lookup"><span data-stu-id="7c770-207">Output instruction numbers in assembly listings.</span></span>

##### <a name="no"></a><span data-ttu-id="7c770-208">/No</span><span class="sxs-lookup"><span data-stu-id="7c770-208">/No</span></span>
<span data-ttu-id="7c770-209">元件清單中的輸出指示位元組位移。</span><span class="sxs-lookup"><span data-stu-id="7c770-209">Output instruction byte offset in assembly listings.</span></span> <span data-ttu-id="7c770-210">當您產生元件時，請使用/No 來標注每個指令的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="7c770-210">When you produce assembly, use /No to annotate it with the byte offset for each instruction.</span></span>

##### <a name="nologo"></a><span data-ttu-id="7c770-211">/nologo</span><span class="sxs-lookup"><span data-stu-id="7c770-211">/nologo</span></span>
<span data-ttu-id="7c770-212">隱藏著作權訊息。</span><span class="sxs-lookup"><span data-stu-id="7c770-212">Suppress copyright message.</span></span>

##### <a name="od"></a><span data-ttu-id="7c770-213">/Od</span><span class="sxs-lookup"><span data-stu-id="7c770-213">/Od</span></span>
<span data-ttu-id="7c770-214">停用最佳化。</span><span class="sxs-lookup"><span data-stu-id="7c770-214">Disable optimizations.</span></span> <span data-ttu-id="7c770-215">/Od 意指/Gfp，不過輸出可能與/Od/Gfp. 相同</span><span class="sxs-lookup"><span data-stu-id="7c770-215">/Od implies /Gfp, though output may not be identical to /Od /Gfp.</span></span>

##### <a name="op"></a><span data-ttu-id="7c770-216">/Op</span><span class="sxs-lookup"><span data-stu-id="7c770-216">/Op</span></span>
<span data-ttu-id="7c770-217">停用 preshaders (已淘汰的) 。</span><span class="sxs-lookup"><span data-stu-id="7c770-217">Disable preshaders (deprecated).</span></span>

##### <a name="o0-o1-o2-o3"></a><span data-ttu-id="7c770-218">/O0/O1、/O2、/O3</span><span class="sxs-lookup"><span data-stu-id="7c770-218">/O0 /O1, /O2, /O3</span></span>
<span data-ttu-id="7c770-219">優化層級。</span><span class="sxs-lookup"><span data-stu-id="7c770-219">Optimization levels.</span></span> <span data-ttu-id="7c770-220">[O1] 是預設設定。</span><span class="sxs-lookup"><span data-stu-id="7c770-220">O1 is the default setting.</span></span>
- <span data-ttu-id="7c770-221">O0-停用指令重新排列。</span><span class="sxs-lookup"><span data-stu-id="7c770-221">O0 - Disables instruction reordering.</span></span> <span data-ttu-id="7c770-222">這有助於減少暫存器負載，並啟用更快的迴圈模擬。</span><span class="sxs-lookup"><span data-stu-id="7c770-222">This helps reduce register load and enables faster loop simulation.</span></span>
- <span data-ttu-id="7c770-223">O1-停用 ps_3_0 和更新的指令重新排列。</span><span class="sxs-lookup"><span data-stu-id="7c770-223">O1 - Disables instruction reordering for ps_3_0 and up.</span></span>
- <span data-ttu-id="7c770-224">O2-與 O1 相同。</span><span class="sxs-lookup"><span data-stu-id="7c770-224">O2 - Same as O1.</span></span> <span data-ttu-id="7c770-225">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="7c770-225">Reserved for future use.</span></span>
- <span data-ttu-id="7c770-226">O3-與 O1 相同。</span><span class="sxs-lookup"><span data-stu-id="7c770-226">O3 - Same as O1.</span></span> <span data-ttu-id="7c770-227">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="7c770-227">Reserved for future use.</span></span>

##### <a name="p-file"></a><span data-ttu-id="7c770-228">/P <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-228">/P <*file*></span></span>
<span data-ttu-id="7c770-229">前置處理至檔案 (必須單獨使用) 。</span><span class="sxs-lookup"><span data-stu-id="7c770-229">Preprocess to file (must be used alone).</span></span>

##### <a name="qstrip_debug"></a><span data-ttu-id="7c770-230">/Qstrip_debug</span><span class="sxs-lookup"><span data-stu-id="7c770-230">/Qstrip_debug</span></span>
<span data-ttu-id="7c770-231">從 4_0 + 設定檔的著色器位元組程式碼中去除偵錯工具資料。</span><span class="sxs-lookup"><span data-stu-id="7c770-231">Strip debug data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_priv"></a><span data-ttu-id="7c770-232">/Qstrip_priv</span><span class="sxs-lookup"><span data-stu-id="7c770-232">/Qstrip_priv</span></span>
<span data-ttu-id="7c770-233">從 4_0 + 著色器位元組線中去除私用資料。</span><span class="sxs-lookup"><span data-stu-id="7c770-233">Strip the private data from 4_0+ shader bytecode.</span></span> <span data-ttu-id="7c770-234">從著色器 blob 中移除私用資料 (任意) 位元組序列， (您先前以選項內嵌的編譯著色器二進位) `/setprivate <file>` 。</span><span class="sxs-lookup"><span data-stu-id="7c770-234">Removes private data (arbitrary sequence of bytes) from the shader blob (compiled shader binary) that you previously embedded with the `/setprivate <file>` option.</span></span>

<span data-ttu-id="7c770-235">您必須使用/Qstrip_priv 指定/dumpbin 選項。</span><span class="sxs-lookup"><span data-stu-id="7c770-235">You must specify the /dumpbin option with /Qstrip_priv.</span></span> <span data-ttu-id="7c770-236">例如：</span><span class="sxs-lookup"><span data-stu-id="7c770-236">For example:</span></span>

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a><span data-ttu-id="7c770-237">/Qstrip_reflect</span><span class="sxs-lookup"><span data-stu-id="7c770-237">/Qstrip_reflect</span></span>
<span data-ttu-id="7c770-238">從 4_0 + 設定檔的著色器位元組程式碼中，去除反映資料。</span><span class="sxs-lookup"><span data-stu-id="7c770-238">Strip reflection data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_rootsignature"></a><span data-ttu-id="7c770-239">/Qstrip_rootsignature</span><span class="sxs-lookup"><span data-stu-id="7c770-239">/Qstrip_rootsignature</span></span>
<span data-ttu-id="7c770-240">從著色器位元組路徑中去除根簽章。</span><span class="sxs-lookup"><span data-stu-id="7c770-240">Strip root signature from shader bytecode.</span></span> <span data-ttu-id="7c770-241">適用于 Direct3D 12 的新。</span><span class="sxs-lookup"><span data-stu-id="7c770-241">New for Direct3D 12.</span></span>

##### <a name="res_may_alias"></a><span data-ttu-id="7c770-242">/res_may_alias</span><span class="sxs-lookup"><span data-stu-id="7c770-242">/res_may_alias</span></span>
<span data-ttu-id="7c770-243">假設 UAVs/SRVs 的別名可能是 cs_5_0 +。</span><span class="sxs-lookup"><span data-stu-id="7c770-243">Assume that UAVs/SRVs may alias for cs_5_0+.</span></span> <span data-ttu-id="7c770-244">需要 D3dcompiler \_47.dll 或更新版本的 DLL。</span><span class="sxs-lookup"><span data-stu-id="7c770-244">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="setprivate-file"></a><span data-ttu-id="7c770-245">/setprivate <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-245">/setprivate <*file*></span></span>
<span data-ttu-id="7c770-246">將指定檔案中的私用資料新增至已編譯的著色器 blob。</span><span class="sxs-lookup"><span data-stu-id="7c770-246">Add private data in the given file to the compiled shader blob.</span></span> <span data-ttu-id="7c770-247">將指定的檔案（被視為原始緩衝區）內嵌至著色器 blob。</span><span class="sxs-lookup"><span data-stu-id="7c770-247">Embeds the given file, which is treated as a raw buffer, to the shader blob.</span></span> <span data-ttu-id="7c770-248">當您編譯著色器時，請使用/setprivate 來新增私用資料。</span><span class="sxs-lookup"><span data-stu-id="7c770-248">Use /setprivate to add private data when you compile a shader.</span></span> <span data-ttu-id="7c770-249">或者，使用/dumpbin 選項搭配/setprivate 載入現有的著色器物件，然後在物件位於記憶體中之後，加入私用資料 blob。</span><span class="sxs-lookup"><span data-stu-id="7c770-249">Or, use the /dumpbin option with /setprivate to load an existing shader object, and then after the object is in memory, to add the private data blob.</span></span> <span data-ttu-id="7c770-250">例如，您可以使用單一命令搭配/setprivate，將私用資料新增至編譯的著色器 blob：</span><span class="sxs-lookup"><span data-stu-id="7c770-250">For example, use either a single command with /setprivate to add private data to a compiled shader blob:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
<span data-ttu-id="7c770-251">或者，使用第二個命令載入著色器物件，然後新增私用資料的兩個命令：</span><span class="sxs-lookup"><span data-stu-id="7c770-251">Or, use two commands where the second command loads a shader object and then adds private data:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a><span data-ttu-id="7c770-252">/setrootsignature <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-252">/setrootsignature <*file*></span></span>
<span data-ttu-id="7c770-253">將根簽章附加到著色器位元組程式碼。</span><span class="sxs-lookup"><span data-stu-id="7c770-253">Attach root signature to shader bytecode.</span></span> <span data-ttu-id="7c770-254">適用于 Direct3D 12 的新。</span><span class="sxs-lookup"><span data-stu-id="7c770-254">New for Direct3D 12.</span></span>

##### <a name="shtemplate-file"></a><span data-ttu-id="7c770-255">/shtemplate <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-255">/shtemplate <*file*></span></span>
<span data-ttu-id="7c770-256">使用指定的範本著色器檔案，將 (/mergeUAVs) 和相符的 (/matchUAVs) 資源合併。</span><span class="sxs-lookup"><span data-stu-id="7c770-256">Use given template shader file for merging (/mergeUAVs) and matching (/matchUAVs) resources.</span></span> <span data-ttu-id="7c770-257">如需詳細資訊，請參閱 <a href="#remarks">備註</a>。</span><span class="sxs-lookup"><span data-stu-id="7c770-257">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="vd"></a><span data-ttu-id="7c770-258">/Vd</span><span class="sxs-lookup"><span data-stu-id="7c770-258">/Vd</span></span>
<span data-ttu-id="7c770-259">停用驗證。</span><span class="sxs-lookup"><span data-stu-id="7c770-259">Disable validation.</span></span>

##### <a name="verifyrootsignature-file"></a><span data-ttu-id="7c770-260">/verifyrootsignature <*檔案*></span><span class="sxs-lookup"><span data-stu-id="7c770-260">/verifyrootsignature <*file*></span></span>
<span data-ttu-id="7c770-261">針對根簽章驗證著色器位元組的位元組。</span><span class="sxs-lookup"><span data-stu-id="7c770-261">Verify shader bytecode against root signature.</span></span> <span data-ttu-id="7c770-262">適用于 Direct3D 12 的新。</span><span class="sxs-lookup"><span data-stu-id="7c770-262">New for Direct3D 12.</span></span>

##### <a name="vi"></a><span data-ttu-id="7c770-263">/Vi</span><span class="sxs-lookup"><span data-stu-id="7c770-263">/Vi</span></span>
<span data-ttu-id="7c770-264">顯示包含進程的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7c770-264">Display details about the include process.</span></span>

##### <a name="vn-name"></a><span data-ttu-id="7c770-265">/Vn <*名稱*></span><span class="sxs-lookup"><span data-stu-id="7c770-265">/Vn <*name*></span></span>
<span data-ttu-id="7c770-266">在標頭檔中使用名稱作為變數名稱。</span><span class="sxs-lookup"><span data-stu-id="7c770-266">Use name as variable name in header file.</span></span>

##### <a name="wx"></a><span data-ttu-id="7c770-267">/WX</span><span class="sxs-lookup"><span data-stu-id="7c770-267">/WX</span></span>
<span data-ttu-id="7c770-268">將警告視為錯誤。</span><span class="sxs-lookup"><span data-stu-id="7c770-268">Treat warnings as errors.</span></span>

##### <a name="zi"></a><span data-ttu-id="7c770-269">/ZI</span><span class="sxs-lookup"><span data-stu-id="7c770-269">/Zi</span></span>
<span data-ttu-id="7c770-270">啟用偵錯資訊。</span><span class="sxs-lookup"><span data-stu-id="7c770-270">Enable debugging information.</span></span>

##### <a name="zpc"></a><span data-ttu-id="7c770-271">/Zpc</span><span class="sxs-lookup"><span data-stu-id="7c770-271">/Zpc</span></span>
<span data-ttu-id="7c770-272">在資料行中封裝矩陣-主要順序。</span><span class="sxs-lookup"><span data-stu-id="7c770-272">Pack matrices in column-major order.</span></span>

##### <a name="zpr"></a><span data-ttu-id="7c770-273">/Zpr</span><span class="sxs-lookup"><span data-stu-id="7c770-273">/Zpr</span></span>
<span data-ttu-id="7c770-274">封裝矩陣（依資料列排列）。</span><span class="sxs-lookup"><span data-stu-id="7c770-274">Pack matrices in row-major order.</span></span>

### <a name="filenames"></a><span data-ttu-id="7c770-275">*檔案名稱*</span><span class="sxs-lookup"><span data-stu-id="7c770-275">*Filenames*</span></span>

<span data-ttu-id="7c770-276">\[在 \] 包含著色器 () 和/或 (s) 效果的檔案中。</span><span class="sxs-lookup"><span data-stu-id="7c770-276">\[in\] The files that contains the shader(s) and/or the effect(s).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c770-277">備註</span><span class="sxs-lookup"><span data-stu-id="7c770-277">Remarks</span></span>

<span data-ttu-id="7c770-278">使用 `/mergeUAVs` 、 `/matchUAVs` 和 `/shtemplate` 選項來對齊一連串著色器的 UAV 系結位置。</span><span class="sxs-lookup"><span data-stu-id="7c770-278">Use the `/mergeUAVs`, `/matchUAVs`, and `/shtemplate` options to align the UAV binding slots for a chain of shaders.</span></span>

<span data-ttu-id="7c770-279">假設您有一個 fx、b. fx 和 .C 的著色器。</span><span class="sxs-lookup"><span data-stu-id="7c770-279">Suppose you have shaders A.fx, B.fx, and C.fx.</span></span> <span data-ttu-id="7c770-280">若要對齊這一層著色器的 UAV 系結位置，您需要兩個編譯階段：</span><span class="sxs-lookup"><span data-stu-id="7c770-280">To align the UAV binding slots for this chain of shaders, you need two passes of compilation:</span></span>

<span data-ttu-id="7c770-281">**對齊一連串著色器的 UAV 系結位置**</span><span class="sxs-lookup"><span data-stu-id="7c770-281">**To align the UAV binding slots for a chain of shaders**</span></span>

1.  <span data-ttu-id="7c770-282">使用/mergeUAVs 編譯著色器，並使用/shtemplate. 指定先前編譯的著色器 blob</span><span class="sxs-lookup"><span data-stu-id="7c770-282">Use /mergeUAVs to compile shaders, and specify a previously-compiled shader blob with /shtemplate.</span></span> <span data-ttu-id="7c770-283">例如：</span><span class="sxs-lookup"><span data-stu-id="7c770-283">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  <span data-ttu-id="7c770-284">使用/matchUAVs 編譯著色器，並使用/shtemplate. 從第一次行程指定最後一個著色器 blob</span><span class="sxs-lookup"><span data-stu-id="7c770-284">Use /matchUAVs to compile shaders, and specify the last shader blob from the first pass with /shtemplate.</span></span> <span data-ttu-id="7c770-285">您可以依任何順序進行編譯。</span><span class="sxs-lookup"><span data-stu-id="7c770-285">You can compile in any order.</span></span> <span data-ttu-id="7c770-286">例如：</span><span class="sxs-lookup"><span data-stu-id="7c770-286">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
<span data-ttu-id="7c770-287">在第二個階段中，您不需要重新編譯 c.。</span><span class="sxs-lookup"><span data-stu-id="7c770-287">You don't have to recompile C.fx in the second pass.</span></span>

<span data-ttu-id="7c770-288">在您執行上述兩個編譯階段之後，您可以使用. o、b. o 和 c. 做為具有對齊 UAV 位置的最終著色器 blob。</span><span class="sxs-lookup"><span data-stu-id="7c770-288">After you perform the preceding two compilation passes, you can use A.o, B.o, and C.o as final shader blobs with aligned UAV slots.</span></span>

## <a name="profiles"></a><span data-ttu-id="7c770-289">Profiles</span><span class="sxs-lookup"><span data-stu-id="7c770-289">Profiles</span></span>

<span data-ttu-id="7c770-290">每個著色器模型都會加上 HLSL 設定檔的標籤。</span><span class="sxs-lookup"><span data-stu-id="7c770-290">Each shader model is labeled with an HLSL profile.</span></span> <span data-ttu-id="7c770-291">若要針對特定著色器模型編譯著色器，請從下表中選擇適當的著色器設定檔。</span><span class="sxs-lookup"><span data-stu-id="7c770-291">To compile a shader against a particular shader model, choose the appropriate shader profile from the following table.</span></span>

<table><thead><tr class="header"><th><span data-ttu-id="7c770-292">著色器類型</span><span class="sxs-lookup"><span data-stu-id="7c770-292">Shader Type</span></span></th><th><span data-ttu-id="7c770-293">Profiles</span><span class="sxs-lookup"><span data-stu-id="7c770-293">Profiles</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="7c770-294">計算著色器</span><span class="sxs-lookup"><span data-stu-id="7c770-294">Compute Shader</span></span></td><td><dl> <span data-ttu-id="7c770-295">cs_4_0</span><span class="sxs-lookup"><span data-stu-id="7c770-295">cs_4_0</span></span><br />
<span data-ttu-id="7c770-296">cs_4_1</span><span class="sxs-lookup"><span data-stu-id="7c770-296">cs_4_1</span></span><br />
<span data-ttu-id="7c770-297">cs_5_0</span><span class="sxs-lookup"><span data-stu-id="7c770-297">cs_5_0</span></span><br />
<span data-ttu-id="7c770-298">cs_5_1</span><span class="sxs-lookup"><span data-stu-id="7c770-298">cs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="7c770-299">網域著色器</span><span class="sxs-lookup"><span data-stu-id="7c770-299">Domain Shader</span></span></td><td><dl> <span data-ttu-id="7c770-300">ds_5_0</span><span class="sxs-lookup"><span data-stu-id="7c770-300">ds_5_0</span></span><br />
<span data-ttu-id="7c770-301">ds_5_1</span><span class="sxs-lookup"><span data-stu-id="7c770-301">ds_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="7c770-302">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="7c770-302">Geometry Shader</span></span></td><td><dl> <span data-ttu-id="7c770-303">gs_4_0</span><span class="sxs-lookup"><span data-stu-id="7c770-303">gs_4_0</span></span><br />
<span data-ttu-id="7c770-304">gs_4_1</span><span class="sxs-lookup"><span data-stu-id="7c770-304">gs_4_1</span></span><br />
<span data-ttu-id="7c770-305">gs_5_0</span><span class="sxs-lookup"><span data-stu-id="7c770-305">gs_5_0</span></span><br />
<span data-ttu-id="7c770-306">gs_5_1</span><span class="sxs-lookup"><span data-stu-id="7c770-306">gs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="7c770-307">HLSL 著色器連結</span><span class="sxs-lookup"><span data-stu-id="7c770-307">HLSL shader linking</span></span> </td><td><dl> <span data-ttu-id="7c770-308">lib_4_0</span><span class="sxs-lookup"><span data-stu-id="7c770-308">lib_4_0</span></span><br />
<span data-ttu-id="7c770-309">lib_4_1</span><span class="sxs-lookup"><span data-stu-id="7c770-309">lib_4_1</span></span><br />
<span data-ttu-id="7c770-310">lib_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="7c770-310">lib_4_0_level_9_1</span></span><br />
<span data-ttu-id="7c770-311">lib_4_0_level_9_1_vs_only</span><span class="sxs-lookup"><span data-stu-id="7c770-311">lib_4_0_level_9_1_vs_only</span></span><br />
<span data-ttu-id="7c770-312">lib_4_0_level_9_1_ps_only</span><span class="sxs-lookup"><span data-stu-id="7c770-312">lib_4_0_level_9_1_ps_only</span></span><br />
<span data-ttu-id="7c770-313">lib_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="7c770-313">lib_4_0_level_9_3</span></span><br />
<span data-ttu-id="7c770-314">lib_4_0_level_9_3_vs_only</span><span class="sxs-lookup"><span data-stu-id="7c770-314">lib_4_0_level_9_3_vs_only</span></span><br />
<span data-ttu-id="7c770-315">lib_4_0_level_9_3_ps_only</span><span class="sxs-lookup"><span data-stu-id="7c770-315">lib_4_0_level_9_3_ps_only</span></span><br />
<span data-ttu-id="7c770-316">lib_5_0</span><span class="sxs-lookup"><span data-stu-id="7c770-316">lib_5_0</span></span><br />
</dl> <span data-ttu-id="7c770-317">如需著色器連結的詳細資訊，請參閱 <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> 和 <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="7c770-317">For more info about shader linking, see <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> and <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span></span> <br/></td></tr><tr class="odd"><td><span data-ttu-id="7c770-318">輪廓著色器</span><span class="sxs-lookup"><span data-stu-id="7c770-318">Hull Shader</span></span></td><td><dl> <span data-ttu-id="7c770-319">hs_5_0</span><span class="sxs-lookup"><span data-stu-id="7c770-319">hs_5_0</span></span><br />
<span data-ttu-id="7c770-320">hs_5_1</span><span class="sxs-lookup"><span data-stu-id="7c770-320">hs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="7c770-321">像素著色器</span><span class="sxs-lookup"><span data-stu-id="7c770-321">Pixel Shader</span></span></td><td><dl> <span data-ttu-id="7c770-322">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="7c770-322">ps_2_0</span></span><br />
<span data-ttu-id="7c770-323">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="7c770-323">ps_2_a</span></span><br />
<span data-ttu-id="7c770-324">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="7c770-324">ps_2_b</span></span><br />
<span data-ttu-id="7c770-325">ps_2_sw</span><span class="sxs-lookup"><span data-stu-id="7c770-325">ps_2_sw</span></span><br />
<span data-ttu-id="7c770-326">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="7c770-326">ps_3_0</span></span><br />
<span data-ttu-id="7c770-327">ps_3_sw</span><span class="sxs-lookup"><span data-stu-id="7c770-327">ps_3_sw</span></span><br />
<span data-ttu-id="7c770-328">ps_4_0</span><span class="sxs-lookup"><span data-stu-id="7c770-328">ps_4_0</span></span><br />
<span data-ttu-id="7c770-329">ps_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="7c770-329">ps_4_0_level_9_0</span></span><br />
<span data-ttu-id="7c770-330">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="7c770-330">ps_4_0_level_9_1</span></span><br />
<span data-ttu-id="7c770-331">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="7c770-331">ps_4_0_level_9_3</span></span><br />
<span data-ttu-id="7c770-332">ps_4_1</span><span class="sxs-lookup"><span data-stu-id="7c770-332">ps_4_1</span></span><br />
<span data-ttu-id="7c770-333">ps_5_0</span><span class="sxs-lookup"><span data-stu-id="7c770-333">ps_5_0</span></span><br />
<span data-ttu-id="7c770-334">ps_5_1</span><span class="sxs-lookup"><span data-stu-id="7c770-334">ps_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="7c770-335">根簽章</span><span class="sxs-lookup"><span data-stu-id="7c770-335">Root Signature</span></span></td><td><dl> <span data-ttu-id="7c770-336">rootsig_1_0</span><span class="sxs-lookup"><span data-stu-id="7c770-336">rootsig_1_0</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="7c770-337">材質著色器</span><span class="sxs-lookup"><span data-stu-id="7c770-337">Texture Shader</span></span></td><td><dl> <span data-ttu-id="7c770-338">tx_1_0</span><span class="sxs-lookup"><span data-stu-id="7c770-338">tx_1_0</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="7c770-339">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="7c770-339">Vertex Shader</span></span></td><td><dl> <span data-ttu-id="7c770-340">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="7c770-340">vs_1_1</span></span><br />
<span data-ttu-id="7c770-341">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="7c770-341">vs_2_0</span></span><br />
<span data-ttu-id="7c770-342">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="7c770-342">vs_2_a</span></span><br />
<span data-ttu-id="7c770-343">vs_2_sw</span><span class="sxs-lookup"><span data-stu-id="7c770-343">vs_2_sw</span></span><br />
<span data-ttu-id="7c770-344">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="7c770-344">vs_3_0</span></span><br />
<span data-ttu-id="7c770-345">vs_3_sw</span><span class="sxs-lookup"><span data-stu-id="7c770-345">vs_3_sw</span></span><br />
<span data-ttu-id="7c770-346">vs_4_0</span><span class="sxs-lookup"><span data-stu-id="7c770-346">vs_4_0</span></span><br />
<span data-ttu-id="7c770-347">vs_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="7c770-347">vs_4_0_level_9_0</span></span><br />
<span data-ttu-id="7c770-348">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="7c770-348">vs_4_0_level_9_1</span></span><br />
<span data-ttu-id="7c770-349">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="7c770-349">vs_4_0_level_9_3</span></span><br />
<span data-ttu-id="7c770-350">vs_4_1</span><span class="sxs-lookup"><span data-stu-id="7c770-350">vs_4_1</span></span><br />
<span data-ttu-id="7c770-351">vs_5_0</span><span class="sxs-lookup"><span data-stu-id="7c770-351">vs_5_0</span></span><br />
<span data-ttu-id="7c770-352">vs_5_1</span><span class="sxs-lookup"><span data-stu-id="7c770-352">vs_5_1</span></span><br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a><span data-ttu-id="7c770-353">版本資訊</span><span class="sxs-lookup"><span data-stu-id="7c770-353">Version notes</span></span>

<span data-ttu-id="7c770-354">針對 Direct3D 12，請參閱在 [HLSL 中指定根](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl)簽章、 [在 HLSL 中使用資源](/windows/desktop/direct3d12/resource-binding-in-hlsl) 系結，以及 [使用 HLSL 5.1 的動態索引](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1)。</span><span class="sxs-lookup"><span data-stu-id="7c770-354">For Direct3D 12 refer to [Specifying Root Signatures in HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Resource Binding in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) and [Dynamic Indexing using HLSL 5.1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span></span>

<span data-ttu-id="7c770-355">在 Direct3D 10 中，藉由呼叫下列函式，使用 API 來取得最適合指定裝置的頂點、幾何和圖元著色器設定檔： [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile)、 [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)和 [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile)。</span><span class="sxs-lookup"><span data-stu-id="7c770-355">In Direct3D 10 use the API to get the vertex, geometry, and pixel-shader profile best suited to a given device by calling these functions: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile), and [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span></span>

<span data-ttu-id="7c770-356">在 Direct3D 9 中，您可以使用 [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) 或 [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) 方法來取出裝置所支援的頂點和圖元著色器設定檔。</span><span class="sxs-lookup"><span data-stu-id="7c770-356">In Direct3D 9 use the [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) or [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) methods to retrieve the vertex and pixel-shader profiles supported by a device.</span></span> <span data-ttu-id="7c770-357">這些方法所傳回的 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) 結構指出裝置在其 **VertexShaderVersion** 和 **PixelShaderVersion** 成員中所支援的頂點和圖元著色器設定檔。</span><span class="sxs-lookup"><span data-stu-id="7c770-357">The [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure returned by those methods indicates the vertex and pixel-shader profiles supported by a device in its **VertexShaderVersion** and **PixelShaderVersion** members.</span></span>

<span data-ttu-id="7c770-358">如需範例，請參閱 [使用目前的編譯器進行編譯](dx-graphics-tools-fxc-using.md)。</span><span class="sxs-lookup"><span data-stu-id="7c770-358">For examples, see [Compiling with the Current Compiler](dx-graphics-tools-fxc-using.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c770-359">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c770-359">Related topics</span></span>

* [<span data-ttu-id="7c770-360">效果-編譯器工具</span><span class="sxs-lookup"><span data-stu-id="7c770-360">Effect-Compiler Tool</span></span>](fxc.md)