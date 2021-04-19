---
description: Msitran.exe 使用 MsiDatabaseGenerateTransform、MsiCreateTransformSummaryInfo 和 MsiDatabaseApplyTransform 來產生或套用轉換檔案。此工具僅適用于 Windows Installer 開發人員的 Windows SDK 元件。
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983820"
---
# <a name="msitranexe"></a><span data-ttu-id="cd007-103">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="cd007-103">Msitran.exe</span></span>

<span data-ttu-id="cd007-104">Msitran.exe 使用 [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)、 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)和 [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) 來產生或套用轉換檔案。</span><span class="sxs-lookup"><span data-stu-id="cd007-104">Msitran.exe uses [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa), and [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) to generate or apply a transform file.</span></span>

<span data-ttu-id="cd007-105">此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="cd007-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd007-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd007-106">Syntax</span></span>

<span data-ttu-id="cd007-107">使用下列語法來產生轉換。</span><span class="sxs-lookup"><span data-stu-id="cd007-107">Use the following syntax to generate a transform.</span></span>

<span data-ttu-id="cd007-108">**msitran.exe-g** *{base db} {ref db} {轉換檔案名} \[ {錯誤條件/驗證條件} \]*</span><span class="sxs-lookup"><span data-stu-id="cd007-108">**msitran -g** *{base db}{ref db}{transform file name}\[{error conditions / validation conditions}\]*</span></span>

<span data-ttu-id="cd007-109">使用下列語法來套用轉換</span><span class="sxs-lookup"><span data-stu-id="cd007-109">Use the following syntax to apply a transform</span></span>

