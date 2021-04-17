---
description: MsiPackageCertificate 資料表會列出數位簽章憑證，用來驗證讓此 Multiple-Package 安裝的安裝套件身分識別。
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: MsiPackageCertificate 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195276"
---
# <a name="msipackagecertificate-table"></a><span data-ttu-id="fd538-103">MsiPackageCertificate 資料表</span><span class="sxs-lookup"><span data-stu-id="fd538-103">MsiPackageCertificate Table</span></span>

<span data-ttu-id="fd538-104">MsiPackageCertificate 資料表會列出用來驗證安裝封裝之身分識別的數位簽章憑證，以進行 [多套件安裝](multiple-package-installations.md)。</span><span class="sxs-lookup"><span data-stu-id="fd538-104">The MsiPackageCertificate Table lists digital signature certificates used to verify the identity of the installation packages that make this [Multiple-Package Installation](multiple-package-installations.md).</span></span>

<span data-ttu-id="fd538-105">您可以使用此資料表，針對包含多個 Windows Installer 套件的產品，撰寫 [多套件安裝](multiple-package-installations.md) 。</span><span class="sxs-lookup"><span data-stu-id="fd538-105">Use this table to author a [multiple-package installation](multiple-package-installations.md) for a product containing multiple Windows Installer packages.</span></span> <span data-ttu-id="fd538-106">如果第一個封裝經過數位簽署，而包含的 MsiPackageCertificate 資料表指定產品中所有其餘套件的數位憑證，則系統管理員只需要針對第一個套件顯示 (UAC) 提示字元，接受 [*使用者帳戶控制*](u-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="fd538-106">If the first package is digitally signed, and contains a MsiPackageCertificate Table specifying digital certificates for all the remaining packages in the product, the administrator needs only accept the [*User Account Control*](u-gly.md) (UAC) prompt displayed for the first package.</span></span> <span data-ttu-id="fd538-107">在接受 UAC 的第一個封裝提示之後， [MsiEmbeddedChainer 資料表](msiembeddedchainer-table.md) 中的使用者定義函數接著可以將其餘套件加入多套件安裝，而不需要顯示 UAC 提示字元，而且需要每個套件的系統管理員回應。</span><span class="sxs-lookup"><span data-stu-id="fd538-107">After accepting the UAC's prompt for the first package, the user-defined functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) can then join the remaining packages to the multiple-package installation without displaying a UAC prompt and requiring an administrator response for each package.</span></span>

<span data-ttu-id="fd538-108">如果 [MsiEmbeddedChainer 資料表](msiembeddedchainer-table.md) 中的一或多個函式要求未簽署的封裝，則會針對每個未簽署的套件顯示另一個需要系統管理員互動的 UAC 提示。</span><span class="sxs-lookup"><span data-stu-id="fd538-108">If one or more of the functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) request an unsigned package, another UAC prompt requiring administrator interaction is displayed for each unsigned package.</span></span> <span data-ttu-id="fd538-109">如果系統管理員接受此 UAC 提示，則會繼續執行多套件安裝。</span><span class="sxs-lookup"><span data-stu-id="fd538-109">If the administrator accepts this UAC prompt, the multi-package installation continues.</span></span> <span data-ttu-id="fd538-110">系統管理員為套件提供認證之後，在此多套件安裝期間不會再顯示該套件的任何 UAC 提示。</span><span class="sxs-lookup"><span data-stu-id="fd538-110">Once an administrator has provided credentials for a package, no UAC prompt will again be displayed for that package during this multi-package installation.</span></span> <span data-ttu-id="fd538-111">如果系統管理員拒絕封裝的 UAC 提示，Windows installer 會在認可安裝任何屬於產品的封裝之前，回復多套件安裝。</span><span class="sxs-lookup"><span data-stu-id="fd538-111">If the administrator rejects a UAC prompt for a package, the Windows installer rolls back the multi-package installation before it commits to install any packages belonging to the product.</span></span>

<span data-ttu-id="fd538-112">**[Windows Installer 4.0 或更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="fd538-112">**[Windows Installer 4.0 or earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="fd538-113">從 Windows Installer 4.5 開始，可以使用此資料表。</span><span class="sxs-lookup"><span data-stu-id="fd538-113">This table is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="fd538-114">MsiPackageCertificate 資料表具有下列資料行：</span><span class="sxs-lookup"><span data-stu-id="fd538-114">The MsiPackageCertificate Table has the following columns:</span></span>



| <span data-ttu-id="fd538-115">Column</span><span class="sxs-lookup"><span data-stu-id="fd538-115">Column</span></span>               | <span data-ttu-id="fd538-116">類型</span><span class="sxs-lookup"><span data-stu-id="fd538-116">Type</span></span>                         | <span data-ttu-id="fd538-117">答案</span><span class="sxs-lookup"><span data-stu-id="fd538-117">Key</span></span> | <span data-ttu-id="fd538-118">Nullable</span><span class="sxs-lookup"><span data-stu-id="fd538-118">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="fd538-119">PackageCertificate</span><span class="sxs-lookup"><span data-stu-id="fd538-119">PackageCertificate</span></span>   | [<span data-ttu-id="fd538-120">識別碼</span><span class="sxs-lookup"><span data-stu-id="fd538-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="fd538-121">Y</span><span class="sxs-lookup"><span data-stu-id="fd538-121">Y</span></span>   | <span data-ttu-id="fd538-122">N</span><span class="sxs-lookup"><span data-stu-id="fd538-122">N</span></span>        |
| <span data-ttu-id="fd538-123">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="fd538-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="fd538-124">識別碼</span><span class="sxs-lookup"><span data-stu-id="fd538-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="fd538-125">N</span><span class="sxs-lookup"><span data-stu-id="fd538-125">N</span></span>   | <span data-ttu-id="fd538-126">N</span><span class="sxs-lookup"><span data-stu-id="fd538-126">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fd538-127">資料行</span><span class="sxs-lookup"><span data-stu-id="fd538-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fd538-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span><span class="sxs-lookup"><span data-stu-id="fd538-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span></span>
</dt> <dd>

<span data-ttu-id="fd538-129">MsiPackageCertificate 資料表中這個資料列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd538-129">The unique identifier for this row in the MsiPackageCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="fd538-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="fd538-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="fd538-131">[MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fd538-131">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="fd538-132">MsiDigitalCertificate 資料表中指出的資料列包含簽署者憑證的二進位標記法。</span><span class="sxs-lookup"><span data-stu-id="fd538-132">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="fd538-133">驗證</span><span class="sxs-lookup"><span data-stu-id="fd538-133">Validation</span></span>

<dl>

[<span data-ttu-id="fd538-134">ICE39</span><span class="sxs-lookup"><span data-stu-id="fd538-134">ICE39</span></span>](ice39.md)  
[<span data-ttu-id="fd538-135">ICE81</span><span class="sxs-lookup"><span data-stu-id="fd538-135">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="fd538-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd538-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd538-137">MsiEmbeddedChainer</span><span class="sxs-lookup"><span data-stu-id="fd538-137">MsiEmbeddedChainer</span></span>](msiembeddedchainer-table.md)
</dt> <dt>

[<span data-ttu-id="fd538-138">MsiDigitalCertificate 資料表</span><span class="sxs-lookup"><span data-stu-id="fd538-138">MsiDigitalCertificate Table</span></span>](msidigitalcertificate-table.md)
</dt> </dl>

 

 



