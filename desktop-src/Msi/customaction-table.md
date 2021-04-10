---
description: CustomAction 資料表提供將自訂程式碼和資料整合至安裝的方法。 所執行程式碼的來源可以是包含在資料庫內的資料流程、最近安裝的檔案，或現有的可執行檔。
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: CustomAction 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690839"
---
# <a name="customaction-table"></a><span data-ttu-id="93e26-104">CustomAction 資料表</span><span class="sxs-lookup"><span data-stu-id="93e26-104">CustomAction Table</span></span>

<span data-ttu-id="93e26-105">CustomAction 資料表提供將自訂程式碼和資料整合至安裝的方法。</span><span class="sxs-lookup"><span data-stu-id="93e26-105">The CustomAction table provides the means of integrating custom code and data into the installation.</span></span> <span data-ttu-id="93e26-106">所執行程式碼的來源可以是包含在資料庫內的資料流程、最近安裝的檔案，或現有的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="93e26-106">The source of the code that is executed can be a stream contained within the database, a recently installed file, or an existing executable file.</span></span>

<span data-ttu-id="93e26-107">CustomAction 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="93e26-107">The CustomAction table has the following columns.</span></span>



| <span data-ttu-id="93e26-108">Column</span><span class="sxs-lookup"><span data-stu-id="93e26-108">Column</span></span>       | <span data-ttu-id="93e26-109">類型</span><span class="sxs-lookup"><span data-stu-id="93e26-109">Type</span></span>                               | <span data-ttu-id="93e26-110">答案</span><span class="sxs-lookup"><span data-stu-id="93e26-110">Key</span></span> | <span data-ttu-id="93e26-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="93e26-111">Nullable</span></span> |
|--------------|------------------------------------|-----|----------|
| <span data-ttu-id="93e26-112">動作</span><span class="sxs-lookup"><span data-stu-id="93e26-112">Action</span></span>       | [<span data-ttu-id="93e26-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="93e26-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="93e26-114">Y</span><span class="sxs-lookup"><span data-stu-id="93e26-114">Y</span></span>   | <span data-ttu-id="93e26-115">N</span><span class="sxs-lookup"><span data-stu-id="93e26-115">N</span></span>        |
| <span data-ttu-id="93e26-116">類型</span><span class="sxs-lookup"><span data-stu-id="93e26-116">Type</span></span>         | [<span data-ttu-id="93e26-117">整數</span><span class="sxs-lookup"><span data-stu-id="93e26-117">Integer</span></span>](integer.md)             | <span data-ttu-id="93e26-118">N</span><span class="sxs-lookup"><span data-stu-id="93e26-118">N</span></span>   | <span data-ttu-id="93e26-119">N</span><span class="sxs-lookup"><span data-stu-id="93e26-119">N</span></span>        |
| <span data-ttu-id="93e26-120">來源</span><span class="sxs-lookup"><span data-stu-id="93e26-120">Source</span></span>       | [<span data-ttu-id="93e26-121">CustomSource</span><span class="sxs-lookup"><span data-stu-id="93e26-121">CustomSource</span></span>](customsource.md)   | <span data-ttu-id="93e26-122">N</span><span class="sxs-lookup"><span data-stu-id="93e26-122">N</span></span>   | <span data-ttu-id="93e26-123">Y</span><span class="sxs-lookup"><span data-stu-id="93e26-123">Y</span></span>        |
| <span data-ttu-id="93e26-124">目標</span><span class="sxs-lookup"><span data-stu-id="93e26-124">Target</span></span>       | [<span data-ttu-id="93e26-125">格式 化</span><span class="sxs-lookup"><span data-stu-id="93e26-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="93e26-126">N</span><span class="sxs-lookup"><span data-stu-id="93e26-126">N</span></span>   | <span data-ttu-id="93e26-127">Y</span><span class="sxs-lookup"><span data-stu-id="93e26-127">Y</span></span>        |
| <span data-ttu-id="93e26-128">ExtendedType</span><span class="sxs-lookup"><span data-stu-id="93e26-128">ExtendedType</span></span> | [<span data-ttu-id="93e26-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="93e26-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="93e26-130">N</span><span class="sxs-lookup"><span data-stu-id="93e26-130">N</span></span>   | <span data-ttu-id="93e26-131">Y</span><span class="sxs-lookup"><span data-stu-id="93e26-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="93e26-132">資料行</span><span class="sxs-lookup"><span data-stu-id="93e26-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="93e26-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="93e26-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="93e26-134">動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="93e26-134">Name of the action.</span></span> <span data-ttu-id="93e26-135">此動作通常會出現在順序資料表中，除非由另一個自訂動作呼叫。</span><span class="sxs-lookup"><span data-stu-id="93e26-135">The action normally appears in a sequence table unless it is called by another custom action.</span></span> <span data-ttu-id="93e26-136">如果名稱符合任何內建的動作，則永遠不會呼叫自訂動作。</span><span class="sxs-lookup"><span data-stu-id="93e26-136">If the name matches any built-in action, then the custom action is never called.</span></span>

<span data-ttu-id="93e26-137">主表索引鍵。</span><span class="sxs-lookup"><span data-stu-id="93e26-137">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="93e26-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型</span><span class="sxs-lookup"><span data-stu-id="93e26-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="93e26-139">旗標位的欄位，指定自訂動作和選項的基本類型。</span><span class="sxs-lookup"><span data-stu-id="93e26-139">A field of flag bits specifying the basic type of custom action and options.</span></span> <span data-ttu-id="93e26-140">如需基本類型清單，請參閱 [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md) 。</span><span class="sxs-lookup"><span data-stu-id="93e26-140">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a list of the basic types.</span></span> <span data-ttu-id="93e26-141">請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)、 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)、 [自訂動作隱藏目標選項](custom-action-hidden-target-option.md)，以及 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="93e26-141">See [Custom Action Return Processing Options](custom-action-return-processing-options.md), [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md), [Custom Action Hidden Target Option](custom-action-hidden-target-option.md), and [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

</dd> <dt>

<span data-ttu-id="93e26-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>源</span><span class="sxs-lookup"><span data-stu-id="93e26-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="93e26-143">另一個資料表中的屬性名稱或外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="93e26-143">A property name or external key into another table.</span></span> <span data-ttu-id="93e26-144">如需可能的自訂動作來源的討論，請參閱 [自訂動作來源](custom-action-sources.md) 和 [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md)。</span><span class="sxs-lookup"><span data-stu-id="93e26-144">For a discussion of the possible custom action sources, see [Custom Action Sources](custom-action-sources.md) and the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span> <span data-ttu-id="93e26-145">例如，來源資料行可能會在下列其中一個資料表的第一個資料行中包含一個外部索引鍵，其中包含自訂動作程式碼的來源。</span><span class="sxs-lookup"><span data-stu-id="93e26-145">For example, the Source column may contain an external key into the first column of one of the following tables containing the source of the custom action code.</span></span>

<span data-ttu-id="93e26-146">用來呼叫現有可執行檔的[目錄資料表](directory-table.md)。</span><span class="sxs-lookup"><span data-stu-id="93e26-146">[Directory table](directory-table.md) for calling existing executables.</span></span>

<span data-ttu-id="93e26-147">用來呼叫剛剛安裝之可執行檔和 Dll 的檔案[資料表](file-table.md)。</span><span class="sxs-lookup"><span data-stu-id="93e26-147">[File table](file-table.md) for calling executables and DLLs that have just been installed.</span></span>

<span data-ttu-id="93e26-148">用於呼叫可執行檔、Dll 和儲存在資料庫中之資料的[二進位資料表](binary-table.md)。</span><span class="sxs-lookup"><span data-stu-id="93e26-148">[Binary table](binary-table.md) for calling executables, DLLs, and data stored in the database.</span></span>

<span data-ttu-id="93e26-149">[屬性工作表](property-table.md) ，用於呼叫屬性所持有之路徑的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="93e26-149">[Property table](property-table.md) for calling executables whose paths are held by a property.</span></span>

</dd> <dt>

<span data-ttu-id="93e26-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>目標</span><span class="sxs-lookup"><span data-stu-id="93e26-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="93e26-151">視自訂動作的基本類型而定的執行參數。</span><span class="sxs-lookup"><span data-stu-id="93e26-151">An execution parameter that depends on the basic type of custom action.</span></span> <span data-ttu-id="93e26-152">如需每個自訂動作類型的說明，請參閱 [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md) 。</span><span class="sxs-lookup"><span data-stu-id="93e26-152">See the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a description of what should be entered in this field for each type of custom action.</span></span> <span data-ttu-id="93e26-153">例如，根據自訂動作而定，此欄位可能包含下列各項。</span><span class="sxs-lookup"><span data-stu-id="93e26-153">For example, this field may contain the following depending on the custom action.</span></span>



| <span data-ttu-id="93e26-154">目標</span><span class="sxs-lookup"><span data-stu-id="93e26-154">Target</span></span>                                    | <span data-ttu-id="93e26-155">自訂動作</span><span class="sxs-lookup"><span data-stu-id="93e26-155">Custom action</span></span>                         |
|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="93e26-156">需要 (進入點) </span><span class="sxs-lookup"><span data-stu-id="93e26-156">Entry point (required)</span></span>                    | <span data-ttu-id="93e26-157">呼叫 DLL。</span><span class="sxs-lookup"><span data-stu-id="93e26-157">Calling a DLL.</span></span>                        |
| <span data-ttu-id="93e26-158">具有引數 (必要) 的可執行檔名稱</span><span class="sxs-lookup"><span data-stu-id="93e26-158">Executable name with arguments (required)</span></span> | <span data-ttu-id="93e26-159">呼叫現有的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="93e26-159">Calling an existing executable.</span></span>       |
| <span data-ttu-id="93e26-160">命令列引數 (選擇性) </span><span class="sxs-lookup"><span data-stu-id="93e26-160">Command line arguments (optional)</span></span>         | <span data-ttu-id="93e26-161">呼叫剛剛安裝的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="93e26-161">Calling an executable just installed.</span></span> |
| <span data-ttu-id="93e26-162">目的檔案名 (必要) </span><span class="sxs-lookup"><span data-stu-id="93e26-162">Target file name (required)</span></span>               | <span data-ttu-id="93e26-163">從自訂資料建立檔案。</span><span class="sxs-lookup"><span data-stu-id="93e26-163">Creating a file from custom data.</span></span>     |
| <span data-ttu-id="93e26-164">Null</span><span class="sxs-lookup"><span data-stu-id="93e26-164">Null</span></span>                                      | <span data-ttu-id="93e26-165">執行腳本。</span><span class="sxs-lookup"><span data-stu-id="93e26-165">Executing script code.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="93e26-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span><span class="sxs-lookup"><span data-stu-id="93e26-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span></span>
</dt> <dd>

<span data-ttu-id="93e26-167">在此欄位中輸入 **msidbCustomActionTypePatchUninstall** 值，以使用 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md)來指定自訂動作。</span><span class="sxs-lookup"><span data-stu-id="93e26-167">Enter the **msidbCustomActionTypePatchUninstall** value in this field to specify a custom action with the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md).</span></span>