<span data-ttu-id="cd007-110">**msitran.exe-a** *{轉換} {資料庫} \[ {錯誤條件} \]*</span><span class="sxs-lookup"><span data-stu-id="cd007-110">**msitran -a** *{transform}{database}\[{error conditions}\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="cd007-111">命令列選項</span><span class="sxs-lookup"><span data-stu-id="cd007-111">Command Line Options</span></span>

<span data-ttu-id="cd007-112">Msitran.exe 會使用下列不區分大小寫的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="cd007-112">Msitran.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="cd007-113">斜線分隔符號也可以用來取代虛線。</span><span class="sxs-lookup"><span data-stu-id="cd007-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="cd007-114">選項</span><span class="sxs-lookup"><span data-stu-id="cd007-114">Option</span></span> | <span data-ttu-id="cd007-115">Description</span><span class="sxs-lookup"><span data-stu-id="cd007-115">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="cd007-116">-g</span><span class="sxs-lookup"><span data-stu-id="cd007-116">-g</span></span>     | <span data-ttu-id="cd007-117">轉換產生。</span><span class="sxs-lookup"><span data-stu-id="cd007-117">Transform generation.</span></span>  |
| <span data-ttu-id="cd007-118">-a</span><span class="sxs-lookup"><span data-stu-id="cd007-118">-a</span></span>     | <span data-ttu-id="cd007-119">轉換應用程式。</span><span class="sxs-lookup"><span data-stu-id="cd007-119">Transform application.</span></span> |



 

<span data-ttu-id="cd007-120">套用轉換時，可能會隱藏下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd007-120">The following errors may be suppressed when applying a transform.</span></span> <span data-ttu-id="cd007-121">若要隱藏錯誤，請在 {error 條件} 引數中包含適當的字元。</span><span class="sxs-lookup"><span data-stu-id="cd007-121">To suppress an error, include the appropriate character in the {error conditions} argument.</span></span> <span data-ttu-id="cd007-122">以-g 指定的條件會放置在轉換的摘要資訊中，但在使用-a 來套用轉換時不會使用。</span><span class="sxs-lookup"><span data-stu-id="cd007-122">Conditions specified with -g are placed in the summary information of the transform, but are not used when applying a transform with -a.</span></span> <span data-ttu-id="cd007-123">如需詳細資訊，請參閱 [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)。</span><span class="sxs-lookup"><span data-stu-id="cd007-123">For information, see [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span></span>



| <span data-ttu-id="cd007-124">選項</span><span class="sxs-lookup"><span data-stu-id="cd007-124">Option</span></span> | <span data-ttu-id="cd007-125">隱藏的錯誤</span><span class="sxs-lookup"><span data-stu-id="cd007-125">Suppressed error</span></span>           |
|--------|----------------------------|
| <span data-ttu-id="cd007-126">a</span><span class="sxs-lookup"><span data-stu-id="cd007-126">a</span></span>      | <span data-ttu-id="cd007-127">加入現有的資料列。</span><span class="sxs-lookup"><span data-stu-id="cd007-127">Add existing row.</span></span>          |
| <span data-ttu-id="cd007-128">b</span><span class="sxs-lookup"><span data-stu-id="cd007-128">b</span></span>      | <span data-ttu-id="cd007-129">刪除不存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="cd007-129">Delete non-existing row.</span></span>   |
| <span data-ttu-id="cd007-130">c</span><span class="sxs-lookup"><span data-stu-id="cd007-130">c</span></span>      | <span data-ttu-id="cd007-131">加入現有的資料表。</span><span class="sxs-lookup"><span data-stu-id="cd007-131">Add existing table.</span></span>        |
| <span data-ttu-id="cd007-132">d</span><span class="sxs-lookup"><span data-stu-id="cd007-132">d</span></span>      | <span data-ttu-id="cd007-133">刪除非現有的資料表。</span><span class="sxs-lookup"><span data-stu-id="cd007-133">Delete non-existing table.</span></span> |
| <span data-ttu-id="cd007-134">e</span><span class="sxs-lookup"><span data-stu-id="cd007-134">e</span></span>      | <span data-ttu-id="cd007-135">修改現有的資料列。</span><span class="sxs-lookup"><span data-stu-id="cd007-135">Modify existing row.</span></span>       |
| <span data-ttu-id="cd007-136">f</span><span class="sxs-lookup"><span data-stu-id="cd007-136">f</span></span>      | <span data-ttu-id="cd007-137">變更字碼頁。</span><span class="sxs-lookup"><span data-stu-id="cd007-137">Change codepage.</span></span>           |



 

<span data-ttu-id="cd007-138">下列驗證條件可用來指出何時可以將轉換套用至封裝。</span><span class="sxs-lookup"><span data-stu-id="cd007-138">The following validation conditions may be used to indicate when a transform may be applied to a package.</span></span> <span data-ttu-id="cd007-139">您可以使用-g 來指定這些條件，但不能指定-a。</span><span class="sxs-lookup"><span data-stu-id="cd007-139">These conditions may be specified with -g, but not -a.</span></span>



| <span data-ttu-id="cd007-140">選項</span><span class="sxs-lookup"><span data-stu-id="cd007-140">Option</span></span> | <span data-ttu-id="cd007-141">驗證條件</span><span class="sxs-lookup"><span data-stu-id="cd007-141">Validation condition</span></span>                                  |
|--------|-------------------------------------------------------|
| <span data-ttu-id="cd007-142">g</span><span class="sxs-lookup"><span data-stu-id="cd007-142">g</span></span>      | <span data-ttu-id="cd007-143">檢查升級程式碼。</span><span class="sxs-lookup"><span data-stu-id="cd007-143">Check upgrade code.</span></span>                                   |
| <span data-ttu-id="cd007-144">l</span><span class="sxs-lookup"><span data-stu-id="cd007-144">l</span></span>      | <span data-ttu-id="cd007-145">檢查語言。</span><span class="sxs-lookup"><span data-stu-id="cd007-145">Check language.</span></span>                                       |
| <span data-ttu-id="cd007-146">p</span><span class="sxs-lookup"><span data-stu-id="cd007-146">p</span></span>      | <span data-ttu-id="cd007-147">檢查平臺。</span><span class="sxs-lookup"><span data-stu-id="cd007-147">Check platform.</span></span>                                       |
| <span data-ttu-id="cd007-148">r</span><span class="sxs-lookup"><span data-stu-id="cd007-148">r</span></span>      | <span data-ttu-id="cd007-149">檢查產品。</span><span class="sxs-lookup"><span data-stu-id="cd007-149">Check product.</span></span>                                        |
| <span data-ttu-id="cd007-150">s</span><span class="sxs-lookup"><span data-stu-id="cd007-150">s</span></span>      | <span data-ttu-id="cd007-151">僅檢查主要版本。</span><span class="sxs-lookup"><span data-stu-id="cd007-151">Check major version only.</span></span>                             |
| <span data-ttu-id="cd007-152">t</span><span class="sxs-lookup"><span data-stu-id="cd007-152">t</span></span>      | <span data-ttu-id="cd007-153">僅檢查主要和次要版本。</span><span class="sxs-lookup"><span data-stu-id="cd007-153">Check major and minor versions only.</span></span>                  |
| <span data-ttu-id="cd007-154">u</span><span class="sxs-lookup"><span data-stu-id="cd007-154">u</span></span>      | <span data-ttu-id="cd007-155">檢查主要、次要和升級版本。</span><span class="sxs-lookup"><span data-stu-id="cd007-155">Check major, minor, and upgrade versions.</span></span>             |
| <span data-ttu-id="cd007-156">v</span><span class="sxs-lookup"><span data-stu-id="cd007-156">v</span></span>      | <span data-ttu-id="cd007-157">應用 < 基底資料庫版本的資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="cd007-157">Applied database version < Base database version.</span></span>  |
| <span data-ttu-id="cd007-158">w</span><span class="sxs-lookup"><span data-stu-id="cd007-158">w</span></span>      | <span data-ttu-id="cd007-159">應用 <的資料庫版本 = 基底資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="cd007-159">Applied database version <= Base database version.</span></span> |
| <span data-ttu-id="cd007-160">x</span><span class="sxs-lookup"><span data-stu-id="cd007-160">x</span></span>      | <span data-ttu-id="cd007-161">套用的資料庫版本 = 基底資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="cd007-161">Applied database version = Base database version.</span></span>     |
| <span data-ttu-id="cd007-162">y</span><span class="sxs-lookup"><span data-stu-id="cd007-162">y</span></span>      | <span data-ttu-id="cd007-163">應用 >的資料庫版本 = 基底資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="cd007-163">Applied database version >= Base database version.</span></span> |
| <span data-ttu-id="cd007-164">z</span><span class="sxs-lookup"><span data-stu-id="cd007-164">z</span></span>      | <span data-ttu-id="cd007-165">應用 > 基底資料庫版本的資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="cd007-165">Applied database version > Base database version.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="cd007-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="cd007-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd007-167">Windows Installer 開發工具</span><span class="sxs-lookup"><span data-stu-id="cd007-167">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="cd007-168">資料庫轉換</span><span class="sxs-lookup"><span data-stu-id="cd007-168">Database Transforms</span></span>](database-transforms.md)
</dt> <dt>

[<span data-ttu-id="cd007-169">自訂轉換範例</span><span class="sxs-lookup"><span data-stu-id="cd007-169">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> <dt>

[<span data-ttu-id="cd007-170">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="cd007-170">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



