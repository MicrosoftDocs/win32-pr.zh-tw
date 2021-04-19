---
description: FILEADDLOCAL 屬性的值代表要安裝以從本機來源媒體執行的逗號分隔檔案索引鍵清單。
ms.assetid: 89ae876e-53f0-4c1d-ba16-7513af79ee5e
title: FILEADDLOCAL 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e3e05a35e5bcd4fc672a2feb6bd2f40619bfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000674"
---
# <a name="fileaddlocal-property"></a><span data-ttu-id="29976-103">FILEADDLOCAL 屬性</span><span class="sxs-lookup"><span data-stu-id="29976-103">FILEADDLOCAL property</span></span>

<span data-ttu-id="29976-104">**FILEADDLOCAL** 屬性的值代表要安裝以從本機來源媒體執行的逗號分隔檔案索引鍵清單。</span><span class="sxs-lookup"><span data-stu-id="29976-104">The value of the **FILEADDLOCAL** property denotes a list of file keys delimited by commas that are to be installed to run from the local source media.</span></span> <span data-ttu-id="29976-105">針對清單中的每個檔案機碼，安裝程式會決定控制該檔案的元件，然後檢查 [FeatureComponents](featurecomponents-table.md) 資料表連結至該元件的所有功能，並安裝需要最少量磁碟空間的功能。</span><span class="sxs-lookup"><span data-stu-id="29976-105">For each file key in the list, the installer determines the component that controls that file, then examines all features linked to that component by the [FeatureComponents](featurecomponents-table.md) table and installs the feature that requires the least amount of disk space.</span></span> <span data-ttu-id="29976-106">清單中的檔案索引鍵必須存在於 [file](file-table.md) 資料表的 file 資料行中。</span><span class="sxs-lookup"><span data-stu-id="29976-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="29976-107">備註</span><span class="sxs-lookup"><span data-stu-id="29976-107">Remarks</span></span>

<span data-ttu-id="29976-108">請注意，檔案索引鍵名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="29976-108">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="29976-109">另請注意，如果在 [元件資料表的 [屬性](component-table.md) ] 資料行中設定 LocalOnly 位旗標，則會將元件安裝在本機執行。</span><span class="sxs-lookup"><span data-stu-id="29976-109">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="29976-110">安裝程式一律會依下列順序評估下列屬性。</span><span class="sxs-lookup"><span data-stu-id="29976-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="29976-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="29976-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="29976-112">**刪除**</span><span class="sxs-lookup"><span data-stu-id="29976-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="29976-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="29976-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="29976-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="29976-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="29976-115">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="29976-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="29976-116">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="29976-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="29976-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="29976-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="29976-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="29976-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="29976-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="29976-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. <span data-ttu-id="29976-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="29976-120">**FILEADDLOCAL**</span></span>
11. [<span data-ttu-id="29976-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="29976-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="29976-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="29976-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="29976-123">例如，如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 MyFeature 設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="29976-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="29976-124">如果命令列是： ADDSOURCE = ALL、ADDLOCAL = MyFeature、first MyFeature 設定為 run-local，則當 ADDSOURCE = ALL 進行評估時，包括 MyFeature) 在內的所有 (功能都會重設為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="29976-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="29976-125">安裝程式在停用的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。</span><span class="sxs-lookup"><span data-stu-id="29976-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="29976-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="29976-126">Requirements</span></span>



| <span data-ttu-id="29976-127">需求</span><span class="sxs-lookup"><span data-stu-id="29976-127">Requirement</span></span> | <span data-ttu-id="29976-128">值</span><span class="sxs-lookup"><span data-stu-id="29976-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29976-129">版本</span><span class="sxs-lookup"><span data-stu-id="29976-129">Version</span></span><br/> | <span data-ttu-id="29976-130">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="29976-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="29976-131">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="29976-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="29976-132">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="29976-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="29976-133">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="29976-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29976-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29976-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29976-135">屬性</span><span class="sxs-lookup"><span data-stu-id="29976-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




