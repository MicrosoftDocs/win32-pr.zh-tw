---
description: ICE69 會檢查格式字串中 $componentkey 格式的所有子字串都 \[ \] 不會交互參照元件。
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194398"
---
# <a name="ice69"></a><span data-ttu-id="079fd-103">ICE69</span><span class="sxs-lookup"><span data-stu-id="079fd-103">ICE69</span></span>

<span data-ttu-id="079fd-104">ICE69 會檢查格式字串中 $componentkey 格式的所有子字串都 \[ \] 不會交互參照元件。 [](formatted.md)</span><span class="sxs-lookup"><span data-stu-id="079fd-104">ICE69 checks that all substrings of the form \[$componentkey\] within a [formatted](formatted.md) string do not cross-reference components.</span></span> <span data-ttu-id="079fd-105">當 \[ 格式化字串的 $componentkey 屬性參考的元件 \] 不是儲存在資料表的元件資料行中的元件時，就會發生跨元件參考 \_ 。</span><span class="sxs-lookup"><span data-stu-id="079fd-105">A cross-component reference occurs when the \[$componentkey\] property of a formatted string refers to a component other than the component stored in the Component\_ column of your tables.</span></span>

<span data-ttu-id="079fd-106">跨元件參考的問題會從評估 [格式化](formatted.md) 字串的方式產生。</span><span class="sxs-lookup"><span data-stu-id="079fd-106">Problems with cross-component referencing arise from the way [formatted](formatted.md) strings are evaluated.</span></span> <span data-ttu-id="079fd-107">如果已安裝 $componentkey 屬性所參考的元件， \[ \] 但目前的安裝期間未變更 (例如，正在重新安裝、移至來源等等) ，運算式 \[ $componentkey \] 會評估為 null，因為 $componentkey 中元件的動作狀態 \[ \] 為 null。</span><span class="sxs-lookup"><span data-stu-id="079fd-107">If the component referenced with the \[$componentkey\] property is already installed and is not being changed during the current installation (for example, being reinstalled, moved to source, and so forth), the expression \[$componentkey\] evaluates to null, because the action state of the component in \[$componentkey\] is null.</span></span> <span data-ttu-id="079fd-108">升級和修復作業期間可能會發生類似的問題。</span><span class="sxs-lookup"><span data-stu-id="079fd-108">Similar problems can occur during upgrade and repair operations.</span></span>

## <a name="result"></a><span data-ttu-id="079fd-109">結果</span><span class="sxs-lookup"><span data-stu-id="079fd-109">Result</span></span>

<span data-ttu-id="079fd-110">如果 \[ \] [格式化](formatted.md) 字串內的 $componentkey 子字串交互參考另一個功能中的元件，ICE69 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="079fd-110">ICE69 returns an error if a \[$componentkey\] substring within a [formatted](formatted.md) string cross-references a component in another feature.</span></span> <span data-ttu-id="079fd-111">如果 \[ \] 格式化字串內的 $componentkey 子字串交互參考相同功能中的元件，ICE69 會傳回警告。</span><span class="sxs-lookup"><span data-stu-id="079fd-111">ICE69 returns a warning if a \[$componentkey\] substring within a formatted string cross-references a component in the same feature.</span></span> <span data-ttu-id="079fd-112"> (使用 [FeatureComponents](featurecomponents-table.md) 資料表來判斷此對應。</span><span class="sxs-lookup"><span data-stu-id="079fd-112">(The [FeatureComponents](featurecomponents-table.md) table is used to determine this mapping.</span></span> <span data-ttu-id="079fd-113">它必須對應至警告的相同功能。</span><span class="sxs-lookup"><span data-stu-id="079fd-113">It must map to the same feature for the warning.</span></span> <span data-ttu-id="079fd-114">參考父功能中的元件或子功能中參考的元件會被視為錯誤。 ) </span><span class="sxs-lookup"><span data-stu-id="079fd-114">Referencing components in parent features or referencing components in child features is considered to be an error.)</span></span>

