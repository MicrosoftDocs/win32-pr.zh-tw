---
description: 識別用來數位簽署修補程式的可能簽署者憑證。
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: MsiPatchCertificate 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01648e792931fd856a1231a5d876c7db843479df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026876"
---
# <a name="msipatchcertificate-table"></a><span data-ttu-id="e23cc-103">MsiPatchCertificate 資料表</span><span class="sxs-lookup"><span data-stu-id="e23cc-103">MsiPatchCertificate Table</span></span>

<span data-ttu-id="e23cc-104">MsiPatchCertificate 資料表會識別用來數位簽署修補程式的可能簽署者憑證。</span><span class="sxs-lookup"><span data-stu-id="e23cc-104">The MsiPatchCertificate Table identifies the possible signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="e23cc-105">MsiPatchCertificate 資料表包含啟用應用程式的 [使用者帳戶控制 (UAC) 修補](user-account-control--uac--patching.md) 所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="e23cc-105">The MsiPatchCertificate Table contains the information that is needed to enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for an application.</span></span>

<span data-ttu-id="e23cc-106">MsiPatchCertificate 資料表具有下列資料行：</span><span class="sxs-lookup"><span data-stu-id="e23cc-106">The MsiPatchCertificate Table has the following columns:</span></span>



| <span data-ttu-id="e23cc-107">Column</span><span class="sxs-lookup"><span data-stu-id="e23cc-107">Column</span></span>               | <span data-ttu-id="e23cc-108">類型</span><span class="sxs-lookup"><span data-stu-id="e23cc-108">Type</span></span>                         | <span data-ttu-id="e23cc-109">答案</span><span class="sxs-lookup"><span data-stu-id="e23cc-109">Key</span></span> | <span data-ttu-id="e23cc-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="e23cc-110">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="e23cc-111">PatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e23cc-111">PatchCertificate</span></span>     | [<span data-ttu-id="e23cc-112">識別碼</span><span class="sxs-lookup"><span data-stu-id="e23cc-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="e23cc-113">Y</span><span class="sxs-lookup"><span data-stu-id="e23cc-113">Y</span></span>   | <span data-ttu-id="e23cc-114">N</span><span class="sxs-lookup"><span data-stu-id="e23cc-114">N</span></span>        |
| <span data-ttu-id="e23cc-115">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="e23cc-115">DigitalCertificate\_</span></span> | [<span data-ttu-id="e23cc-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="e23cc-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="e23cc-117">N</span><span class="sxs-lookup"><span data-stu-id="e23cc-117">N</span></span>   | <span data-ttu-id="e23cc-118">N</span><span class="sxs-lookup"><span data-stu-id="e23cc-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e23cc-119">資料行</span><span class="sxs-lookup"><span data-stu-id="e23cc-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e23cc-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e23cc-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span></span>
</dt> <dd>

<span data-ttu-id="e23cc-121">MsiPatchCertificate 資料表中這個資料列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e23cc-121">The unique identifier for this row in the MsiPatchCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="e23cc-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="e23cc-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="e23cc-123">[MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e23cc-123">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="e23cc-124">MsiDigitalCertificate 資料表中指出的資料列包含簽署者憑證的二進位標記法。</span><span class="sxs-lookup"><span data-stu-id="e23cc-124">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e23cc-125">備註</span><span class="sxs-lookup"><span data-stu-id="e23cc-125">Remarks</span></span>

<span data-ttu-id="e23cc-126">在套用修補程式時，一律會針對目前的 MsiPatchCertificate 資料表評估修補程式。</span><span class="sxs-lookup"><span data-stu-id="e23cc-126">Patches are always evaluated against the MsiPatchCertificate Table that is current at the time the patch is applied.</span></span> <span data-ttu-id="e23cc-127">Patch 可以藉由新增或移除專案來修改 MsiPatchCertificate 資料表。</span><span class="sxs-lookup"><span data-stu-id="e23cc-127">A patch can modify the MsiPatchCertificate Table by adding or removing entries.</span></span> <span data-ttu-id="e23cc-128">這可讓修補程式修改稍後在修補順序中套用的未來修補程式評估。</span><span class="sxs-lookup"><span data-stu-id="e23cc-128">This enables a patch to modify the evaluation of future patches that are applied later in the patching sequence.</span></span> <span data-ttu-id="e23cc-129">資料表中可以有多個憑證，且修補程式必須至少符合一個要套用的憑證。</span><span class="sxs-lookup"><span data-stu-id="e23cc-129">Multiple certificates can exist in the table, and the patch must match at least one certificate to be applied.</span></span>

## <a name="validation"></a><span data-ttu-id="e23cc-130">驗證</span><span class="sxs-lookup"><span data-stu-id="e23cc-130">Validation</span></span>

<dl>

[<span data-ttu-id="e23cc-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="e23cc-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e23cc-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="e23cc-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e23cc-133">ICE32</span><span class="sxs-lookup"><span data-stu-id="e23cc-133">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e23cc-134">ICE81</span><span class="sxs-lookup"><span data-stu-id="e23cc-134">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="e23cc-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="e23cc-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e23cc-136">DisableLUAPatching</span><span class="sxs-lookup"><span data-stu-id="e23cc-136">DisableLUAPatching</span></span>](disableluapatching.md)
</dt> <dt>

[<span data-ttu-id="e23cc-137"> (UAC) 修補的使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="e23cc-137">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
</dt> <dt>

[<span data-ttu-id="e23cc-138">**MSIDISABLELUAPATCHING**</span><span class="sxs-lookup"><span data-stu-id="e23cc-138">**MSIDISABLELUAPATCHING**</span></span>](msidisableluapatching.md)
</dt> <dt>

[<span data-ttu-id="e23cc-139">數位簽章和 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e23cc-139">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="e23cc-140">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="e23cc-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