<span data-ttu-id="93e26-168">**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="93e26-168">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="93e26-169">從 Windows Installer 4.5 開始，可以使用此選項。</span><span class="sxs-lookup"><span data-stu-id="93e26-169">This option is available beginning with Windows Installer 4.5.</span></span>

</dd> </dl>

<span data-ttu-id="93e26-170">如需詳細資訊，請參閱 [自訂動作](custom-actions.md)底下的所有主題。</span><span class="sxs-lookup"><span data-stu-id="93e26-170">For more information, see all the topics under [Custom Actions](custom-actions.md).</span></span>

## <a name="validation"></a><span data-ttu-id="93e26-171">驗證</span><span class="sxs-lookup"><span data-stu-id="93e26-171">Validation</span></span>

<dl>

[<span data-ttu-id="93e26-172">ICE03</span><span class="sxs-lookup"><span data-stu-id="93e26-172">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="93e26-173">ICE06</span><span class="sxs-lookup"><span data-stu-id="93e26-173">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="93e26-174">ICE12</span><span class="sxs-lookup"><span data-stu-id="93e26-174">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="93e26-175">ICE27</span><span class="sxs-lookup"><span data-stu-id="93e26-175">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="93e26-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="93e26-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="93e26-177">ICE63</span><span class="sxs-lookup"><span data-stu-id="93e26-177">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="93e26-178">ICE68</span><span class="sxs-lookup"><span data-stu-id="93e26-178">ICE68</span></span>](ice68.md)  
[<span data-ttu-id="93e26-179">ICE72</span><span class="sxs-lookup"><span data-stu-id="93e26-179">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="93e26-180">ICE75</span><span class="sxs-lookup"><span data-stu-id="93e26-180">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="93e26-181">ICE77</span><span class="sxs-lookup"><span data-stu-id="93e26-181">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="93e26-182">ICE80</span><span class="sxs-lookup"><span data-stu-id="93e26-182">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="93e26-183">ICE88</span><span class="sxs-lookup"><span data-stu-id="93e26-183">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="93e26-184">ICE93</span><span class="sxs-lookup"><span data-stu-id="93e26-184">ICE93</span></span>](ice93.md)  
</dl>

 

 



