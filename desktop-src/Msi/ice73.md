---
description: ICE73 會確認您的套件未重複使用封裝程式碼、升級程式碼或 Windows Installer SDK 範例的產品代碼。 套件永遠不應該重複使用另一個產品的封裝、升級或產品代碼。
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac0e192f7c2ab7fb6f6236e45e0e4da70157e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998466"
---
# <a name="ice73"></a><span data-ttu-id="c039d-104">ICE73</span><span class="sxs-lookup"><span data-stu-id="c039d-104">ICE73</span></span>

<span data-ttu-id="c039d-105">ICE73 會確認您的套件未重複使用封裝程式碼、升級程式碼或 Windows Installer SDK 範例的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="c039d-105">ICE73 verifies that your package does not reuse package codes, upgrade codes, or product codes of the Windows Installer SDK samples.</span></span> <span data-ttu-id="c039d-106">套件永遠不應該重複使用另一個產品的封裝、升級或產品代碼。</span><span class="sxs-lookup"><span data-stu-id="c039d-106">Packages should never reuse the package, upgrade, or product codes of another product.</span></span>

## <a name="result"></a><span data-ttu-id="c039d-107">結果</span><span class="sxs-lookup"><span data-stu-id="c039d-107">Result</span></span>

<span data-ttu-id="c039d-108">如果您的產品套件重複使用 Windows Installer SDK 範例的封裝或產品代碼，ICE73 會輸出警告。</span><span class="sxs-lookup"><span data-stu-id="c039d-108">ICE73 outputs a warning if your product's package reuses a package or product code of a Windows Installer SDK sample.</span></span>

## <a name="example"></a><span data-ttu-id="c039d-109">範例</span><span class="sxs-lookup"><span data-stu-id="c039d-109">Example</span></span>

<span data-ttu-id="c039d-110">ICE73 會針對所顯示的範例報告下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="c039d-110">ICE73 reports the following errors for the example shown:</span></span>

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> <span data-ttu-id="c039d-111">GUID 中的星號 (\* \* \* \*) 代表針對後續 Windows Installer SDK 套件保留的 guid 範圍。</span><span class="sxs-lookup"><span data-stu-id="c039d-111">The asterisks (\*\*\*\*) in the GUID represent the range of GUIDs reserved for subsequent Windows Installer SDK packages.</span></span>

 

<span data-ttu-id="c039d-112">若要修正錯誤，請針對套件的產品和套件代碼產生新的唯一 GUID。</span><span class="sxs-lookup"><span data-stu-id="c039d-112">To fix the errors, generate a new unique GUID for your package's product and package codes.</span></span> <span data-ttu-id="c039d-113">您也需要套件升級程式碼的新唯一 GUID。</span><span class="sxs-lookup"><span data-stu-id="c039d-113">You will also need a new unique GUID for your package's upgrade code.</span></span>

<span data-ttu-id="c039d-114">[摘要資訊串流](summary-information-stream.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="c039d-114">[Summary Information Stream](summary-information-stream.md) (partial)</span></span>



| <span data-ttu-id="c039d-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c039d-115">Property</span></span>       | <span data-ttu-id="c039d-116">值</span><span class="sxs-lookup"><span data-stu-id="c039d-116">Value</span></span>                                  |
|----------------|----------------------------------------|
| <span data-ttu-id="c039d-117">PID \_ REVNUMBER</span><span class="sxs-lookup"><span data-stu-id="c039d-117">PID\_REVNUMBER</span></span> | <span data-ttu-id="c039d-118">{000C1101-0000-0000-C000-000000000047}</span><span class="sxs-lookup"><span data-stu-id="c039d-118">{000C1101-0000-0000-C000-000000000047}</span></span> |



 

<span data-ttu-id="c039d-119">[屬性工作表](property-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="c039d-119">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="c039d-120">屬性</span><span class="sxs-lookup"><span data-stu-id="c039d-120">Property</span></span>                           | <span data-ttu-id="c039d-121">值</span><span class="sxs-lookup"><span data-stu-id="c039d-121">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| [<span data-ttu-id="c039d-122">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="c039d-122">**ProductCode**</span></span>](productcode.md) | <span data-ttu-id="c039d-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span><span class="sxs-lookup"><span data-stu-id="c039d-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span></span> |
| [<span data-ttu-id="c039d-124">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="c039d-124">**UpgradeCode**</span></span>](upgradecode.md) | <span data-ttu-id="c039d-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span><span class="sxs-lookup"><span data-stu-id="c039d-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c039d-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="c039d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c039d-127">封裝碼</span><span class="sxs-lookup"><span data-stu-id="c039d-127">Package Codes</span></span>](package-codes.md)
</dt> <dt>

[<span data-ttu-id="c039d-128">產品代碼</span><span class="sxs-lookup"><span data-stu-id="c039d-128">Product Codes</span></span>](product-codes.md)
</dt> <dt>

[<span data-ttu-id="c039d-129">**修訂編號摘要屬性**</span><span class="sxs-lookup"><span data-stu-id="c039d-129">**Revision Number Summary Property**</span></span>](revision-number-summary.md)
</dt> <dt>

[<span data-ttu-id="c039d-130">**UpgradeCode 屬性**</span><span class="sxs-lookup"><span data-stu-id="c039d-130">**UpgradeCode Property**</span></span>](upgradecode.md)
</dt> <dt>

[<span data-ttu-id="c039d-131">**ProductCode 屬性**</span><span class="sxs-lookup"><span data-stu-id="c039d-131">**ProductCode Property**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="c039d-132">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="c039d-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



