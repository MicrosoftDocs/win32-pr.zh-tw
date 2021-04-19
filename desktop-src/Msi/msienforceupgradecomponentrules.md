---
description: 在命令列上或在屬性工作表中，將 MSIENFORCEUPGRADECOMPONENTRULES 屬性設定為1，以便在小型更新和特定產品的次要升級期間套用升級元件規則。
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: MSIENFORCEUPGRADECOMPONENTRULES 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d5946ba3a0001c988ddfe76eeaf95c008205b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992585"
---
# <a name="msienforceupgradecomponentrules-property"></a><span data-ttu-id="14bcb-103">MSIENFORCEUPGRADECOMPONENTRULES 屬性</span><span class="sxs-lookup"><span data-stu-id="14bcb-103">MSIENFORCEUPGRADECOMPONENTRULES property</span></span>

<span data-ttu-id="14bcb-104">在命令列上或在 [屬性工作表](property-table.md)中，將 **MSIENFORCEUPGRADECOMPONENTRULES** 屬性設定為1，以便在 [小型更新](small-updates.md)和特定產品的 [次要升級](minor-upgrades.md)期間套用升級元件規則。</span><span class="sxs-lookup"><span data-stu-id="14bcb-104">Set the **MSIENFORCEUPGRADECOMPONENTRULES** property to 1 on the command line or in the [Property table](property-table.md) to apply the upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of a particular product.</span></span> <span data-ttu-id="14bcb-105">若要在小型更新和電腦上所有產品的次要升級期間套用規則，請將 [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) 原則設定為1。</span><span class="sxs-lookup"><span data-stu-id="14bcb-105">To apply the rules during small updates and minor upgrades of all products on the computer, set the [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) policy to 1.</span></span>

<span data-ttu-id="14bcb-106">當屬性或原則設定為1時， [小更新](small-updates.md) 和 [次要升級](minor-upgrades.md) 可能會失敗，因為更新會嘗試執行下列違反升級元件規則的動作：</span><span class="sxs-lookup"><span data-stu-id="14bcb-106">When the property or policy is set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update tries to do the following that violates the upgrade component rules:</span></span>

-   <span data-ttu-id="14bcb-107">將新功能新增至現有功能樹狀結構的頂端或中間。</span><span class="sxs-lookup"><span data-stu-id="14bcb-107">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="14bcb-108">新的功能必須新增為現有功能樹狀目錄的新分葉功能。</span><span class="sxs-lookup"><span data-stu-id="14bcb-108">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="14bcb-109">在此情況下，產品的 [**ProductCode**](productcode.md) 可以變更，並可將更新視為 [主要升級](major-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="14bcb-109">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="14bcb-110">從功能移除元件。</span><span class="sxs-lookup"><span data-stu-id="14bcb-110">Remove a component from a feature.</span></span>

    <span data-ttu-id="14bcb-111">如果您變更元件的 GUID，也可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="14bcb-111">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="14bcb-112">原始 GUID 所識別的元件會被移除，而新 GUID 所識別的元件會顯示為新的元件。</span><span class="sxs-lookup"><span data-stu-id="14bcb-112">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="14bcb-113">**Windows Installer 4.5 和更新版本：** 您可以藉由在 [元件資料表](component-table.md)中設定 **msidbComponentAttributesUninstallOnSupersedence** 屬性，或設定 [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)屬性，以正確地移除元件，方法是使用 Windows Installer 4.5 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="14bcb-113">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 and later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component Table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="14bcb-114">或者，您可以變更產品的 [**ProductCode**](productcode.md) ，也可以將更新視為 [主要升級](major-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="14bcb-114">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14bcb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="14bcb-115">Requirements</span></span>



| <span data-ttu-id="14bcb-116">需求</span><span class="sxs-lookup"><span data-stu-id="14bcb-116">Requirement</span></span> | <span data-ttu-id="14bcb-117">值</span><span class="sxs-lookup"><span data-stu-id="14bcb-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14bcb-118">版本</span><span class="sxs-lookup"><span data-stu-id="14bcb-118">Version</span></span><br/> | <span data-ttu-id="14bcb-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="14bcb-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="14bcb-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="14bcb-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="14bcb-121">Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="14bcb-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="14bcb-122">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="14bcb-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14bcb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14bcb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14bcb-124">屬性</span><span class="sxs-lookup"><span data-stu-id="14bcb-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="14bcb-125">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="14bcb-125">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




