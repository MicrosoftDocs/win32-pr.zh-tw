---
description: REMOVE 屬性的值是以逗號分隔的功能清單，要移除這些功能。
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999702"
---
# <a name="remove-property"></a><span data-ttu-id="d8e14-103">REMOVE 屬性</span><span class="sxs-lookup"><span data-stu-id="d8e14-103">REMOVE property</span></span>

<span data-ttu-id="d8e14-104">**REMOVE** 屬性的值是以逗號分隔的功能清單，要移除這些功能。</span><span class="sxs-lookup"><span data-stu-id="d8e14-104">The value of the **REMOVE** property is a list of features delimited by commas that are to be removed.</span></span> <span data-ttu-id="d8e14-105">功能必須出現在 [功能資料表](feature-table.md)的功能資料行中。</span><span class="sxs-lookup"><span data-stu-id="d8e14-105">The features must be present in the Feature column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="d8e14-106">請注意，如果您在命令列上使用 REMOVE = ALL，安裝程式會移除安裝層級大於0的所有功能。</span><span class="sxs-lookup"><span data-stu-id="d8e14-106">Note that if you use REMOVE=ALL on the command line, the installer removes all features having an install level greater than 0.</span></span> <span data-ttu-id="d8e14-107">在此情況下，安裝程式不會移除安裝層級為0的功能。</span><span class="sxs-lookup"><span data-stu-id="d8e14-107">In this case, the installer does not remove features having an install level of 0.</span></span> <span data-ttu-id="d8e14-108">如需安裝層級功能的詳細資訊，請參閱 [功能表](feature-table.md)。</span><span class="sxs-lookup"><span data-stu-id="d8e14-108">For more information about the install level of features see [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8e14-109">備註</span><span class="sxs-lookup"><span data-stu-id="d8e14-109">Remarks</span></span>

<span data-ttu-id="d8e14-110">若要判斷產品是否已設定為完全卸載，封裝作者可以使用條件運算式來檢查是否要移除 = 全部。</span><span class="sxs-lookup"><span data-stu-id="d8e14-110">To determine whether a product has been set to be completely uninstalled, a package author may use a conditional expression to check whether REMOVE=ALL.</span></span> <span data-ttu-id="d8e14-111">請注意，如果產品是藉由將其最上層功能設定為 [不存在] 來移除，則 [ **移除** ] 屬性在 [InstallValidate 動作](installvalidate-action.md)之後可能不會完全相同。</span><span class="sxs-lookup"><span data-stu-id="d8e14-111">Note that if the product is removed by setting its top feature to absent, the **REMOVE** property may not equal ALL until after the [InstallValidate action](installvalidate-action.md).</span></span> <span data-ttu-id="d8e14-112">這表示任何相依于 REMOVE = ALL 的自訂動作都必須在 InstallValidate 之後排序。</span><span class="sxs-lookup"><span data-stu-id="d8e14-112">This means that any custom action that depends upon REMOVE=ALL must be sequenced after the InstallValidate.</span></span> <span data-ttu-id="d8e14-113">如需詳細資訊，請參閱 [在移除期間要執行的調節動作](conditioning-actions-to-run-during-removal.md)。</span><span class="sxs-lookup"><span data-stu-id="d8e14-113">For more information see also [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span> <span data-ttu-id="d8e14-114">請注意，功能名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d8e14-114">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="d8e14-115">安裝程式一律會依下列順序評估下列屬性：</span><span class="sxs-lookup"><span data-stu-id="d8e14-115">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="d8e14-116">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d8e14-116">**ADDLOCAL**</span></span>](addlocal.md)
2.  <span data-ttu-id="d8e14-117">**刪除**</span><span class="sxs-lookup"><span data-stu-id="d8e14-117">**REMOVE**</span></span>
3.  [<span data-ttu-id="d8e14-118">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d8e14-118">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="d8e14-119">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d8e14-119">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="d8e14-120">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="d8e14-120">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="d8e14-121">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="d8e14-121">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="d8e14-122">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d8e14-122">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="d8e14-123">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d8e14-123">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="d8e14-124">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d8e14-124">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="d8e14-125">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d8e14-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="d8e14-126">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d8e14-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="d8e14-127">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d8e14-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="d8e14-128">例如，如果命令列指定 ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 MyFeature 設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="d8e14-128">For example, if the command line specifies ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="d8e14-129">如果命令列是 ADDSOURCE = ALL、ADDLOCAL = MyFeature、first MyFeature 設定為 local local，則當 ADDSOURCE = ALL 進行評估時，所有功能 (包括 MyFeature) 都會重設為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="d8e14-129">If the command line is ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="d8e14-130">安裝程式在停用的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。</span><span class="sxs-lookup"><span data-stu-id="d8e14-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e14-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8e14-131">Requirements</span></span>



| <span data-ttu-id="d8e14-132">需求</span><span class="sxs-lookup"><span data-stu-id="d8e14-132">Requirement</span></span> | <span data-ttu-id="d8e14-133">值</span><span class="sxs-lookup"><span data-stu-id="d8e14-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e14-134">版本</span><span class="sxs-lookup"><span data-stu-id="d8e14-134">Version</span></span><br/> | <span data-ttu-id="d8e14-135">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d8e14-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d8e14-136">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d8e14-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d8e14-137">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="d8e14-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d8e14-138">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="d8e14-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8e14-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8e14-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e14-140">屬性</span><span class="sxs-lookup"><span data-stu-id="d8e14-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




