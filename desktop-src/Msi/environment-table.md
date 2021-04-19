---
description: 環境資料表是用來設定環境變數的值。
ms.assetid: f7106ed6-706f-4e57-989f-030066bcecd3
title: 環境資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a4db2e33c01685bdc40475f659e1b03b69b6c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987482"
---
# <a name="environment-table"></a><span data-ttu-id="993c3-103">環境資料表</span><span class="sxs-lookup"><span data-stu-id="993c3-103">Environment Table</span></span>

<span data-ttu-id="993c3-104">環境資料表是用來設定環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="993c3-104">The Environment table is used to set the values of environment variables.</span></span>

<span data-ttu-id="993c3-105">環境資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="993c3-105">The Environment table has the following columns.</span></span>



| <span data-ttu-id="993c3-106">Column</span><span class="sxs-lookup"><span data-stu-id="993c3-106">Column</span></span>      | <span data-ttu-id="993c3-107">類型</span><span class="sxs-lookup"><span data-stu-id="993c3-107">Type</span></span>                         | <span data-ttu-id="993c3-108">答案</span><span class="sxs-lookup"><span data-stu-id="993c3-108">Key</span></span> | <span data-ttu-id="993c3-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="993c3-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="993c3-110">環境</span><span class="sxs-lookup"><span data-stu-id="993c3-110">Environment</span></span> | [<span data-ttu-id="993c3-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="993c3-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="993c3-112">Y</span><span class="sxs-lookup"><span data-stu-id="993c3-112">Y</span></span>   | <span data-ttu-id="993c3-113">N</span><span class="sxs-lookup"><span data-stu-id="993c3-113">N</span></span>        |
| <span data-ttu-id="993c3-114">Name</span><span class="sxs-lookup"><span data-stu-id="993c3-114">Name</span></span>        | [<span data-ttu-id="993c3-115">Text</span><span class="sxs-lookup"><span data-stu-id="993c3-115">Text</span></span>](text.md)             | <span data-ttu-id="993c3-116">N</span><span class="sxs-lookup"><span data-stu-id="993c3-116">N</span></span>   | <span data-ttu-id="993c3-117">N</span><span class="sxs-lookup"><span data-stu-id="993c3-117">N</span></span>        |
| <span data-ttu-id="993c3-118">值</span><span class="sxs-lookup"><span data-stu-id="993c3-118">Value</span></span>       | [<span data-ttu-id="993c3-119">格式 化</span><span class="sxs-lookup"><span data-stu-id="993c3-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="993c3-120">N</span><span class="sxs-lookup"><span data-stu-id="993c3-120">N</span></span>   | <span data-ttu-id="993c3-121">Y</span><span class="sxs-lookup"><span data-stu-id="993c3-121">Y</span></span>        |
| <span data-ttu-id="993c3-122">元件\_</span><span class="sxs-lookup"><span data-stu-id="993c3-122">Component\_</span></span> | [<span data-ttu-id="993c3-123">識別碼</span><span class="sxs-lookup"><span data-stu-id="993c3-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="993c3-124">N</span><span class="sxs-lookup"><span data-stu-id="993c3-124">N</span></span>   | <span data-ttu-id="993c3-125">N</span><span class="sxs-lookup"><span data-stu-id="993c3-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="993c3-126">資料行</span><span class="sxs-lookup"><span data-stu-id="993c3-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="993c3-127"><span id="Environment"></span><span id="environment"></span><span id="ENVIRONMENT"></span>環境</span><span class="sxs-lookup"><span data-stu-id="993c3-127"><span id="Environment"></span><span id="environment"></span><span id="ENVIRONMENT"></span>Environment</span></span>
</dt> <dd>

<span data-ttu-id="993c3-128">這是資料表的主鍵，而且是非當地語系化的標記。</span><span class="sxs-lookup"><span data-stu-id="993c3-128">This is the primary key of the table and is a non-localized token.</span></span>

</dd> <dt>

<span data-ttu-id="993c3-129"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="993c3-129"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="993c3-130">此資料行是環境變數的可當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="993c3-130">This column is the localizable name of the environment variable.</span></span> <span data-ttu-id="993c3-131">系統會根據下表中的哪些字元前面加上名稱，來寫入或移除索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="993c3-131">The key values are written or removed depending upon which of the characters in the following table are prefixed to the name.</span></span> <span data-ttu-id="993c3-132">前置詞中使用的符號順序不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="993c3-132">There is no effect in the ordering of the symbols used in a prefix.</span></span>



| <span data-ttu-id="993c3-133">前置詞</span><span class="sxs-lookup"><span data-stu-id="993c3-133">Prefix</span></span>                         | <span data-ttu-id="993c3-134">描述</span><span class="sxs-lookup"><span data-stu-id="993c3-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =                              | <span data-ttu-id="993c3-135">如果環境變數不存在，請建立環境變數，然後在安裝期間進行設定。</span><span class="sxs-lookup"><span data-stu-id="993c3-135">Create the environment variable if it does not exist, and then set it during installation.</span></span> <span data-ttu-id="993c3-136">如果環境變數存在，請在安裝期間進行設定。</span><span class="sxs-lookup"><span data-stu-id="993c3-136">If the environment variable exists, set it during the installation.</span></span>                                                                                                                                                                                                                                                                                                                                   |
| \+                             | <span data-ttu-id="993c3-137">如果環境變數不存在，請建立環境變數，然後在安裝期間進行設定。</span><span class="sxs-lookup"><span data-stu-id="993c3-137">Create the environment variable if it does not exist, then set it during installation.</span></span> <span data-ttu-id="993c3-138">如果環境變數的值已存在，則不會對其產生任何影響。</span><span class="sxs-lookup"><span data-stu-id="993c3-138">This has no effect on the value of the environment variable if it already exists.</span></span>                                                                                                                                                                                                                                                                                                                         |
| \-                             | <span data-ttu-id="993c3-139">移除元件時，移除環境變數。</span><span class="sxs-lookup"><span data-stu-id="993c3-139">Remove the environment variable when the component is removed.</span></span> <span data-ttu-id="993c3-140">這個符號可以與任何前置詞結合。</span><span class="sxs-lookup"><span data-stu-id="993c3-140">This symbol can be combined with any prefix.</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="993c3-141">!</span><span class="sxs-lookup"><span data-stu-id="993c3-141">!</span></span>                              | <span data-ttu-id="993c3-142">在安裝期間移除環境變數。</span><span class="sxs-lookup"><span data-stu-id="993c3-142">Remove the environment variable during an installation.</span></span> <span data-ttu-id="993c3-143">如果變數的名稱和值與環境資料表的 [名稱] 和 [值] 欄位中的專案相符，則安裝程式只會在安裝期間移除環境變數。</span><span class="sxs-lookup"><span data-stu-id="993c3-143">The installer only removes an environment variable during an installation if the name and value of the variable match the entries in the Name and Value fields of the Environment table.</span></span> <span data-ttu-id="993c3-144">如果您想要移除環境變數（不論其值為何），請使用 '！ ' 語法，並將 [值] 欄位保留空白。</span><span class="sxs-lookup"><span data-stu-id="993c3-144">If you want to remove an environment variable, regardless of its value, use the '!' syntax, and leave the Value field empty.</span></span>                                                                                                                    |
| \*                             | <span data-ttu-id="993c3-145">這個前置詞會與 Windows 2000 搭配使用，指出名稱是指系統內容變數。</span><span class="sxs-lookup"><span data-stu-id="993c3-145">This prefix is used with Windows 2000 to indicate that the name refers to a system environment variable.</span></span> <span data-ttu-id="993c3-146">如果沒有星號存在，安裝程式會將變數寫入使用者的環境。</span><span class="sxs-lookup"><span data-stu-id="993c3-146">If no asterisk is present, the installer writes the variable to the user's environment.</span></span> <span data-ttu-id="993c3-147">這個符號可以與任何前置詞結合。</span><span class="sxs-lookup"><span data-stu-id="993c3-147">This symbol can be combined with any prefix.</span></span> <span data-ttu-id="993c3-148">在每一部電腦的 [安裝內容](installation-context.md) 中，用於安裝的封裝應該包含 \* 在名稱資料行中，以將環境變數寫入機器的環境中。</span><span class="sxs-lookup"><span data-stu-id="993c3-148">A package that is used for installation in the per-machine [installation context](installation-context.md) should write environment variables to the machine's environment by including \* in the Name column.</span></span> <span data-ttu-id="993c3-149">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="993c3-149">For more information, see Remarks.</span></span> |
| =-                             | <span data-ttu-id="993c3-150">環境變數會在安裝時設定，並在卸載時移除。</span><span class="sxs-lookup"><span data-stu-id="993c3-150">The environment variable is set on install and removed on uninstall.</span></span> <span data-ttu-id="993c3-151">這是一般的行為。</span><span class="sxs-lookup"><span data-stu-id="993c3-151">This is the usual behavior.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="993c3-152">!-</span><span class="sxs-lookup"><span data-stu-id="993c3-152">!-</span></span>                             | <span data-ttu-id="993c3-153">在安裝或卸載期間移除環境變數。</span><span class="sxs-lookup"><span data-stu-id="993c3-153">Removes an environment variable during an install or uninstall.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="993c3-154">=+ !+</span><span class="sxs-lookup"><span data-stu-id="993c3-154">=+ !+</span></span><br/> <span data-ttu-id="993c3-155">!=</span><span class="sxs-lookup"><span data-stu-id="993c3-155">!=</span></span><br/> | <span data-ttu-id="993c3-156">這些不是有效的首碼</span><span class="sxs-lookup"><span data-stu-id="993c3-156">These are not a valid prefixes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

<span data-ttu-id="993c3-157">如果資料表中的 [值] 欄位包含 \[ ~ \] ，則前置詞字元只適用于字串的指定部分。</span><span class="sxs-lookup"><span data-stu-id="993c3-157">If the Value field in the table includes a \[~\], then the prefix characters apply to only the specified portion of the string.</span></span> <span data-ttu-id="993c3-158">在以下的 [ \[ ~ \] 值資料行] 區段中描述的用法。</span><span class="sxs-lookup"><span data-stu-id="993c3-158">The use of \[~\] is described below in the Value column section.</span></span>

<span data-ttu-id="993c3-159">如果資料表的 [值] 欄位是空白的，則會移除環境變數。</span><span class="sxs-lookup"><span data-stu-id="993c3-159">The environment variable is removed if the Value field of the table is blank.</span></span> <span data-ttu-id="993c3-160">因此，在 [值] 欄位中有空白的 = 前置詞會在安裝時刪除環境變數，而-前置詞則會在卸載時刪除任何目前的值。</span><span class="sxs-lookup"><span data-stu-id="993c3-160">Therefore, with a blank in the Value field, an = prefix deletes the environment variable on install and a - prefix deletes any current values on uninstall.</span></span>

</dd> <dt>

<span data-ttu-id="993c3-161"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="993c3-161"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="993c3-162">此資料行包含要設定為格式化字串的可當地語系化值。</span><span class="sxs-lookup"><span data-stu-id="993c3-162">This column contains the localizable value that is to be set as a formatted string.</span></span> <span data-ttu-id="993c3-163">請參閱 [格式化](formatted.md)。</span><span class="sxs-lookup"><span data-stu-id="993c3-163">See [Formatted](formatted.md).</span></span> <span data-ttu-id="993c3-164">如果此欄位保留空白，則會移除該變數。</span><span class="sxs-lookup"><span data-stu-id="993c3-164">If this field is left blank, the variable is removed.</span></span> <span data-ttu-id="993c3-165">如果欄位是空白的，且 [名稱] 欄位中的字串前面加上-符號，則只有在移除元件時，才會移除該變數。</span><span class="sxs-lookup"><span data-stu-id="993c3-165">If the field is blank and the string in the Name field is prefixed by the - symbol, the variable is removed only when the component is removed.</span></span>

<span data-ttu-id="993c3-166">若要將值附加至現有變數的結尾，請在此欄位中的字串前面加上 Null 字元 \[ ~ \] 和分隔字元。</span><span class="sxs-lookup"><span data-stu-id="993c3-166">To append a value to the end of an existing variable, prefix the string in this field by the Null character \[~\] and the separator character.</span></span> <span data-ttu-id="993c3-167">例如，如果分號是選擇的分隔符號： \[ ~ \] ;*值*。</span><span class="sxs-lookup"><span data-stu-id="993c3-167">For example, if the semicolon is the chosen separator: \[~\];*Value*.</span></span>

<span data-ttu-id="993c3-168">若要將值的前置詞加到現有變數的前面，請在此欄位中，依分隔符號和 Null 字元附加字串 \[ ~ \] 。</span><span class="sxs-lookup"><span data-stu-id="993c3-168">To prefix a value to the front of an existing variable, append the string in this field by the separator character and the Null character \[~\].</span></span> <span data-ttu-id="993c3-169">例如，如果分號是選擇的分隔符號： *Value*; \[ ~ \].</span><span class="sxs-lookup"><span data-stu-id="993c3-169">For example, if the semicolon is the chosen separator: *Value*;\[~\] .</span></span>

<span data-ttu-id="993c3-170">如果 \[ ~ \] 欄位中沒有任何，則字串代表要設定或刪除的整個值。</span><span class="sxs-lookup"><span data-stu-id="993c3-170">If no \[~\] is present in the field, the string represents the entire value to be set or deleted.</span></span>

<span data-ttu-id="993c3-171">每個資料列只能包含一個值。</span><span class="sxs-lookup"><span data-stu-id="993c3-171">Each row can contain only one value.</span></span> <span data-ttu-id="993c3-172">例如，專案 *值*;*值* \[ ~ ; \]是一個以上的值，不應使用，因為它會造成無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="993c3-172">For example, the entry *Value*;*Value*;\[~\] is more than one value and should not be used because it causes unpredictable results.</span></span> <span data-ttu-id="993c3-173">專案 *值*; \[ ~ \]只是一個值。</span><span class="sxs-lookup"><span data-stu-id="993c3-173">The entry *Value*;\[~\] is just one value.</span></span>

<span data-ttu-id="993c3-174">如果名稱前面加上 +，就 \[ ~ \] 不能在 Value 資料行中使用。</span><span class="sxs-lookup"><span data-stu-id="993c3-174">If Name is prefixed with +, then \[~\] must not be used in Value column.</span></span> <span data-ttu-id="993c3-175">這是因為 "+" 和 "" 的意義 \[ ~ \] 明確地彼此互斥。</span><span class="sxs-lookup"><span data-stu-id="993c3-175">This is because the meaning of "+" and "\[~\]" are clearly exclusive of one another.</span></span>

</dd> <dt>

<span data-ttu-id="993c3-176"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="993c3-176"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="993c3-177">[元件資料表](component-table.md)第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="993c3-177">An external key to the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="993c3-178">此資料行參考控制環境值安裝的元件。</span><span class="sxs-lookup"><span data-stu-id="993c3-178">This column references the component that controls the installation of the environment values.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="993c3-179">備註</span><span class="sxs-lookup"><span data-stu-id="993c3-179">Remarks</span></span>

<span data-ttu-id="993c3-180">若要讓安裝程式設定環境變數，必須在[InstallExecuteSequence 資料表](installexecutesequence-table.md)中列出[WriteEnvironmentStrings 動作](writeenvironmentstrings-action.md)和[RemoveEnvironmentStrings 動作](removeenvironmentstrings-action.md)。</span><span class="sxs-lookup"><span data-stu-id="993c3-180">For the installer to set environment variables, the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) and [RemoveEnvironmentStrings action](removeenvironmentstrings-action.md) need to be listed in the [InstallExecuteSequence Table](installexecutesequence-table.md).</span></span>

<span data-ttu-id="993c3-181">請注意，執行 [WriteEnvironmentStrings 動作](writeenvironmentstrings-action.md) 或 [RemoveEnvironmentStrings 動作](removeenvironmentstrings-action.md) 時，環境變數不會變更進行中的安裝。</span><span class="sxs-lookup"><span data-stu-id="993c3-181">Note that environment variables do not change for the installation in progress when either the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) or [RemoveEnvironmentStrings action](removeenvironmentstrings-action.md) are run.</span></span> <span data-ttu-id="993c3-182">在 Windows 2000 上，這項資訊會儲存在登錄中，而訊息則會在安裝完成時通知系統變更。</span><span class="sxs-lookup"><span data-stu-id="993c3-182">On Windows 2000, this information is stored in the registry and a message notifies the system of changes when the installation completes.</span></span> <span data-ttu-id="993c3-183">新的進程或另一個檢查這些訊息的程式會使用新的環境變數。</span><span class="sxs-lookup"><span data-stu-id="993c3-183">A new process, or another process that checks for these messages, uses the new environment variables.</span></span>

<span data-ttu-id="993c3-184">使用環境資料表修改 path 環境變數時，請勿嘗試將整個新路徑明確地輸入到 [值] 欄位中。</span><span class="sxs-lookup"><span data-stu-id="993c3-184">When modifying the path environment variable with the Environment table, do not attempt to enter the entire new path explicitly into the Value field.</span></span> <span data-ttu-id="993c3-185">請改為將現有的路徑加上首碼或附加值和分隔符號 (; ) \[ ~ \] 。</span><span class="sxs-lookup"><span data-stu-id="993c3-185">Instead, extend the existing path by prefixing or appending a value and delimiter (;) to \[~\].</span></span> <span data-ttu-id="993c3-186">如果未 \[ ~ \] 出現在 [值] 欄位中，則會遺失現有的路徑資訊，而且安裝 .msi 檔案可能會導致電腦無法開機。</span><span class="sxs-lookup"><span data-stu-id="993c3-186">If \[~\] is not present in the Value field, the existing path information is lost and installing the .msi file may prevent the computer from booting.</span></span> <span data-ttu-id="993c3-187">Path 變數通常是使用語法： \[ ~ \] ;價值。</span><span class="sxs-lookup"><span data-stu-id="993c3-187">The path variable is mostly commonly set using the syntax: \[~\];Value.</span></span>

<span data-ttu-id="993c3-188">從終端機伺服器執行每部電腦安裝時，安裝程式會將每個使用者的環境變數寫入 **HKU \\ 。預設 \\ 環境**。</span><span class="sxs-lookup"><span data-stu-id="993c3-188">When performing per-machine installations from a terminal server, the installer writes per-user environment variables to **HKU\\.Default\\Environment**.</span></span> <span data-ttu-id="993c3-189">因為終端機服務不會複寫登錄的這個區段，所以安裝不會設定每個使用者的環境變數。</span><span class="sxs-lookup"><span data-stu-id="993c3-189">Because Terminal Services does not replicate this section of the registry, the installation does not set the per-user environment variables.</span></span> <span data-ttu-id="993c3-190">針對每部電腦安裝所使用的套件，應該包含在 [名稱] 資料行中，以將環境變數寫入電腦的環境 \* 中。</span><span class="sxs-lookup"><span data-stu-id="993c3-190">A package used for per-machine installations should write environment variables to the computer's environment by including \* in the Name column.</span></span> <span data-ttu-id="993c3-191">如果可以為每位使用者或每部電腦安裝封裝，請建立兩個元件： (1) 具有針對使用者設定撰寫之環境資料表專案的每個使用者元件，以及 (2) 個別電腦的元件，以及針對電腦設定所撰寫的環境資料表。</span><span class="sxs-lookup"><span data-stu-id="993c3-191">If the package can be installed per-user or per-machine, create two components: (1) a per-user component with the Environment table entries authored for user settings, and (2) a per-machine component with the Environment table authored for computer settings.</span></span> <span data-ttu-id="993c3-192">條件：使用具特殊 [**許可權**](privileged.md) 的屬性安裝此元件。</span><span class="sxs-lookup"><span data-stu-id="993c3-192">Condition the installation of this component using the [**Privileged**](privileged.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="993c3-193">驗證</span><span class="sxs-lookup"><span data-stu-id="993c3-193">Validation</span></span>

<dl>

[<span data-ttu-id="993c3-194">ICE03</span><span class="sxs-lookup"><span data-stu-id="993c3-194">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="993c3-195">ICE06</span><span class="sxs-lookup"><span data-stu-id="993c3-195">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="993c3-196">ICE32</span><span class="sxs-lookup"><span data-stu-id="993c3-196">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="993c3-197">ICE46</span><span class="sxs-lookup"><span data-stu-id="993c3-197">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="993c3-198">ICE65</span><span class="sxs-lookup"><span data-stu-id="993c3-198">ICE65</span></span>](ice65.md)  
[<span data-ttu-id="993c3-199">ICE69</span><span class="sxs-lookup"><span data-stu-id="993c3-199">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="993c3-200">ICE80</span><span class="sxs-lookup"><span data-stu-id="993c3-200">ICE80</span></span>](ice80.md)  
</dl>

 

 