<span data-ttu-id="079fd-115">如果 \[ \# \] [格式化](formatted.md)字串中的 FileKey 子字串參考[的檔案](file-table.md)未在檔案資料表中指定為屬於相同元件，ICE69 會報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="079fd-115">ICE69 reports an error if the \[\#FileKey\] substring within a [formatted](formatted.md) string references a file which is not specified in the [File](file-table.md) table as belonging to the same component.</span></span>

## <a name="example"></a><span data-ttu-id="079fd-116">範例</span><span class="sxs-lookup"><span data-stu-id="079fd-116">Example</span></span>

<span data-ttu-id="079fd-117">ICE69 會報告下列範例所示的範例。</span><span class="sxs-lookup"><span data-stu-id="079fd-117">ICE69 reports the following for the examples shown.</span></span>

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

<span data-ttu-id="079fd-118">若要修正這個錯誤，請不要交互參照元件。</span><span class="sxs-lookup"><span data-stu-id="079fd-118">To fix this error, do not cross-reference components.</span></span> <span data-ttu-id="079fd-119">將 \[ $componentkey 變更 \] 為符合快速鍵的元件。</span><span class="sxs-lookup"><span data-stu-id="079fd-119">Change the \[$componentkey\] to match the component of the shortcut.</span></span>

<span data-ttu-id="079fd-120"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="079fd-120">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="079fd-121">快速鍵</span><span class="sxs-lookup"><span data-stu-id="079fd-121">Shortcut</span></span>  | <span data-ttu-id="079fd-122">元件\_</span><span class="sxs-lookup"><span data-stu-id="079fd-122">Component\_</span></span> | <span data-ttu-id="079fd-123">引數</span><span class="sxs-lookup"><span data-stu-id="079fd-123">Argument</span></span>     |
|-----------|-------------|--------------|
| <span data-ttu-id="079fd-124">測試</span><span class="sxs-lookup"><span data-stu-id="079fd-124">Test</span></span>      | <span data-ttu-id="079fd-125">QuickTest</span><span class="sxs-lookup"><span data-stu-id="079fd-125">QuickTest</span></span>   | <span data-ttu-id="079fd-126">-v \[ $Test\]</span><span class="sxs-lookup"><span data-stu-id="079fd-126">-v \[$Test\]</span></span> |
| <span data-ttu-id="079fd-127">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="079fd-127">Shortcut2</span></span> | <span data-ttu-id="079fd-128">QuickTest</span><span class="sxs-lookup"><span data-stu-id="079fd-128">QuickTest</span></span>   | <span data-ttu-id="079fd-129">\[$Test 2\]</span><span class="sxs-lookup"><span data-stu-id="079fd-129">\[$Test2\]</span></span>   |



 

<span data-ttu-id="079fd-130">[動詞](verb-table.md)和[延伸](extension-table.md)資料表是特殊案例，因為動詞資料表會參考屬於元件的副檔名。</span><span class="sxs-lookup"><span data-stu-id="079fd-130">The [Verb](verb-table.md) and [Extension](extension-table.md) tables are special cases in that the Verb table references an extension that belongs to a component.</span></span> <span data-ttu-id="079fd-131">不過，延伸模組可以屬於多個元件，因為擴充功能資料表的主鍵是由擴充功能和元件資料行所組成 \_ 。</span><span class="sxs-lookup"><span data-stu-id="079fd-131">An Extension, however, can belong to multiple components because the primary key for the extension table is made up of the Extension and Component\_ columns.</span></span> <span data-ttu-id="079fd-132">在邏輯上，您可能會發生下列情況。</span><span class="sxs-lookup"><span data-stu-id="079fd-132">You can logically have the following situation.</span></span>

<span data-ttu-id="079fd-133">[動詞資料表](verb-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="079fd-133">[Verb Table](verb-table.md) (partial)</span></span>



| <span data-ttu-id="079fd-134">分機</span><span class="sxs-lookup"><span data-stu-id="079fd-134">Extension</span></span> | <span data-ttu-id="079fd-135">動詞\_</span><span class="sxs-lookup"><span data-stu-id="079fd-135">Verb\_</span></span> | <span data-ttu-id="079fd-136">引數</span><span class="sxs-lookup"><span data-stu-id="079fd-136">Argument</span></span>                |
|-----------|--------|-------------------------|
| <span data-ttu-id="079fd-137">Tst</span><span class="sxs-lookup"><span data-stu-id="079fd-137">tst</span></span>       | <span data-ttu-id="079fd-138">開啟</span><span class="sxs-lookup"><span data-stu-id="079fd-138">open</span></span>   | <span data-ttu-id="079fd-139">-v \[ $comp 1 \] \[ $comp 2\]</span><span class="sxs-lookup"><span data-stu-id="079fd-139">-v \[$comp1\]\[$comp2\]</span></span> |



 

<span data-ttu-id="079fd-140">[延伸模組資料表](extension-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="079fd-140">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="079fd-141">分機</span><span class="sxs-lookup"><span data-stu-id="079fd-141">Extension</span></span> | <span data-ttu-id="079fd-142">元件\_</span><span class="sxs-lookup"><span data-stu-id="079fd-142">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="079fd-143">Tst</span><span class="sxs-lookup"><span data-stu-id="079fd-143">tst</span></span>       | <span data-ttu-id="079fd-144">comp1</span><span class="sxs-lookup"><span data-stu-id="079fd-144">comp1</span></span>       |
| <span data-ttu-id="079fd-145">Tst</span><span class="sxs-lookup"><span data-stu-id="079fd-145">tst</span></span>       | <span data-ttu-id="079fd-146">comp2</span><span class="sxs-lookup"><span data-stu-id="079fd-146">comp2</span></span>       |



 

[<span data-ttu-id="079fd-147">FeatureComponents 資料表</span><span class="sxs-lookup"><span data-stu-id="079fd-147">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="079fd-148">功能\_</span><span class="sxs-lookup"><span data-stu-id="079fd-148">Feature\_</span></span> | <span data-ttu-id="079fd-149">元件\_</span><span class="sxs-lookup"><span data-stu-id="079fd-149">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="079fd-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="079fd-150">Feature1</span></span>  | <span data-ttu-id="079fd-151">QuickTest</span><span class="sxs-lookup"><span data-stu-id="079fd-151">QuickTest</span></span>   |
| <span data-ttu-id="079fd-152">Feature1</span><span class="sxs-lookup"><span data-stu-id="079fd-152">Feature1</span></span>  | <span data-ttu-id="079fd-153">測試</span><span class="sxs-lookup"><span data-stu-id="079fd-153">Test</span></span>        |
| <span data-ttu-id="079fd-154">Feature2</span><span class="sxs-lookup"><span data-stu-id="079fd-154">Feature2</span></span>  | <span data-ttu-id="079fd-155">Test2</span><span class="sxs-lookup"><span data-stu-id="079fd-155">Test2</span></span>       |



 

<span data-ttu-id="079fd-156">在此情況下，您必須確定至少有一個 \[ $componentkey \] 屬性評估為非 null 值。</span><span class="sxs-lookup"><span data-stu-id="079fd-156">In this case, you must ensure that at least one of the \[$componentkey\] properties evaluates to a non-null value.</span></span> <span data-ttu-id="079fd-157">不過，在 \[ \] 上述範例中，動詞資料表的 Argument 資料行中的每個 $componentkey 屬性 (\[ $comp 1 \] 和 \[ $comp 2 \]) 必須參考與動詞相關聯之延伸模組隨附的可能元件。</span><span class="sxs-lookup"><span data-stu-id="079fd-157">However, every \[$componentkey\] property in the Argument column of the Verb table (\[$comp1\] and \[$comp2\] in the above example) must reference a possible component included with the extension associated with the verb.</span></span> <span data-ttu-id="079fd-158">類似 \[ $comp 3 的參考 \] 會導致 ICE69 的警告。</span><span class="sxs-lookup"><span data-stu-id="079fd-158">A reference like \[$comp3\] would result in a warning from ICE69.</span></span>

<span data-ttu-id="079fd-159">[AppId 資料表](appid-table.md)與動詞資料表有類似的情況。</span><span class="sxs-lookup"><span data-stu-id="079fd-159">The [AppId table](appid-table.md) has a similar situation to the Verb table.</span></span> <span data-ttu-id="079fd-160">它會使用 [類別表](class-table.md) 作為其元件參考。</span><span class="sxs-lookup"><span data-stu-id="079fd-160">It uses the [Class table](class-table.md) for its component reference.</span></span> <span data-ttu-id="079fd-161">在此情況下，AppId 資料表的驗證方式與 Verb-Extension 驗證 (現在是 AppId 類別) 。</span><span class="sxs-lookup"><span data-stu-id="079fd-161">In this case, the AppId table is validated in the same way as the Verb-Extension validation (now AppId-Class).</span></span>

<span data-ttu-id="079fd-162">類別資料表的引數資料行會像 [快速鍵](shortcut-table.md) [、登錄和類似](registry-table.md)的資料表一樣進行驗證。</span><span class="sxs-lookup"><span data-stu-id="079fd-162">The Class table's Argument column is validated like the [Shortcut](shortcut-table.md), [Registry](registry-table.md), and similar tables.</span></span>

## <a name="table-used-during-execution-only-if-found"></a><span data-ttu-id="079fd-163">只有在找到時，才會在執行 (中使用資料表) </span><span class="sxs-lookup"><span data-stu-id="079fd-163">Table used during execution (only if found)</span></span>

[<span data-ttu-id="079fd-164">IniFile</span><span class="sxs-lookup"><span data-stu-id="079fd-164">IniFile</span></span>](inifile-table.md)

[<span data-ttu-id="079fd-165">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="079fd-165">RemoveIniFile</span></span>](removeinifile-table.md)

[<span data-ttu-id="079fd-166">登錄</span><span class="sxs-lookup"><span data-stu-id="079fd-166">Registry</span></span>](registry-table.md)

[<span data-ttu-id="079fd-167">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="079fd-167">RemoveRegistry</span></span>](removeregistry-table.md)

[<span data-ttu-id="079fd-168">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="079fd-168">ServiceControl</span></span>](servicecontrol-table.md)

[<span data-ttu-id="079fd-169">ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="079fd-169">ServiceInstall</span></span>](serviceinstall-table.md)

[<span data-ttu-id="079fd-170">快速鍵</span><span class="sxs-lookup"><span data-stu-id="079fd-170">Shortcut</span></span>](shortcut-table.md)

[<span data-ttu-id="079fd-171">動詞</span><span class="sxs-lookup"><span data-stu-id="079fd-171">Verb</span></span>](verb-table.md)

[<span data-ttu-id="079fd-172">分機</span><span class="sxs-lookup"><span data-stu-id="079fd-172">Extension</span></span>](extension-table.md)

[<span data-ttu-id="079fd-173">類別</span><span class="sxs-lookup"><span data-stu-id="079fd-173">Class</span></span>](class-table.md)

[<span data-ttu-id="079fd-174">AppId</span><span class="sxs-lookup"><span data-stu-id="079fd-174">AppId</span></span>](appid-table.md)

[<span data-ttu-id="079fd-175">環境</span><span class="sxs-lookup"><span data-stu-id="079fd-175">Environment</span></span>](environment-table.md)

## <a name="related-topics"></a><span data-ttu-id="079fd-176">相關主題</span><span class="sxs-lookup"><span data-stu-id="079fd-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="079fd-177">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="079fd-177">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



