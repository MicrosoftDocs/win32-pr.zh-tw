---
description: 快速鍵表格會保存應用程式在使用者電腦上建立快捷方式所需的資訊。
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: 快速鍵資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56482f1d2d5521bede54c781c91d2de2bc39e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850167"
---
# <a name="shortcut-table"></a><span data-ttu-id="fe966-103">快速鍵資料表</span><span class="sxs-lookup"><span data-stu-id="fe966-103">Shortcut Table</span></span>

<span data-ttu-id="fe966-104">快速鍵表格會保存應用程式在使用者電腦上建立快捷方式所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="fe966-104">The Shortcut table holds the information the application needs to create shortcuts on the user's computer.</span></span>

<span data-ttu-id="fe966-105">快速鍵資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="fe966-105">The Shortcut table has the following columns.</span></span>



| <span data-ttu-id="fe966-106">Column</span><span class="sxs-lookup"><span data-stu-id="fe966-106">Column</span></span>                 | <span data-ttu-id="fe966-107">類型</span><span class="sxs-lookup"><span data-stu-id="fe966-107">Type</span></span>                         | <span data-ttu-id="fe966-108">答案</span><span class="sxs-lookup"><span data-stu-id="fe966-108">Key</span></span> | <span data-ttu-id="fe966-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="fe966-109">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="fe966-110">快速鍵</span><span class="sxs-lookup"><span data-stu-id="fe966-110">Shortcut</span></span>               | [<span data-ttu-id="fe966-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="fe966-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="fe966-112">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-112">Y</span></span>   | <span data-ttu-id="fe966-113">N</span><span class="sxs-lookup"><span data-stu-id="fe966-113">N</span></span>        |
| <span data-ttu-id="fe966-114">目錄\_</span><span class="sxs-lookup"><span data-stu-id="fe966-114">Directory\_</span></span>            | [<span data-ttu-id="fe966-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="fe966-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="fe966-116">N</span><span class="sxs-lookup"><span data-stu-id="fe966-116">N</span></span>   | <span data-ttu-id="fe966-117">N</span><span class="sxs-lookup"><span data-stu-id="fe966-117">N</span></span>        |
| <span data-ttu-id="fe966-118">Name</span><span class="sxs-lookup"><span data-stu-id="fe966-118">Name</span></span>                   | [<span data-ttu-id="fe966-119">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="fe966-119">Filename</span></span>](filename.md)     | <span data-ttu-id="fe966-120">N</span><span class="sxs-lookup"><span data-stu-id="fe966-120">N</span></span>   | <span data-ttu-id="fe966-121">N</span><span class="sxs-lookup"><span data-stu-id="fe966-121">N</span></span>        |
| <span data-ttu-id="fe966-122">元件\_</span><span class="sxs-lookup"><span data-stu-id="fe966-122">Component\_</span></span>            | [<span data-ttu-id="fe966-123">識別碼</span><span class="sxs-lookup"><span data-stu-id="fe966-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="fe966-124">N</span><span class="sxs-lookup"><span data-stu-id="fe966-124">N</span></span>   | <span data-ttu-id="fe966-125">N</span><span class="sxs-lookup"><span data-stu-id="fe966-125">N</span></span>        |
| <span data-ttu-id="fe966-126">目標</span><span class="sxs-lookup"><span data-stu-id="fe966-126">Target</span></span>                 | [<span data-ttu-id="fe966-127">快速鍵</span><span class="sxs-lookup"><span data-stu-id="fe966-127">Shortcut</span></span>](shortcut.md)     | <span data-ttu-id="fe966-128">N</span><span class="sxs-lookup"><span data-stu-id="fe966-128">N</span></span>   | <span data-ttu-id="fe966-129">N</span><span class="sxs-lookup"><span data-stu-id="fe966-129">N</span></span>        |
| <span data-ttu-id="fe966-130">引數</span><span class="sxs-lookup"><span data-stu-id="fe966-130">Arguments</span></span>              | [<span data-ttu-id="fe966-131">格式 化</span><span class="sxs-lookup"><span data-stu-id="fe966-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="fe966-132">N</span><span class="sxs-lookup"><span data-stu-id="fe966-132">N</span></span>   | <span data-ttu-id="fe966-133">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-133">Y</span></span>        |
| <span data-ttu-id="fe966-134">Description</span><span class="sxs-lookup"><span data-stu-id="fe966-134">Description</span></span>            | [<span data-ttu-id="fe966-135">Text</span><span class="sxs-lookup"><span data-stu-id="fe966-135">Text</span></span>](text.md)             | <span data-ttu-id="fe966-136">N</span><span class="sxs-lookup"><span data-stu-id="fe966-136">N</span></span>   | <span data-ttu-id="fe966-137">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-137">Y</span></span>        |
| <span data-ttu-id="fe966-138">熱鍵</span><span class="sxs-lookup"><span data-stu-id="fe966-138">Hotkey</span></span>                 | [<span data-ttu-id="fe966-139">整數</span><span class="sxs-lookup"><span data-stu-id="fe966-139">Integer</span></span>](integer.md)       | <span data-ttu-id="fe966-140">N</span><span class="sxs-lookup"><span data-stu-id="fe966-140">N</span></span>   | <span data-ttu-id="fe966-141">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-141">Y</span></span>        |
| <span data-ttu-id="fe966-142">圖示\_</span><span class="sxs-lookup"><span data-stu-id="fe966-142">Icon\_</span></span>                 | [<span data-ttu-id="fe966-143">識別碼</span><span class="sxs-lookup"><span data-stu-id="fe966-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="fe966-144">N</span><span class="sxs-lookup"><span data-stu-id="fe966-144">N</span></span>   | <span data-ttu-id="fe966-145">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-145">Y</span></span>        |
| <span data-ttu-id="fe966-146">>iconindex</span><span class="sxs-lookup"><span data-stu-id="fe966-146">IconIndex</span></span>              | [<span data-ttu-id="fe966-147">整數</span><span class="sxs-lookup"><span data-stu-id="fe966-147">Integer</span></span>](integer.md)       | <span data-ttu-id="fe966-148">N</span><span class="sxs-lookup"><span data-stu-id="fe966-148">N</span></span>   | <span data-ttu-id="fe966-149">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-149">Y</span></span>        |
| <span data-ttu-id="fe966-150">ShowCmd</span><span class="sxs-lookup"><span data-stu-id="fe966-150">ShowCmd</span></span>                | [<span data-ttu-id="fe966-151">整數</span><span class="sxs-lookup"><span data-stu-id="fe966-151">Integer</span></span>](integer.md)       | <span data-ttu-id="fe966-152">N</span><span class="sxs-lookup"><span data-stu-id="fe966-152">N</span></span>   | <span data-ttu-id="fe966-153">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-153">Y</span></span>        |
| <span data-ttu-id="fe966-154">WkDir</span><span class="sxs-lookup"><span data-stu-id="fe966-154">WkDir</span></span>                  | [<span data-ttu-id="fe966-155">識別碼</span><span class="sxs-lookup"><span data-stu-id="fe966-155">Identifier</span></span>](identifier.md) | <span data-ttu-id="fe966-156">N</span><span class="sxs-lookup"><span data-stu-id="fe966-156">N</span></span>   | <span data-ttu-id="fe966-157">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-157">Y</span></span>        |
| <span data-ttu-id="fe966-158">DisplayResourceDLL</span><span class="sxs-lookup"><span data-stu-id="fe966-158">DisplayResourceDLL</span></span>     | [<span data-ttu-id="fe966-159">格式 化</span><span class="sxs-lookup"><span data-stu-id="fe966-159">Formatted</span></span>](formatted.md)   | <span data-ttu-id="fe966-160">N</span><span class="sxs-lookup"><span data-stu-id="fe966-160">N</span></span>   | <span data-ttu-id="fe966-161">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-161">Y</span></span>        |
| <span data-ttu-id="fe966-162">DisplayResourceId</span><span class="sxs-lookup"><span data-stu-id="fe966-162">DisplayResourceId</span></span>      | [<span data-ttu-id="fe966-163">整數</span><span class="sxs-lookup"><span data-stu-id="fe966-163">Integer</span></span>](integer.md)       | <span data-ttu-id="fe966-164">N</span><span class="sxs-lookup"><span data-stu-id="fe966-164">N</span></span>   | <span data-ttu-id="fe966-165">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-165">Y</span></span>        |
| <span data-ttu-id="fe966-166">DescriptionResourceDLL</span><span class="sxs-lookup"><span data-stu-id="fe966-166">DescriptionResourceDLL</span></span> | [<span data-ttu-id="fe966-167">格式 化</span><span class="sxs-lookup"><span data-stu-id="fe966-167">Formatted</span></span>](formatted.md)   | <span data-ttu-id="fe966-168">N</span><span class="sxs-lookup"><span data-stu-id="fe966-168">N</span></span>   | <span data-ttu-id="fe966-169">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-169">Y</span></span>        |
| <span data-ttu-id="fe966-170">DescriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="fe966-170">DescriptionResourceId</span></span>  | [<span data-ttu-id="fe966-171">整數</span><span class="sxs-lookup"><span data-stu-id="fe966-171">Integer</span></span>](integer.md)       | <span data-ttu-id="fe966-172">N</span><span class="sxs-lookup"><span data-stu-id="fe966-172">N</span></span>   | <span data-ttu-id="fe966-173">Y</span><span class="sxs-lookup"><span data-stu-id="fe966-173">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fe966-174">資料行</span><span class="sxs-lookup"><span data-stu-id="fe966-174">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fe966-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>快捷方式</span><span class="sxs-lookup"><span data-stu-id="fe966-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Shortcut</span></span>
</dt> <dd>

<span data-ttu-id="fe966-176">此資料表的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="fe966-176">The key value for this table.</span></span>

</dd> <dt>

<span data-ttu-id="fe966-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>目錄\_</span><span class="sxs-lookup"><span data-stu-id="fe966-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="fe966-178">[目錄資料表](directory-table.md)第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fe966-178">The external key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="fe966-179">此資料行指定建立快捷方式檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="fe966-179">This column specifies the directory in which the Shortcut file is created.</span></span>

</dd> <dt>

<span data-ttu-id="fe966-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="fe966-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="fe966-181">要建立之快捷方式的可當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="fe966-181">The localizable name of the shortcut to be created.</span></span>

</dd> <dt>

<span data-ttu-id="fe966-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="fe966-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="fe966-183">在 [元件資料表](component-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fe966-183">The external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="fe966-184">安裝程式會使用此資料行中所指定之元件的安裝狀態，來判斷是否已建立或刪除快捷方式。</span><span class="sxs-lookup"><span data-stu-id="fe966-184">The installer uses the installation state of the component specified in this column to determine whether the shortcut is created or deleted.</span></span> <span data-ttu-id="fe966-185">此元件必須有有效的金鑰路徑，才能安裝快捷方式。</span><span class="sxs-lookup"><span data-stu-id="fe966-185">This component must have a valid key path for the shortcut to be installed.</span></span> <span data-ttu-id="fe966-186">如果目標資料行包含功能的名稱，快捷方式所啟動的檔案就是此資料行中所列元件的金鑰檔。</span><span class="sxs-lookup"><span data-stu-id="fe966-186">If the Target column contains the name of a feature, the file launched by the shortcut is the key file of the component listed in this column.</span></span>

</dd> <dt>

<span data-ttu-id="fe966-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>目標</span><span class="sxs-lookup"><span data-stu-id="fe966-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="fe966-188">快捷方式目標。</span><span class="sxs-lookup"><span data-stu-id="fe966-188">The shortcut target.</span></span>

<span data-ttu-id="fe966-189">若為已公告的快捷方式，這個資料行必須是 [功能資料表](feature-table.md)第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fe966-189">For an advertised shortcut, this column must be an external key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="fe966-190">安裝程式會評估目標欄位中的專案做為 [識別碼](identifier.md) ，而專案必須是 [功能資料表](feature-table.md)中的有效外鍵。</span><span class="sxs-lookup"><span data-stu-id="fe966-190">The installer evaluates the entry in the Target field as an [Identifier](identifier.md) and the entry must be a valid foreign key into the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="fe966-191">在此情況下，快捷方式所啟動的檔案是元件資料行中所列元件的金鑰檔 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fe966-191">The file launched by the shortcut in this case is the key file of the component listed in the Component\_ column.</span></span> <span data-ttu-id="fe966-192">當快捷方式啟用時，安裝程式會先確認功能中的所有元件都已安裝，然後再啟動此檔案。</span><span class="sxs-lookup"><span data-stu-id="fe966-192">When the shortcut is activated, the installer verifies that all the components in the feature are installed before launching this file.</span></span>

<span data-ttu-id="fe966-193">若為非公告的快捷方式，安裝程式會將此欄位評估為 [格式化](formatted.md) 字串。</span><span class="sxs-lookup"><span data-stu-id="fe966-193">For a non-advertised shortcut, the installer evaluates this field as a [Formatted](formatted.md) string.</span></span> <span data-ttu-id="fe966-194">欄位應包含以方括弧括住的屬性識別碼 (\[ \]) ），該識別碼會展開至檔案或快捷方式指向的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="fe966-194">The field should contains a property identifier enclosed by square brackets (\[ \]), that is expanded into the file or a folder pointed to by the shortcut.</span></span> <span data-ttu-id="fe966-195">如需詳細資訊，請參閱 [CreateShortcuts 動作](createshortcuts-action.md)。</span><span class="sxs-lookup"><span data-stu-id="fe966-195">For more information, see the [CreateShortcuts action](createshortcuts-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe966-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>參數</span><span class="sxs-lookup"><span data-stu-id="fe966-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="fe966-197">快速鍵的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="fe966-197">The command-line arguments for the shortcut.</span></span>

<span data-ttu-id="fe966-198">請注意，[引數] 欄位中的屬性解析有限。</span><span class="sxs-lookup"><span data-stu-id="fe966-198">Note that the resolution of properties in the Arguments field is limited.</span></span> <span data-ttu-id="fe966-199">\[  \] 只有在已安裝擁有快捷方式的元件時，如果屬性已經有預期的值，則只能解析此欄位中格式化為屬性的屬性。</span><span class="sxs-lookup"><span data-stu-id="fe966-199">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component that owns the shortcut is installed.</span></span> <span data-ttu-id="fe966-200">例如，若要解析為引數 "MyDoc.doc" 的正確值 \[ \# \] ，相同的進程必須安裝檔案 MyDoc.doc 和擁有快捷方式的元件。</span><span class="sxs-lookup"><span data-stu-id="fe966-200">For example, to resolve to the correct value for the argument "\[\#MyDoc.doc\]", the same process must be installing the file MyDoc.doc and the component that owns the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="fe966-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="fe966-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="fe966-202">快速鍵的可當地語系化描述。</span><span class="sxs-lookup"><span data-stu-id="fe966-202">The localizable description of the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="fe966-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>熱鍵</span><span class="sxs-lookup"><span data-stu-id="fe966-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey</span></span>
</dt> <dd>

<span data-ttu-id="fe966-204">快速鍵的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="fe966-204">The hotkey for the shortcut.</span></span> <span data-ttu-id="fe966-205">低序位位元組包含金鑰的虛擬金鑰程式碼，而高序位位元組包含修飾詞旗標。</span><span class="sxs-lookup"><span data-stu-id="fe966-205">The low-order byte contains the virtual-key code for the key, and the high-order byte contains modifier flags.</span></span> <span data-ttu-id="fe966-206">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="fe966-206">This must be a non-negative number.</span></span> <span data-ttu-id="fe966-207">通常建議不要設定此選項，因為此選項的設定可將重複的快速鍵新增至使用者的桌面。</span><span class="sxs-lookup"><span data-stu-id="fe966-207">Authors of installation packages are generally recommended not to set this option, because the setting of this option can add duplicate hotkeys to a user's desktop.</span></span> <span data-ttu-id="fe966-208">此外，將快速鍵指派給快速鍵的做法，對於使用快速鍵來 [存取協助工具](accessibility.md)的使用者來說可能會有問題。</span><span class="sxs-lookup"><span data-stu-id="fe966-208">In addition, the practice of assigning hotkeys to shortcuts can be problematic for users using hotkeys for [accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe966-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>圖示\_</span><span class="sxs-lookup"><span data-stu-id="fe966-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="fe966-210">[圖示資料表](icon-table.md)的第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fe966-210">The external key to column one of the [Icon table](icon-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe966-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>>iconindex</span><span class="sxs-lookup"><span data-stu-id="fe966-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="fe966-212">快速鍵的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="fe966-212">The icon index for the shortcut.</span></span> <span data-ttu-id="fe966-213">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="fe966-213">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="fe966-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span><span class="sxs-lookup"><span data-stu-id="fe966-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span></span>
</dt> <dd>

<span data-ttu-id="fe966-215">應用程式視窗的 [顯示] 命令。</span><span class="sxs-lookup"><span data-stu-id="fe966-215">The Show command for the application window.</span></span>

<span data-ttu-id="fe966-216">您可以使用下列值。</span><span class="sxs-lookup"><span data-stu-id="fe966-216">The following values may be used.</span></span> <span data-ttu-id="fe966-217">這些值會如 Windows API 函數 ShowWindow 所定義。</span><span class="sxs-lookup"><span data-stu-id="fe966-217">The values are as defined for the Windows API function ShowWindow.</span></span>



| <span data-ttu-id="fe966-218">值</span><span class="sxs-lookup"><span data-stu-id="fe966-218">Value</span></span> | <span data-ttu-id="fe966-219">意義</span><span class="sxs-lookup"><span data-stu-id="fe966-219">Meaning</span></span>             |
|-------|---------------------|
| <span data-ttu-id="fe966-220">1</span><span class="sxs-lookup"><span data-stu-id="fe966-220">1</span></span>     | <span data-ttu-id="fe966-221">SW \_ SHOWNORMAL</span><span class="sxs-lookup"><span data-stu-id="fe966-221">SW\_SHOWNORMAL</span></span>      |
| <span data-ttu-id="fe966-222">3</span><span class="sxs-lookup"><span data-stu-id="fe966-222">3</span></span>     | <span data-ttu-id="fe966-223">SW \_ SHOWMAXIMIZED</span><span class="sxs-lookup"><span data-stu-id="fe966-223">SW\_SHOWMAXIMIZED</span></span>   |
| <span data-ttu-id="fe966-224">7</span><span class="sxs-lookup"><span data-stu-id="fe966-224">7</span></span>     | <span data-ttu-id="fe966-225">SW \_ SHOWMINNOACTIVE</span><span class="sxs-lookup"><span data-stu-id="fe966-225">SW\_SHOWMINNOACTIVE</span></span> |



 

</dd> <dt>

<span data-ttu-id="fe966-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir</span><span class="sxs-lookup"><span data-stu-id="fe966-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir</span></span>
</dt> <dd>

<span data-ttu-id="fe966-227">屬性的名稱，該屬性具有快捷方式的工作目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="fe966-227">The name of the property that has the path of the working directory for the shortcut.</span></span> <span data-ttu-id="fe966-228">此值可以使用 Windows 格式參考環境變數，例如% USERPROFILE%。</span><span class="sxs-lookup"><span data-stu-id="fe966-228">The value can use the Windows format to reference environment variables, for example %USERPROFILE%.</span></span> <span data-ttu-id="fe966-229">當安裝程式解析工作目錄以建立快捷方式時，參考會解析為實際的路徑。</span><span class="sxs-lookup"><span data-stu-id="fe966-229">The references are resolved to an actual path when the installer resolves the working directory to create the shortcut.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="fe966-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL</span><span class="sxs-lookup"><span data-stu-id="fe966-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="fe966-231">此欄位包含 [格式化](formatted.md) 的字串值，適用于非語言相關可攜性可執行檔的完整路徑 (LN 檔案) ，其中包含資源設定 (RC Config) 資料。</span><span class="sxs-lookup"><span data-stu-id="fe966-231">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="fe966-232">格式化的字串可以使用 \[ \# filekey \] 慣例。</span><span class="sxs-lookup"><span data-stu-id="fe966-232">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="fe966-233">如果此欄位包含值，則會忽略 [名稱] 資料行。</span><span class="sxs-lookup"><span data-stu-id="fe966-233">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="fe966-234">如果這個欄位是空的，安裝程式會使用 [名稱] 資料行中的值。</span><span class="sxs-lookup"><span data-stu-id="fe966-234">If this field is empty, the installer uses the value in the Name column.</span></span> <span data-ttu-id="fe966-235">當此欄位包含一個值時， **DisplayResourceId** 欄位也必須包含值，否則安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="fe966-235">When this field contains a value, the **DisplayResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="fe966-236">只有在 Windows Vista 或 Windows Server 2008 上執行時，才會使用這個快速鍵表格的資料行，否則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="fe966-236">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="fe966-237">此資料行適用于 Windows Installer 4.0 之前的版本。</span><span class="sxs-lookup"><span data-stu-id="fe966-237">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="fe966-238">如需有關如何新增快捷方式資料表的快捷方式以搭配 MUI 資源使用的詳細資訊，請參閱 [Mui 快捷方式範例](a-mui-shortcut-example.md)。</span><span class="sxs-lookup"><span data-stu-id="fe966-238">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe966-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId</span><span class="sxs-lookup"><span data-stu-id="fe966-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId</span></span>
</dt> <dd>

<span data-ttu-id="fe966-240">快速鍵的顯示名稱索引。</span><span class="sxs-lookup"><span data-stu-id="fe966-240">The display name index for the shortcut.</span></span> <span data-ttu-id="fe966-241">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="fe966-241">This must be a non-negative number.</span></span> <span data-ttu-id="fe966-242">當此欄位包含一個值時， **DisplayResourceDLL** 欄位也必須包含值，否則安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="fe966-242">When this field contains a value, the **DisplayResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="fe966-243">只有在 Windows Vista 或 Windows Server 2008 上執行時，才會使用這個快速鍵表格的資料行，否則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="fe966-243">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="fe966-244">此資料行適用于 Windows Installer 4.0 之前的版本。</span><span class="sxs-lookup"><span data-stu-id="fe966-244">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> <dt>

<span data-ttu-id="fe966-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL</span><span class="sxs-lookup"><span data-stu-id="fe966-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="fe966-246">此欄位包含 [格式化](formatted.md) 的字串值，適用于非語言相關可攜性可執行檔的完整路徑 (LN 檔案) ，其中包含資源設定 (RC Config) 資料。</span><span class="sxs-lookup"><span data-stu-id="fe966-246">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="fe966-247">格式化的字串可以使用 \[ \# filekey \] 慣例。</span><span class="sxs-lookup"><span data-stu-id="fe966-247">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="fe966-248">如果此欄位包含值，則會忽略 [名稱] 資料行。</span><span class="sxs-lookup"><span data-stu-id="fe966-248">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="fe966-249">如果這個欄位是空的，安裝程式會使用 [描述] 欄中的值。</span><span class="sxs-lookup"><span data-stu-id="fe966-249">If this field is empty, the installer uses the value in the Description column.</span></span> <span data-ttu-id="fe966-250">當此欄位包含一個值時， **DescriptionResourceId** 欄位也必須包含值，否則安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="fe966-250">When this field contains a value, the **DescriptionResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="fe966-251">只有在 Windows Vista 或 Windows Server 2008 上執行時，才會使用這個快速鍵表格的資料行，否則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="fe966-251">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="fe966-252">此資料行適用于 Windows Installer 4.0 之前的版本。</span><span class="sxs-lookup"><span data-stu-id="fe966-252">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="fe966-253">如需有關如何新增快捷方式資料表的快捷方式以搭配 MUI 資源使用的詳細資訊，請參閱 [Mui 快捷方式範例](a-mui-shortcut-example.md)。</span><span class="sxs-lookup"><span data-stu-id="fe966-253">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe966-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="fe966-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId</span></span>
</dt> <dd>

<span data-ttu-id="fe966-255">快速鍵的描述名稱索引。</span><span class="sxs-lookup"><span data-stu-id="fe966-255">The description name index for the shortcut.</span></span> <span data-ttu-id="fe966-256">此值必須是非負數。</span><span class="sxs-lookup"><span data-stu-id="fe966-256">This must be a non-negative number.</span></span> <span data-ttu-id="fe966-257">當此欄位包含一個值時， **DescriptionResourceDLL** 欄位也必須包含值，否則安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="fe966-257">When this field contains a value, the **DescriptionResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="fe966-258">只有在 Windows Vista 或 Windows Server 2008 上執行時，才會使用這個快速鍵表格的資料行，否則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="fe966-258">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="fe966-259">此資料行適用于 Windows Installer 4.0 之前的版本。</span><span class="sxs-lookup"><span data-stu-id="fe966-259">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe966-260">備註</span><span class="sxs-lookup"><span data-stu-id="fe966-260">Remarks</span></span>

<span data-ttu-id="fe966-261">只有在系統的 IShellLink 介面支援安裝程式描述項解析時，啟用功能才會建立公告的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="fe966-261">The enabling of a feature creates an advertised shortcut only if the system's IShellLink interface supports installer descriptor resolution.</span></span> <span data-ttu-id="fe966-262">Microsoft Windows 2000 和執行 Microsoft Internet Explorer 4.01 的系統都支援此功能。</span><span class="sxs-lookup"><span data-stu-id="fe966-262">This is supported by Microsoft Windows 2000 and systems running Microsoft Internet Explorer 4.01.</span></span> <span data-ttu-id="fe966-263">如果不支援，安裝程式會在安裝功能元件時，在本機或從來源執行，建立非公告的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="fe966-263">If unsupported, the installer creates a non-advertised shortcut upon the installation of the feature's component, either locally or run from source.</span></span>

<span data-ttu-id="fe966-264">請注意，公告的快捷方式一律指向特定的應用程式，由 [**ProductCode**](productcode.md)識別，且不應在應用程式之間共用。</span><span class="sxs-lookup"><span data-stu-id="fe966-264">Note that advertised shortcuts always point at a particular application, identified by a [**ProductCode**](productcode.md), and should not be shared between applications.</span></span> <span data-ttu-id="fe966-265">公告的快捷方式只適用于最近安裝的應用程式，而且會在移除應用程式時移除。</span><span class="sxs-lookup"><span data-stu-id="fe966-265">Advertised shortcuts only work for the most recently installed application, and are removed when that application is removed.</span></span>

<span data-ttu-id="fe966-266">當 [CreateShortcuts 動作](createshortcuts-action.md) 和 [RemoveShortcuts 動作](removeshortcuts-action.md) 執行時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="fe966-266">This table is referred to when the [CreateShortcuts action](createshortcuts-action.md) and the [RemoveShortcuts action](removeshortcuts-action.md) is executed.</span></span>

<span data-ttu-id="fe966-267">另請參閱 [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="fe966-267">See also the [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="fe966-268">驗證</span><span class="sxs-lookup"><span data-stu-id="fe966-268">Validation</span></span>

<dl>

[<span data-ttu-id="fe966-269">ICE03</span><span class="sxs-lookup"><span data-stu-id="fe966-269">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="fe966-270">ICE06</span><span class="sxs-lookup"><span data-stu-id="fe966-270">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="fe966-271">ICE19</span><span class="sxs-lookup"><span data-stu-id="fe966-271">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="fe966-272">ICE32</span><span class="sxs-lookup"><span data-stu-id="fe966-272">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="fe966-273">ICE36</span><span class="sxs-lookup"><span data-stu-id="fe966-273">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="fe966-274">ICE46</span><span class="sxs-lookup"><span data-stu-id="fe966-274">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="fe966-275">ICE50</span><span class="sxs-lookup"><span data-stu-id="fe966-275">ICE50</span></span>](ice50.md)  
[<span data-ttu-id="fe966-276">ICE57</span><span class="sxs-lookup"><span data-stu-id="fe966-276">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="fe966-277">ICE59</span><span class="sxs-lookup"><span data-stu-id="fe966-277">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="fe966-278">ICE67</span><span class="sxs-lookup"><span data-stu-id="fe966-278">ICE67</span></span>](ice67.md)  
[<span data-ttu-id="fe966-279">ICE69</span><span class="sxs-lookup"><span data-stu-id="fe966-279">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="fe966-280">ICE80</span><span class="sxs-lookup"><span data-stu-id="fe966-280">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="fe966-281">ICE90</span><span class="sxs-lookup"><span data-stu-id="fe966-281">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="fe966-282">ICE91</span><span class="sxs-lookup"><span data-stu-id="fe966-282">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="fe966-283">ICE94</span><span class="sxs-lookup"><span data-stu-id="fe966-283">ICE94</span></span>](ice94.md)  
</dl>

 

 



