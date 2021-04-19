---
description: RegLocator 資料表會保存使用登錄搜尋檔案或目錄所需的資訊，或是搜尋特定的登錄專案本身。 此資料表包含下列資料行。
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: RegLocator 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988776"
---
# <a name="reglocator-table"></a><span data-ttu-id="a2683-104">RegLocator 資料表</span><span class="sxs-lookup"><span data-stu-id="a2683-104">RegLocator Table</span></span>

<span data-ttu-id="a2683-105">RegLocator 資料表會保存使用登錄搜尋檔案或目錄所需的資訊，或是搜尋特定的登錄專案本身。</span><span class="sxs-lookup"><span data-stu-id="a2683-105">The RegLocator table holds the information needed to search for a file or directory using the registry, or to search for a particular registry entry itself.</span></span> <span data-ttu-id="a2683-106">此資料表包含下列資料行。</span><span class="sxs-lookup"><span data-stu-id="a2683-106">This table has the following columns.</span></span>



| <span data-ttu-id="a2683-107">Column</span><span class="sxs-lookup"><span data-stu-id="a2683-107">Column</span></span>      | <span data-ttu-id="a2683-108">類型</span><span class="sxs-lookup"><span data-stu-id="a2683-108">Type</span></span>                         | <span data-ttu-id="a2683-109">答案</span><span class="sxs-lookup"><span data-stu-id="a2683-109">Key</span></span> | <span data-ttu-id="a2683-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="a2683-110">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="a2683-111">簽名\_</span><span class="sxs-lookup"><span data-stu-id="a2683-111">Signature\_</span></span> | [<span data-ttu-id="a2683-112">識別碼</span><span class="sxs-lookup"><span data-stu-id="a2683-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="a2683-113">Y</span><span class="sxs-lookup"><span data-stu-id="a2683-113">Y</span></span>   | <span data-ttu-id="a2683-114">N</span><span class="sxs-lookup"><span data-stu-id="a2683-114">N</span></span>        |
| <span data-ttu-id="a2683-115">Root</span><span class="sxs-lookup"><span data-stu-id="a2683-115">Root</span></span>        | [<span data-ttu-id="a2683-116">整數</span><span class="sxs-lookup"><span data-stu-id="a2683-116">Integer</span></span>](integer.md)       | <span data-ttu-id="a2683-117">N</span><span class="sxs-lookup"><span data-stu-id="a2683-117">N</span></span>   | <span data-ttu-id="a2683-118">N</span><span class="sxs-lookup"><span data-stu-id="a2683-118">N</span></span>        |
| <span data-ttu-id="a2683-119">答案</span><span class="sxs-lookup"><span data-stu-id="a2683-119">Key</span></span>         | [<span data-ttu-id="a2683-120">RegPath</span><span class="sxs-lookup"><span data-stu-id="a2683-120">RegPath</span></span>](regpath.md)       | <span data-ttu-id="a2683-121">N</span><span class="sxs-lookup"><span data-stu-id="a2683-121">N</span></span>   | <span data-ttu-id="a2683-122">N</span><span class="sxs-lookup"><span data-stu-id="a2683-122">N</span></span>        |
| <span data-ttu-id="a2683-123">Name</span><span class="sxs-lookup"><span data-stu-id="a2683-123">Name</span></span>        | [<span data-ttu-id="a2683-124">格式 化</span><span class="sxs-lookup"><span data-stu-id="a2683-124">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a2683-125">N</span><span class="sxs-lookup"><span data-stu-id="a2683-125">N</span></span>   | <span data-ttu-id="a2683-126">Y</span><span class="sxs-lookup"><span data-stu-id="a2683-126">Y</span></span>        |
| <span data-ttu-id="a2683-127">類型</span><span class="sxs-lookup"><span data-stu-id="a2683-127">Type</span></span>        | [<span data-ttu-id="a2683-128">整數</span><span class="sxs-lookup"><span data-stu-id="a2683-128">Integer</span></span>](integer.md)       | <span data-ttu-id="a2683-129">N</span><span class="sxs-lookup"><span data-stu-id="a2683-129">N</span></span>   | <span data-ttu-id="a2683-130">Y</span><span class="sxs-lookup"><span data-stu-id="a2683-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a2683-131">資料行</span><span class="sxs-lookup"><span data-stu-id="a2683-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a2683-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_</span><span class="sxs-lookup"><span data-stu-id="a2683-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="a2683-133">[簽章] 欄位中的值 \_ 代表唯一簽章，這是簽章資料表 [的資料](signature-table.md) 行之一的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a2683-133">The value in the Signature\_ field represents a unique signature that is an external key into column one of the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="a2683-134">如果簽章資料表中有這個簽章，則會搜尋檔案。</span><span class="sxs-lookup"><span data-stu-id="a2683-134">If this signature is present in the Signature table, the search is for a file.</span></span> <span data-ttu-id="a2683-135">如果簽章資料表中沒有這個簽章，而且 [類型] 資料行的值是 **msidbLocatorTypeRawValue**，則搜尋是針對 RegLocator 資料表所指向的登錄機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="a2683-135">If this signature is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the registry key name pointed to by the RegLocator table.</span></span> <span data-ttu-id="a2683-136">否則搜尋是針對 RegLocator 資料表所指向的目錄。</span><span class="sxs-lookup"><span data-stu-id="a2683-136">Otherwise the search is for a directory pointed to by the RegLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="a2683-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>根</span><span class="sxs-lookup"><span data-stu-id="a2683-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="a2683-138">登錄值的預先定義根金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2683-138">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="a2683-139">常數</span><span class="sxs-lookup"><span data-stu-id="a2683-139">Constant</span></span>                          | <span data-ttu-id="a2683-140">十六進位</span><span class="sxs-lookup"><span data-stu-id="a2683-140">Hexadecimal</span></span> | <span data-ttu-id="a2683-141">Decimal</span><span class="sxs-lookup"><span data-stu-id="a2683-141">Decimal</span></span> | <span data-ttu-id="a2683-142">根金鑰</span><span class="sxs-lookup"><span data-stu-id="a2683-142">Root key</span></span>             |
|-----------------------------------|-------------|---------|----------------------|
| <span data-ttu-id="a2683-143">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="a2683-143">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="a2683-144">0x000</span><span class="sxs-lookup"><span data-stu-id="a2683-144">0x000</span></span>       | <span data-ttu-id="a2683-145">0</span><span class="sxs-lookup"><span data-stu-id="a2683-145">0</span></span>       | <span data-ttu-id="a2683-146">HKEY \_ 類別 \_ 根目錄</span><span class="sxs-lookup"><span data-stu-id="a2683-146">HKEY\_CLASSES\_ROOT</span></span>  |
| <span data-ttu-id="a2683-147">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="a2683-147">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="a2683-148">0x001</span><span class="sxs-lookup"><span data-stu-id="a2683-148">0x001</span></span>       | <span data-ttu-id="a2683-149">1</span><span class="sxs-lookup"><span data-stu-id="a2683-149">1</span></span>       | <span data-ttu-id="a2683-150">HKEY \_ 目前的 \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="a2683-150">HKEY\_CURRENT\_USER</span></span>  |
| <span data-ttu-id="a2683-151">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="a2683-151">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="a2683-152">0x002</span><span class="sxs-lookup"><span data-stu-id="a2683-152">0x002</span></span>       | <span data-ttu-id="a2683-153">2</span><span class="sxs-lookup"><span data-stu-id="a2683-153">2</span></span>       | <span data-ttu-id="a2683-154">HKEY \_ 本機 \_ 電腦</span><span class="sxs-lookup"><span data-stu-id="a2683-154">HKEY\_LOCAL\_MACHINE</span></span> |
| <span data-ttu-id="a2683-155">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="a2683-155">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="a2683-156">0x003</span><span class="sxs-lookup"><span data-stu-id="a2683-156">0x003</span></span>       | <span data-ttu-id="a2683-157">3</span><span class="sxs-lookup"><span data-stu-id="a2683-157">3</span></span>       | <span data-ttu-id="a2683-158">HKEY \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="a2683-158">HKEY\_USERS</span></span>          |



 

</dd> <dt>

<span data-ttu-id="a2683-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵</span><span class="sxs-lookup"><span data-stu-id="a2683-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="a2683-160">登錄值的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a2683-160">The key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="a2683-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="a2683-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="a2683-162">登錄值名稱。</span><span class="sxs-lookup"><span data-stu-id="a2683-162">The registry value name.</span></span> <span data-ttu-id="a2683-163">如果這個值為 null，則會抓取索引鍵未命名或預設值（如果有的話）的值。</span><span class="sxs-lookup"><span data-stu-id="a2683-163">If this value is null, then the value from the key's unnamed or default value, if any, is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="a2683-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型</span><span class="sxs-lookup"><span data-stu-id="a2683-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="a2683-165">判斷登錄值是否為檔案名、目錄位置或原始登錄值的值。</span><span class="sxs-lookup"><span data-stu-id="a2683-165">A value that determines if the registry value is a file name, a directory location, or raw registry value.</span></span>

<span data-ttu-id="a2683-166">下表列出有效的值。</span><span class="sxs-lookup"><span data-stu-id="a2683-166">The following table lists valid values.</span></span> <span data-ttu-id="a2683-167">如有必要，請設定前三個值的其中一個，並 **msidbLocatorType64bit** 。</span><span class="sxs-lookup"><span data-stu-id="a2683-167">Set one of the first three values and **msidbLocatorType64bit** if necessary.</span></span> <span data-ttu-id="a2683-168">如果此欄位中的專案不存在，則類型會設定為1。</span><span class="sxs-lookup"><span data-stu-id="a2683-168">If the entry in this field is absent, Type is set to be 1.</span></span>



| <span data-ttu-id="a2683-169">常數</span><span class="sxs-lookup"><span data-stu-id="a2683-169">Constant</span></span>                      | <span data-ttu-id="a2683-170">十六進位</span><span class="sxs-lookup"><span data-stu-id="a2683-170">Hexadecimal</span></span> | <span data-ttu-id="a2683-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="a2683-171">Decimal</span></span> | <span data-ttu-id="a2683-172">Description</span><span class="sxs-lookup"><span data-stu-id="a2683-172">Description</span></span>                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2683-173">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="a2683-173">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="a2683-174">0x000</span><span class="sxs-lookup"><span data-stu-id="a2683-174">0x000</span></span>       | <span data-ttu-id="a2683-175">0</span><span class="sxs-lookup"><span data-stu-id="a2683-175">0</span></span>       | <span data-ttu-id="a2683-176">金鑰路徑是目錄。</span><span class="sxs-lookup"><span data-stu-id="a2683-176">Key path is a directory.</span></span>                                                                                                                                           |
| <span data-ttu-id="a2683-177">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="a2683-177">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="a2683-178">0x001</span><span class="sxs-lookup"><span data-stu-id="a2683-178">0x001</span></span>       | <span data-ttu-id="a2683-179">1</span><span class="sxs-lookup"><span data-stu-id="a2683-179">1</span></span>       | <span data-ttu-id="a2683-180">金鑰路徑是檔案名。</span><span class="sxs-lookup"><span data-stu-id="a2683-180">Key path is a file name.</span></span>                                                                                                                                           |
| <span data-ttu-id="a2683-181">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="a2683-181">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="a2683-182">0x002</span><span class="sxs-lookup"><span data-stu-id="a2683-182">0x002</span></span>       | <span data-ttu-id="a2683-183">2</span><span class="sxs-lookup"><span data-stu-id="a2683-183">2</span></span>       | <span data-ttu-id="a2683-184">金鑰路徑是登錄值。</span><span class="sxs-lookup"><span data-stu-id="a2683-184">Key path is a registry value.</span></span>                                                                                                                                      |
| <span data-ttu-id="a2683-185">**msidbLocatorType64bit**</span><span class="sxs-lookup"><span data-stu-id="a2683-185">**msidbLocatorType64bit**</span></span>     | <span data-ttu-id="a2683-186">0x010</span><span class="sxs-lookup"><span data-stu-id="a2683-186">0x010</span></span>       | <span data-ttu-id="a2683-187">16</span><span class="sxs-lookup"><span data-stu-id="a2683-187">16</span></span>      | <span data-ttu-id="a2683-188">設定此位，讓安裝程式搜尋登錄的64位部分。</span><span class="sxs-lookup"><span data-stu-id="a2683-188">Set this bit to have the installer search the 64-bit portion of the registry.</span></span> <span data-ttu-id="a2683-189">請勿將此位設定為讓安裝程式搜尋登錄的32位部分。</span><span class="sxs-lookup"><span data-stu-id="a2683-189">Do not set this bit to have the installer search the 32-bit portion of the registry.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2683-190">備註</span><span class="sxs-lookup"><span data-stu-id="a2683-190">Remarks</span></span>

<span data-ttu-id="a2683-191">請注意，如果 [類型] 欄位中的值是 **msidbLocatorTypeRawValue**，安裝程式會將 [AppSearch](appsearch-table.md) 資料表的屬性欄位中指定的屬性值設定為登錄值。</span><span class="sxs-lookup"><span data-stu-id="a2683-191">Note that if the value in the Type field is **msidbLocatorTypeRawValue**, the installer sets the value of the property specified in the Property field of the [AppSearch](appsearch-table.md) table to the registry value.</span></span> <span data-ttu-id="a2683-192">安裝程式會將前置詞新增至登錄值，以識別登錄值的型別。</span><span class="sxs-lookup"><span data-stu-id="a2683-192">The installer adds a prefix to the registry value that identifies the type of registry value.</span></span> <span data-ttu-id="a2683-193">如需登錄數值型別的詳細資訊，請參閱登錄 [數值型別](../sysinfo/registry-value-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a2683-193">For more information about types of registry values, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>



| <span data-ttu-id="a2683-194">登錄類型</span><span class="sxs-lookup"><span data-stu-id="a2683-194">Registry type</span></span>   | <span data-ttu-id="a2683-195">安裝程式新增的前置詞</span><span class="sxs-lookup"><span data-stu-id="a2683-195">Prefix added by Installer</span></span>                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2683-196">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a2683-196">REG\_SZ</span></span>         | <span data-ttu-id="a2683-197">無，但是如果登錄值的第一個字元是 \# ，則安裝程式會在前面加上一個字元來將該字元轉義 \# 。</span><span class="sxs-lookup"><span data-stu-id="a2683-197">None, but if the first character of the registry value is \#, the installer escapes the character by prefixing a another \#.</span></span>            |
| <span data-ttu-id="a2683-198">DWORD</span><span class="sxs-lookup"><span data-stu-id="a2683-198">DWORD</span></span>           | <span data-ttu-id="a2683-199">" \# " （選擇性），後面接著 ' + ' 或 '-'</span><span class="sxs-lookup"><span data-stu-id="a2683-199">"\#" optionally followed by '+' or '-'</span></span>                                                                                                  |
| <span data-ttu-id="a2683-200">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a2683-200">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="a2683-201">"\#%"</span><span class="sxs-lookup"><span data-stu-id="a2683-201">"\#%"</span></span>                                                                                                                                   |
| <span data-ttu-id="a2683-202">REG \_ 多重 \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a2683-202">REG\_MULTI\_SZ</span></span>  | <span data-ttu-id="a2683-203">Null。</span><span class="sxs-lookup"><span data-stu-id="a2683-203">Null.</span></span> <span data-ttu-id="a2683-204">安裝程式會將屬性設定為開頭為 null 的值，並以 null 結尾。</span><span class="sxs-lookup"><span data-stu-id="a2683-204">The installer sets the property to a value beginning with a null and ending with a null.</span></span>                                          |
| <span data-ttu-id="a2683-205">REG \_ 二進位檔</span><span class="sxs-lookup"><span data-stu-id="a2683-205">REG\_BINARY</span></span>     | <span data-ttu-id="a2683-206">" \# x" 如果是 REG \_ 二進位，則安裝程式會將每個十六進位數位轉換成 (半個十六進位數位，並將其儲存為前面加上 "x" 的 ASCII 字元) \# 。</span><span class="sxs-lookup"><span data-stu-id="a2683-206">"\#x" In case of REG\_BINARY, the installer converts and saves each hexadecimal digit (nibble) as an ASCII character prefixed by "\#x".</span></span> |



 

<span data-ttu-id="a2683-207">一般而言，此資料表中的資料行並不會當地語系化。</span><span class="sxs-lookup"><span data-stu-id="a2683-207">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="a2683-208">如果作者決定要搜尋多種語言的產品，則每種語言的表格中都必須包含個別的專案。</span><span class="sxs-lookup"><span data-stu-id="a2683-208">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="a2683-209">請注意，您不能使用 RegLocator 資料表來檢查索引鍵是否存在。</span><span class="sxs-lookup"><span data-stu-id="a2683-209">Note that it is not possible to use the RegLocator table to check only for the presence of the key.</span></span> <span data-ttu-id="a2683-210">不過，您可以搜尋索引鍵的預設值，如果不是空的，則會取出其值。</span><span class="sxs-lookup"><span data-stu-id="a2683-210">However, you can search for the default value of a key and retrieve its value if it is not empty.</span></span>

<span data-ttu-id="a2683-211">如需詳細資訊，請參閱 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)。</span><span class="sxs-lookup"><span data-stu-id="a2683-211">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="a2683-212">驗證</span><span class="sxs-lookup"><span data-stu-id="a2683-212">Validation</span></span>

<dl>

[<span data-ttu-id="a2683-213">ICE03</span><span class="sxs-lookup"><span data-stu-id="a2683-213">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a2683-214">ICE06</span><span class="sxs-lookup"><span data-stu-id="a2683-214">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a2683-215">ICE46</span><span class="sxs-lookup"><span data-stu-id="a2683-215">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="a2683-216">ICE80</span><span class="sxs-lookup"><span data-stu-id="a2683-216">ICE80</span></span>](ice80.md)  
</dl>

 

 
