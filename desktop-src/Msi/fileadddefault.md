---
description: FILEADDDEFAULT 屬性的值是以逗號分隔的檔案索引鍵清單，會安裝在其預設設定中。
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: FILEADDDEFAULT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c1afc9658c58b048c4e75232d7e550acb36e57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985972"
---
# <a name="fileadddefault-property"></a><span data-ttu-id="a0cd5-103">FILEADDDEFAULT 屬性</span><span class="sxs-lookup"><span data-stu-id="a0cd5-103">FILEADDDEFAULT property</span></span>

<span data-ttu-id="a0cd5-104">**FILEADDDEFAULT** 屬性的值是以逗號分隔的檔案索引鍵清單，會安裝在其預設設定中。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-104">The value of the **FILEADDDEFAULT** property is a list of file keys delimited by commas that are installed in their default configuration.</span></span> <span data-ttu-id="a0cd5-105">針對清單中的每個檔案機碼，安裝程式會決定控制該檔案的元件，並安裝需要最少磁碟空間的功能。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-105">For each file key in the list, the installer determines the component that controls that file and installs the feature that requires the least disk space.</span></span> <span data-ttu-id="a0cd5-106">清單中的檔案索引鍵必須存在於 [file](file-table.md) 資料表的 file 資料行中。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="a0cd5-107">某項功能的安裝狀態與使用者要求安裝時所需的功能相同。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="a0cd5-108">狀態是由 [功能資料表](feature-table.md)的 [屬性] 資料行中的功能所設定的位，以及 [元件資料表](component-table.md)的 [屬性] 資料行中的功能元件所設定的位所決定。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0cd5-109">備註</span><span class="sxs-lookup"><span data-stu-id="a0cd5-109">Remarks</span></span>

<span data-ttu-id="a0cd5-110">請注意，檔案索引鍵名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-110">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="a0cd5-111">另請注意，如果在 [元件資料表的 [屬性](component-table.md) ] 資料行中設定 SourceOnly 位旗標，則元件會安裝成從來源執行。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-111">Also note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="a0cd5-112">安裝程式一律會依下列順序評估下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-112">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="a0cd5-113">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-113">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="a0cd5-114">**刪除**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-114">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="a0cd5-115">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-115">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="a0cd5-116">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-116">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="a0cd5-117">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-117">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="a0cd5-118">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-118">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="a0cd5-119">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-119">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="a0cd5-120">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-120">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="a0cd5-121">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-121">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="a0cd5-122">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-122">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="a0cd5-123">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-123">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. <span data-ttu-id="a0cd5-124">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a0cd5-124">**FILEADDDEFAULT**</span></span>

<span data-ttu-id="a0cd5-125">例如，如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 MyFeature 設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-125">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="a0cd5-126">如果命令列是： ADDSOURCE = ALL、ADDLOCAL = MyFeature、first MyFeature 設定為 run-local，則當 ADDSOURCE = ALL 進行評估時，包括 MyFeature) 在內的所有 (功能都會重設為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="a0cd5-127">安裝程式在停用的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0cd5-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0cd5-128">Requirements</span></span>



| <span data-ttu-id="a0cd5-129">需求</span><span class="sxs-lookup"><span data-stu-id="a0cd5-129">Requirement</span></span> | <span data-ttu-id="a0cd5-130">值</span><span class="sxs-lookup"><span data-stu-id="a0cd5-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0cd5-131">版本</span><span class="sxs-lookup"><span data-stu-id="a0cd5-131">Version</span></span><br/> | <span data-ttu-id="a0cd5-132">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a0cd5-133">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a0cd5-134">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a0cd5-135">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="a0cd5-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a0cd5-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0cd5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0cd5-137">屬性</span><span class="sxs-lookup"><span data-stu-id="a0cd5-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




