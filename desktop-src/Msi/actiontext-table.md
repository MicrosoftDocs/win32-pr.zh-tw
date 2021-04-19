---
description: ActionText 資料表包含要在 [進度] 對話方塊中顯示的文字，並會寫入記錄檔中，以找出需要很長時間才能執行的動作。 顯示的文字包含動作描述，以及來自動作的選擇性格式化資料。
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: ActionText 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980813"
---
# <a name="actiontext-table"></a><span data-ttu-id="05170-104">ActionText 資料表</span><span class="sxs-lookup"><span data-stu-id="05170-104">ActionText Table</span></span>

<span data-ttu-id="05170-105">ActionText 資料表包含要在 [進度] 對話方塊中顯示的文字，並會寫入記錄檔中，以找出需要很長時間才能執行的動作。</span><span class="sxs-lookup"><span data-stu-id="05170-105">The ActionText Table contains text to be displayed in a progress dialog box, and written to the log for actions that take a long time to execute.</span></span> <span data-ttu-id="05170-106">顯示的文字包含動作描述，以及來自動作的選擇性格式化資料。</span><span class="sxs-lookup"><span data-stu-id="05170-106">The displayed text consists of the action description and optionally formatted data from the action.</span></span>

<span data-ttu-id="05170-107">ActionText 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="05170-107">The ActionText Table has the following columns.</span></span>



