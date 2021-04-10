---
description: 轉換是套用至安裝的變更集合。 藉由將轉換套用至基底安裝套件，安裝程式可以新增或取代安裝資料庫中的資料。 安裝程式只能在安裝期間套用轉換。
ms.assetid: 1edc5227-70ac-4769-ab7f-67d01031dc33
title: 關於轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbae9f21ec71209116f3c8eadffca20381cfe71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192475"
---
# <a name="about-transforms"></a><span data-ttu-id="325e3-105">關於轉換</span><span class="sxs-lookup"><span data-stu-id="325e3-105">About Transforms</span></span>

<span data-ttu-id="325e3-106">轉換是套用至安裝的變更集合。</span><span class="sxs-lookup"><span data-stu-id="325e3-106">A transform is a collection of changes applied to an installation.</span></span> <span data-ttu-id="325e3-107">藉由將轉換套用至基底安裝套件，安裝程式可以新增或取代安裝資料庫中的資料。</span><span class="sxs-lookup"><span data-stu-id="325e3-107">By applying a transform to a base installation package, the installer can add or replace data in the installation database.</span></span> <span data-ttu-id="325e3-108">安裝程式只能在安裝期間套用轉換。</span><span class="sxs-lookup"><span data-stu-id="325e3-108">The installer can only apply transforms during an installation.</span></span>

<span data-ttu-id="325e3-109">安裝程式會在安裝期間註冊產品所需的轉換清單。</span><span class="sxs-lookup"><span data-stu-id="325e3-109">The installer registers a list of transforms required by the product during the installation.</span></span> <span data-ttu-id="325e3-110">設定或安裝產品時，安裝程式必須將這些轉換套用至產品的安裝套件。</span><span class="sxs-lookup"><span data-stu-id="325e3-110">The installer must apply these transforms to the product's installation package when configuring or installing the product.</span></span> <span data-ttu-id="325e3-111">如果列出的轉換無法使用，且轉換來源復原無法還原，則安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="325e3-111">If a listed transform is unavailable, and if the transform source resiliency cannot restore it, the installation fails.</span></span>

<span data-ttu-id="325e3-112">轉換可以修改 [安裝程式資料庫](installer-database.md)中任何持續性資料表內的資訊。</span><span class="sxs-lookup"><span data-stu-id="325e3-112">A transform can modify information that is in any persistent table in the [installer database](installer-database.md).</span></span> <span data-ttu-id="325e3-113">轉換也可以新增或移除安裝程式資料庫中的持續性資料表。</span><span class="sxs-lookup"><span data-stu-id="325e3-113">A transform can also add or remove persistent tables in the installer database.</span></span> <span data-ttu-id="325e3-114">轉換無法修改不在資料庫資料表中之安裝封裝的任何部分，例如 [摘要資訊資料流程](summary-information-stream.md)中的資訊、substorages 中的資訊，或是內嵌封包中的檔案。</span><span class="sxs-lookup"><span data-stu-id="325e3-114">Transforms cannot modify any part of an installation package that is not in a database table, such as information in the [summary information stream](summary-information-stream.md), information in substorages, or files in embedded cabinets.</span></span>

<span data-ttu-id="325e3-115">轉換具有可包含驗證條件和錯誤條件的摘要資訊串流。</span><span class="sxs-lookup"><span data-stu-id="325e3-115">Transforms have a summary information stream that can contain validation conditions and error conditions.</span></span> <span data-ttu-id="325e3-116">您可以使用 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) 函式，將轉換驗證和錯誤條件新增至摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="325e3-116">The transform validation and error conditions can be added to the summary information using the [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) function.</span></span> <span data-ttu-id="325e3-117">驗證條件可控制安裝程式是否可以將轉換套用至指定的安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="325e3-117">The validation conditions control whether the installer can apply the transform to a given installation database.</span></span> <span data-ttu-id="325e3-118">轉換的驗證可以根據在轉換中指定的 [**UpgradeCode**](upgradecode.md)、 [**ProductCode**](productcode.md)、 [**ProductVersion**](productversion.md) 和 [**ProductLanguage**](productlanguage.md) 屬性值，以及安裝資料庫中的屬性來進行。</span><span class="sxs-lookup"><span data-stu-id="325e3-118">Validation of the transform can be conditioned upon the values of the [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md) and [**ProductLanguage**](productlanguage.md) properties specified in the transform and those in the installation database.</span></span> <span data-ttu-id="325e3-119">轉換錯誤條件可控制套用轉換時要隱藏的錯誤。</span><span class="sxs-lookup"><span data-stu-id="325e3-119">The transform error conditions control which errors get suppressed when the transform is applied.</span></span> <span data-ttu-id="325e3-120">轉換中包含的錯誤條件會由使用 [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) 和 [**ApplyTransform**](database-applytransform.md) 方法指定的錯誤條件覆寫。</span><span class="sxs-lookup"><span data-stu-id="325e3-120">The error conditions included within the transform are overridden by the error conditions specified using the [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) and [**ApplyTransform**](database-applytransform.md) methods.</span></span>

> [!Note]  
> <span data-ttu-id="325e3-121">一般的自訂轉換不會有驗證條件或針對 [**ProductCode**](productcode.md)進行驗證。</span><span class="sxs-lookup"><span data-stu-id="325e3-121">Typical customization transforms have no validation conditions or validate against the [**ProductCode**](productcode.md).</span></span> <span data-ttu-id="325e3-122">存放在 [修補程式套件](patch-packages.md) 內的轉換通常會有嚴格的驗證條件，以確保將正確的轉換套用至修補程式目標。</span><span class="sxs-lookup"><span data-stu-id="325e3-122">The transforms stored within [patch packages](patch-packages.md) generally have strict validation conditions to ensure that the correct transform is applied to the patch target.</span></span>

 

<span data-ttu-id="325e3-123">有三種類型的 Windows Installer 轉換：</span><span class="sxs-lookup"><span data-stu-id="325e3-123">There are three types of Windows Installer transforms:</span></span>

-   [<span data-ttu-id="325e3-124">內嵌轉換</span><span class="sxs-lookup"><span data-stu-id="325e3-124">Embedded Transforms</span></span>](embedded-transforms.md)
-   [<span data-ttu-id="325e3-125">安全的轉換</span><span class="sxs-lookup"><span data-stu-id="325e3-125">Secured Transforms</span></span>](secured-transforms.md)
-   [<span data-ttu-id="325e3-126">不安全的轉換</span><span class="sxs-lookup"><span data-stu-id="325e3-126">Unsecured Transforms</span></span>](unsecured-transforms.md)

 

 



