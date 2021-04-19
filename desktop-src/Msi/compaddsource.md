---
description: COMPADDSOURCE 屬性的值是從元件資料表的 [元件] 資料行（以逗號分隔）的元件 Guid 清單，將會安裝成從來源媒體執行。
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: COMPADDSOURCE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f59526196a75599dbd2a535db6dcda4fb733936
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997686"
---
# <a name="compaddsource-property"></a><span data-ttu-id="c976c-103">COMPADDSOURCE 屬性</span><span class="sxs-lookup"><span data-stu-id="c976c-103">COMPADDSOURCE property</span></span>

<span data-ttu-id="c976c-104">**COMPADDSOURCE** 屬性的值是從 [元件](component-table.md)資料表的 [元件] 資料行（以逗號分隔）的元件 guid 清單，將會安裝成從來源媒體執行。</span><span class="sxs-lookup"><span data-stu-id="c976c-104">The value of the **COMPADDSOURCE** property is a list of component GUIDs from the ComponentId column of the [Component](component-table.md) table, delimited by commas, that are to be installed to run from the source media.</span></span> <span data-ttu-id="c976c-105">安裝程式會根據指定的元件，使用此值來判斷哪些功能已設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="c976c-105">The installer uses this value to determine which features are set to be installed to run from source, based on the specified components.</span></span> <span data-ttu-id="c976c-106">針對每個列出的元件識別碼，安裝程式會透過 [FeatureComponents](featurecomponents-table.md) 資料表檢查連結 (的所有功能) 至該元件，並安裝需要最少磁碟空間才能安裝的功能。</span><span class="sxs-lookup"><span data-stu-id="c976c-106">For each listed component ID, the installer examines all features linked (through the [FeatureComponents](featurecomponents-table.md) table) to that component, and installs the feature that requires the least amount of disk space to install.</span></span> <span data-ttu-id="c976c-107">列出的元件必須存在於 [元件](component-table.md) 資料表的元件資料行中。</span><span class="sxs-lookup"><span data-stu-id="c976c-107">The components listed must be present in the Component column of the [Component](component-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="c976c-108">備註</span><span class="sxs-lookup"><span data-stu-id="c976c-108">Remarks</span></span>

<span data-ttu-id="c976c-109">請注意，元件名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c976c-109">Note that the component names are case-sensitive.</span></span> <span data-ttu-id="c976c-110">另請注意，如果在 [元件資料表的 [屬性](component-table.md) ] 資料行中設定 LocalOnly 位旗標，則會將元件安裝在本機執行。</span><span class="sxs-lookup"><span data-stu-id="c976c-110">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="c976c-111">安裝程式一律會依下列順序評估下列屬性：</span><span class="sxs-lookup"><span data-stu-id="c976c-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="c976c-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="c976c-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="c976c-113">**刪除**</span><span class="sxs-lookup"><span data-stu-id="c976c-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="c976c-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="c976c-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="c976c-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c976c-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="c976c-116">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="c976c-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="c976c-117">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="c976c-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="c976c-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="c976c-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  <span data-ttu-id="c976c-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="c976c-119">**COMPADDSOURCE**</span></span>
9.  [<span data-ttu-id="c976c-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c976c-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="c976c-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="c976c-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="c976c-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="c976c-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="c976c-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c976c-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="c976c-124">例如，如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 MyFeature 設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="c976c-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="c976c-125">如果命令列是： ADDSOURCE = ALL、ADDLOCAL = MyFeature、first MyFeature 設定為 run-local，則當 ADDSOURCE = ALL 進行評估時，包括 MyFeature) 在內的所有 (功能都會重設為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="c976c-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="c976c-126">安裝程式在停用的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。</span><span class="sxs-lookup"><span data-stu-id="c976c-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="c976c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c976c-127">Requirements</span></span>



| <span data-ttu-id="c976c-128">需求</span><span class="sxs-lookup"><span data-stu-id="c976c-128">Requirement</span></span> | <span data-ttu-id="c976c-129">值</span><span class="sxs-lookup"><span data-stu-id="c976c-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c976c-130">版本</span><span class="sxs-lookup"><span data-stu-id="c976c-130">Version</span></span><br/> | <span data-ttu-id="c976c-131">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c976c-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c976c-132">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c976c-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c976c-133">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="c976c-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c976c-134">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="c976c-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c976c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c976c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c976c-136">屬性</span><span class="sxs-lookup"><span data-stu-id="c976c-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




