---
description: ADDLOCAL 屬性的值是以逗號分隔，且要在本機安裝的功能清單。
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: ADDLOCAL 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9618389d6e409829dce1eb7bb3a38c1269a2e06d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996510"
---
# <a name="addlocal-property"></a><span data-ttu-id="83606-103">ADDLOCAL 屬性</span><span class="sxs-lookup"><span data-stu-id="83606-103">ADDLOCAL property</span></span>

<span data-ttu-id="83606-104">**ADDLOCAL** 屬性的值是以逗號分隔，且要在本機安裝的功能清單。</span><span class="sxs-lookup"><span data-stu-id="83606-104">The value of the **ADDLOCAL** property is a list of features that are delimited by commas, and are to be installed locally.</span></span> <span data-ttu-id="83606-105">功能必須出現在 [功能資料表](feature-table.md)的功能資料行中。</span><span class="sxs-lookup"><span data-stu-id="83606-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="83606-106">若要在本機安裝所有功能，請在命令列上使用 ADDLOCAL = ALL。</span><span class="sxs-lookup"><span data-stu-id="83606-106">To install all features locally, use ADDLOCAL=ALL on the command line.</span></span> <span data-ttu-id="83606-107">請勿將 ADDLOCAL = 全部輸入至 [屬性工作表](property-table.md)，因為這樣會產生無法正確移除的本機安裝套件。</span><span class="sxs-lookup"><span data-stu-id="83606-107">Do not enter ADDLOCAL=ALL into the [Property Table](property-table.md), because this generates a locally installed package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="83606-108">備註</span><span class="sxs-lookup"><span data-stu-id="83606-108">Remarks</span></span>

<span data-ttu-id="83606-109">功能名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="83606-109">Feature names are case sensitive.</span></span> <span data-ttu-id="83606-110">如果在清單中功能元件的 [元件資料表](component-table.md) 的 [屬性] 資料行中設定 SourceOnly 位旗標，該元件會安裝為 [從來源執行]。</span><span class="sxs-lookup"><span data-stu-id="83606-110">If the SourceOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed as run from source.</span></span>

<span data-ttu-id="83606-111">安裝程式一律會依下列順序評估下列屬性：</span><span class="sxs-lookup"><span data-stu-id="83606-111">The installer always evaluates the following properties in the following order:</span></span>

1.  <span data-ttu-id="83606-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="83606-112">**ADDLOCAL**</span></span>
2.  [<span data-ttu-id="83606-113">**刪除**</span><span class="sxs-lookup"><span data-stu-id="83606-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="83606-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="83606-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="83606-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="83606-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="83606-116">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="83606-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="83606-117">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="83606-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="83606-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="83606-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="83606-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="83606-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="83606-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="83606-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="83606-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="83606-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="83606-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="83606-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="83606-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="83606-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="83606-124">例如：</span><span class="sxs-lookup"><span data-stu-id="83606-124">For example:</span></span>

-   <span data-ttu-id="83606-125">如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = **MyFeature**，則所有功能都會先設定為執行本機，然後 **MyFeature** 設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="83606-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="83606-126">如果命令列是： ADDSOURCE = ALL、ADDLOCAL =**MyFeature**、first **MyFeature** 設定為 run-LOCAL，則當 ADDSOURCE = ALL 進行評估時，包括 **MyFeature**) 在內的所有 (功能都會重設為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="83606-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="83606-127">安裝程式在暫停的安裝期間，或在命令列上指定任何先前的屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。</span><span class="sxs-lookup"><span data-stu-id="83606-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the previous properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="83606-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="83606-128">Requirements</span></span>



| <span data-ttu-id="83606-129">需求</span><span class="sxs-lookup"><span data-stu-id="83606-129">Requirement</span></span> | <span data-ttu-id="83606-130">值</span><span class="sxs-lookup"><span data-stu-id="83606-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83606-131">版本</span><span class="sxs-lookup"><span data-stu-id="83606-131">Version</span></span><br/> | <span data-ttu-id="83606-132">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="83606-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="83606-133">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="83606-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="83606-134">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="83606-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="83606-135">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="83606-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83606-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83606-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83606-137">屬性</span><span class="sxs-lookup"><span data-stu-id="83606-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




