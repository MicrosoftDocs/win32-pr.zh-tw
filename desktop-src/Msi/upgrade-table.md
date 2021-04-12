---
description: 升級資料表包含主要升級期間所需的資訊。
ms.assetid: f5fda405-8a09-495e-aa8c-b808a2f02b0f
title: 升級資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b48ce49f0f931209ccf472cd74b352c270353a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320560"
---
# <a name="upgrade-table"></a><span data-ttu-id="099f9-103">升級資料表</span><span class="sxs-lookup"><span data-stu-id="099f9-103">Upgrade Table</span></span>

<span data-ttu-id="099f9-104">升級資料表包含 [主要升級](major-upgrades.md)期間所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="099f9-104">The Upgrade table contains information required during [major upgrades](major-upgrades.md).</span></span> <span data-ttu-id="099f9-105">若要完全啟用安裝程式的升級功能，每個封裝都應該有 [**UpgradeCode**](upgradecode.md) 屬性和升級資料表。</span><span class="sxs-lookup"><span data-stu-id="099f9-105">To fully enable the installer's upgrade capabilities, every package should have an [**UpgradeCode**](upgradecode.md) property and an Upgrade table.</span></span> <span data-ttu-id="099f9-106">升級資料表中的每一筆記錄都會提供升級程式碼、產品版本和語言資訊的特性組合，用來識別一組受升級影響的產品。</span><span class="sxs-lookup"><span data-stu-id="099f9-106">Each record in the Upgrade table gives a characteristic combination of upgrade code, product version, and language information used to identify a set of products affected by the upgrade.</span></span> <span data-ttu-id="099f9-107">當 [FindRelatedProducts](findrelatedproducts-action.md) 動作偵測到安裝在系統上的受影響產品時，會將產品程式碼附加至 ActionProperty 資料行中指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="099f9-107">When the [FindRelatedProducts](findrelatedproducts-action.md) action detects an affected product installed on the system, it appends the product code to a property specified in the ActionProperty column.</span></span> <span data-ttu-id="099f9-108">[RemoveExistingProducts](removeexistingproducts-action.md)動作和[MigrateFeatureStates](migratefeaturestates-action.md)動作只會移除或遷移 ActionProperty 資料行中所列的產品。</span><span class="sxs-lookup"><span data-stu-id="099f9-108">The [RemoveExistingProducts](removeexistingproducts-action.md) action and the [MigrateFeatureStates](migratefeaturestates-action.md) action only remove or migrate products listed in the ActionProperty column.</span></span>

