---
description: COMPADDDEFAULT 屬性的值是元件資料表的 [元件] 資料行中的元件 Guid 清單（以逗號分隔），會安裝在其預設設定中。
ms.assetid: 1bf05680-fcba-4fbb-8f8c-4203a90346ce
title: COMPADDDEFAULT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e96d2259f0610a3030e79f8685c498a0fb2d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989767"
---
# <a name="compadddefault-property"></a><span data-ttu-id="085f9-103">COMPADDDEFAULT 屬性</span><span class="sxs-lookup"><span data-stu-id="085f9-103">COMPADDDEFAULT property</span></span>

<span data-ttu-id="085f9-104">**COMPADDDEFAULT** 屬性的值是元件 [資料表](component-table.md)的 [元件] 資料行中的元件 guid 清單（以逗號分隔），會安裝在其預設設定中。</span><span class="sxs-lookup"><span data-stu-id="085f9-104">The value of the **COMPADDDEFAULT** property is a list of component GUIDs from the ComponentId column of the [Component table](component-table.md), delimited by commas, that are installed in their default configuration.</span></span> <span data-ttu-id="085f9-105">針對清單中的每個元件識別碼，安裝程式會安裝需要最少磁碟空間的功能。</span><span class="sxs-lookup"><span data-stu-id="085f9-105">For each component ID in the list, the installer installs the feature that requires the least disk space.</span></span> <span data-ttu-id="085f9-106">清單中的元件識別碼必須存在於 [元件資料表](component-table.md)的 [元件識別碼] 資料行中。</span><span class="sxs-lookup"><span data-stu-id="085f9-106">The component IDs in the list must be present in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="085f9-107">某項功能的安裝狀態與使用者要求安裝時所需的功能相同。</span><span class="sxs-lookup"><span data-stu-id="085f9-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="085f9-108">狀態是由 [功能資料表](feature-table.md)的 [屬性] 資料行中的功能所設定的位，以及元件資料表的 [屬性] 資料行中的功能元件所設定的位所決定。</span><span class="sxs-lookup"><span data-stu-id="085f9-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="085f9-109">備註</span><span class="sxs-lookup"><span data-stu-id="085f9-109">Remarks</span></span>

<span data-ttu-id="085f9-110">請注意，如果在 [元件資料表的 [屬性](component-table.md) ] 資料行中設定 SourceOnly 位旗標，則元件會安裝成從來源執行。</span><span class="sxs-lookup"><span data-stu-id="085f9-110">Note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="085f9-111">安裝程式一律會依下列順序評估下列屬性。</span><span class="sxs-lookup"><span data-stu-id="085f9-111">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="085f9-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="085f9-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="085f9-113">**刪除**</span><span class="sxs-lookup"><span data-stu-id="085f9-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="085f9-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="085f9-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="085f9-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="085f9-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="085f9-116">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="085f9-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="085f9-117">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="085f9-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="085f9-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="085f9-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="085f9-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="085f9-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  <span data-ttu-id="085f9-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="085f9-120">**COMPADDDEFAULT**</span></span>
10. [<span data-ttu-id="085f9-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="085f9-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="085f9-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="085f9-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="085f9-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="085f9-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="085f9-124">例如，如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 MyFeature 設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="085f9-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="085f9-125">如果命令列是： ADDSOURCE = ALL、ADDLOCAL = MyFeature、first MyFeature 設定為 run-local，則當 ADDSOURCE = ALL 進行評估時，包括 MyFeature) 在內的所有 (功能都會重設為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="085f9-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="085f9-126">安裝程式在停用的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。</span><span class="sxs-lookup"><span data-stu-id="085f9-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="085f9-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="085f9-127">Requirements</span></span>



| <span data-ttu-id="085f9-128">需求</span><span class="sxs-lookup"><span data-stu-id="085f9-128">Requirement</span></span> | <span data-ttu-id="085f9-129">值</span><span class="sxs-lookup"><span data-stu-id="085f9-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="085f9-130">版本</span><span class="sxs-lookup"><span data-stu-id="085f9-130">Version</span></span><br/> | <span data-ttu-id="085f9-131">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="085f9-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="085f9-132">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="085f9-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="085f9-133">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="085f9-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="085f9-134">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="085f9-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="085f9-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="085f9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="085f9-136">屬性</span><span class="sxs-lookup"><span data-stu-id="085f9-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




