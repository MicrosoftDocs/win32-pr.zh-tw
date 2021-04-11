---
description: 登錄資料表會保存應用程式必須在系統登錄中設定的登錄資訊。
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: 登錄資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944152"
---
# <a name="registry-table"></a><span data-ttu-id="ec6a2-103">登錄資料表</span><span class="sxs-lookup"><span data-stu-id="ec6a2-103">Registry Table</span></span>

<span data-ttu-id="ec6a2-104">登錄資料表會保存應用程式必須在系統登錄中設定的登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-104">The Registry table holds the registry information that the application needs to set in the system registry.</span></span>

<span data-ttu-id="ec6a2-105">登錄資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-105">The Registry table has the following columns.</span></span>



| <span data-ttu-id="ec6a2-106">Column</span><span class="sxs-lookup"><span data-stu-id="ec6a2-106">Column</span></span>      | <span data-ttu-id="ec6a2-107">類型</span><span class="sxs-lookup"><span data-stu-id="ec6a2-107">Type</span></span>                         | <span data-ttu-id="ec6a2-108">答案</span><span class="sxs-lookup"><span data-stu-id="ec6a2-108">Key</span></span> | <span data-ttu-id="ec6a2-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="ec6a2-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="ec6a2-110">登錄</span><span class="sxs-lookup"><span data-stu-id="ec6a2-110">Registry</span></span>    | [<span data-ttu-id="ec6a2-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="ec6a2-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="ec6a2-112">Y</span><span class="sxs-lookup"><span data-stu-id="ec6a2-112">Y</span></span>   | <span data-ttu-id="ec6a2-113">N</span><span class="sxs-lookup"><span data-stu-id="ec6a2-113">N</span></span>        |
| <span data-ttu-id="ec6a2-114">Root</span><span class="sxs-lookup"><span data-stu-id="ec6a2-114">Root</span></span>        | [<span data-ttu-id="ec6a2-115">整數</span><span class="sxs-lookup"><span data-stu-id="ec6a2-115">Integer</span></span>](integer.md)       | <span data-ttu-id="ec6a2-116">N</span><span class="sxs-lookup"><span data-stu-id="ec6a2-116">N</span></span>   | <span data-ttu-id="ec6a2-117">N</span><span class="sxs-lookup"><span data-stu-id="ec6a2-117">N</span></span>        |
| <span data-ttu-id="ec6a2-118">答案</span><span class="sxs-lookup"><span data-stu-id="ec6a2-118">Key</span></span>         | [<span data-ttu-id="ec6a2-119">RegPath</span><span class="sxs-lookup"><span data-stu-id="ec6a2-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="ec6a2-120">N</span><span class="sxs-lookup"><span data-stu-id="ec6a2-120">N</span></span>   | <span data-ttu-id="ec6a2-121">N</span><span class="sxs-lookup"><span data-stu-id="ec6a2-121">N</span></span>        |
| <span data-ttu-id="ec6a2-122">Name</span><span class="sxs-lookup"><span data-stu-id="ec6a2-122">Name</span></span>        | [<span data-ttu-id="ec6a2-123">格式 化</span><span class="sxs-lookup"><span data-stu-id="ec6a2-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="ec6a2-124">N</span><span class="sxs-lookup"><span data-stu-id="ec6a2-124">N</span></span>   | <span data-ttu-id="ec6a2-125">Y</span><span class="sxs-lookup"><span data-stu-id="ec6a2-125">Y</span></span>        |
| <span data-ttu-id="ec6a2-126">值</span><span class="sxs-lookup"><span data-stu-id="ec6a2-126">Value</span></span>       | [<span data-ttu-id="ec6a2-127">格式 化</span><span class="sxs-lookup"><span data-stu-id="ec6a2-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="ec6a2-128">N</span><span class="sxs-lookup"><span data-stu-id="ec6a2-128">N</span></span>   | <span data-ttu-id="ec6a2-129">Y</span><span class="sxs-lookup"><span data-stu-id="ec6a2-129">Y</span></span>        |
| <span data-ttu-id="ec6a2-130">元件\_</span><span class="sxs-lookup"><span data-stu-id="ec6a2-130">Component\_</span></span> | [<span data-ttu-id="ec6a2-131">識別碼</span><span class="sxs-lookup"><span data-stu-id="ec6a2-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="ec6a2-132">N</span><span class="sxs-lookup"><span data-stu-id="ec6a2-132">N</span></span>   | <span data-ttu-id="ec6a2-133">N</span><span class="sxs-lookup"><span data-stu-id="ec6a2-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ec6a2-134">資料行</span><span class="sxs-lookup"><span data-stu-id="ec6a2-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ec6a2-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>註冊 表</span><span class="sxs-lookup"><span data-stu-id="ec6a2-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registry</span></span>
</dt> <dd>

<span data-ttu-id="ec6a2-136">用來識別登錄記錄的主要金鑰。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-136">Primary key used to identify a registry record.</span></span>

</dd> <dt>

<span data-ttu-id="ec6a2-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>根</span><span class="sxs-lookup"><span data-stu-id="ec6a2-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="ec6a2-138">登錄值的預先定義根金鑰。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-138">The predefined root key for the registry value.</span></span> <span data-ttu-id="ec6a2-139">在此欄位中輸入-1 的值，可讓根金鑰與安裝類型相依。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-139">Enter a value of -1 in this field to make the root key dependent on the type of installation.</span></span> <span data-ttu-id="ec6a2-140">輸入下表中的其中一個值，以強制將登錄值寫入至特定根金鑰。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-140">Enter one of the other values in the following table to force the registry value to be written under a particular root key.</span></span>



| <span data-ttu-id="ec6a2-141">常數</span><span class="sxs-lookup"><span data-stu-id="ec6a2-141">Constant</span></span>                          | <span data-ttu-id="ec6a2-142">十六進位</span><span class="sxs-lookup"><span data-stu-id="ec6a2-142">Hexadecimal</span></span> | <span data-ttu-id="ec6a2-143">Decimal</span><span class="sxs-lookup"><span data-stu-id="ec6a2-143">Decimal</span></span> | <span data-ttu-id="ec6a2-144">根金鑰</span><span class="sxs-lookup"><span data-stu-id="ec6a2-144">Root key</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec6a2-145">(無)</span><span class="sxs-lookup"><span data-stu-id="ec6a2-145">(none)</span></span>                            | <span data-ttu-id="ec6a2-146">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="ec6a2-146">\- 0x001</span></span>    | <span data-ttu-id="ec6a2-147">-1</span><span class="sxs-lookup"><span data-stu-id="ec6a2-147">-1</span></span>      | <span data-ttu-id="ec6a2-148">如果這是每一使用者的安裝，登錄值會以 **HKEY \_ CURRENT \_ user** 撰寫。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-148">If this is a per-user installation, the registry value is written under **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="ec6a2-149">如果這是每部電腦的安裝，登錄值會寫入 **HKEY \_ 本機 \_ 電腦**。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-149">If this is a per-machine installation, the registry value is written under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="ec6a2-150">請注意，您可以藉由將 [**ALLUSERS**](allusers.md) 屬性設定為1來指定每部電腦安裝。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-150">Note that a per-machine installation is specified by setting the [**ALLUSERS**](allusers.md) property to 1.</span></span><br/>                |
| <span data-ttu-id="ec6a2-151">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="ec6a2-151">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="ec6a2-152">0x000</span><span class="sxs-lookup"><span data-stu-id="ec6a2-152">0x000</span></span>       | <span data-ttu-id="ec6a2-153">0</span><span class="sxs-lookup"><span data-stu-id="ec6a2-153">0</span></span>       | <span data-ttu-id="ec6a2-154">**HKEY \_在 \_ 安裝期間，安裝** 程式會在每個使用者 [安裝內容](installation-context.md)中，從 **HKCU \\ Software \\** class hive 寫入或移除值。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-154">**HKEY\_CLASSES\_ROOT** The installer writes or removes the value from the **HKCU\\Software\\Classes** hive during installation in the per-user [installation context](installation-context.md).</span></span><br/> <span data-ttu-id="ec6a2-155">安裝程式會在每一部電腦安裝期間，寫入或移除 **HKLM \\ Software \\** class hive 中的值。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-155">The installer writes or removes the value from the **HKLM\\Software\\Classes** hive during per-machine installations.</span></span><br/> |
| <span data-ttu-id="ec6a2-156">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="ec6a2-156">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="ec6a2-157">0x001</span><span class="sxs-lookup"><span data-stu-id="ec6a2-157">0x001</span></span>       | <span data-ttu-id="ec6a2-158">1</span><span class="sxs-lookup"><span data-stu-id="ec6a2-158">1</span></span>       | <span data-ttu-id="ec6a2-159">**HKEY \_ 目前的 \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="ec6a2-159">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ec6a2-160">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="ec6a2-160">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="ec6a2-161">0x002</span><span class="sxs-lookup"><span data-stu-id="ec6a2-161">0x002</span></span>       | <span data-ttu-id="ec6a2-162">2</span><span class="sxs-lookup"><span data-stu-id="ec6a2-162">2</span></span>       | <span data-ttu-id="ec6a2-163">**HKEY \_ 本機 \_ 電腦**</span><span class="sxs-lookup"><span data-stu-id="ec6a2-163">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ec6a2-164">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="ec6a2-164">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="ec6a2-165">0x003</span><span class="sxs-lookup"><span data-stu-id="ec6a2-165">0x003</span></span>       | <span data-ttu-id="ec6a2-166">3</span><span class="sxs-lookup"><span data-stu-id="ec6a2-166">3</span></span>       | <span data-ttu-id="ec6a2-167">**HKEY \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="ec6a2-167">**HKEY\_USERS**</span></span>                                                                                                                                                                                                                                                                                                                              |



 

<span data-ttu-id="ec6a2-168">請注意，建議寫入 **HKCU** hive 的登錄專案參考在 [元件資料表](component-table.md)的 [屬性] 資料行中設定 RegistryKeyPath 位的元件。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-168">Note that it is recommended that registry entries written to the **HKCU** hive reference a component having the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="ec6a2-169">這可確保當相同電腦上有多個使用者時，安裝程式會寫入必要的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-169">This ensures that the installer writes the necessary registry entries when there are multiple users on the same computer.</span></span>

</dd> <dt>

<span data-ttu-id="ec6a2-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵</span><span class="sxs-lookup"><span data-stu-id="ec6a2-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="ec6a2-171">登錄值的可當地語系化金鑰。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-171">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="ec6a2-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="ec6a2-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="ec6a2-173">此資料行包含可當地語系化)  (的登錄值名稱。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-173">This column contains the registry value name (localizable).</span></span> <span data-ttu-id="ec6a2-174">如果這是 Null，則會將輸入到 [值] 資料行中的資料寫入預設的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-174">If this is Null, then the data entered into the Value column are written to the default registry key.</span></span>

<span data-ttu-id="ec6a2-175">如果 [值] 資料行是 Null，則 [名稱] 資料行中的下表所示的字串會有特殊意義。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-175">If the Value column is Null, then the strings shown in the following table in the Name column have special significance.</span></span>



| <span data-ttu-id="ec6a2-176">String</span><span class="sxs-lookup"><span data-stu-id="ec6a2-176">String</span></span> | <span data-ttu-id="ec6a2-177">意義</span><span class="sxs-lookup"><span data-stu-id="ec6a2-177">Meaning</span></span>                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | <span data-ttu-id="ec6a2-178">安裝元件時，就會建立金鑰（如果不存在）。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-178">The key is to be created, if absent, when the component is installed.</span></span>                                                                                                                            |
| \-     | <span data-ttu-id="ec6a2-179">卸載元件時，將會刪除金鑰（如果有的話）及其所有值和子機碼。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-179">The key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span>                                                                                     |
| \*     | <span data-ttu-id="ec6a2-180">安裝元件時，就會建立金鑰（如果不存在）。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-180">The key is to be created, if absent, when the component is installed.</span></span> <span data-ttu-id="ec6a2-181">此外，卸載元件時，將會刪除金鑰（如果有的話）及其所有值和子機碼。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-181">Additionally, the key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span> |



 

<span data-ttu-id="ec6a2-182">請注意，安裝元件時，如果已安裝的登錄機碼具有其值和子機碼，就必須使用 [RemoveRegistry 資料表](removeregistry-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-182">Note that the [RemoveRegistry table](removeregistry-table.md) must be used if an installed registry key is to be deleted, with its values and subkeys, when the component is installed.</span></span>

</dd> <dt>

<span data-ttu-id="ec6a2-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="ec6a2-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="ec6a2-184">此資料行是可當地語系化的登錄值。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-184">This column is the localizable registry value.</span></span> <span data-ttu-id="ec6a2-185">此欄位已 [格式化](formatted.md)。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-185">The field is [Formatted](formatted.md).</span></span> <span data-ttu-id="ec6a2-186">如果值附加至下列其中一個前置詞 (即 \# % *值*) 則會解讀此值，如表格中所述。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-186">If the value is attached to one of the following prefixes (i.e. \#%*value*) then the value is interpreted as described in the table.</span></span> <span data-ttu-id="ec6a2-187">請注意，每個前置詞的開頭都是數位記號 (\#) 。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-187">Note that each prefix begins with a number sign (\#).</span></span> <span data-ttu-id="ec6a2-188">如果值的開頭為兩個以上的連續數位記號 (\#) ，則 \# 會忽略第一個，並將值轉譯並儲存為字串。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-188">If the value begins with two or more consecutive number signs (\#), the first \# is ignored and value is interpreted and stored as a string.</span></span>



| <span data-ttu-id="ec6a2-189">前置詞</span><span class="sxs-lookup"><span data-stu-id="ec6a2-189">Prefix</span></span> | <span data-ttu-id="ec6a2-190">意義</span><span class="sxs-lookup"><span data-stu-id="ec6a2-190">Meaning</span></span>                                                                        |
|--------|--------------------------------------------------------------------------------|
| <span data-ttu-id="ec6a2-191">\#X</span><span class="sxs-lookup"><span data-stu-id="ec6a2-191">\#x</span></span>    | <span data-ttu-id="ec6a2-192">值會以十六進位值的形式加以解讀和儲存 (REG \_ BINARY) 。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-192">The value is interpreted and stored as a hexadecimal value (REG\_BINARY).</span></span>      |
| \#%    | <span data-ttu-id="ec6a2-193">值會被解讀並儲存為可擴充的字串， (REG \_ EXPAND \_ SZ) 。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-193">The value is interpreted and stored as an expandable string (REG\_EXPAND\_SZ).</span></span> |
| \#     | <span data-ttu-id="ec6a2-194">值會被解讀並儲存為整數 (REG \_ DWORD) 。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-194">The value is interpreted and stored as an integer (REG\_DWORD).</span></span>                |



 

-   <span data-ttu-id="ec6a2-195">如果值包含序列波狀 \[ ~ \] 符號，則會將值解釋為以 Null 分隔的字串清單， (REG \_ 多重 \_ SZ) 。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-195">If the value contains the sequence tilde \[~\], then the value is interpreted as a Null-delimited list of strings (REG\_MULTI\_SZ).</span></span> <span data-ttu-id="ec6a2-196">例如，若要指定包含三個字串 a、b 和 c 的清單，請使用 "a \[ ~ \] b \[ ~ \] c"。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-196">For example, to specify a list containing the three strings a, b and c, use "a\[~\]b\[~\]c".</span></span>
-   <span data-ttu-id="ec6a2-197">\[ ~ \] 值內的序列會分隔個別字串，並將其解釋並儲存為 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-197">The sequence \[~\] within the value separates the individual strings and is interpreted and stored as a Null character.</span></span>
-   <span data-ttu-id="ec6a2-198">如果在 \[ ~ \] 字串清單之前，則字串會附加到任何現有的登錄值字串。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-198">If a \[~\] precedes the string list, the strings are to be appended to any existing registry value strings.</span></span> <span data-ttu-id="ec6a2-199">如果登錄值中已出現附加字串，則會移除字串的原始出現位置。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-199">If an appending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="ec6a2-200">如果在 \[ ~ \] 字串清單結尾之後，字串就會加到任何現有的登錄值字串前面。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-200">If a \[~\] follows the end of the string list, the strings are to be prepended to any existing registry value strings.</span></span> <span data-ttu-id="ec6a2-201">如果登錄值中已有前置字串，則會移除字串的原始出現位置。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-201">If a prepending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="ec6a2-202">如果 \[ ~ \] 是在開頭和結尾，或是字串清單的開頭或結尾都不是，則字串會取代任何現有的登錄值字串。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-202">If a \[~\] is at both the beginning and the end or at neither the beginning nor the end of the string list, the strings are to replace any existing registry value strings.</span></span>
-   <span data-ttu-id="ec6a2-203">否則，值會以字串的形式來解讀和儲存 (REG \_ SZ) 。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-203">Otherwise, the value is interpreted and stored as a string (REG\_SZ).</span></span>

</dd> <dt>

<span data-ttu-id="ec6a2-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="ec6a2-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="ec6a2-205">在 [元件資料表](component-table.md) 的第一個資料行中，外部索引鍵參考控制登錄值安裝的元件。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-205">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec6a2-206">備註</span><span class="sxs-lookup"><span data-stu-id="ec6a2-206">Remarks</span></span>

<span data-ttu-id="ec6a2-207">[*順序資料表*](s-gly.md)中的 [WriteRegistryValues](writeregistryvalues-action.md)和 [RemoveRegistryValues](removeregistryvalues-action.md)動作會處理此資料表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-207">The [WriteRegistryValues](writeregistryvalues-action.md) and [RemoveRegistryValues](removeregistryvalues-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="ec6a2-208">如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-208">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="ec6a2-209">當已選取要在本機安裝或從來源執行的對應元件時，系統會將登錄資訊寫出至系統登錄。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-209">The registry information is written out to the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="ec6a2-210">請注意，在移除機碼下的最後一個值或子機碼之後，安裝程式會移除登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-210">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="ec6a2-211">若要避免在卸載時移除空白的登錄機碼，請在您需要保留的機碼底下寫入虛擬值，然後在 [名稱] 資料行中輸入 +。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-211">To prevent an empty registry key from being removed when uninstalling, write a dummy value under the key you need to keep and enter + in the Name column.</span></span> <span data-ttu-id="ec6a2-212">如果 \* 是在 [名稱] 資料行中，當移除元件時，就會刪除該索引鍵及其所有值和子機碼。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-212">If \* is in the Name column, the key is deleted, with all of its values and subkeys, when the component is removed.</span></span>

<span data-ttu-id="ec6a2-213">自訂動作可在安裝、卸載或修復交易期間，用來將資料列新增至登錄資料表。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-213">A custom action can be used to add rows to the Registry table during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="ec6a2-214">這些資料列不會保存在登錄資料表中，而且只有在目前的交易期間，才可使用此資訊。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-214">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="ec6a2-215">因此，自訂動作必須在需要這些額外資料列資訊的每個安裝、卸載或修復交易中執行。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-215">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="ec6a2-216">自訂動作必須位於動作順序中的 [RemoveRegistryValues](removeregistryvalues-action.md) 和 [WriteRegistryValues](writeregistryvalues-action.md) 動作之前。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-216">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

<span data-ttu-id="ec6a2-217">如需如何保護登錄機碼的詳細資訊，請參閱 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md) 和 [LockPermissions 資料表](lockpermissions-table.md)。</span><span class="sxs-lookup"><span data-stu-id="ec6a2-217">For information on how to secure a registry key see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="ec6a2-218">驗證</span><span class="sxs-lookup"><span data-stu-id="ec6a2-218">Validation</span></span>

<dl>

[<span data-ttu-id="ec6a2-219">ICE02</span><span class="sxs-lookup"><span data-stu-id="ec6a2-219">ICE02</span></span>](ice02.md)  
[<span data-ttu-id="ec6a2-220">ICE03</span><span class="sxs-lookup"><span data-stu-id="ec6a2-220">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ec6a2-221">ICE06</span><span class="sxs-lookup"><span data-stu-id="ec6a2-221">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ec6a2-222">ICE32</span><span class="sxs-lookup"><span data-stu-id="ec6a2-222">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ec6a2-223">ICE38</span><span class="sxs-lookup"><span data-stu-id="ec6a2-223">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="ec6a2-224">ICE43</span><span class="sxs-lookup"><span data-stu-id="ec6a2-224">ICE43</span></span>](ice43.md)  
[<span data-ttu-id="ec6a2-225">ICE46</span><span class="sxs-lookup"><span data-stu-id="ec6a2-225">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="ec6a2-226">ICE49</span><span class="sxs-lookup"><span data-stu-id="ec6a2-226">ICE49</span></span>](ice49.md)  
[<span data-ttu-id="ec6a2-227">ICE53</span><span class="sxs-lookup"><span data-stu-id="ec6a2-227">ICE53</span></span>](ice53.md)  
[<span data-ttu-id="ec6a2-228">ICE55</span><span class="sxs-lookup"><span data-stu-id="ec6a2-228">ICE55</span></span>](ice55.md)  
[<span data-ttu-id="ec6a2-229">ICE57</span><span class="sxs-lookup"><span data-stu-id="ec6a2-229">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="ec6a2-230">ICE70</span><span class="sxs-lookup"><span data-stu-id="ec6a2-230">ICE70</span></span>](ice70.md)  
[<span data-ttu-id="ec6a2-231">ICE80</span><span class="sxs-lookup"><span data-stu-id="ec6a2-231">ICE80</span></span>](ice80.md)  
</dl>

 

 




