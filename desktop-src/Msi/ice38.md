---
description: ICE38 會驗證在目前使用者的設定檔下安裝的每個元件，也會在 \_ \_ 元件資料表的 KeyPath 資料行中的 [HKEY 目前的使用者根目錄] 下指定一個登錄機碼。
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d001d244160f939a73e697e677bf43a1f5f825f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027023"
---
# <a name="ice38"></a><span data-ttu-id="f668c-103">ICE38</span><span class="sxs-lookup"><span data-stu-id="f668c-103">ICE38</span></span>

<span data-ttu-id="f668c-104">ICE38 會驗證在目前使用者的設定檔下安裝的每個元件，也會在 [元件資料表](component-table.md)的 KeyPath 資料行中的 [ **HKEY \_ 目前的 \_ 使用者** 根目錄] 下指定一個登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="f668c-104">ICE38 validates that every component being installed under the current user's profile also specifies a registry key under the **HKEY\_CURRENT\_USER** root in the KeyPath column of the [Component table](component-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="f668c-105">結果</span><span class="sxs-lookup"><span data-stu-id="f668c-105">Result</span></span>

<span data-ttu-id="f668c-106">如果安裝在使用者設定檔之下的元件未指定 HKCU 登錄機碼，ICE38 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="f668c-106">ICE38 posts an error if a component installed under the user's profile does not specify a HKCU registry key.</span></span>

## <a name="example"></a><span data-ttu-id="f668c-107">範例</span><span class="sxs-lookup"><span data-stu-id="f668c-107">Example</span></span>

<span data-ttu-id="f668c-108">ICE38 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="f668c-108">ICE38 reports the following errors for the sample shown.</span></span>



