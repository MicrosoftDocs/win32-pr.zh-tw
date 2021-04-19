---
description: ICE61 會驗證 Windows Installer 資料庫的升級資料表。
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979920"
---
# <a name="ice61"></a><span data-ttu-id="04cf2-103">ICE61</span><span class="sxs-lookup"><span data-stu-id="04cf2-103">ICE61</span></span>

<span data-ttu-id="04cf2-104">ICE61 會檢查升級資料表，以確定下列條件成立：</span><span class="sxs-lookup"><span data-stu-id="04cf2-104">ICE61 checks the upgrade table to ensure that the following conditions are true:</span></span>

-   <span data-ttu-id="04cf2-105">所有 ActionProperty 屬性都不是在屬性工作表中預先撰寫的。</span><span class="sxs-lookup"><span data-stu-id="04cf2-105">All ActionProperty properties are not pre-authored in the Property table.</span></span>
-   <span data-ttu-id="04cf2-106">所有 ActionProperty 屬性都是公用屬性。</span><span class="sxs-lookup"><span data-stu-id="04cf2-106">All ActionProperty properties are Public Properties.</span></span>
-   <span data-ttu-id="04cf2-107">所有 ActionProperty 屬性都包含在 [**SecureCustomProperties**](securecustomproperties.md) 屬性中。</span><span class="sxs-lookup"><span data-stu-id="04cf2-107">All ActionProperty properties are included in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>
-   <span data-ttu-id="04cf2-108">所有 ActionProperty 屬性對升級資料表中的每一筆記錄而言是唯一的。</span><span class="sxs-lookup"><span data-stu-id="04cf2-108">All ActionProperty properties are unique to each record in the Upgrade table.</span></span>
-   <span data-ttu-id="04cf2-109">所有 VersionMax 值都不小於對應的 VersionMin 值。</span><span class="sxs-lookup"><span data-stu-id="04cf2-109">All VersionMax values are not less than the corresponding VersionMin values.</span></span>
-   <span data-ttu-id="04cf2-110">VersionMin 和 VersionMax 值都是有效的產品版本。</span><span class="sxs-lookup"><span data-stu-id="04cf2-110">VersionMin and VersionMax values are valid product versions.</span></span> <span data-ttu-id="04cf2-111">如需有效的產品版本格式，請參閱 [**ProductVersion**](productversion.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="04cf2-111">See the [**ProductVersion**](productversion.md) property for the valid product version format.</span></span>
-   <span data-ttu-id="04cf2-112">不嘗試移除目前產品的較新或相同版本。</span><span class="sxs-lookup"><span data-stu-id="04cf2-112">No attempt is made to remove a newer or equal version of the current product.</span></span>

<span data-ttu-id="04cf2-113">若無法修正 ICE61 回報的警告或錯誤，通常會導致升級應用程式時發生問題。</span><span class="sxs-lookup"><span data-stu-id="04cf2-113">Failure to fix a warning or error reported by ICE61 generally leads to problems in upgrading your application.</span></span> <span data-ttu-id="04cf2-114">視確切的錯誤而定，這可能是因為新的應用程式需要離開舊版本的檔案、從較舊版本刪除檔案，或升級完成失敗的任何事項。</span><span class="sxs-lookup"><span data-stu-id="04cf2-114">Depending on the exact error, this could be anything from leaving files from the older version behind, deleting files from the older version even though they are needed by the new application, or complete failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="04cf2-115">結果</span><span class="sxs-lookup"><span data-stu-id="04cf2-115">Result</span></span>

<span data-ttu-id="04cf2-116">如果上述任何條件不成立，ICE61 會張貼警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="04cf2-116">ICE61 posts a warning or error if any of the above conditions are not true.</span></span>

## <a name="example"></a><span data-ttu-id="04cf2-117">範例</span><span class="sxs-lookup"><span data-stu-id="04cf2-117">Example</span></span>

<span data-ttu-id="04cf2-118">ICE61 會針對所顯示的範例報告下列錯誤和警告。</span><span class="sxs-lookup"><span data-stu-id="04cf2-118">ICE61 reports the following errors and warning for the examples shown.</span></span>

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

<span data-ttu-id="04cf2-119">在此情況下，第一個資料列會嘗試移除相同版本的產品。</span><span class="sxs-lookup"><span data-stu-id="04cf2-119">In this case, the first row would try to remove a product of the same version.</span></span> <span data-ttu-id="04cf2-120"> (的 VersionMax 資料行等於屬性工作表) 中的產品版本。</span><span class="sxs-lookup"><span data-stu-id="04cf2-120">(VersionMax column is equal to the product version in the Property table).</span></span>

<span data-ttu-id="04cf2-121">若要修正這個錯誤，請使用 VersionMax 資料行中的版本低於屬性工作表中指定的目前版本。</span><span class="sxs-lookup"><span data-stu-id="04cf2-121">To fix this error, use a version in the VersionMax column lower than the current version specified in the Property table.</span></span> <span data-ttu-id="04cf2-122">如果 VersionMax 等於目前的版本，請從 [屬性] 資料行中移除 **msidbUpgradeAttributesVersionMaxInclusive** 位。</span><span class="sxs-lookup"><span data-stu-id="04cf2-122">Remove the **msidbUpgradeAttributesVersionMaxInclusive** bit from the Attributes column if the VersionMax is equal to the current version.</span></span> <span data-ttu-id="04cf2-123">如果目的只是要偵測產品而不移除它，則將 **msidbUpgradeAttributesOnlyDetect** 位新增至 [屬性] 欄也會修正這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="04cf2-123">If the intent is only to detect the product and not remove it, adding the **msidbUpgradeAttributesOnlyDetect** bit to the Attributes column will also fix this error.</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

<span data-ttu-id="04cf2-124">除非在 [**SecureCustomProperties**](securecustomproperties.md) 屬性中列出屬性，否則在找到屬性時，不會將屬性傳遞至安裝的伺服器端。</span><span class="sxs-lookup"><span data-stu-id="04cf2-124">Unless the property is listed in the [**SecureCustomProperties**](securecustomproperties.md) property, the property is not passed to the server side of the install when the property is found.</span></span>

<span data-ttu-id="04cf2-125">若要修正這個錯誤，請將屬性新增至 [**SecureCustomProperties**](securecustomproperties.md)。</span><span class="sxs-lookup"><span data-stu-id="04cf2-125">To fix this error, add the property to [**SecureCustomProperties**](securecustomproperties.md).</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

<span data-ttu-id="04cf2-126">升級屬性必須是公用屬性，才能將結果傳遞給安裝的伺服器端。</span><span class="sxs-lookup"><span data-stu-id="04cf2-126">Upgrade properties must be public properties for the result to be passed to the server side of the installation.</span></span>

<span data-ttu-id="04cf2-127">若要修正這個錯誤，請在屬性名稱中使用所有大寫字母。</span><span class="sxs-lookup"><span data-stu-id="04cf2-127">To fix this error, use all uppercase letters in the property name.</span></span>

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

<span data-ttu-id="04cf2-128">屬性只能用於升級資料表的一個資料列。</span><span class="sxs-lookup"><span data-stu-id="04cf2-128">A property can only be used in one row of the Upgrade table.</span></span>

<span data-ttu-id="04cf2-129">若要修正這個錯誤，請針對第二個數據列使用不同的屬性。</span><span class="sxs-lookup"><span data-stu-id="04cf2-129">To fix this error, use a different property for the second row.</span></span>

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

<span data-ttu-id="04cf2-130">最小版本必須小於最大版本。</span><span class="sxs-lookup"><span data-stu-id="04cf2-130">The minimum version must be less than the maximum version.</span></span>

<span data-ttu-id="04cf2-131">若要修正這個錯誤，請檢查您的版本號碼是否出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="04cf2-131">To fix this error, check your version numbers for typos.</span></span> <span data-ttu-id="04cf2-132">如果是正確的，而且您想要使用兩個版本之間的範圍，請將它們切換成使 VersionMin 小於 VersionMax。</span><span class="sxs-lookup"><span data-stu-id="04cf2-132">If they are correct and you want to use the range between the two versions, switch them so that VersionMin is less than VersionMax.</span></span>

[<span data-ttu-id="04cf2-133">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="04cf2-133">Property Table</span></span>](property-table.md)



| <span data-ttu-id="04cf2-134">屬性</span><span class="sxs-lookup"><span data-stu-id="04cf2-134">Property</span></span>                                                 | <span data-ttu-id="04cf2-135">值</span><span class="sxs-lookup"><span data-stu-id="04cf2-135">Value</span></span>                                  |
|----------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="04cf2-136">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="04cf2-136">**UpgradeCode**</span></span>](upgradecode.md)                       | <span data-ttu-id="04cf2-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="04cf2-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |
| [<span data-ttu-id="04cf2-138">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="04cf2-138">**ProductVersion**</span></span>](productversion.md)                 | <span data-ttu-id="04cf2-139">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="04cf2-139">2.01.0000</span></span>                              |
| [<span data-ttu-id="04cf2-140">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="04cf2-140">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="04cf2-141">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="04cf2-141">OLDAPPFOUND</span></span>                            |



 

[<span data-ttu-id="04cf2-142">升級資料表</span><span class="sxs-lookup"><span data-stu-id="04cf2-142">Upgrade Table</span></span>](upgrade-table.md)



| <span data-ttu-id="04cf2-143">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="04cf2-143">UpgradeCode</span></span>                            | <span data-ttu-id="04cf2-144">VersionMin</span><span class="sxs-lookup"><span data-stu-id="04cf2-144">VersionMin</span></span> | <span data-ttu-id="04cf2-145">VersionMax</span><span class="sxs-lookup"><span data-stu-id="04cf2-145">VersionMax</span></span> | <span data-ttu-id="04cf2-146">語言</span><span class="sxs-lookup"><span data-stu-id="04cf2-146">Language</span></span> | <span data-ttu-id="04cf2-147">屬性</span><span class="sxs-lookup"><span data-stu-id="04cf2-147">Attributes</span></span> | <span data-ttu-id="04cf2-148">移除</span><span class="sxs-lookup"><span data-stu-id="04cf2-148">Remove</span></span>                | <span data-ttu-id="04cf2-149">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="04cf2-149">ActionProperty</span></span>  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| <span data-ttu-id="04cf2-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="04cf2-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |            | <span data-ttu-id="04cf2-151">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="04cf2-151">2.01.0000</span></span>  |          | <span data-ttu-id="04cf2-152">513</span><span class="sxs-lookup"><span data-stu-id="04cf2-152">513</span></span>        |                       | <span data-ttu-id="04cf2-153">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="04cf2-153">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="04cf2-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="04cf2-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> | <span data-ttu-id="04cf2-155">2.01.0001</span><span class="sxs-lookup"><span data-stu-id="04cf2-155">2.01.0001</span></span>  | <span data-ttu-id="04cf2-156">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="04cf2-156">2.01.0000</span></span>  |          |            |                       | <span data-ttu-id="04cf2-157">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="04cf2-157">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="04cf2-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span><span class="sxs-lookup"><span data-stu-id="04cf2-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span></span> | <span data-ttu-id="04cf2-159">1.00.0000</span><span class="sxs-lookup"><span data-stu-id="04cf2-159">1.00.0000</span></span>  | <span data-ttu-id="04cf2-160">2.00.0000</span><span class="sxs-lookup"><span data-stu-id="04cf2-160">2.00.0000</span></span>  | <span data-ttu-id="04cf2-161">1033</span><span class="sxs-lookup"><span data-stu-id="04cf2-161">1033</span></span>     |            | <span data-ttu-id="04cf2-162">\[AppFeatureEnglish\]</span><span class="sxs-lookup"><span data-stu-id="04cf2-162">\[AppFeatureEnglish\]</span></span> | <span data-ttu-id="04cf2-163">EnglishAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="04cf2-163">EnglishAPPFOUND</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="04cf2-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="04cf2-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04cf2-165">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="04cf2-165">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



