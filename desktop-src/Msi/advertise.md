---
description: '[公告] 屬性的值是以逗號分隔的功能清單，這些功能是以要通告的逗號分隔。'
ms.assetid: ef97f70b-e4bf-4eb3-b643-046a9c348823
title: 公告屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e768f22f86dacf35009ca0e0e3ef9337ef84ab70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999622"
---
# <a name="advertise-property"></a><span data-ttu-id="d9662-103">公告屬性</span><span class="sxs-lookup"><span data-stu-id="d9662-103">ADVERTISE property</span></span>

<span data-ttu-id="d9662-104">[ **公告** ] 屬性的值是以逗號分隔的功能清單，這些功能是以要通告的逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="d9662-104">The value of the **ADVERTISE** property is a list of features delimited by commas that are to be advertised.</span></span> <span data-ttu-id="d9662-105">功能必須出現在 [功能](feature-table.md) 資料表的功能資料行中。</span><span class="sxs-lookup"><span data-stu-id="d9662-105">The features must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="d9662-106">若要安裝所有功能，請在命令列上使用公告 = 全部。</span><span class="sxs-lookup"><span data-stu-id="d9662-106">To install all features as advertised, use ADVERTISE=ALL on the command line.</span></span> <span data-ttu-id="d9662-107">請勿在 [屬性工作表](property-table.md) 中輸入 [公告 = 全部]，因為這會產生無法安裝或移除的公告套件。</span><span class="sxs-lookup"><span data-stu-id="d9662-107">Do not enter ADVERTISE=ALL into the [Property table](property-table.md) because this generates an advertised package that cannot be installed or removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9662-108">備註</span><span class="sxs-lookup"><span data-stu-id="d9662-108">Remarks</span></span>

<span data-ttu-id="d9662-109">請注意，功能名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d9662-109">Note that feature names are case-sensitive.</span></span>

<span data-ttu-id="d9662-110">安裝程式一律會依下列順序評估下列屬性。</span><span class="sxs-lookup"><span data-stu-id="d9662-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="d9662-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d9662-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="d9662-112">**刪除**</span><span class="sxs-lookup"><span data-stu-id="d9662-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="d9662-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d9662-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="d9662-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d9662-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="d9662-115">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="d9662-115">**REINSTALL**</span></span>](reinstall.md)
6.  <span data-ttu-id="d9662-116">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="d9662-116">**ADVERTISE**</span></span>
7.  [<span data-ttu-id="d9662-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d9662-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="d9662-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d9662-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="d9662-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d9662-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="d9662-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d9662-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="d9662-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d9662-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="d9662-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d9662-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="d9662-123">例如，如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 MyFeature 設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="d9662-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="d9662-124">如果命令列是： ADDSOURCE = ALL、ADDLOCAL = MyFeature、first MyFeature 設定為 run-local，則當 ADDSOURCE = ALL 進行評估時，包括 MyFeature) 在內的所有 (功能都會重設為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="d9662-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="d9662-125">安裝程式在停用的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。</span><span class="sxs-lookup"><span data-stu-id="d9662-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9662-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9662-126">Requirements</span></span>



| <span data-ttu-id="d9662-127">需求</span><span class="sxs-lookup"><span data-stu-id="d9662-127">Requirement</span></span> | <span data-ttu-id="d9662-128">值</span><span class="sxs-lookup"><span data-stu-id="d9662-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9662-129">版本</span><span class="sxs-lookup"><span data-stu-id="d9662-129">Version</span></span><br/> | <span data-ttu-id="d9662-130">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d9662-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d9662-131">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d9662-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d9662-132">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="d9662-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d9662-133">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="d9662-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9662-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9662-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9662-135">屬性</span><span class="sxs-lookup"><span data-stu-id="d9662-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