| <span data-ttu-id="f668c-109">ICE38 錯誤</span><span class="sxs-lookup"><span data-stu-id="f668c-109">ICE38 error</span></span>                                                                                                                         | <span data-ttu-id="f668c-110">Description</span><span class="sxs-lookup"><span data-stu-id="f668c-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f668c-111">元件 Component1 會安裝到使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="f668c-111">Component Component1 installs to user profile.</span></span> <span data-ttu-id="f668c-112">它必須使用 HKCU 下的登錄機碼作為其 KeyPath，而不是檔案。</span><span class="sxs-lookup"><span data-stu-id="f668c-112">It must use a registry key under HKCU as its KeyPath, not a file.</span></span>                    | <span data-ttu-id="f668c-113">Component1 的 attributes 資料行值為0，表示元件必須使用檔案作為其 KeyPath。</span><span class="sxs-lookup"><span data-stu-id="f668c-113">The value of the attributes column of Component1 is 0, meaning that the component must use a file as its KeyPath.</span></span> <span data-ttu-id="f668c-114">當多位使用者在同一部電腦上安裝元件時，這會造成困難。</span><span class="sxs-lookup"><span data-stu-id="f668c-114">This causes difficulties when multiple users install the component on the same computer.</span></span> <span data-ttu-id="f668c-115">若要在 Component1 上修正這個錯誤，請在 [元件資料表](component-table.md) 的 [屬性] 資料行中設定 RegistryKeyPath 位，然後將 [KeyPath] 資料行中的專案變更為登錄 [資料表](registry-table.md)的登錄資料行中所列的值。</span><span class="sxs-lookup"><span data-stu-id="f668c-115">To fix this error on Component1, set the RegistryKeyPath bit in the Attributes column of the [Component table](component-table.md) and change the entry in the KeyPath column to a value listed in the Registry column of the [Registry table](registry-table.md).</span></span><br/>                                                                                |
| <span data-ttu-id="f668c-116">元件 Component2 會安裝到使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="f668c-116">Component Component2 installs to user profile.</span></span> <span data-ttu-id="f668c-117">它必須使用 HKCU 下的登錄機碼作為其 KeyPath。</span><span class="sxs-lookup"><span data-stu-id="f668c-117">It must use a registry key under HKCU as its KeyPath.</span></span> <span data-ttu-id="f668c-118">KeyPath 目前為 Null。</span><span class="sxs-lookup"><span data-stu-id="f668c-118">The KeyPath is currently NULL.</span></span> | <span data-ttu-id="f668c-119">Component2 已在 [元件資料表](component-table.md)的 [屬性] 資料行中設定 RegistryKeyPath 位。</span><span class="sxs-lookup"><span data-stu-id="f668c-119">Component2 has the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="f668c-120">因此，KeyPath 欄位必須包含登錄 [資料表](registry-table.md) 登錄資料行的索引鍵，但 KeyPath 資料行則為 Null。</span><span class="sxs-lookup"><span data-stu-id="f668c-120">The KeyPath field must therefore contain a key to the Registry column of the [Registry Table](registry-table.md) but the KeyPath column is Null.</span></span> <span data-ttu-id="f668c-121">若要修正這個錯誤，請將 KeyPath 值變更為登錄資料表中的有效專案。</span><span class="sxs-lookup"><span data-stu-id="f668c-121">To fix this error, change the KeyPath value to a valid entry into the Registry table.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="f668c-122">元件 Component3 會安裝到使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="f668c-122">Component Component3 installs to user profile.</span></span> <span data-ttu-id="f668c-123">它的 KeyPath 登錄機碼必須落在 HKCU 下。</span><span class="sxs-lookup"><span data-stu-id="f668c-123">It's KeyPath registry key must fall under HKCU.</span></span>                                      | <span data-ttu-id="f668c-124">Component3 在 [元件資料表](component-table.md) 的 [屬性] 資料行中設定 RegistryKeyPath 位，但登錄表的根資料行中所指定之登錄專案的根目錄指定 **了 \_ HKEY \_ 本機電腦** ，而不是 **HKEY 目前的 \_ \_ 使用者**。</span><span class="sxs-lookup"><span data-stu-id="f668c-124">Component3 has the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md) but the root of the registry entry specified in the Root column of the Registry table specifies **HKEY\_LOCAL\_MACHINE** rather than **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="f668c-125">若要修正這個錯誤，請使用 **HKEY \_ 本機 \_ 電腦** 下的有效登錄專案作為此元件的 KeyPath，或將登錄 [資料表](registry-table.md) 之根資料行中的值變更為-1 或1。</span><span class="sxs-lookup"><span data-stu-id="f668c-125">To fix this error, use a valid registry entry under **HKEY\_LOCAL\_MACHINE** as the KeyPath for this component or change the value in the Root column of the [Registry table](registry-table.md) to -1 or 1.</span></span><br/>                                                                  |
| <span data-ttu-id="f668c-126">元件 Component4 的 KeyPath 登錄專案不存在。</span><span class="sxs-lookup"><span data-stu-id="f668c-126">The KeyPath registry entry for component Component4 does not exist.</span></span>                                                                 | <span data-ttu-id="f668c-127">Component4 在 [Component 資料表](component-table.md) 的 Attributes 資料行中設定 RegistryKeyPath 位，但 KeyPath 資料行中的專案不存在於登錄 [資料表](registry-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="f668c-127">Component4 has the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md) but the entry in the KeyPath column does not exist in the [Registry Table](registry-table.md).</span></span> <span data-ttu-id="f668c-128">若要修正這個錯誤，請將 Reg4 的專案加入至 **HKEY \_ 目前 \_ 使用者** 底下的登錄資料表。</span><span class="sxs-lookup"><span data-stu-id="f668c-128">To fix this error, add an entry for Reg4 to the Registry table that is a under **HKEY\_CURRENT\_USER**.</span></span><br/>                                                                                                                                                                                                                                      |
| <span data-ttu-id="f668c-129">登錄專案 Reg5 設定為元件 Component5 的 KeyPath，但該登錄專案不屬於 Component5。</span><span class="sxs-lookup"><span data-stu-id="f668c-129">The Registry Entry Reg5 is set as the KeyPath for component Component5, but that registry entry does not belong to Component5.</span></span>      | <span data-ttu-id="f668c-130">在元件的 KeyPath 資料行中所參考的登錄專案是在 HKCU 樹狀目錄下找到，但登錄專案的 [元件] 資料 \_ 行不會回頭參考列為 KeyPath 的相同元件。</span><span class="sxs-lookup"><span data-stu-id="f668c-130">The Registry entry referenced in the KeyPath column of the component was found and lies under the HKCU tree, but the registry entry's Component\_ column does not refer back to the same component that listed it as the KeyPath.</span></span> <span data-ttu-id="f668c-131">這表示只會在安裝其他元件時，才會建立用來作為元件 KeyPath 的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="f668c-131">This means that the registry entry used as the KeyPath of the component would only be created when some other component was installed.</span></span> <span data-ttu-id="f668c-132">若要修正這個錯誤，請將 KeyPath 值變更為參考屬於元件的登錄專案，或是將登錄專案變更為屬於 KeyPath 的元件。</span><span class="sxs-lookup"><span data-stu-id="f668c-132">To fix this error change the KeyPath value to refer to a registry entry that belongs to the component, or change the registry entry to belong to the component using it as a KeyPath.</span></span><br/> |



 

