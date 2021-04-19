---
description: ADDDEFAULT 屬性的值是以逗號分隔的功能清單，這些功能會安裝在其預設設定中。
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: ADDDEFAULT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43960b6d70d704337f373031ab4972bcb95dada7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998746"
---
# <a name="adddefault-property"></a><span data-ttu-id="9010e-103">ADDDEFAULT 屬性</span><span class="sxs-lookup"><span data-stu-id="9010e-103">ADDDEFAULT property</span></span>

<span data-ttu-id="9010e-104">**ADDDEFAULT** 屬性的值是以逗號分隔的功能清單，這些功能會安裝在其預設設定中。</span><span class="sxs-lookup"><span data-stu-id="9010e-104">The value of the **ADDDEFAULT** property is a list of features delimited by commas, which are to be installed in their default configuration.</span></span> <span data-ttu-id="9010e-105">功能必須出現在[功能資料表](feature-table.md)的功能資料行中。</span><span class="sxs-lookup"><span data-stu-id="9010e-105">The features must be present in the Feature column of the [Feature Table.](feature-table.md)</span></span> <span data-ttu-id="9010e-106">若要安裝預設設定中的所有功能，請在命令列上使用 ADDDEFAULT = ALL。</span><span class="sxs-lookup"><span data-stu-id="9010e-106">To install all features in their default configurations, use ADDDEFAULT=ALL on the command line.</span></span>

<span data-ttu-id="9010e-107">**ADDDEFAULT** 屬性中所列的功能會安裝在與使用者要求安裝功能時相同的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="9010e-107">A feature listed in the **ADDDEFAULT** property is installed in the same installation state as if the user requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="9010e-108">狀態是由 [功能資料表](feature-table.md)的 [屬性] 資料行中針對功能所設定的位來決定，而在 [元件資料表](component-table.md)的 [屬性] 資料行中，為功能元件設定的位。</span><span class="sxs-lookup"><span data-stu-id="9010e-108">The state is determined by the bits that are set for the feature in the Attributes column of the [Feature Table](feature-table.md), and which bits are set for the feature components in the Attributes column of the [Component Table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9010e-109">備註</span><span class="sxs-lookup"><span data-stu-id="9010e-109">Remarks</span></span>

<span data-ttu-id="9010e-110">功能名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9010e-110">The feature names are case sensitive.</span></span>

<span data-ttu-id="9010e-111">安裝程式一律會依下列順序評估下列屬性：</span><span class="sxs-lookup"><span data-stu-id="9010e-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="9010e-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9010e-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="9010e-113">**刪除**</span><span class="sxs-lookup"><span data-stu-id="9010e-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="9010e-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9010e-114">**ADDSOURCE**</span></span>](addsource.md)
4.  <span data-ttu-id="9010e-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9010e-115">**ADDDEFAULT**</span></span>
5.  [<span data-ttu-id="9010e-116">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="9010e-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="9010e-117">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="9010e-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="9010e-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9010e-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="9010e-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9010e-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="9010e-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9010e-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="9010e-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9010e-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="9010e-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9010e-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="9010e-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9010e-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="9010e-124">例如：</span><span class="sxs-lookup"><span data-stu-id="9010e-124">For example:</span></span>

-   <span data-ttu-id="9010e-125">如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 **MyFeature** 設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="9010e-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="9010e-126">如果命令列是： ADDSOURCE = ALL、ADDLOCAL = MyFeature、first **MyFeature** 設定為 run-local，則當 ADDSOURCE = ALL 進行評估時，包括 **MyFeature**) 在內的所有 (功能都會重設為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="9010e-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="9010e-127">安裝程式在暫停的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。</span><span class="sxs-lookup"><span data-stu-id="9010e-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="9010e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="9010e-128">Requirements</span></span>



| <span data-ttu-id="9010e-129">需求</span><span class="sxs-lookup"><span data-stu-id="9010e-129">Requirement</span></span> | <span data-ttu-id="9010e-130">值</span><span class="sxs-lookup"><span data-stu-id="9010e-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9010e-131">版本</span><span class="sxs-lookup"><span data-stu-id="9010e-131">Version</span></span><br/> | <span data-ttu-id="9010e-132">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="9010e-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9010e-133">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="9010e-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9010e-134">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="9010e-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9010e-135">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="9010e-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9010e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9010e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9010e-137">屬性</span><span class="sxs-lookup"><span data-stu-id="9010e-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




