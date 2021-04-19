---
description: 簽章資料表會保存唯一識別檔案簽章的資訊。 如需有關簽章的詳細資訊，請參閱數位簽章和 Windows Installer。
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: 簽名表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987227"
---
# <a name="signature-table"></a><span data-ttu-id="7c67e-104">簽名表</span><span class="sxs-lookup"><span data-stu-id="7c67e-104">Signature Table</span></span>

<span data-ttu-id="7c67e-105">簽章資料表會保存唯一識別檔案簽章的資訊。</span><span class="sxs-lookup"><span data-stu-id="7c67e-105">The Signature table holds the information that uniquely identifies a file signature.</span></span> <span data-ttu-id="7c67e-106">如需有關簽章的詳細資訊，請參閱 [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)。</span><span class="sxs-lookup"><span data-stu-id="7c67e-106">For more information regarding signatures see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="7c67e-107">簽章資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="7c67e-107">The Signature table has the following columns.</span></span>



| <span data-ttu-id="7c67e-108">Column</span><span class="sxs-lookup"><span data-stu-id="7c67e-108">Column</span></span>     | <span data-ttu-id="7c67e-109">類型</span><span class="sxs-lookup"><span data-stu-id="7c67e-109">Type</span></span>                               | <span data-ttu-id="7c67e-110">答案</span><span class="sxs-lookup"><span data-stu-id="7c67e-110">Key</span></span> | <span data-ttu-id="7c67e-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="7c67e-111">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="7c67e-112">簽名</span><span class="sxs-lookup"><span data-stu-id="7c67e-112">Signature</span></span>  | [<span data-ttu-id="7c67e-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="7c67e-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="7c67e-114">Y</span><span class="sxs-lookup"><span data-stu-id="7c67e-114">Y</span></span>   | <span data-ttu-id="7c67e-115">N</span><span class="sxs-lookup"><span data-stu-id="7c67e-115">N</span></span>        |
| <span data-ttu-id="7c67e-116">FileName</span><span class="sxs-lookup"><span data-stu-id="7c67e-116">FileName</span></span>   | [<span data-ttu-id="7c67e-117">Text</span><span class="sxs-lookup"><span data-stu-id="7c67e-117">Text</span></span>](text.md)                   | <span data-ttu-id="7c67e-118">N</span><span class="sxs-lookup"><span data-stu-id="7c67e-118">N</span></span>   | <span data-ttu-id="7c67e-119">N</span><span class="sxs-lookup"><span data-stu-id="7c67e-119">N</span></span>        |
| <span data-ttu-id="7c67e-120">MinVersion</span><span class="sxs-lookup"><span data-stu-id="7c67e-120">MinVersion</span></span> | [<span data-ttu-id="7c67e-121">Text</span><span class="sxs-lookup"><span data-stu-id="7c67e-121">Text</span></span>](text.md)                   | <span data-ttu-id="7c67e-122">N</span><span class="sxs-lookup"><span data-stu-id="7c67e-122">N</span></span>   | <span data-ttu-id="7c67e-123">Y</span><span class="sxs-lookup"><span data-stu-id="7c67e-123">Y</span></span>        |
| <span data-ttu-id="7c67e-124">Odata-maxversion</span><span class="sxs-lookup"><span data-stu-id="7c67e-124">MaxVersion</span></span> | [<span data-ttu-id="7c67e-125">Text</span><span class="sxs-lookup"><span data-stu-id="7c67e-125">Text</span></span>](text.md)                   | <span data-ttu-id="7c67e-126">N</span><span class="sxs-lookup"><span data-stu-id="7c67e-126">N</span></span>   | <span data-ttu-id="7c67e-127">Y</span><span class="sxs-lookup"><span data-stu-id="7c67e-127">Y</span></span>        |
| <span data-ttu-id="7c67e-128">MinSize</span><span class="sxs-lookup"><span data-stu-id="7c67e-128">MinSize</span></span>    | [<span data-ttu-id="7c67e-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="7c67e-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="7c67e-130">N</span><span class="sxs-lookup"><span data-stu-id="7c67e-130">N</span></span>   | <span data-ttu-id="7c67e-131">Y</span><span class="sxs-lookup"><span data-stu-id="7c67e-131">Y</span></span>        |
| <span data-ttu-id="7c67e-132">MaxSize</span><span class="sxs-lookup"><span data-stu-id="7c67e-132">MaxSize</span></span>    | [<span data-ttu-id="7c67e-133">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="7c67e-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="7c67e-134">N</span><span class="sxs-lookup"><span data-stu-id="7c67e-134">N</span></span>   | <span data-ttu-id="7c67e-135">Y</span><span class="sxs-lookup"><span data-stu-id="7c67e-135">Y</span></span>        |
| <span data-ttu-id="7c67e-136">MinDate</span><span class="sxs-lookup"><span data-stu-id="7c67e-136">MinDate</span></span>    | [<span data-ttu-id="7c67e-137">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="7c67e-137">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="7c67e-138">N</span><span class="sxs-lookup"><span data-stu-id="7c67e-138">N</span></span>   | <span data-ttu-id="7c67e-139">Y</span><span class="sxs-lookup"><span data-stu-id="7c67e-139">Y</span></span>        |
| <span data-ttu-id="7c67e-140">MaxDate</span><span class="sxs-lookup"><span data-stu-id="7c67e-140">MaxDate</span></span>    | [<span data-ttu-id="7c67e-141">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="7c67e-141">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="7c67e-142">N</span><span class="sxs-lookup"><span data-stu-id="7c67e-142">N</span></span>   | <span data-ttu-id="7c67e-143">Y</span><span class="sxs-lookup"><span data-stu-id="7c67e-143">Y</span></span>        |
| <span data-ttu-id="7c67e-144">語言</span><span class="sxs-lookup"><span data-stu-id="7c67e-144">Languages</span></span>  | [<span data-ttu-id="7c67e-145">Text</span><span class="sxs-lookup"><span data-stu-id="7c67e-145">Text</span></span>](text.md)                   | <span data-ttu-id="7c67e-146">N</span><span class="sxs-lookup"><span data-stu-id="7c67e-146">N</span></span>   | <span data-ttu-id="7c67e-147">Y</span><span class="sxs-lookup"><span data-stu-id="7c67e-147">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7c67e-148">資料行</span><span class="sxs-lookup"><span data-stu-id="7c67e-148">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7c67e-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>簽名</span><span class="sxs-lookup"><span data-stu-id="7c67e-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="7c67e-150">簽章資料行是唯一的檔案簽章。</span><span class="sxs-lookup"><span data-stu-id="7c67e-150">The Signature column is a unique file signature.</span></span>

</dd> <dt>

<span data-ttu-id="7c67e-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名</span><span class="sxs-lookup"><span data-stu-id="7c67e-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="7c67e-152">檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c67e-152">The name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="7c67e-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span><span class="sxs-lookup"><span data-stu-id="7c67e-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span></span>
</dt> <dd>

<span data-ttu-id="7c67e-154">檔案的最小版本，使用語言比較。</span><span class="sxs-lookup"><span data-stu-id="7c67e-154">The minimum version of the file, with a language comparison.</span></span> <span data-ttu-id="7c67e-155">如果指定此欄位，則檔案的版本必須至少等於 MinVersion。</span><span class="sxs-lookup"><span data-stu-id="7c67e-155">If this field is specified, then the file must have a version that is at least equal to MinVersion.</span></span> <span data-ttu-id="7c67e-156">如果檔案的版本等同于 MinVersion 域值，但 [語言] 資料行中指定的語言不同，則檔案不會滿足簽章篩選準則。</span><span class="sxs-lookup"><span data-stu-id="7c67e-156">If the file has an equal version to the MinVersion field value but the language specified in the Languages column differs, the file does not satisfy the signature filter criteria.</span></span>

> [!Note]  
> <span data-ttu-id="7c67e-157">在比較中使用語言資料行中指定的語言，而且沒有任何方法可忽略語言。</span><span class="sxs-lookup"><span data-stu-id="7c67e-157">The language specified in the Languages column is used in the comparison and there is no way to ignore language.</span></span> <span data-ttu-id="7c67e-158">如果您希望檔案符合 MinVersion 欄位需求（不論語言為何），您必須在 [MinVersion] 欄位中輸入一個小於實際值的值。</span><span class="sxs-lookup"><span data-stu-id="7c67e-158">If you want a file to meet the MinVersion field requirement regardless of language, you must enter a value in the MinVersion field that is one less than the actual value.</span></span> <span data-ttu-id="7c67e-159">例如，如果篩選的最小版本是2.0.2600.1183，請使用2.0.2600.1182 來尋找檔案，但不符合語言資訊。</span><span class="sxs-lookup"><span data-stu-id="7c67e-159">For example, if the minimum version for the filter is 2.0.2600.1183, use 2.0.2600.1182 to find the file without matching the language information.</span></span>

 

</dd> <dt>

<span data-ttu-id="7c67e-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>Odata-maxversion</span><span class="sxs-lookup"><span data-stu-id="7c67e-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="7c67e-161">檔案的最大版本。</span><span class="sxs-lookup"><span data-stu-id="7c67e-161">The maximum version of the file.</span></span> <span data-ttu-id="7c67e-162">如果指定此欄位，則檔案的版本必須最等於 Odata-maxversion。</span><span class="sxs-lookup"><span data-stu-id="7c67e-162">If this field is specified, then the file must have a version that is at most equal to MaxVersion.</span></span>

</dd> <dt>

<span data-ttu-id="7c67e-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span><span class="sxs-lookup"><span data-stu-id="7c67e-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span></span>
</dt> <dd>

<span data-ttu-id="7c67e-164">檔案的大小下限。</span><span class="sxs-lookup"><span data-stu-id="7c67e-164">The minimum size of the file.</span></span> <span data-ttu-id="7c67e-165">如果指定此欄位，則檢查中的檔案必須具有至少等於 MinSize 的大小。</span><span class="sxs-lookup"><span data-stu-id="7c67e-165">If this field is specified, then the file under inspection must have a size that is at least equal to MinSize.</span></span> <span data-ttu-id="7c67e-166">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="7c67e-166">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="7c67e-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span><span class="sxs-lookup"><span data-stu-id="7c67e-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span></span>
</dt> <dd>

<span data-ttu-id="7c67e-168">檔案的大小上限。</span><span class="sxs-lookup"><span data-stu-id="7c67e-168">The maximum size of the file.</span></span> <span data-ttu-id="7c67e-169">如果指定此欄位，則檢查中的檔案必須具有最等於 MaxSize 的大小。</span><span class="sxs-lookup"><span data-stu-id="7c67e-169">If this field is specified, then the file under inspection must have a size that is at most equal to MaxSize.</span></span> <span data-ttu-id="7c67e-170">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="7c67e-170">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="7c67e-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span><span class="sxs-lookup"><span data-stu-id="7c67e-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span></span>
</dt> <dd>

<span data-ttu-id="7c67e-172">檔案的最小修改日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7c67e-172">The minimum modification date and time of the file.</span></span> <span data-ttu-id="7c67e-173">如果指定此欄位，則檢查中的檔案必須具有至少等於 MinDate 的修改日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7c67e-173">If this field is specified, then the file under inspection must have a modification date and time that is at least equal to MinDate.</span></span> <span data-ttu-id="7c67e-174">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="7c67e-174">This must be a non-negative number.</span></span> <span data-ttu-id="7c67e-175">此欄位的格式為 " **WORD**" 類型的兩個壓縮的16位值。</span><span class="sxs-lookup"><span data-stu-id="7c67e-175">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="7c67e-176">高序位 **單字** 值會以 MS-DOS 日期格式來指定日期。</span><span class="sxs-lookup"><span data-stu-id="7c67e-176">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="7c67e-177">低序位 **單字** 值以 MS-DOS 時間格式指定時間。</span><span class="sxs-lookup"><span data-stu-id="7c67e-177">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="7c67e-178">時間值的0值代表午夜。</span><span class="sxs-lookup"><span data-stu-id="7c67e-178">A value of 0 for the time value represents midnight.</span></span> <span data-ttu-id="7c67e-179">請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="7c67e-179">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="7c67e-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span><span class="sxs-lookup"><span data-stu-id="7c67e-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span></span>
</dt> <dd>

<span data-ttu-id="7c67e-181">檔案的最大建立日期。</span><span class="sxs-lookup"><span data-stu-id="7c67e-181">The maximum creation date of the file.</span></span> <span data-ttu-id="7c67e-182">如果指定此欄位，則正在檢查的檔案必須具有最等於 MaxDate 的建立日期。</span><span class="sxs-lookup"><span data-stu-id="7c67e-182">If this field is specified, then the file under inspection must have a creation date that is at most equal to MaxDate.</span></span> <span data-ttu-id="7c67e-183">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="7c67e-183">This must be a non-negative number.</span></span> <span data-ttu-id="7c67e-184">此欄位的格式為 " **WORD**" 類型的兩個壓縮的16位值。</span><span class="sxs-lookup"><span data-stu-id="7c67e-184">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="7c67e-185">高序位 **單字** 值會以 MS-DOS 日期格式來指定日期。</span><span class="sxs-lookup"><span data-stu-id="7c67e-185">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="7c67e-186">低序位 **單字** 值以 MS-DOS 時間格式指定時間。</span><span class="sxs-lookup"><span data-stu-id="7c67e-186">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="7c67e-187">時間值的0值代表午夜。</span><span class="sxs-lookup"><span data-stu-id="7c67e-187">A value of 0 for the time value represent midnight.</span></span> <span data-ttu-id="7c67e-188">請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="7c67e-188">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="7c67e-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>語言</span><span class="sxs-lookup"><span data-stu-id="7c67e-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Languages</span></span>
</dt> <dd>

<span data-ttu-id="7c67e-190">檔案所支援的語言。</span><span class="sxs-lookup"><span data-stu-id="7c67e-190">The languages supported by the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c67e-191">備註</span><span class="sxs-lookup"><span data-stu-id="7c67e-191">Remarks</span></span>

<span data-ttu-id="7c67e-192">此資料表與 [AppSearch 資料表](appsearch-table.md)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="7c67e-192">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="7c67e-193">使用 [RegLocator 資料表](reglocator-table.md)、 [IniLocator 資料表](inilocator-table.md)、 [CompLocator 資料表](complocator-table.md)和 [DrLocator 資料表](drlocator-table.md)來搜尋簽章。</span><span class="sxs-lookup"><span data-stu-id="7c67e-193">The signature is searched for using the [RegLocator table](reglocator-table.md), the [IniLocator table](inilocator-table.md), the [CompLocator table](complocator-table.md), and the [DrLocator table](drlocator-table.md).</span></span> <span data-ttu-id="7c67e-194">此資料表的資料行通常不會當地語系化。</span><span class="sxs-lookup"><span data-stu-id="7c67e-194">This table's columns are generally not localized.</span></span> <span data-ttu-id="7c67e-195">如果作者決定搜尋多種語言的產品，則每種語言的表格中都可以有個別的專案。</span><span class="sxs-lookup"><span data-stu-id="7c67e-195">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="7c67e-196">簽名表通常會遵循 Windows Installer 檔案 [版本控制規則](file-versioning-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="7c67e-196">The Signature table generally follows the Windows Installer [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="7c67e-197">除非檔案版本相等，否則不會評估簽章資料表的 [語言] 資料行中指定的語言。</span><span class="sxs-lookup"><span data-stu-id="7c67e-197">Languages specified in the Languages column of the Signature table are not evaluated unless the file versions are equivalent.</span></span> <span data-ttu-id="7c67e-198">[語言] 資料行可確保檔案為所要求版本的特定語言。</span><span class="sxs-lookup"><span data-stu-id="7c67e-198">The Languages column will ensure that a file is of a particular language if it is of the requested version.</span></span> <span data-ttu-id="7c67e-199">沒有任何方法可忽略 [語言] 資料行。</span><span class="sxs-lookup"><span data-stu-id="7c67e-199">There is no method available to ignore the Languages column.</span></span> <span data-ttu-id="7c67e-200">在 [語言] 資料行中輸入的 Null 值會被視為沒有語言的檔案，而且不符合簽章資料表中出現之語言的檔案簽章。</span><span class="sxs-lookup"><span data-stu-id="7c67e-200">A NULL value entered in the Languages column is treated as a file without a language and does not match the file signature of a file with a language appearing in the Signature table.</span></span> <span data-ttu-id="7c67e-201">下列範例會搜尋特定版本的 MSI.DLL。</span><span class="sxs-lookup"><span data-stu-id="7c67e-201">The following example searches for a particular version of MSI.DLL.</span></span>

[<span data-ttu-id="7c67e-202">DrLocator 資料表</span><span class="sxs-lookup"><span data-stu-id="7c67e-202">DrLocator table</span></span>](drlocator-table.md)

| <span data-ttu-id="7c67e-203">簽名\_</span><span class="sxs-lookup"><span data-stu-id="7c67e-203">Signature\_</span></span> | <span data-ttu-id="7c67e-204">父代</span><span class="sxs-lookup"><span data-stu-id="7c67e-204">Parent</span></span> | <span data-ttu-id="7c67e-205">路徑</span><span class="sxs-lookup"><span data-stu-id="7c67e-205">Path</span></span>                  | <span data-ttu-id="7c67e-206">深度</span><span class="sxs-lookup"><span data-stu-id="7c67e-206">Depth</span></span> |
|-------------|--------|-----------------------|-------|
| <span data-ttu-id="7c67e-207">MsiDll</span><span class="sxs-lookup"><span data-stu-id="7c67e-207">MsiDll</span></span>      | <span data-ttu-id="7c67e-208">;</span><span class="sxs-lookup"><span data-stu-id="7c67e-208">{null}</span></span> | <span data-ttu-id="7c67e-209">c： \\ windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="7c67e-209">c:\\windows\\system32</span></span> | <span data-ttu-id="7c67e-210">0</span><span class="sxs-lookup"><span data-stu-id="7c67e-210">0</span></span>     |



 

[<span data-ttu-id="7c67e-211">AppSearch 資料表</span><span class="sxs-lookup"><span data-stu-id="7c67e-211">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="7c67e-212">屬性</span><span class="sxs-lookup"><span data-stu-id="7c67e-212">Property</span></span> | <span data-ttu-id="7c67e-213">簽名\_</span><span class="sxs-lookup"><span data-stu-id="7c67e-213">Signature\_</span></span> |
|----------|-------------|
| <span data-ttu-id="7c67e-214">MSIDLL</span><span class="sxs-lookup"><span data-stu-id="7c67e-214">MSIDLL</span></span>   | <span data-ttu-id="7c67e-215">MsiDll</span><span class="sxs-lookup"><span data-stu-id="7c67e-215">MsiDll</span></span>      |



 

<span data-ttu-id="7c67e-216">簽名表</span><span class="sxs-lookup"><span data-stu-id="7c67e-216">Signature table</span></span>



| <span data-ttu-id="7c67e-217">簽名</span><span class="sxs-lookup"><span data-stu-id="7c67e-217">Signature</span></span> | <span data-ttu-id="7c67e-218">FileName</span><span class="sxs-lookup"><span data-stu-id="7c67e-218">FileName</span></span> | <span data-ttu-id="7c67e-219">MinVersion</span><span class="sxs-lookup"><span data-stu-id="7c67e-219">MinVersion</span></span>    | <span data-ttu-id="7c67e-220">Odata-maxversion</span><span class="sxs-lookup"><span data-stu-id="7c67e-220">MaxVersion</span></span> | <span data-ttu-id="7c67e-221">MinSize</span><span class="sxs-lookup"><span data-stu-id="7c67e-221">MinSize</span></span> | <span data-ttu-id="7c67e-222">MaxSize</span><span class="sxs-lookup"><span data-stu-id="7c67e-222">MaxSize</span></span> | <span data-ttu-id="7c67e-223">MinDate</span><span class="sxs-lookup"><span data-stu-id="7c67e-223">MinDate</span></span> | <span data-ttu-id="7c67e-224">MaxDate</span><span class="sxs-lookup"><span data-stu-id="7c67e-224">MaxDate</span></span> | <span data-ttu-id="7c67e-225">語言</span><span class="sxs-lookup"><span data-stu-id="7c67e-225">Languages</span></span> |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| <span data-ttu-id="7c67e-226">MsiDll</span><span class="sxs-lookup"><span data-stu-id="7c67e-226">MsiDll</span></span>    | <span data-ttu-id="7c67e-227">msi.dll</span><span class="sxs-lookup"><span data-stu-id="7c67e-227">msi.dll</span></span>  | <span data-ttu-id="7c67e-228">2.0.2600.1106</span><span class="sxs-lookup"><span data-stu-id="7c67e-228">2.0.2600.1106</span></span> | <span data-ttu-id="7c67e-229">;</span><span class="sxs-lookup"><span data-stu-id="7c67e-229">{null}</span></span>     | <span data-ttu-id="7c67e-230">;</span><span class="sxs-lookup"><span data-stu-id="7c67e-230">{null}</span></span>  | <span data-ttu-id="7c67e-231">;</span><span class="sxs-lookup"><span data-stu-id="7c67e-231">{null}</span></span>  | <span data-ttu-id="7c67e-232">;</span><span class="sxs-lookup"><span data-stu-id="7c67e-232">{null}</span></span>  | <span data-ttu-id="7c67e-233">;</span><span class="sxs-lookup"><span data-stu-id="7c67e-233">{null}</span></span>  | <span data-ttu-id="7c67e-234">0</span><span class="sxs-lookup"><span data-stu-id="7c67e-234">0</span></span>         |



 

<span data-ttu-id="7c67e-235">在此情況下，以及在 Windows XP SP1 上， [AppSearch 動作](appsearch-action.md) 會將 MSIDLL 設定為 c： \\ Windows \\ system32 \\msi.dll，因為 MSI.DLL 是中性語言的檔案。</span><span class="sxs-lookup"><span data-stu-id="7c67e-235">In this case, and on Windows XP SP1, the [AppSearch action](appsearch-action.md) sets MSIDLL to c:\\windows\\system32\\msi.dll because MSI.DLL is a language neutral file.</span></span> <span data-ttu-id="7c67e-236">如果 [語言] 資料行的值從0變更為1033，則 AppSearch 動作會找不到相符的 msi.dll，且 MSIDLL 屬性未定義。</span><span class="sxs-lookup"><span data-stu-id="7c67e-236">If the value of the Languages column is changed from 0 to 1033, then the AppSearch action fails to find the matching msi.dll and the MSIDLL property is undefined.</span></span>

<span data-ttu-id="7c67e-237">您無法使用簽章資料表來單獨查詢語言。</span><span class="sxs-lookup"><span data-stu-id="7c67e-237">You cannot use the Signature table to query on languages alone.</span></span> <span data-ttu-id="7c67e-238">若要搜尋檔案的不同語言版本，每個語言版本的簽章資料表中都必須有不同的專案。</span><span class="sxs-lookup"><span data-stu-id="7c67e-238">To search for different language versions of a file, you must have a separate entry in the Signature table for each language version.</span></span> <span data-ttu-id="7c67e-239">如果 [語言] 欄中提供多種語言，則搜尋是針對支援所有語言的檔案。</span><span class="sxs-lookup"><span data-stu-id="7c67e-239">If multiple languages are provided in the Languages column, then the search is for a file that supports all of those languages.</span></span>

<span data-ttu-id="7c67e-240">MinDate 和 MaxDate 資料行的格式為類型為 **WORD** 的兩個壓縮16位值。</span><span class="sxs-lookup"><span data-stu-id="7c67e-240">The format of MinDate and MaxDate columns are two packed 16-bit values of type **WORD**.</span></span>

<span data-ttu-id="7c67e-241">日期 **文字**</span><span class="sxs-lookup"><span data-stu-id="7c67e-241">Date **WORD**</span></span>



| <span data-ttu-id="7c67e-242">Bits</span><span class="sxs-lookup"><span data-stu-id="7c67e-242">Bits</span></span> | <span data-ttu-id="7c67e-243">Content</span><span class="sxs-lookup"><span data-stu-id="7c67e-243">Content</span></span>                                             |
|------|-----------------------------------------------------|
| <span data-ttu-id="7c67e-244">0–4</span><span class="sxs-lookup"><span data-stu-id="7c67e-244">0–4</span></span>  | <span data-ttu-id="7c67e-245">每月的日 (1-31) </span><span class="sxs-lookup"><span data-stu-id="7c67e-245">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="7c67e-246">5-8</span><span class="sxs-lookup"><span data-stu-id="7c67e-246">5-8</span></span>  | <span data-ttu-id="7c67e-247">月 (1 = 一月、2 = 二月，依此類推) </span><span class="sxs-lookup"><span data-stu-id="7c67e-247">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="7c67e-248">9-15</span><span class="sxs-lookup"><span data-stu-id="7c67e-248">9-15</span></span> | <span data-ttu-id="7c67e-249">從1980算起的年位移 (新增1980以取得實際年份) </span><span class="sxs-lookup"><span data-stu-id="7c67e-249">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

<span data-ttu-id="7c67e-250">時間 **單字**</span><span class="sxs-lookup"><span data-stu-id="7c67e-250">Time **WORD**</span></span>



| <span data-ttu-id="7c67e-251">Bits</span><span class="sxs-lookup"><span data-stu-id="7c67e-251">Bits</span></span>  | <span data-ttu-id="7c67e-252">Content</span><span class="sxs-lookup"><span data-stu-id="7c67e-252">Content</span></span>                     |
|-------|-----------------------------|
| <span data-ttu-id="7c67e-253">0–4</span><span class="sxs-lookup"><span data-stu-id="7c67e-253">0–4</span></span>   | <span data-ttu-id="7c67e-254">秒除以2</span><span class="sxs-lookup"><span data-stu-id="7c67e-254">Seconds divided by 2</span></span>        |
| <span data-ttu-id="7c67e-255">5-10</span><span class="sxs-lookup"><span data-stu-id="7c67e-255">5-10</span></span>  | <span data-ttu-id="7c67e-256"> (0-59) 分鐘</span><span class="sxs-lookup"><span data-stu-id="7c67e-256">Minutes (0-59)</span></span>              |
| <span data-ttu-id="7c67e-257">11-15</span><span class="sxs-lookup"><span data-stu-id="7c67e-257">11-15</span></span> | <span data-ttu-id="7c67e-258">24小時制的小時 (0-23) </span><span class="sxs-lookup"><span data-stu-id="7c67e-258">Hour(0-23 on 24 hour clock)</span></span> |



 

<span data-ttu-id="7c67e-259">計算 MinDate 和 MaxDate 域值的公式如下：</span><span class="sxs-lookup"><span data-stu-id="7c67e-259">The formula for calculating the MinDate and MaxDate field values is:</span></span>

<span data-ttu-id="7c67e-260"> ( (年 1980) \* 512 + 月 \* 32 + 天 ) \* 65536 + 小時 \* 2048 + 分鐘 \* 32 + 秒/2</span><span class="sxs-lookup"><span data-stu-id="7c67e-260">( (Year - 1980) \* 512 + Month \* 32 + Day ) \* 65536 + Hours \* 2048 + Minutes \* 32 + Seconds/2</span></span>

## <a name="validation"></a><span data-ttu-id="7c67e-261">驗證</span><span class="sxs-lookup"><span data-stu-id="7c67e-261">Validation</span></span>

<dl>

[<span data-ttu-id="7c67e-262">ICE03</span><span class="sxs-lookup"><span data-stu-id="7c67e-262">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7c67e-263">ICE06</span><span class="sxs-lookup"><span data-stu-id="7c67e-263">ICE06</span></span>](ice06.md)  
</dl>

 

 



