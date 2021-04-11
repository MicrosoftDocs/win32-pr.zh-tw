---
description: 目錄資料表會指定產品的目錄配置。 資料表的每個資料列都表示來源與目標的目錄。
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: 目錄資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944554"
---
# <a name="directory-table"></a><span data-ttu-id="957b2-104">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="957b2-104">Directory Table</span></span>

<span data-ttu-id="957b2-105">目錄資料表會指定產品的目錄配置。</span><span class="sxs-lookup"><span data-stu-id="957b2-105">The Directory table specifies the directory layout for the product.</span></span> <span data-ttu-id="957b2-106">資料表的每個資料列都表示來源與目標的目錄。</span><span class="sxs-lookup"><span data-stu-id="957b2-106">Each row of the table indicates a directory both at the source and the target.</span></span>

<span data-ttu-id="957b2-107">目錄資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="957b2-107">The Directory table has the following columns.</span></span>



| <span data-ttu-id="957b2-108">Column</span><span class="sxs-lookup"><span data-stu-id="957b2-108">Column</span></span>            | <span data-ttu-id="957b2-109">類型</span><span class="sxs-lookup"><span data-stu-id="957b2-109">Type</span></span>                         | <span data-ttu-id="957b2-110">答案</span><span class="sxs-lookup"><span data-stu-id="957b2-110">Key</span></span> | <span data-ttu-id="957b2-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="957b2-111">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="957b2-112">目錄</span><span class="sxs-lookup"><span data-stu-id="957b2-112">Directory</span></span>         | [<span data-ttu-id="957b2-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="957b2-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="957b2-114">Y</span><span class="sxs-lookup"><span data-stu-id="957b2-114">Y</span></span>   | <span data-ttu-id="957b2-115">N</span><span class="sxs-lookup"><span data-stu-id="957b2-115">N</span></span>        |
| <span data-ttu-id="957b2-116">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="957b2-116">Directory\_Parent</span></span> | [<span data-ttu-id="957b2-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="957b2-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="957b2-118">N</span><span class="sxs-lookup"><span data-stu-id="957b2-118">N</span></span>   | <span data-ttu-id="957b2-119">Y</span><span class="sxs-lookup"><span data-stu-id="957b2-119">Y</span></span>        |
| <span data-ttu-id="957b2-120">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="957b2-120">DefaultDir</span></span>        | [<span data-ttu-id="957b2-121">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="957b2-121">DefaultDir</span></span>](defaultdir.md) | <span data-ttu-id="957b2-122">N</span><span class="sxs-lookup"><span data-stu-id="957b2-122">N</span></span>   | <span data-ttu-id="957b2-123">N</span><span class="sxs-lookup"><span data-stu-id="957b2-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="957b2-124">資料行</span><span class="sxs-lookup"><span data-stu-id="957b2-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="957b2-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>目錄</span><span class="sxs-lookup"><span data-stu-id="957b2-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory</span></span>
</dt> <dd>

<span data-ttu-id="957b2-126">目錄資料行包含目錄或目錄路徑的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="957b2-126">The Directory column contains a unique identifier for a directory or directory path.</span></span> <span data-ttu-id="957b2-127">此資料行可以包含屬性的名稱，該屬性會設定為目標目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="957b2-127">This column can contain the name of a property that is set to the full path of a target directory.</span></span> <span data-ttu-id="957b2-128">如果此資料行包含屬性，則目標目錄會使用 DefaultDir 資料行中指定的名稱，並採用目錄父資料行中指定的上層目錄 \_ 。</span><span class="sxs-lookup"><span data-stu-id="957b2-128">If this column contains a property, the target directory takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="957b2-129">來原始目錄一律採用 DefaultDir 資料行中指定的名稱，並採用目錄父資料行中指定的上層目錄 \_ 。</span><span class="sxs-lookup"><span data-stu-id="957b2-129">The source directory always takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="957b2-130">如果目錄 \_ 父資料行的值為 null 或等於目錄資料行的值，則目錄資料行代表根目標目錄。</span><span class="sxs-lookup"><span data-stu-id="957b2-130">If the Directory\_Parent column is either null or equal to the value of the Directory column, the Directory column represents a root target directory.</span></span> <span data-ttu-id="957b2-131">目錄資料表中只能指定一個根目錄。</span><span class="sxs-lookup"><span data-stu-id="957b2-131">Only one root directory may be specified in the Directory table.</span></span>

</dd> <dt>

<span data-ttu-id="957b2-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="957b2-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Directory\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="957b2-133">此資料行是目錄的上層目錄參考。</span><span class="sxs-lookup"><span data-stu-id="957b2-133">This column is a reference to the directory's parent directory.</span></span> <span data-ttu-id="957b2-134">具有 \_ 等於 null 或等於目錄資料行之目錄父資料行的記錄，代表根目錄。</span><span class="sxs-lookup"><span data-stu-id="957b2-134">A record that has a Directory\_Parent column equal to null or equal to the Directory column represents a root directory.</span></span> <span data-ttu-id="957b2-135">父目錄的完整路徑會以傳址方式解析，目錄 \_ 父資料行是目錄資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="957b2-135">The full path of the parent directory is resolved by reference in the Directory\_Parent column is an external key into the Directory column.</span></span> <span data-ttu-id="957b2-136">例如，如果資料夾具有名為 PDIR 的父目錄，則 PDIR 的父目錄會在目錄資料行中具有 PDIR 的資料列的目錄父資料行中提供 \_ 。</span><span class="sxs-lookup"><span data-stu-id="957b2-136">For example, if a folder has a parent directory named PDIR, the parent directory of PDIR is given in the Directory\_Parent column of the row with PDIR in the Directory column.</span></span>

</dd> <dt>

<span data-ttu-id="957b2-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span><span class="sxs-lookup"><span data-stu-id="957b2-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span></span>
</dt> <dd>

<span data-ttu-id="957b2-138">DefaultDir 資料行包含目錄名稱 (可當地語系化的) 在上層目錄下。</span><span class="sxs-lookup"><span data-stu-id="957b2-138">The DefaultDir column contains the directory's name (localizable)under the parent directory.</span></span> <span data-ttu-id="957b2-139">根據預設，這是目標和來原始目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="957b2-139">By default, this is the name of both the target and source directories.</span></span> <span data-ttu-id="957b2-140">若要指定不同的來源和目標目錄名稱，請以冒號分隔目標和來源名稱，如下所示： \[ targetname：未通過 \] \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="957b2-140">To specify different source and target directory names, separate the target and source names with a colon as follows: \[targetname\]:\[sourcename\].</span></span>

<span data-ttu-id="957b2-141">如果目錄父資料行的值 \_ 為 null 或等於目錄資料行，DefaultDir 資料行會指定根來原始目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="957b2-141">If the value of the Directory\_Parent column is null or is equal to the Directory column, the DefaultDir column specifies the name of a root source directory.</span></span>

<span data-ttu-id="957b2-142">針對非根目錄來原始目錄， (. ) 在來原始目錄名稱的 DefaultDir 資料行或目標目錄名稱中輸入，表示目錄應該位於其父目錄中，而不含子目錄。</span><span class="sxs-lookup"><span data-stu-id="957b2-142">For a non-root source directory, a period (.) entered in the DefaultDir column for the source directory name or the target directory name indicates the directory should be located in its parent directory without a subdirectory.</span></span>

<span data-ttu-id="957b2-143">此資料行中的目錄名稱可能會格式化為簡短的檔案名組 \| 長檔名組。</span><span class="sxs-lookup"><span data-stu-id="957b2-143">The directory names in this column may be formatted as short filename \| long filename pairs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="957b2-144">備註</span><span class="sxs-lookup"><span data-stu-id="957b2-144">Remarks</span></span>

<span data-ttu-id="957b2-145">資料表中的每一筆記錄都代表來源和目的地影像中的目錄。</span><span class="sxs-lookup"><span data-stu-id="957b2-145">Each record in the table represents a directory in both the source and the destination images.</span></span> <span data-ttu-id="957b2-146">目錄資料表必須指定目錄資料行值等於 [**TARGETDIR**](targetdir.md) 屬性的單一根目錄。</span><span class="sxs-lookup"><span data-stu-id="957b2-146">The Directory table must specify a single root directory with a Directory column value equal to the [**TARGETDIR**](targetdir.md) property.</span></span>

<span data-ttu-id="957b2-147">針對 [系統管理安裝](administrative-installation.md)，請將系統管理映射安裝到名為 TARGETDIR 的根目錄，並使用來原始目錄名稱來解析目標目錄。</span><span class="sxs-lookup"><span data-stu-id="957b2-147">For an [administrative installation](administrative-installation.md), install the administrative image into the root directory named TARGETDIR and use the source directory names to resolve the target directories.</span></span>

<span data-ttu-id="957b2-148">請注意，安裝程式會將一些標準 [屬性](properties.md) 設定為系統資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="957b2-148">Note the installer sets a number of standard [properties](properties.md) to system folder paths.</span></span> <span data-ttu-id="957b2-149">如需設定為系統資料夾的屬性清單，請參閱 [屬性參考](property-reference.md) 。</span><span class="sxs-lookup"><span data-stu-id="957b2-149">See the [Property Reference](property-reference.md) for a list of the properties that are set to system folders.</span></span>

<span data-ttu-id="957b2-150">目錄解析會在 [CostFinalize 動作](costfinalize-action.md) 期間執行，如下所示：</span><span class="sxs-lookup"><span data-stu-id="957b2-150">Directory resolution is performed during the [CostFinalize action](costfinalize-action.md) and is done as follows:</span></span>

### <a name="root-destination-directory"></a><span data-ttu-id="957b2-151">根目的地目錄</span><span class="sxs-lookup"><span data-stu-id="957b2-151">Root Destination Directory</span></span>

<span data-ttu-id="957b2-152">可能只有一個根目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="957b2-152">There may only be a single root destination directory.</span></span> <span data-ttu-id="957b2-153">若要指定根目的地目錄，請將 [目錄] 資料行設定為 [ [**TARGETDIR**](targetdir.md) ] 屬性，並將 [DefaultDir] 資料行設定為 [ [**SourceDir**](sourcedir.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="957b2-153">To specify the root destination directory, set the Directory column to the [**TARGETDIR**](targetdir.md) property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="957b2-154">如果定義了 **TARGETDIR** 屬性，則會將目的地目錄解析為屬性的值。</span><span class="sxs-lookup"><span data-stu-id="957b2-154">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="957b2-155">如果未定義 **TARGETDIR** 屬性，則會使用 [**ROOTDRIVE**](rootdrive.md) 屬性來解析路徑。</span><span class="sxs-lookup"><span data-stu-id="957b2-155">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span>

### <a name="root-source-directory"></a><span data-ttu-id="957b2-156">根來原始目錄</span><span class="sxs-lookup"><span data-stu-id="957b2-156">Root Source Directory</span></span>

<span data-ttu-id="957b2-157">根目錄專案的 DefaultDir 資料行值必須設定為 [**SourceDir**](sourcedir.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="957b2-157">The value of the DefaultDir column for the root directory entry must be set to the [**SourceDir**](sourcedir.md) property.</span></span>

### <a name="non-root-destination-directories"></a><span data-ttu-id="957b2-158">非根目錄目的地目錄</span><span class="sxs-lookup"><span data-stu-id="957b2-158">Non-root Destination Directories</span></span>

<span data-ttu-id="957b2-159">非根目錄的目錄值也會被解釋為定義目的地位置之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="957b2-159">The Directory value for a non-root directory is also interpreted as the name of a property defining the location of the destination.</span></span> <span data-ttu-id="957b2-160">如果已定義屬性，則會將目的地目錄解析為屬性的值。</span><span class="sxs-lookup"><span data-stu-id="957b2-160">If the property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="957b2-161">如果未定義屬性，則會將目的地目錄解析為目錄父專案的已解析目的地目錄下的子目錄 \_ 。</span><span class="sxs-lookup"><span data-stu-id="957b2-161">If the property is not defined, the destination directory is resolved to a subdirectory beneath the resolved destination directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="957b2-162">DefaultDir 值會定義子目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="957b2-162">The DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="non-root-source-directories"></a><span data-ttu-id="957b2-163">非根目錄來原始目錄</span><span class="sxs-lookup"><span data-stu-id="957b2-163">Non-root Source Directories</span></span>

<span data-ttu-id="957b2-164">非根目錄的來原始目錄會解析為目錄父專案之已解析來原始目錄的子目錄 \_ 。</span><span class="sxs-lookup"><span data-stu-id="957b2-164">The source directory for a non-root directory is resolved to a subdirectory of the resolved source directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="957b2-165">同樣地，DefaultDir 值會定義子目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="957b2-165">Again, the DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="short-or-long-file-names"></a><span data-ttu-id="957b2-166">簡短或長檔名</span><span class="sxs-lookup"><span data-stu-id="957b2-166">Short or Long File Names</span></span>

<span data-ttu-id="957b2-167">解析目的地目錄時，如果已設定 [**SHORTFILENAMES**](shortfilenames.md) 屬性，或目錄所在的磁片區不支援長檔名，則會使用 DefaultDir 資料行中指定的簡短檔案名。</span><span class="sxs-lookup"><span data-stu-id="957b2-167">When resolving destination directories, the short file names specified in the DefaultDir column are used if either the [**SHORTFILENAMES**](shortfilenames.md) property is set or the volume the directory is located on does not support long file names.</span></span> <span data-ttu-id="957b2-168">否則，會使用完整的檔案名。</span><span class="sxs-lookup"><span data-stu-id="957b2-168">Otherwise, the long file name is used.</span></span>

<span data-ttu-id="957b2-169">請注意，當您在 CostFinalize 動作期間解析目錄時，目錄資料表中的索引鍵會變成將 [屬性](properties.md) 設為目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="957b2-169">Note that when the directories are resolved during the CostFinalize action, the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span>

[<span data-ttu-id="957b2-170">CreateFolder 資料表</span><span class="sxs-lookup"><span data-stu-id="957b2-170">CreateFolder Table</span></span>](createfolder-table.md)

<span data-ttu-id="957b2-171">若要在安裝期間建立空的資料夾，請參閱 [CreateFolder Table](createfolder-table.md)。</span><span class="sxs-lookup"><span data-stu-id="957b2-171">For creating empty folders during an installation, see [CreateFolder Table](createfolder-table.md).</span></span>

[<span data-ttu-id="957b2-172">使用目錄資料表</span><span class="sxs-lookup"><span data-stu-id="957b2-172">Using the Directory Table</span></span>](using-the-directory-table.md)

<span data-ttu-id="957b2-173">如需目錄資料表（包括範例）的詳細資訊，請參閱 [使用目錄資料表](using-the-directory-table.md)。</span><span class="sxs-lookup"><span data-stu-id="957b2-173">For more information about the Directory table, including samples, see [Using the Directory Table](using-the-directory-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="957b2-174">驗證</span><span class="sxs-lookup"><span data-stu-id="957b2-174">Validation</span></span>

<dl>

[<span data-ttu-id="957b2-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="957b2-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="957b2-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="957b2-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="957b2-177">ICE07</span><span class="sxs-lookup"><span data-stu-id="957b2-177">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="957b2-178">ICE30</span><span class="sxs-lookup"><span data-stu-id="957b2-178">ICE30</span></span>](ice30.md)  
[<span data-ttu-id="957b2-179">ICE32</span><span class="sxs-lookup"><span data-stu-id="957b2-179">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="957b2-180">ICE38</span><span class="sxs-lookup"><span data-stu-id="957b2-180">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="957b2-181">ICE46</span><span class="sxs-lookup"><span data-stu-id="957b2-181">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="957b2-182">ICE48</span><span class="sxs-lookup"><span data-stu-id="957b2-182">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="957b2-183">ICE56</span><span class="sxs-lookup"><span data-stu-id="957b2-183">ICE56</span></span>](ice56.md)  
[<span data-ttu-id="957b2-184">ICE57</span><span class="sxs-lookup"><span data-stu-id="957b2-184">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="957b2-185">ICE64</span><span class="sxs-lookup"><span data-stu-id="957b2-185">ICE64</span></span>](ice64.md)  
[<span data-ttu-id="957b2-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="957b2-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="957b2-187">ICE90</span><span class="sxs-lookup"><span data-stu-id="957b2-187">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="957b2-188">ICE91</span><span class="sxs-lookup"><span data-stu-id="957b2-188">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="957b2-189">ICE99</span><span class="sxs-lookup"><span data-stu-id="957b2-189">ICE99</span></span>](ice99.md)  
</dl>

 

 



