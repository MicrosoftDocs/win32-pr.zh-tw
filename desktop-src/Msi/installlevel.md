---
description: INSTALLLEVEL 屬性是選取功能的初始層級 &\# 0034;&\# 0034; 預設為安裝。
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: INSTALLLEVEL 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc0616fdf49e2c713c65017a202320fa6ea9622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999239"
---
# <a name="installlevel-property"></a><span data-ttu-id="fec45-103">INSTALLLEVEL 屬性</span><span class="sxs-lookup"><span data-stu-id="fec45-103">INSTALLLEVEL property</span></span>

<span data-ttu-id="fec45-104">**INSTALLLEVEL** 屬性是在預設情況下，選取 [開啟] 來安裝特徵的初始層級。</span><span class="sxs-lookup"><span data-stu-id="fec45-104">The **INSTALLLEVEL** property is the initial level at which features are selected "ON" for installation by default.</span></span> <span data-ttu-id="fec45-105">只有當 [功能資料表](feature-table.md) 的 [層級] 欄位中的值小於或等於目前的 INSTALLLEVEL 值時，才會安裝功能。</span><span class="sxs-lookup"><span data-stu-id="fec45-105">A feature is installed only if the value in the Level field of the [Feature table](feature-table.md) is less than or equal to the current INSTALLLEVEL value.</span></span> <span data-ttu-id="fec45-106">任何安裝的安裝層級都是由 **INSTALLLEVEL** 屬性指定，而且可以是從1到32767的整數。</span><span class="sxs-lookup"><span data-stu-id="fec45-106">The installation level for any installation is specified by the **INSTALLLEVEL** property, and can be an integral from 1 to 32,767.</span></span> <span data-ttu-id="fec45-107">如需安裝層級的進一步討論，請參閱 [功能表](feature-table.md)。</span><span class="sxs-lookup"><span data-stu-id="fec45-107">For further discussion of installation levels, see [Feature Table](feature-table.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="fec45-108">預設值</span><span class="sxs-lookup"><span data-stu-id="fec45-108">Default Value</span></span>

<span data-ttu-id="fec45-109">如果未指定任何值，則安裝層級預設為1。</span><span class="sxs-lookup"><span data-stu-id="fec45-109">If no value is specified, the install level defaults to 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="fec45-110">備註</span><span class="sxs-lookup"><span data-stu-id="fec45-110">Remarks</span></span>

<span data-ttu-id="fec45-111">**INSTALLLEVEL** 屬性指定的安裝層級可以由下列屬性覆寫：</span><span class="sxs-lookup"><span data-stu-id="fec45-111">The installation level specified by the **INSTALLLEVEL** property can be overridden by the following properties:</span></span>

-   [<span data-ttu-id="fec45-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="fec45-112">**ADDLOCAL**</span></span>](addlocal.md)
-   [<span data-ttu-id="fec45-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="fec45-113">**ADDSOURCE**</span></span>](addsource.md)
-   [<span data-ttu-id="fec45-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="fec45-114">**ADDDEFAULT**</span></span>](adddefault.md)
-   [<span data-ttu-id="fec45-115">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="fec45-115">**COMPADDLOCAL**</span></span>](compaddlocal.md)
-   [<span data-ttu-id="fec45-116">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="fec45-116">**COMPADDSOURCE**</span></span>](compaddsource.md)
-   [<span data-ttu-id="fec45-117">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="fec45-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="fec45-118">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="fec45-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="fec45-119">**刪除**</span><span class="sxs-lookup"><span data-stu-id="fec45-119">**REMOVE**</span></span>](remove.md)
-   [<span data-ttu-id="fec45-120">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="fec45-120">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="fec45-121">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="fec45-121">**ADVERTISE**</span></span>](advertise.md)

<span data-ttu-id="fec45-122">例如，不論 **INSTALLLEVEL** 屬性的值為何，設定 ADDLOCAL = all 都會在本機安裝所有功能。</span><span class="sxs-lookup"><span data-stu-id="fec45-122">For example, setting ADDLOCAL=ALL installs all features locally regardless of the value of the **INSTALLLEVEL** property.</span></span> <span data-ttu-id="fec45-123">如果 [功能資料表](feature-table.md) 中層級資料行的值為0，則不會安裝該功能，也不會顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="fec45-123">If the value of the Level column in the [Feature table](feature-table.md) is 0, that feature is not installed and not displayed in the UI.</span></span>

<span data-ttu-id="fec45-124">系統管理員可以藉由套用自訂轉換，在該功能的層級資料行中設定0，以永久停用功能。</span><span class="sxs-lookup"><span data-stu-id="fec45-124">An administrator can permanently disable a feature by applying a customization transform that sets a 0 in the Level column for that feature.</span></span> <span data-ttu-id="fec45-125">自訂轉換的應用會防止安裝和顯示功能，即使使用者使用 UI 選取完整安裝，或在命令列上將 ADDLOCAL 設定為 [全部]。</span><span class="sxs-lookup"><span data-stu-id="fec45-125">The application of the customization transform prevents the installation and display of the feature even if the user selects a complete installation using the UI or by setting ADDLOCAL to ALL on the command line.</span></span> <span data-ttu-id="fec45-126">請參閱 [自訂轉換範例](a-customization-transform-example.md)。</span><span class="sxs-lookup"><span data-stu-id="fec45-126">See [A Customization Transform Example](a-customization-transform-example.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fec45-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="fec45-127">Requirements</span></span>



| <span data-ttu-id="fec45-128">需求</span><span class="sxs-lookup"><span data-stu-id="fec45-128">Requirement</span></span> | <span data-ttu-id="fec45-129">值</span><span class="sxs-lookup"><span data-stu-id="fec45-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec45-130">版本</span><span class="sxs-lookup"><span data-stu-id="fec45-130">Version</span></span><br/> | <span data-ttu-id="fec45-131">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="fec45-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fec45-132">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="fec45-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fec45-133">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="fec45-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fec45-134">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="fec45-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fec45-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fec45-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec45-136">屬性</span><span class="sxs-lookup"><span data-stu-id="fec45-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




