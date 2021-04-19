---
description: 重新安裝屬性的值是以逗號分隔的功能清單，這些功能是以要重新安裝的逗號分隔。 列出的功能必須存在於功能資料表的 [功能] 資料行中。 若要重新安裝所有功能，請使用命令列上的 [重新安裝 = 全部]。
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: 重新安裝屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976093"
---
# <a name="reinstall-property"></a><span data-ttu-id="1bbf9-105">重新安裝屬性</span><span class="sxs-lookup"><span data-stu-id="1bbf9-105">REINSTALL property</span></span>

<span data-ttu-id="1bbf9-106">**重新安裝** 屬性的值是以逗號分隔的功能清單，這些功能是以要重新安裝的逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-106">The value of the **REINSTALL** property is a list of features delimited by commas that are to be reinstalled.</span></span> <span data-ttu-id="1bbf9-107">列出的功能必須存在於 [功能](feature-table.md) 資料表的 [功能] 資料行中。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-107">The features listed must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="1bbf9-108">若要重新安裝所有功能，請使用命令列上的 [重新安裝 = 全部]。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-108">To reinstall all features use REINSTALL=ALL on the command line.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bbf9-109">備註</span><span class="sxs-lookup"><span data-stu-id="1bbf9-109">Remarks</span></span>

<span data-ttu-id="1bbf9-110">請注意，功能名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-110">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="1bbf9-111">如果已設定 [ **重新安裝** ] 屬性，則也應該設定 [**REINSTALLMODE**](reinstallmode.md) 屬性，以指出要執行的重新安裝類型。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-111">If the **REINSTALL** property is set, the [**REINSTALLMODE**](reinstallmode.md) property should also be set, to indicate the type of reinstall to be performed.</span></span> <span data-ttu-id="1bbf9-112">如果未設定 **REINSTALLMODE** 屬性，則根據預設，如果目前安裝的檔案是較小的版本 (或不存在) ，則預設會重新安裝目前安裝的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-112">If the **REINSTALLMODE** property is not set, then by default all files that are currently installed are reinstalled, IF the currently installed file is a lesser version (or is not present).</span></span> <span data-ttu-id="1bbf9-113">依預設，不會重新寫入任何登錄專案。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-113">By default, no registry entries are rewritten.</span></span>

<span data-ttu-id="1bbf9-114">請注意，即使 **重新安裝** 已設定為 [全部]，也只會重新安裝先前已安裝的功能。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-114">Note that even if **REINSTALL** is set to ALL, only those features that were already installed previously are reinstalled.</span></span> <span data-ttu-id="1bbf9-115">因此，如果已針對尚未安裝的產品設定 **重新安裝** ，則完全不會進行任何安裝動作。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-115">Thus, if **REINSTALL** is set for a product that is yet to be installed, no installation action will take place at all.</span></span>

<span data-ttu-id="1bbf9-116">安裝程式一律會依下列順序評估下列屬性：</span><span class="sxs-lookup"><span data-stu-id="1bbf9-116">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="1bbf9-117">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="1bbf9-117">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="1bbf9-118">**刪除**</span><span class="sxs-lookup"><span data-stu-id="1bbf9-118">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="1bbf9-119">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="1bbf9-119">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="1bbf9-120">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1bbf9-120">**ADDDEFAULT**</span></span>](adddefault.md)
5.  <span data-ttu-id="1bbf9-121">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="1bbf9-121">**REINSTALL**</span></span>
6.  [<span data-ttu-id="1bbf9-122">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="1bbf9-122">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="1bbf9-123">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="1bbf9-123">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="1bbf9-124">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="1bbf9-124">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="1bbf9-125">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="1bbf9-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
10. [<span data-ttu-id="1bbf9-126">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="1bbf9-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
11. [<span data-ttu-id="1bbf9-127">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1bbf9-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="1bbf9-128">例如，如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 MyFeature 設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-128">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="1bbf9-129">如果命令列是： ADDSOURCE = ALL、ADDLOCAL = MyFeature、first MyFeature 設定為 run-local，則當 ADDSOURCE = ALL 進行評估時，包括 MyFeature) 在內的所有 (功能都會重設為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-129">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="1bbf9-130">安裝程式在停用的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bbf9-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bbf9-131">Requirements</span></span>



| <span data-ttu-id="1bbf9-132">需求</span><span class="sxs-lookup"><span data-stu-id="1bbf9-132">Requirement</span></span> | <span data-ttu-id="1bbf9-133">值</span><span class="sxs-lookup"><span data-stu-id="1bbf9-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bbf9-134">版本</span><span class="sxs-lookup"><span data-stu-id="1bbf9-134">Version</span></span><br/> | <span data-ttu-id="1bbf9-135">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1bbf9-136">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1bbf9-137">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1bbf9-138">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="1bbf9-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1bbf9-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bbf9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bbf9-140">屬性</span><span class="sxs-lookup"><span data-stu-id="1bbf9-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