| <span data-ttu-id="05170-108">Column</span><span class="sxs-lookup"><span data-stu-id="05170-108">Column</span></span>      | <span data-ttu-id="05170-109">類型</span><span class="sxs-lookup"><span data-stu-id="05170-109">Type</span></span>                         | <span data-ttu-id="05170-110">答案</span><span class="sxs-lookup"><span data-stu-id="05170-110">Key</span></span> | <span data-ttu-id="05170-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="05170-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="05170-112">動作</span><span class="sxs-lookup"><span data-stu-id="05170-112">Action</span></span>      | [<span data-ttu-id="05170-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="05170-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="05170-114">Y</span><span class="sxs-lookup"><span data-stu-id="05170-114">Y</span></span>   | <span data-ttu-id="05170-115">N</span><span class="sxs-lookup"><span data-stu-id="05170-115">N</span></span>        |
| <span data-ttu-id="05170-116">Description</span><span class="sxs-lookup"><span data-stu-id="05170-116">Description</span></span> | [<span data-ttu-id="05170-117">Text</span><span class="sxs-lookup"><span data-stu-id="05170-117">Text</span></span>](text.md)             | <span data-ttu-id="05170-118">N</span><span class="sxs-lookup"><span data-stu-id="05170-118">N</span></span>   | <span data-ttu-id="05170-119">Y</span><span class="sxs-lookup"><span data-stu-id="05170-119">Y</span></span>        |
| <span data-ttu-id="05170-120">範本</span><span class="sxs-lookup"><span data-stu-id="05170-120">Template</span></span>    | [<span data-ttu-id="05170-121">範本</span><span class="sxs-lookup"><span data-stu-id="05170-121">Template</span></span>](template.md)     | <span data-ttu-id="05170-122">N</span><span class="sxs-lookup"><span data-stu-id="05170-122">N</span></span>   | <span data-ttu-id="05170-123">Y</span><span class="sxs-lookup"><span data-stu-id="05170-123">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="05170-124">資料行</span><span class="sxs-lookup"><span data-stu-id="05170-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="05170-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="05170-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="05170-126">動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="05170-126">Name of the action.</span></span>

<span data-ttu-id="05170-127">主表索引鍵。</span><span class="sxs-lookup"><span data-stu-id="05170-127">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="05170-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="05170-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="05170-129">顯示在 [進度] 對話方塊中，或在執行動作時寫入至記錄檔的當地語系化描述。</span><span class="sxs-lookup"><span data-stu-id="05170-129">Localized description that is displayed in the progress dialog box, or written to the log when the action is executing.</span></span>

</dd> <dt>

<span data-ttu-id="05170-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>範本</span><span class="sxs-lookup"><span data-stu-id="05170-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Template</span></span>
</dt> <dd>

<span data-ttu-id="05170-131">當地語系化的格式範本，用來格式化動作資料記錄，以便在執行動作時顯示。</span><span class="sxs-lookup"><span data-stu-id="05170-131">A localized format template that is used to format action data records to display during action execution.</span></span> <span data-ttu-id="05170-132">如果未提供範本，則不會顯示動作資料。</span><span class="sxs-lookup"><span data-stu-id="05170-132">If a template is not supplied, then the action data is not displayed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05170-133">備註</span><span class="sxs-lookup"><span data-stu-id="05170-133">Remarks</span></span>

<span data-ttu-id="05170-134">一般而言，ActionText 資料表中的專案會參考順序資料表中的動作。</span><span class="sxs-lookup"><span data-stu-id="05170-134">Typically, the entries in the ActionText table refer to actions in sequence tables.</span></span> <span data-ttu-id="05170-135">安裝程式所執行的其他動作不會列在順序資料表中，但仍然需要在資料表中指定。</span><span class="sxs-lookup"><span data-stu-id="05170-135">There are other actions the installer performs that are not listed in the sequence table, but still need to be specified in the table.</span></span> <span data-ttu-id="05170-136">下表識別必要的資料表專案，其中必須完全依照顯示的方式撰寫動作名稱和範本，但是可以自訂描述。</span><span class="sxs-lookup"><span data-stu-id="05170-136">The following table identifies the required table entries where the action name and template must be authored exactly as shown, but the description can be customized.</span></span>



| <span data-ttu-id="05170-137">動作</span><span class="sxs-lookup"><span data-stu-id="05170-137">Action</span></span>          | <span data-ttu-id="05170-138">描述</span><span class="sxs-lookup"><span data-stu-id="05170-138">Description</span></span>                             | <span data-ttu-id="05170-139">範本</span><span class="sxs-lookup"><span data-stu-id="05170-139">Template</span></span> |
|-----------------|-----------------------------------------|----------|
| <span data-ttu-id="05170-140">復原</span><span class="sxs-lookup"><span data-stu-id="05170-140">Rollback</span></span>        | <span data-ttu-id="05170-141">復原動作。</span><span class="sxs-lookup"><span data-stu-id="05170-141">Undoes actions.</span></span>                         | <span data-ttu-id="05170-142">\[1\]</span><span class="sxs-lookup"><span data-stu-id="05170-142">\[1\]</span></span>    |
| <span data-ttu-id="05170-143">RollbackCleanup</span><span class="sxs-lookup"><span data-stu-id="05170-143">RollbackCleanup</span></span> | <span data-ttu-id="05170-144">移除舊檔案。</span><span class="sxs-lookup"><span data-stu-id="05170-144">Removes old files.</span></span>                      | <span data-ttu-id="05170-145">\[1\]</span><span class="sxs-lookup"><span data-stu-id="05170-145">\[1\]</span></span>    |
| <span data-ttu-id="05170-146">GenerateScript</span><span class="sxs-lookup"><span data-stu-id="05170-146">GenerateScript</span></span>  | <span data-ttu-id="05170-147">產生動作的系統作業。</span><span class="sxs-lookup"><span data-stu-id="05170-147">Generates system operations for action.</span></span> | <span data-ttu-id="05170-148">\[1\]</span><span class="sxs-lookup"><span data-stu-id="05170-148">\[1\]</span></span>    |



 

> [!Note]  
> <span data-ttu-id="05170-149">只有在安裝腳本內執行的動作才會顯示動作文字。</span><span class="sxs-lookup"><span data-stu-id="05170-149">Action text is only displayed for actions that run within the installation script.</span></span> <span data-ttu-id="05170-150">因此，只有在 [InstallInitialize](installinitialize-action.md) 和 [InstallFinalize](installfinalize-action.md) 動作之間排序的動作才會顯示動作文字。</span><span class="sxs-lookup"><span data-stu-id="05170-150">Therefore, action text is only displayed for actions that are sequenced between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

 

<span data-ttu-id="05170-151">您可以使用 Msidb.exe 或 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)，將當地語系化的 ActionText 資料表匯入資料庫中。</span><span class="sxs-lookup"><span data-stu-id="05170-151">You can import a localized ActionText table into your database by using Msidb.exe or [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="05170-152">SDK 包含當地語系化的 ActionText 資料表，適用于「 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md) 」一節中所列的每一種語言。</span><span class="sxs-lookup"><span data-stu-id="05170-152">The SDK includes a localized ActionText Table for each of the languages listed in the [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) section.</span></span> <span data-ttu-id="05170-153">如果未填入 ActionText 資料表，安裝程式會針對 [**ProductLanguage**](productlanguage.md) 屬性所指定的語言載入當地語系化的字串。</span><span class="sxs-lookup"><span data-stu-id="05170-153">If the ActionText table is not populated, the installer loads localized strings for the language specified by the [**ProductLanguage**](productlanguage.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="05170-154">驗證</span><span class="sxs-lookup"><span data-stu-id="05170-154">Validation</span></span>

<dl>

[<span data-ttu-id="05170-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="05170-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="05170-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="05170-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="05170-157">ICE46</span><span class="sxs-lookup"><span data-stu-id="05170-157">ICE46</span></span>](ice46.md)  
</dl>

 

 