<span data-ttu-id="f668c-133">[目錄資料表](directory-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="f668c-133">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="f668c-134">目錄</span><span class="sxs-lookup"><span data-stu-id="f668c-134">Directory</span></span> | <span data-ttu-id="f668c-135">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="f668c-135">Directory\_Parent</span></span> | <span data-ttu-id="f668c-136">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="f668c-136">DefaultDir</span></span>      |
|-----------|-------------------|-----------------|
| <span data-ttu-id="f668c-137">Dir1</span><span class="sxs-lookup"><span data-stu-id="f668c-137">Dir1</span></span>      |                   | <span data-ttu-id="f668c-138">StartMenuFolder</span><span class="sxs-lookup"><span data-stu-id="f668c-138">StartMenuFolder</span></span> |
| <span data-ttu-id="f668c-139">Dir2</span><span class="sxs-lookup"><span data-stu-id="f668c-139">Dir2</span></span>      |                   | <span data-ttu-id="f668c-140">DesktopFolder</span><span class="sxs-lookup"><span data-stu-id="f668c-140">DesktopFolder</span></span>   |
| <span data-ttu-id="f668c-141">Dir3</span><span class="sxs-lookup"><span data-stu-id="f668c-141">Dir3</span></span>      | <span data-ttu-id="f668c-142">Dir3</span><span class="sxs-lookup"><span data-stu-id="f668c-142">Dir3</span></span>              | <span data-ttu-id="f668c-143">AppData</span><span class="sxs-lookup"><span data-stu-id="f668c-143">AppData</span></span>         |
| <span data-ttu-id="f668c-144">Dir4</span><span class="sxs-lookup"><span data-stu-id="f668c-144">Dir4</span></span>      | <span data-ttu-id="f668c-145">Dir3</span><span class="sxs-lookup"><span data-stu-id="f668c-145">Dir3</span></span>              | <span data-ttu-id="f668c-146">SubDir</span><span class="sxs-lookup"><span data-stu-id="f668c-146">SubDir</span></span>          |



 

<span data-ttu-id="f668c-147">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="f668c-147">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="f668c-148">元件</span><span class="sxs-lookup"><span data-stu-id="f668c-148">Component</span></span>  | <span data-ttu-id="f668c-149">目錄\_</span><span class="sxs-lookup"><span data-stu-id="f668c-149">Directory\_</span></span> | <span data-ttu-id="f668c-150">屬性</span><span class="sxs-lookup"><span data-stu-id="f668c-150">Attributes</span></span> | <span data-ttu-id="f668c-151">KeyPath</span><span class="sxs-lookup"><span data-stu-id="f668c-151">KeyPath</span></span> |
|------------|-------------|------------|---------|
| <span data-ttu-id="f668c-152">Component1</span><span class="sxs-lookup"><span data-stu-id="f668c-152">Component1</span></span> | <span data-ttu-id="f668c-153">Dir1</span><span class="sxs-lookup"><span data-stu-id="f668c-153">Dir1</span></span>        | <span data-ttu-id="f668c-154">0</span><span class="sxs-lookup"><span data-stu-id="f668c-154">0</span></span>          | <span data-ttu-id="f668c-155">File1</span><span class="sxs-lookup"><span data-stu-id="f668c-155">File1</span></span>   |
| <span data-ttu-id="f668c-156">Component2</span><span class="sxs-lookup"><span data-stu-id="f668c-156">Component2</span></span> | <span data-ttu-id="f668c-157">Dir2</span><span class="sxs-lookup"><span data-stu-id="f668c-157">Dir2</span></span>        | <span data-ttu-id="f668c-158">4</span><span class="sxs-lookup"><span data-stu-id="f668c-158">4</span></span>          |         |
| <span data-ttu-id="f668c-159">Component3</span><span class="sxs-lookup"><span data-stu-id="f668c-159">Component3</span></span> | <span data-ttu-id="f668c-160">Dir3</span><span class="sxs-lookup"><span data-stu-id="f668c-160">Dir3</span></span>        | <span data-ttu-id="f668c-161">4</span><span class="sxs-lookup"><span data-stu-id="f668c-161">4</span></span>          | <span data-ttu-id="f668c-162">Reg3</span><span class="sxs-lookup"><span data-stu-id="f668c-162">Reg3</span></span>    |
| <span data-ttu-id="f668c-163">Component4</span><span class="sxs-lookup"><span data-stu-id="f668c-163">Component4</span></span> | <span data-ttu-id="f668c-164">Dir4</span><span class="sxs-lookup"><span data-stu-id="f668c-164">Dir4</span></span>        | <span data-ttu-id="f668c-165">4</span><span class="sxs-lookup"><span data-stu-id="f668c-165">4</span></span>          | <span data-ttu-id="f668c-166">Reg4</span><span class="sxs-lookup"><span data-stu-id="f668c-166">Reg4</span></span>    |
| <span data-ttu-id="f668c-167">Component5</span><span class="sxs-lookup"><span data-stu-id="f668c-167">Component5</span></span> | <span data-ttu-id="f668c-168">Dir5</span><span class="sxs-lookup"><span data-stu-id="f668c-168">Dir5</span></span>        | <span data-ttu-id="f668c-169">4</span><span class="sxs-lookup"><span data-stu-id="f668c-169">4</span></span>          | <span data-ttu-id="f668c-170">Reg5</span><span class="sxs-lookup"><span data-stu-id="f668c-170">Reg5</span></span>    |



 

<span data-ttu-id="f668c-171">登錄[表](registry-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="f668c-171">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="f668c-172">登錄</span><span class="sxs-lookup"><span data-stu-id="f668c-172">Registry</span></span> | <span data-ttu-id="f668c-173">Root</span><span class="sxs-lookup"><span data-stu-id="f668c-173">Root</span></span> | <span data-ttu-id="f668c-174">值</span><span class="sxs-lookup"><span data-stu-id="f668c-174">Value</span></span> | <span data-ttu-id="f668c-175">元件\_</span><span class="sxs-lookup"><span data-stu-id="f668c-175">Component\_</span></span> |
|----------|------|-------|-------------|
| <span data-ttu-id="f668c-176">Reg3</span><span class="sxs-lookup"><span data-stu-id="f668c-176">Reg3</span></span>     | <span data-ttu-id="f668c-177">2</span><span class="sxs-lookup"><span data-stu-id="f668c-177">2</span></span>    |       | <span data-ttu-id="f668c-178">Component3</span><span class="sxs-lookup"><span data-stu-id="f668c-178">Component3</span></span>  |
| <span data-ttu-id="f668c-179">Reg5</span><span class="sxs-lookup"><span data-stu-id="f668c-179">Reg5</span></span>     | <span data-ttu-id="f668c-180">0</span><span class="sxs-lookup"><span data-stu-id="f668c-180">0</span></span>    |       | <span data-ttu-id="f668c-181">Component4</span><span class="sxs-lookup"><span data-stu-id="f668c-181">Component4</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="f668c-182">相關主題</span><span class="sxs-lookup"><span data-stu-id="f668c-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f668c-183">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="f668c-183">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




