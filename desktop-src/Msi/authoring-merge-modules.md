---
description: 下列程式說明撰寫合併模組的一般步驟。
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: 撰寫合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192455"
---
# <a name="authoring-merge-modules"></a><span data-ttu-id="f4bf7-103">撰寫合併模組</span><span class="sxs-lookup"><span data-stu-id="f4bf7-103">Authoring Merge Modules</span></span>

<span data-ttu-id="f4bf7-104">下列程式說明撰寫合併模組的一般步驟。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-104">The following procedure describes the general steps to authoring merge modules.</span></span>

<span data-ttu-id="f4bf7-105">**若要建立新的合併模組**</span><span class="sxs-lookup"><span data-stu-id="f4bf7-105">**To create a new merge module**</span></span>

1.  <span data-ttu-id="f4bf7-106">取得可用來編輯合併模組資料庫的軟體工具。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-106">Obtain a software tool you can use to edit the merge module database.</span></span>
2.  <span data-ttu-id="f4bf7-107">取得空白的合併模組資料庫。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-107">Obtain a blank merge module database.</span></span>
3.  <span data-ttu-id="f4bf7-108">產生合併模組的 [GUID](guid.md) 。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-108">Generate a [GUID](guid.md) for the merge module.</span></span> <span data-ttu-id="f4bf7-109">在合併模組中撰寫資料庫資料表的主鍵時，您必須使用此 GUID。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-109">You need to use this GUID when authoring the primary keys of database tables in the merge module.</span></span>
4.  <span data-ttu-id="f4bf7-110">將記錄加入至合併所傳遞之每個元件的 [元件資料表](component-table.md) 中。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-110">Add a record to the [Component table](component-table.md) for each component delivered by the merge.</span></span> <span data-ttu-id="f4bf7-111">每個合併模組都需要元件資料表。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-111">A Component table is required in every merge module.</span></span> <span data-ttu-id="f4bf7-112">請注意，合併模組會操作元件，而不是功能。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-112">Note that merge modules operate with components and not with features.</span></span> <span data-ttu-id="f4bf7-113">不過，在某些情況下，資料庫資料表專案可能需要參考功能。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-113">In certain cases, however, a database table entry may need to reference a feature.</span></span> <span data-ttu-id="f4bf7-114">如需詳細資訊，請參閱 [合併模組中的參考功能](referencing-features-in-merge-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-114">For details, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>
5.  <span data-ttu-id="f4bf7-115">將 [目錄資料表](directory-table.md) 加入至合併模組，以指定合併模組新增至目標資料庫的目錄配置。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-115">Add a [Directory table](directory-table.md) to the merge module that specifies the layout of directories the merge module adds to the target database.</span></span> <span data-ttu-id="f4bf7-116">每個合併模組都需要目錄資料表。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-116">A Directory table is required in every merge module.</span></span>
6.  <span data-ttu-id="f4bf7-117">將空白的 [FeatureComponents 資料表](featurecomponents-table.md) 匯入到合併模組資料庫中。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-117">Import a blank [FeatureComponents table](featurecomponents-table.md) into the merge module database.</span></span> <span data-ttu-id="f4bf7-118">如果 .msi 檔案未包含它自己的 FeatureComponents 資料表，這個空白資料表就會提供合併工具的指導方針。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-118">This empty table provides a guideline for the merge tool in cases where the .msi file does not contain its own FeatureComponents table.</span></span>
7.  <span data-ttu-id="f4bf7-119">收集由此合併模組提供的所有檔案，並建立 [MergeModule.CABinet](mergemodule-cabinet.md) 封包檔。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-119">Collect all the files delivered by this merge module and create the [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file.</span></span> <span data-ttu-id="f4bf7-120">將封包加入至合併模組，作為 .msm 檔案內的資料流程。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-120">Add the cabinet to the merge module as a stream inside the .msm file.</span></span>
8.  <span data-ttu-id="f4bf7-121">針對儲存在 MergeModule.CABinet 中的每個檔案，將記錄新增至檔案資料表。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-121">Add a record to the File table for every file stored in MergeModule.CABinet.</span></span>
9.  <span data-ttu-id="f4bf7-122">在 [ModuleSignature 資料表](modulesignature-table.md)中，加入識別合併模組所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-122">Add the information necessary to identify the merge module in the [ModuleSignature table](modulesignature-table.md).</span></span> <span data-ttu-id="f4bf7-123">每個合併模組都需要 ModuleSignature 資料表。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-123">Every merge module requires a ModuleSignature table.</span></span>
10. <span data-ttu-id="f4bf7-124">列出 [ModuleComponents 資料表](modulecomponents-table.md)中 merge 模組的元件。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-124">List the components in the merge module in the [ModuleComponents table](modulecomponents-table.md).</span></span> <span data-ttu-id="f4bf7-125">每個合併模組都需要 ModuleComponents 資料表。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-125">Every merge module requires a ModuleComponents table.</span></span>
11. <span data-ttu-id="f4bf7-126">只有在合併模組必須修改目標安裝資料庫的 [*順序資料表*](s-gly.md) 時，才將 merge module sequence 資料表加入至 .msm 檔。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-126">Add merge module sequence tables to the .msm file only if the merge module needs to modify the [*sequence tables*](s-gly.md) of the target installation database.</span></span>
12. <span data-ttu-id="f4bf7-127">將 \_ 驗證資料表加入至合併模組。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-127">Add a \_Validation table to the merge module.</span></span> <span data-ttu-id="f4bf7-128">合併模組需要 \_ 驗證資料表才能通過驗證。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-128">A merge module requires a \_Validation table to pass validation.</span></span>
13. <span data-ttu-id="f4bf7-129">合併模組在少數情況下只需要使用者介面。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-129">Merge modules require a user interface in only rare cases.</span></span> <span data-ttu-id="f4bf7-130">不建議包含包含合併模組的 UI。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-130">Including a UI with a merge module is not recommended.</span></span> <span data-ttu-id="f4bf7-131">在需要使用者介面的情況下，可以將 UI 資料表合併到 .msi 檔案中，與其他資料表相同。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-131">In cases where a user interface is required, the UI tables can be merged into the .msi file the same as other tables.</span></span>
14. <span data-ttu-id="f4bf7-132">將登錄資訊加入至合併模組資料庫中的適當登錄資料表。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-132">Add registry information to the appropriate registry tables in the merge module database.</span></span> <span data-ttu-id="f4bf7-133">將類型程式庫、類別、延伸模組和動詞的登錄資訊新增至 [TypeLib](typelib-table.md)、 [類別](class-table.md)、 [AppId](appid-table.md)、 [ProgId](progid-table.md)、 [延伸](extension-table.md)模組、 [動詞](verb-table.md)或 [MIME](mime-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-133">Add registry information for type libraries, classes, extensions, and verbs into the [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="f4bf7-134">所有其他登錄資訊都可以進入登錄 [表](registry-table.md)。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-134">All other registry information can go into the [Registry table](registry-table.md).</span></span> <span data-ttu-id="f4bf7-135">不建議使用 SelfReg 資料表。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-135">The use of the SelfReg table is not recommended.</span></span>
15. <span data-ttu-id="f4bf7-136">將摘要資訊加入至 [合併模組摘要資訊資料流程](merge-module-summary-information-stream-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-136">Add the summary information to the [Merge Module Summary Information Stream](merge-module-summary-information-stream-reference.md).</span></span>
16. <span data-ttu-id="f4bf7-137">請先在所有合併模組上執行驗證，再嘗試安裝。</span><span class="sxs-lookup"><span data-stu-id="f4bf7-137">Run validation on all merge modules before attempting to install.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4bf7-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="f4bf7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4bf7-139">取得空白合併模組資料庫</span><span class="sxs-lookup"><span data-stu-id="f4bf7-139">Obtaining Blank Merge Module Databases</span></span>](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-140">取得合併模組撰寫工具</span><span class="sxs-lookup"><span data-stu-id="f4bf7-140">Obtaining Merge Module Authoring Tools</span></span>](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-141">命名合併模組資料庫中的主鍵</span><span class="sxs-lookup"><span data-stu-id="f4bf7-141">Naming Primary Keys in Merge Module Databases</span></span>](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-142">撰寫合併模組元件資料表</span><span class="sxs-lookup"><span data-stu-id="f4bf7-142">Authoring Merge Module Component Tables</span></span>](authoring-merge-module-component-tables.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-143">撰寫合併模組目錄資料表</span><span class="sxs-lookup"><span data-stu-id="f4bf7-143">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-144">撰寫合併模組 FeatureComponents 資料表</span><span class="sxs-lookup"><span data-stu-id="f4bf7-144">Authoring Merge Module FeatureComponents Tables</span></span>](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-145">產生 MergeModule.CABinet 封包檔</span><span class="sxs-lookup"><span data-stu-id="f4bf7-145">Generating MergeModule.CABinet Cabinet Files</span></span>](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-146">撰寫合併模組檔案資料表</span><span class="sxs-lookup"><span data-stu-id="f4bf7-146">Authoring Merge Module File Tables</span></span>](authoring-merge-module-file-tables.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-147">撰寫 ModuleSignature 資料表</span><span class="sxs-lookup"><span data-stu-id="f4bf7-147">Authoring ModuleSignature Tables</span></span>](authoring-modulesignature-tables.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-148">撰寫 ModuleComponents 資料表</span><span class="sxs-lookup"><span data-stu-id="f4bf7-148">Authoring ModuleComponents Tables</span></span>](authoring-modulecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-149">撰寫合併模組順序資料表</span><span class="sxs-lookup"><span data-stu-id="f4bf7-149">Authoring Merge Module Sequence Tables</span></span>](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-150">驗證合併模組</span><span class="sxs-lookup"><span data-stu-id="f4bf7-150">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-151">在合併模組中撰寫使用者介面</span><span class="sxs-lookup"><span data-stu-id="f4bf7-151">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-152">撰寫合併模組登錄資料表</span><span class="sxs-lookup"><span data-stu-id="f4bf7-152">Authoring Merge Module Registry Tables</span></span>](authoring-merge-module-registry-tables.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-153">撰寫合併模組摘要資訊資料流程</span><span class="sxs-lookup"><span data-stu-id="f4bf7-153">Authoring Merge Module Summary Information Streams</span></span>](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[<span data-ttu-id="f4bf7-154">合併模組摘要資訊資料流程參考</span><span class="sxs-lookup"><span data-stu-id="f4bf7-154">Merge Module Summary Information Stream Reference</span></span>](merge-module-summary-information-stream-reference.md)
</dt> <dt>

<span data-ttu-id="f4bf7-155">驗證合併模組</span><span class="sxs-lookup"><span data-stu-id="f4bf7-155">Validating Merge Modules</span></span>
</dt> <dt>

[<span data-ttu-id="f4bf7-156">使用64位合併模組</span><span class="sxs-lookup"><span data-stu-id="f4bf7-156">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



