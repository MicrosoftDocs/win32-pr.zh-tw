---
description: 這是每部電腦的系統原則，可用來在小型更新和次要升級期間套用升級元件規則。
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944427"
---
# <a name="enforceupgradecomponentrules"></a><span data-ttu-id="cf1a5-103">EnforceUpgradeComponentRules</span><span class="sxs-lookup"><span data-stu-id="cf1a5-103">EnforceUpgradeComponentRules</span></span>

<span data-ttu-id="cf1a5-104">這是每部電腦的 [系統原則](system-policy.md) ，可用來在 [小型更新](small-updates.md) 和 [次要升級](minor-upgrades.md)期間套用升級元件規則。</span><span class="sxs-lookup"><span data-stu-id="cf1a5-104">This is a per-machine [system policy](system-policy.md) that can be used to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md).</span></span>

<span data-ttu-id="cf1a5-105">將 EnforceUpgradeComponentRules 原則設定為1，在 [小型更新](small-updates.md) 和電腦上所有產品的 [次要升級](minor-upgrades.md) 期間，套用升級元件規則。</span><span class="sxs-lookup"><span data-stu-id="cf1a5-105">Set the EnforceUpgradeComponentRules policy to 1 to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of all products on the computer.</span></span> <span data-ttu-id="cf1a5-106">若要在小型更新和特定產品的次要升級期間套用規則，請在命令列上或在 [屬性工作表](property-table.md)中，將 [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="cf1a5-106">To apply the rules during small updates and minor upgrades of a particular product, set the [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) property to 1 on the command line or in the [Property table](property-table.md).</span></span>

<span data-ttu-id="cf1a5-107">當屬性或原則設定為1時， [小更新](small-updates.md) 和 [次要升級](minor-upgrades.md) 可能會失敗，因為更新會嘗試執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="cf1a5-107">When the property or policy has been set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update attempts to do the following:</span></span>

-   <span data-ttu-id="cf1a5-108">將新功能新增至現有功能樹狀結構的頂端或中間。</span><span class="sxs-lookup"><span data-stu-id="cf1a5-108">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="cf1a5-109">新的功能必須新增為現有功能樹狀目錄的新分葉功能。</span><span class="sxs-lookup"><span data-stu-id="cf1a5-109">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="cf1a5-110">在此情況下，產品的 [**ProductCode**](productcode.md) 可以變更，而且可以將更新視為 [主要升級](major-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="cf1a5-110">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="cf1a5-111">從功能移除元件。</span><span class="sxs-lookup"><span data-stu-id="cf1a5-111">Remove a component from a feature.</span></span>

    <span data-ttu-id="cf1a5-112">如果您變更元件的 GUID，也可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="cf1a5-112">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="cf1a5-113">原始 GUID 所識別的元件會被移除，而新 GUID 所識別的元件會顯示為新的元件。</span><span class="sxs-lookup"><span data-stu-id="cf1a5-113">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="cf1a5-114">**Windows Installer 4.5 和更新版本：** 您可以藉由在 [元件資料表](component-table.md)中設定 **msidbComponentAttributesUninstallOnSupersedence** 屬性，或設定 [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)屬性，以正確地移除元件，方法是使用 Windows Installer 4.5 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="cf1a5-114">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 or later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="cf1a5-115">或者，您可以變更產品的 [**ProductCode**](productcode.md) ，也可以將更新視為 [主要升級](major-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="cf1a5-115">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="cf1a5-116">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="cf1a5-116">Registry Key</span></span>

<span data-ttu-id="cf1a5-117">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="cf1a5-117">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="cf1a5-118">資料類型</span><span class="sxs-lookup"><span data-stu-id="cf1a5-118">Data Type</span></span>

<span data-ttu-id="cf1a5-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cf1a5-119">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf1a5-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="cf1a5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf1a5-121">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="cf1a5-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