<span data-ttu-id="099f9-109">升級資料表包含下表所示的資料行。</span><span class="sxs-lookup"><span data-stu-id="099f9-109">The Upgrade table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="099f9-110">Column</span><span class="sxs-lookup"><span data-stu-id="099f9-110">Column</span></span>         | <span data-ttu-id="099f9-111">類型</span><span class="sxs-lookup"><span data-stu-id="099f9-111">Type</span></span>                         | <span data-ttu-id="099f9-112">答案</span><span class="sxs-lookup"><span data-stu-id="099f9-112">Key</span></span> | <span data-ttu-id="099f9-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="099f9-113">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="099f9-114">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="099f9-114">UpgradeCode</span></span>    | [<span data-ttu-id="099f9-115">GUID</span><span class="sxs-lookup"><span data-stu-id="099f9-115">GUID</span></span>](guid.md)             | <span data-ttu-id="099f9-116">Y</span><span class="sxs-lookup"><span data-stu-id="099f9-116">Y</span></span>   | <span data-ttu-id="099f9-117">N</span><span class="sxs-lookup"><span data-stu-id="099f9-117">N</span></span>        |
| <span data-ttu-id="099f9-118">VersionMin</span><span class="sxs-lookup"><span data-stu-id="099f9-118">VersionMin</span></span>     | [<span data-ttu-id="099f9-119">Text</span><span class="sxs-lookup"><span data-stu-id="099f9-119">Text</span></span>](text.md)             | <span data-ttu-id="099f9-120">Y</span><span class="sxs-lookup"><span data-stu-id="099f9-120">Y</span></span>   | <span data-ttu-id="099f9-121">Y</span><span class="sxs-lookup"><span data-stu-id="099f9-121">Y</span></span>        |
| <span data-ttu-id="099f9-122">VersionMax</span><span class="sxs-lookup"><span data-stu-id="099f9-122">VersionMax</span></span>     | [<span data-ttu-id="099f9-123">Text</span><span class="sxs-lookup"><span data-stu-id="099f9-123">Text</span></span>](text.md)             | <span data-ttu-id="099f9-124">Y</span><span class="sxs-lookup"><span data-stu-id="099f9-124">Y</span></span>   | <span data-ttu-id="099f9-125">Y</span><span class="sxs-lookup"><span data-stu-id="099f9-125">Y</span></span>        |
| <span data-ttu-id="099f9-126">語言</span><span class="sxs-lookup"><span data-stu-id="099f9-126">Language</span></span>       | [<span data-ttu-id="099f9-127">Text</span><span class="sxs-lookup"><span data-stu-id="099f9-127">Text</span></span>](text.md)             | <span data-ttu-id="099f9-128">Y</span><span class="sxs-lookup"><span data-stu-id="099f9-128">Y</span></span>   | <span data-ttu-id="099f9-129">Y</span><span class="sxs-lookup"><span data-stu-id="099f9-129">Y</span></span>        |
| <span data-ttu-id="099f9-130">屬性</span><span class="sxs-lookup"><span data-stu-id="099f9-130">Attributes</span></span>     | [<span data-ttu-id="099f9-131">整數</span><span class="sxs-lookup"><span data-stu-id="099f9-131">Integer</span></span>](integer.md)       | <span data-ttu-id="099f9-132">Y</span><span class="sxs-lookup"><span data-stu-id="099f9-132">Y</span></span>   | <span data-ttu-id="099f9-133">N</span><span class="sxs-lookup"><span data-stu-id="099f9-133">N</span></span>        |
| <span data-ttu-id="099f9-134">移除</span><span class="sxs-lookup"><span data-stu-id="099f9-134">Remove</span></span>         | [<span data-ttu-id="099f9-135">格式 化</span><span class="sxs-lookup"><span data-stu-id="099f9-135">Formatted</span></span>](formatted.md)   | <span data-ttu-id="099f9-136">N</span><span class="sxs-lookup"><span data-stu-id="099f9-136">N</span></span>   | <span data-ttu-id="099f9-137">Y</span><span class="sxs-lookup"><span data-stu-id="099f9-137">Y</span></span>        |
| <span data-ttu-id="099f9-138">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="099f9-138">ActionProperty</span></span> | [<span data-ttu-id="099f9-139">識別碼</span><span class="sxs-lookup"><span data-stu-id="099f9-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="099f9-140">N</span><span class="sxs-lookup"><span data-stu-id="099f9-140">N</span></span>   | <span data-ttu-id="099f9-141">N</span><span class="sxs-lookup"><span data-stu-id="099f9-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="099f9-142">資料行</span><span class="sxs-lookup"><span data-stu-id="099f9-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="099f9-143"><span id="UpgradeCode"></span><span id="upgradecode"></span><span id="UPGRADECODE"></span>UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="099f9-143"><span id="UpgradeCode"></span><span id="upgradecode"></span><span id="UPGRADECODE"></span>UpgradeCode</span></span>
</dt> <dd>

<span data-ttu-id="099f9-144">此資料行中的 [UpgradeCode](upgradecode.md) 屬性會指定 [FindRelatedProducts](findrelatedproducts-action.md) 動作要偵測的所有產品的升級程式碼。</span><span class="sxs-lookup"><span data-stu-id="099f9-144">The [UpgradeCode](upgradecode.md) property in this column specifies the upgrade code of all products that are to be detected by the [FindRelatedProducts](findrelatedproducts-action.md) action.</span></span>

</dd> <dt>

<span data-ttu-id="099f9-145"><span id="VersionMin"></span><span id="versionmin"></span><span id="VERSIONMIN"></span>VersionMin</span><span class="sxs-lookup"><span data-stu-id="099f9-145"><span id="VersionMin"></span><span id="versionmin"></span><span id="VERSIONMIN"></span>VersionMin</span></span>
</dt> <dd>

<span data-ttu-id="099f9-146">[FindRelatedProducts](findrelatedproducts-action.md)所偵測到的產品版本範圍下限。</span><span class="sxs-lookup"><span data-stu-id="099f9-146">Lower boundary of the range of product versions detected by [FindRelatedProducts](findrelatedproducts-action.md).</span></span> <span data-ttu-id="099f9-147">在 [屬性] 中輸入 **msidbUpgradeAttributesVersionMinInclusive** ，以包含範圍內的 VersionMin。</span><span class="sxs-lookup"><span data-stu-id="099f9-147">Enter **msidbUpgradeAttributesVersionMinInclusive** in Attributes to include VersionMin in the range.</span></span> <span data-ttu-id="099f9-148">如果 VersionMin 等於空字串 ( "" ) 它會評估為與0相同。</span><span class="sxs-lookup"><span data-stu-id="099f9-148">If VersionMin equals an empty string ("") it is evaluated the same as 0.</span></span> <span data-ttu-id="099f9-149">如果 VersionMin 為 null，FindRelatedProducts 會忽略 **msidbUpgradeAttributesVersionMinInclusive** 並偵測所有先前的版本。</span><span class="sxs-lookup"><span data-stu-id="099f9-149">If VersionMin is null, FindRelatedProducts ignores **msidbUpgradeAttributesVersionMinInclusive** and detects all previous versions.</span></span> <span data-ttu-id="099f9-150">VersionMin 和 VersionMax 不得同時為 null。</span><span class="sxs-lookup"><span data-stu-id="099f9-150">VersionMin and VersionMax must not both be null.</span></span>

<span data-ttu-id="099f9-151">VersionMin 必須是有效的產品版本，如 [**ProductVersion**](productversion.md) 屬性所述。</span><span class="sxs-lookup"><span data-stu-id="099f9-151">VersionMin must be a valid product version as described for the [**ProductVersion**](productversion.md) property.</span></span> <span data-ttu-id="099f9-152">請注意，Windows Installer 只會使用產品版本的前三個欄位。</span><span class="sxs-lookup"><span data-stu-id="099f9-152">Note that Windows Installer uses only the first three fields of the product version.</span></span> <span data-ttu-id="099f9-153">如果您在產品版本中包含第四個欄位，安裝程式會忽略第四個欄位。</span><span class="sxs-lookup"><span data-stu-id="099f9-153">If you include a fourth field in your product version, the installer ignores the fourth field.</span></span>

</dd> <dt>

<span data-ttu-id="099f9-154"><span id="VersionMax"></span><span id="versionmax"></span><span id="VERSIONMAX"></span>VersionMax</span><span class="sxs-lookup"><span data-stu-id="099f9-154"><span id="VersionMax"></span><span id="versionmax"></span><span id="VERSIONMAX"></span>VersionMax</span></span>
</dt> <dd>

<span data-ttu-id="099f9-155">[FindRelatedProducts](findrelatedproducts-action.md)動作所偵測到之產品版本範圍的上限。</span><span class="sxs-lookup"><span data-stu-id="099f9-155">Upper boundary of the range of product versions detected by the [FindRelatedProducts](findrelatedproducts-action.md) action.</span></span> <span data-ttu-id="099f9-156">在 [屬性] 中輸入 **msidbUpgradeAttributesVersionMaxInclusive** ，以包含範圍內的 VersionMax。</span><span class="sxs-lookup"><span data-stu-id="099f9-156">Enter **msidbUpgradeAttributesVersionMaxInclusive** in Attributes to include VersionMax in the range.</span></span> <span data-ttu-id="099f9-157">如果 VersionMax 是 ( "" ) 的空字串，則會評估為與0相同。</span><span class="sxs-lookup"><span data-stu-id="099f9-157">If VersionMax is an empty string (""), it is evaluated the same as 0.</span></span> <span data-ttu-id="099f9-158">如果 VersionMax 為 null，FindRelatedProducts 會忽略 **msidbUpgradeAttributesVersionMaxInclusive** ，並偵測大於 (或大於或等於) VersionMin 和 **msidbUpgradeAttributesVersionMinInclusive** 指定之下限的所有產品版本。</span><span class="sxs-lookup"><span data-stu-id="099f9-158">If VersionMax is null, FindRelatedProducts ignores **msidbUpgradeAttributesVersionMaxInclusive** and detects all product versions greater than (or greater than or equal to) the lower boundary specified by VersionMin and **msidbUpgradeAttributesVersionMinInclusive**.</span></span> <span data-ttu-id="099f9-159">VersionMin 和 VersionMax 不得同時為 null。</span><span class="sxs-lookup"><span data-stu-id="099f9-159">VersionMin and VersionMax must not both be null.</span></span>

<span data-ttu-id="099f9-160">VersionMax 必須是有效的產品版本，如 [**ProductVersion**](productversion.md) 屬性所述。</span><span class="sxs-lookup"><span data-stu-id="099f9-160">VersionMax must be a valid product version as described for the [**ProductVersion**](productversion.md) property.</span></span> <span data-ttu-id="099f9-161">請注意，Windows Installer 只會使用產品版本的前三個欄位。</span><span class="sxs-lookup"><span data-stu-id="099f9-161">Note that Windows Installer uses only the first three fields of the product version.</span></span> <span data-ttu-id="099f9-162">如果您在產品版本中包含第四個欄位，安裝程式會忽略第四個欄位。</span><span class="sxs-lookup"><span data-stu-id="099f9-162">If you include a fourth field in your product version, the installer ignores the fourth field.</span></span>

</dd> <dt>

<span data-ttu-id="099f9-163"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>語言</span><span class="sxs-lookup"><span data-stu-id="099f9-163"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="099f9-164">[FindRelatedProducts](findrelatedproducts-action.md)偵測到的語言集合。</span><span class="sxs-lookup"><span data-stu-id="099f9-164">The set of languages detected by [FindRelatedProducts](findrelatedproducts-action.md).</span></span> <span data-ttu-id="099f9-165">輸入數位語言識別項的清單 (LANGID) 以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="099f9-165">Enter a list of numeric language identifiers (LANGID) separated by commas.</span></span> <span data-ttu-id="099f9-166">在 [屬性] 中輸入 **msidbUpgradeAttributesLanguagesExclusive** ，以偵測語言中列出的所有語言。</span><span class="sxs-lookup"><span data-stu-id="099f9-166">Enter **msidbUpgradeAttributesLanguagesExclusive** in Attributes to detect all languages exclusive of those listed in Language.</span></span> <span data-ttu-id="099f9-167">如果 Language 為 null 或空字串 ( "" ) ，FindRelatedProducts 會忽略 **msidbUpgradeAttributesLanguagesExclusive** 並偵測所有語言。</span><span class="sxs-lookup"><span data-stu-id="099f9-167">If Language is null or an empty string (""), FindRelatedProducts ignores **msidbUpgradeAttributesLanguagesExclusive** and detects all languages.</span></span>

</dd> <dt>

<span data-ttu-id="099f9-168"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="099f9-168"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="099f9-169">此資料行包含指定升級資料表之屬性的位旗標。</span><span class="sxs-lookup"><span data-stu-id="099f9-169">This column contains bit flags specifying attributes of the Upgrade table.</span></span>



| <span data-ttu-id="099f9-170">位旗標名稱</span><span class="sxs-lookup"><span data-stu-id="099f9-170">Bit flag name</span></span>                                 | <span data-ttu-id="099f9-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="099f9-171">Decimal</span></span> | <span data-ttu-id="099f9-172">十六進位</span><span class="sxs-lookup"><span data-stu-id="099f9-172">Hexadecimal</span></span> | <span data-ttu-id="099f9-173">屬性</span><span class="sxs-lookup"><span data-stu-id="099f9-173">Attribute</span></span>                                                                                                            |
|-----------------------------------------------|---------|-------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="099f9-174">**msidbUpgradeAttributesMigrateFeatures**</span><span class="sxs-lookup"><span data-stu-id="099f9-174">**msidbUpgradeAttributesMigrateFeatures**</span></span>     | <span data-ttu-id="099f9-175">1</span><span class="sxs-lookup"><span data-stu-id="099f9-175">1</span></span>       | <span data-ttu-id="099f9-176">0x001</span><span class="sxs-lookup"><span data-stu-id="099f9-176">0x001</span></span>       | <span data-ttu-id="099f9-177">藉由啟用 [MigrateFeatureStates](migratefeaturestates-action.md) 動作中的邏輯來遷移功能狀態。</span><span class="sxs-lookup"><span data-stu-id="099f9-177">Migrates feature states by enabling the logic in the [MigrateFeatureStates](migratefeaturestates-action.md) action.</span></span> |
| <span data-ttu-id="099f9-178">**msidbUpgradeAttributesOnlyDetect**</span><span class="sxs-lookup"><span data-stu-id="099f9-178">**msidbUpgradeAttributesOnlyDetect**</span></span>          | <span data-ttu-id="099f9-179">2</span><span class="sxs-lookup"><span data-stu-id="099f9-179">2</span></span>       | <span data-ttu-id="099f9-180">0x002</span><span class="sxs-lookup"><span data-stu-id="099f9-180">0x002</span></span>       | <span data-ttu-id="099f9-181">偵測產品和應用程式，但不會移除。</span><span class="sxs-lookup"><span data-stu-id="099f9-181">Detects products and applications but does not remove.</span></span>                                                               |
| <span data-ttu-id="099f9-182">**msidbUpgradeAttributesIgnoreRemoveFailure**</span><span class="sxs-lookup"><span data-stu-id="099f9-182">**msidbUpgradeAttributesIgnoreRemoveFailure**</span></span> | <span data-ttu-id="099f9-183">4</span><span class="sxs-lookup"><span data-stu-id="099f9-183">4</span></span>       | <span data-ttu-id="099f9-184">0x004</span><span class="sxs-lookup"><span data-stu-id="099f9-184">0x004</span></span>       | <span data-ttu-id="099f9-185">在無法移除產品或應用程式時，繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="099f9-185">Continues installation upon failure to remove a product or application.</span></span>                                              |
| <span data-ttu-id="099f9-186">**msidbUpgradeAttributesVersionMinInclusive**</span><span class="sxs-lookup"><span data-stu-id="099f9-186">**msidbUpgradeAttributesVersionMinInclusive**</span></span> | <span data-ttu-id="099f9-187">256</span><span class="sxs-lookup"><span data-stu-id="099f9-187">256</span></span>     | <span data-ttu-id="099f9-188">0x100</span><span class="sxs-lookup"><span data-stu-id="099f9-188">0x100</span></span>       | <span data-ttu-id="099f9-189">偵測版本的範圍，包括 VersionMin 中的值。</span><span class="sxs-lookup"><span data-stu-id="099f9-189">Detects the range of versions including the value in VersionMin.</span></span>                                                     |
| <span data-ttu-id="099f9-190">**msidbUpgradeAttributesVersionMaxInclusive**</span><span class="sxs-lookup"><span data-stu-id="099f9-190">**msidbUpgradeAttributesVersionMaxInclusive**</span></span> | <span data-ttu-id="099f9-191">512</span><span class="sxs-lookup"><span data-stu-id="099f9-191">512</span></span>     | <span data-ttu-id="099f9-192">0x200</span><span class="sxs-lookup"><span data-stu-id="099f9-192">0x200</span></span>       | <span data-ttu-id="099f9-193">偵測版本的範圍，包括 VersionMax 中的值。</span><span class="sxs-lookup"><span data-stu-id="099f9-193">Detects the range of versions including the value in VersionMax.</span></span>                                                     |
| <span data-ttu-id="099f9-194">**msidbUpgradeAttributesLanguagesExclusive**</span><span class="sxs-lookup"><span data-stu-id="099f9-194">**msidbUpgradeAttributesLanguagesExclusive**</span></span>  | <span data-ttu-id="099f9-195">1024</span><span class="sxs-lookup"><span data-stu-id="099f9-195">1024</span></span>    | <span data-ttu-id="099f9-196">0x400</span><span class="sxs-lookup"><span data-stu-id="099f9-196">0x400</span></span>       | <span data-ttu-id="099f9-197">偵測語言資料行中所列語言以外的所有語言。</span><span class="sxs-lookup"><span data-stu-id="099f9-197">Detects all languages, excluding the languages listed in the Language column.</span></span>                                        |



 

</dd> <dt>

<span data-ttu-id="099f9-198"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>刪除</span><span class="sxs-lookup"><span data-stu-id="099f9-198"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>Remove</span></span>
</dt> <dd>

<span data-ttu-id="099f9-199">安裝程式會將 [ [**移除**](remove.md) ] 屬性設定為此資料行中指定的功能。</span><span class="sxs-lookup"><span data-stu-id="099f9-199">The installer sets the [**REMOVE**](remove.md) property to features specified in this column.</span></span> <span data-ttu-id="099f9-200">您可以在執行時間判斷要移除的功能。</span><span class="sxs-lookup"><span data-stu-id="099f9-200">The features to be removed can be determined at run time.</span></span> <span data-ttu-id="099f9-201">在此欄位中輸入的 [格式化](formatted.md) 字串必須評估為功能名稱的逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="099f9-201">The [Formatted](formatted.md) string entered in this field must evaluate to a comma-delimited list of feature names.</span></span> <span data-ttu-id="099f9-202">例如： \[ Feature1 \] 、 \[ Feature2 \] 、 \[ Feature3 \] 。</span><span class="sxs-lookup"><span data-stu-id="099f9-202">For example: \[Feature1\],\[Feature2\],\[Feature3\].</span></span> <span data-ttu-id="099f9-203">如果欄位包含的格式化文字會評估為空字串 ( "" ) ，則不會移除任何功能。</span><span class="sxs-lookup"><span data-stu-id="099f9-203">No features are removed if the field contains formatted text that evaluates to an empty string ("").</span></span> <span data-ttu-id="099f9-204">只有當 [移除] 欄位是空的時，安裝程式才會設定 REMOVE = ALL。</span><span class="sxs-lookup"><span data-stu-id="099f9-204">The installer sets REMOVE=ALL only if the Remove field is empty.</span></span> <span data-ttu-id="099f9-205">請注意空字串與空白欄位之間的差異。</span><span class="sxs-lookup"><span data-stu-id="099f9-205">Note the difference between an empty string and empty field.</span></span> <span data-ttu-id="099f9-206">如果欄位是空的，則為 null。</span><span class="sxs-lookup"><span data-stu-id="099f9-206">If the field is empty, it is null.</span></span>

</dd> <dt>

<span data-ttu-id="099f9-207"><span id="ActionProperty"></span><span id="actionproperty"></span><span id="ACTIONPROPERTY"></span>ActionProperty</span><span class="sxs-lookup"><span data-stu-id="099f9-207"><span id="ActionProperty"></span><span id="actionproperty"></span><span id="ACTIONPROPERTY"></span>ActionProperty</span></span>
</dt> <dd>

<span data-ttu-id="099f9-208">當 [FindRelatedProducts](findrelatedproducts-action.md) 動作偵測到安裝在系統上的相關產品時，會將產品程式碼附加至此欄位中指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="099f9-208">When the [FindRelatedProducts](findrelatedproducts-action.md) action detects a related product installed on the system, it appends the product code to the property specified in this field.</span></span> <span data-ttu-id="099f9-209">在此資料行中指定的屬性必須是公用屬性，而且封裝作者必須將屬性加入至 [**SecureCustomProperties**](securecustomproperties.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="099f9-209">The property specified in this column must be a public property and the package author must add the property to the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span> <span data-ttu-id="099f9-210">升級資料表中的每個資料列都必須有唯一的 ActionProperty 值。</span><span class="sxs-lookup"><span data-stu-id="099f9-210">Each row in the Upgrade table must have a unique ActionProperty value.</span></span> <span data-ttu-id="099f9-211">FindRelatedProducts 之後，此屬性的值為清單產品代碼，並以分號分隔 (; ) ，在系統上偵測到。</span><span class="sxs-lookup"><span data-stu-id="099f9-211">After FindRelatedProducts, the value of this property is a list product codes, separated by semicolons (;), detected on the system.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="099f9-212">驗證</span><span class="sxs-lookup"><span data-stu-id="099f9-212">Validation</span></span>

<dl>

[<span data-ttu-id="099f9-213">ICE03</span><span class="sxs-lookup"><span data-stu-id="099f9-213">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="099f9-214">ICE06</span><span class="sxs-lookup"><span data-stu-id="099f9-214">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="099f9-215">ICE46</span><span class="sxs-lookup"><span data-stu-id="099f9-215">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="099f9-216">ICE61</span><span class="sxs-lookup"><span data-stu-id="099f9-216">ICE61</span></span>](ice61.md)  
[<span data-ttu-id="099f9-217">ICE66</span><span class="sxs-lookup"><span data-stu-id="099f9-217">ICE66</span></span>](ice66.md)  
</dl>

 

 



