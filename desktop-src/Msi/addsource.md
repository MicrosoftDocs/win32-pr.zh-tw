---
description: ADDSOURCE 屬性的值是以逗號分隔的功能清單，會安裝成從來源執行。
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: ADDSOURCE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd51d6f86060def1a7536134a0041f1e15178a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996317"
---
# <a name="addsource-property"></a><span data-ttu-id="d7bcc-103">ADDSOURCE 屬性</span><span class="sxs-lookup"><span data-stu-id="d7bcc-103">ADDSOURCE property</span></span>

<span data-ttu-id="d7bcc-104">**ADDSOURCE** 屬性的值是以逗號分隔的功能清單，會安裝成從來源執行。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-104">The value of the **ADDSOURCE** property is a list of features that are delimited by commas, and are to be installed to run from the source.</span></span> <span data-ttu-id="d7bcc-105">功能必須出現在 [功能資料表](feature-table.md)的功能資料行中。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="d7bcc-106">若要安裝從來源執行的所有功能，請在命令列上使用 ADDSOURCE = ALL。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-106">To install all features as run from source, use ADDSOURCE=ALL on the command line.</span></span> <span data-ttu-id="d7bcc-107">請勿將 ADDSOURCE = 全部輸入至 [屬性工作表](property-table.md)，因為這會產生無法正確移除的來源來源封裝。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-107">Do not enter ADDSOURCE=ALL into the [Property Table](property-table.md), because this generates a run-from-source package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7bcc-108">備註</span><span class="sxs-lookup"><span data-stu-id="d7bcc-108">Remarks</span></span>

<span data-ttu-id="d7bcc-109">功能名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-109">The feature names are case sensitive.</span></span> <span data-ttu-id="d7bcc-110">如果在清單中功能元件的 [元件資料表](component-table.md) 的 [屬性] 資料行中設定 LocalOnly 位旗標，該元件就會安裝在本機執行。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-110">If the LocalOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed to run locally.</span></span>

<span data-ttu-id="d7bcc-111">安裝程式一律會依下列順序評估下列屬性：</span><span class="sxs-lookup"><span data-stu-id="d7bcc-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="d7bcc-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="d7bcc-113">**刪除**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-113">**REMOVE**</span></span>](remove.md)
3.  <span data-ttu-id="d7bcc-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-114">**ADDSOURCE**</span></span>
4.  [<span data-ttu-id="d7bcc-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="d7bcc-116">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="d7bcc-117">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="d7bcc-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="d7bcc-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="d7bcc-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="d7bcc-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="d7bcc-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="d7bcc-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d7bcc-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="d7bcc-124">例如：</span><span class="sxs-lookup"><span data-stu-id="d7bcc-124">For example:</span></span>

-   <span data-ttu-id="d7bcc-125">如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = **MyFeature**，則所有功能都會先設定為執行本機，然後 **MyFeature** 設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="d7bcc-126">如果命令列是： ADDSOURCE = ALL、ADDLOCAL =**MyFeature**、first **MyFeature** 設定為 run-LOCAL，則當 ADDSOURCE = ALL 進行評估時，包括 **MyFeature**) 在內的所有 (功能都會重設為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="d7bcc-127">安裝程式在暫停的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7bcc-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7bcc-128">Requirements</span></span>



| <span data-ttu-id="d7bcc-129">需求</span><span class="sxs-lookup"><span data-stu-id="d7bcc-129">Requirement</span></span> | <span data-ttu-id="d7bcc-130">值</span><span class="sxs-lookup"><span data-stu-id="d7bcc-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bcc-131">版本</span><span class="sxs-lookup"><span data-stu-id="d7bcc-131">Version</span></span><br/> | <span data-ttu-id="d7bcc-132">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d7bcc-133">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d7bcc-134">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d7bcc-135">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="d7bcc-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7bcc-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7bcc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bcc-137">屬性</span><span class="sxs-lookup"><span data-stu-id="d7bcc-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




