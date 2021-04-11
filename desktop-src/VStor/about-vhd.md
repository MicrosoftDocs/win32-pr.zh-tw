---
description: 虛擬硬碟 (VHD) 格式是公開可用的映射格式規格，可將硬碟封裝成個別的檔案，以供作業系統作為虛擬磁片使用，方法與使用實體硬碟的方式相同。
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 關於 VHD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ea37851360e70c1108e0715a47c77163c2c2fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690439"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span data-ttu-id="8edda-103"><span id="vhd.about_vhd"></span>關於 VHD</span><span class="sxs-lookup"><span data-stu-id="8edda-103"><span id="vhd.about_vhd"></span>About VHD</span></span>

<span data-ttu-id="8edda-104">虛擬硬碟 (VHD) 格式是公開可用的映射格式 [規格](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) ，可將硬碟封裝成個別的檔案，以供作業系統作為 *虛擬磁片* 使用，方法與使用實體硬碟的方式相同。</span><span class="sxs-lookup"><span data-stu-id="8edda-104">The Virtual Hard Disk (VHD) format is a publicly-available image format [specification](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) that allows encapsulation of the hard disk into an individual file for use by the operating system as a *virtual disk* in all the same ways physical hard disks are used.</span></span> <span data-ttu-id="8edda-105">這些虛擬磁片可以裝載原生檔案系統 (NTFS、FAT、exFAT 和 UDF) ，同時支援標準磁片和檔案作業。</span><span class="sxs-lookup"><span data-stu-id="8edda-105">These virtual disks are capable of hosting native file systems (NTFS, FAT, exFAT, and UDFS) while supporting standard disk and file operations.</span></span> <span data-ttu-id="8edda-106">VHD API 支援可讓您管理虛擬磁片。</span><span class="sxs-lookup"><span data-stu-id="8edda-106">VHD API support allows management of the virtual disks.</span></span> <span data-ttu-id="8edda-107">使用 VHD API 建立的虛擬磁片可以作為開機磁片。</span><span class="sxs-lookup"><span data-stu-id="8edda-107">Virtual disks created with the VHD API can function as boot disks.</span></span>

<span data-ttu-id="8edda-108">如何使用 VHD 檔案的範例是 Windows 7、Windows Server 2008、Virtual Server 和 Windows Virtual PC 中的 [hyper-v](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) 功能。</span><span class="sxs-lookup"><span data-stu-id="8edda-108">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows 7, Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="8edda-109">這些產品使用 VHD API 來包含虛擬機器用來作為其系統開機磁片的 Windows 作業系統映射。</span><span class="sxs-lookup"><span data-stu-id="8edda-109">These products use the VHD API to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

<span data-ttu-id="8edda-110">Microsoft Windows 軟體開發套件 (SDK) 整合原生 VHD 支援以使用虛擬磁片，讓開發人員和系統管理員可以使用平臺 API 支援或管理工具，更輕鬆地在 VHD 檔案中建立、管理及部署 Windows 映像。</span><span class="sxs-lookup"><span data-stu-id="8edda-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with virtual disks, making it easier for developers and administrators to create, manage, and deploy Windows images in VHD files using either the platform API support or management tools.</span></span> <span data-ttu-id="8edda-111">不需要安裝個別的應用程式，也不需要執行 VHD 格式剖析器來啟用這些作業。</span><span class="sxs-lookup"><span data-stu-id="8edda-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="8edda-112">這些 Api 可讓您一般使用虛擬磁片，而不受任何其他虛擬化技術的影響。</span><span class="sxs-lookup"><span data-stu-id="8edda-112">These APIs allow for generic use of virtual disks independent of any other virtualization technologies.</span></span>

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span data-ttu-id="8edda-113"><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>術語</span><span class="sxs-lookup"><span data-stu-id="8edda-113"><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminology</span></span>

<span data-ttu-id="8edda-114">「 *備份存放區* 」一詞是用來參考存在於實際硬碟的實體檔案。</span><span class="sxs-lookup"><span data-stu-id="8edda-114">The term *backing store* is used to refer to the physical file that exists on the actual hard disk.</span></span> <span data-ttu-id="8edda-115">備份存放區是以 *VHD 影像檔* 表示。</span><span class="sxs-lookup"><span data-stu-id="8edda-115">The backing store is represented by a *VHD image file*.</span></span>

<span data-ttu-id="8edda-116">*動態*、*可擴充* 和 *稀疏* 這些詞彙通常會在參考動態可擴充的虛擬磁片時交替使用。</span><span class="sxs-lookup"><span data-stu-id="8edda-116">The terms *dynamic*, *expandable*, and *sparse* are often used interchangeably when referring to dynamically expandable virtual disks.</span></span> <span data-ttu-id="8edda-117">針對 VHD 技術，這些詞彙是相同的。</span><span class="sxs-lookup"><span data-stu-id="8edda-117">For VHD technology, these terms are identical.</span></span>

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span data-ttu-id="8edda-118"><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>VHD 系統功能總覽</span><span class="sxs-lookup"><span data-stu-id="8edda-118"><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>VHD System Features Overview</span></span>

<span data-ttu-id="8edda-119">下圖顯示 VHD 功能及其關聯性的總覽。</span><span class="sxs-lookup"><span data-stu-id="8edda-119">The following diagram presents an overview of the VHD features and their relationships.</span></span>

![vhd 區塊圖表](images/vhd.png)

<span data-ttu-id="8edda-121">以下是先前所述功能的摘要說明。</span><span class="sxs-lookup"><span data-stu-id="8edda-121">The following is a summary explanation of the previously described features.</span></span>

<span data-ttu-id="8edda-122">使用者模式原生 Windows Api：</span><span class="sxs-lookup"><span data-stu-id="8edda-122">User Mode Native Windows APIs:</span></span>

-   <span data-ttu-id="8edda-123">VirtDisk.dll-適用于 VHD 管理 Api 的通用程式庫。</span><span class="sxs-lookup"><span data-stu-id="8edda-123">VirtDisk.dll - Common library for VHD management APIs.</span></span>

<span data-ttu-id="8edda-124">使用者模式網域特定的管理包裝函式：</span><span class="sxs-lookup"><span data-stu-id="8edda-124">User Mode Domain-specific Management Wrappers:</span></span>

-   <span data-ttu-id="8edda-125">[VDS Vhd api](/windows/desktop/VDS/about-vds) -適用于 VHD Windows api 的 Vds 物件模型包裝函式。</span><span class="sxs-lookup"><span data-stu-id="8edda-125">[VDS VHD APIs](/windows/desktop/VDS/about-vds) - VDS Object Model wrappers for the VHD Windows APIs.</span></span>

<span data-ttu-id="8edda-126">核心模式驅動程式：</span><span class="sxs-lookup"><span data-stu-id="8edda-126">Kernel Mode Drivers:</span></span>

-   <span data-ttu-id="8edda-127">VDrvRoot.sys 根虛擬磁片磁碟機枚舉器。</span><span class="sxs-lookup"><span data-stu-id="8edda-127">VDrvRoot.sys - Root virtual drive enumerator.</span></span>
-   <span data-ttu-id="8edda-128">FsDepends.sys 嵌套的磁片區相依性管理。</span><span class="sxs-lookup"><span data-stu-id="8edda-128">FsDepends.sys - Nested volume dependency management.</span></span>
-   <span data-ttu-id="8edda-129">Vhdmp.sys-VHD 剖析器和相依性屬性提供者。</span><span class="sxs-lookup"><span data-stu-id="8edda-129">Vhdmp.sys - VHD parser and dependency property provider.</span></span>

<span data-ttu-id="8edda-130">本節中的 SDK 檔涵蓋使用者模式原生 Windows VHD Api。</span><span class="sxs-lookup"><span data-stu-id="8edda-130">The SDK documentation in this section covers the user-mode native Windows VHD APIs.</span></span>

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span data-ttu-id="8edda-131"><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>虛擬磁片類型</span><span class="sxs-lookup"><span data-stu-id="8edda-131"><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Virtual Disk Types</span></span>

<span data-ttu-id="8edda-132">使用虛擬磁片以及可用的虛擬磁片類型有一些考慮：</span><span class="sxs-lookup"><span data-stu-id="8edda-132">There are considerations for using virtual disks, and what types of virtual disks are available:</span></span>

-   <span data-ttu-id="8edda-133">已 **修正**-已在備份存放區上預先配置 VHD 映射檔案，以取得所要求的最大大小。</span><span class="sxs-lookup"><span data-stu-id="8edda-133">**Fixed**—The VHD image file is pre-allocated on the backing store for the maximum size requested.</span></span>
-   <span data-ttu-id="8edda-134">可 **展開**（又稱為「動態」、「動態可擴充」和「稀疏」）的 VHD 影像檔案，在儲存虛擬磁片目前包含的實際資料時，只會在備份存放區上使用多少空間。</span><span class="sxs-lookup"><span data-stu-id="8edda-134">**Expandable**—Also known as "dynamic", "dynamically expandable", and "sparse", the VHD image file uses only as much space on the backing store as needed to store the actual data the virtual disk currently contains.</span></span> <span data-ttu-id="8edda-135">當您建立這種類型的虛擬磁片時，VHD API 不會根據要求的大小上限來測試實體磁片上的可用空間，因此可以成功建立大小上限大於可用實體磁片可用空間的動態虛擬磁片。</span><span class="sxs-lookup"><span data-stu-id="8edda-135">When creating this type of virtual disk, the VHD API does not test for free space on the physical disk based on the maximum size requested, therefore it is possible to successfully create a dynamic virtual disk with a maximum size larger than the available physical disk free space.</span></span> <span data-ttu-id="8edda-136">如需詳細資訊，請參閱 [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk)。</span><span class="sxs-lookup"><span data-stu-id="8edda-136">For more information, see [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).</span></span>
    <span data-ttu-id="8edda-137">**注意**  動態虛擬磁片的大小上限為 2040 GB。</span><span class="sxs-lookup"><span data-stu-id="8edda-137">**Note**  The maximum size of a dynamic virtual disk is 2,040 GB.</span></span>

     

-   <span data-ttu-id="8edda-138">**差異**：使用父虛擬磁片做為此類型的基礎，且寫入虛擬磁片的任何後續寫入都與新的差異 vhd 映射檔案差異，而且不會修改父 VHD 映射檔案。</span><span class="sxs-lookup"><span data-stu-id="8edda-138">**Differencing**—A parent virtual disk is used as the basis of this type, with any subsequent writes written to the virtual disk as differences to the new differencing VHD image file, and the parent VHD image file is not modified.</span></span> <span data-ttu-id="8edda-139">例如，如果您有一個全新安裝的系統開機作業系統虛擬磁片做為父系，並將差異虛擬磁片指定為系統要使用的目前虛擬磁片，則父虛擬磁片上的作業系統會保持其原始狀態以進行快速復原，或根據其他差異虛擬磁片快速建立更多開機映射。</span><span class="sxs-lookup"><span data-stu-id="8edda-139">For example, if you have a clean-install system boot operating system virtual disk as a parent and designate the differencing virtual disk as the current virtual disk for the system to use, then the operating system on the parent virtual disk stays in its original state for quick recovery or for quickly creating more boot images based on additional differencing virtual disks.</span></span> <span data-ttu-id="8edda-140">如需詳細資訊，請參閱 [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk)。</span><span class="sxs-lookup"><span data-stu-id="8edda-140">For more information, see [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).</span></span>
    <span data-ttu-id="8edda-141">**注意**  差異虛擬磁片的大小上限為 2040 GB。</span><span class="sxs-lookup"><span data-stu-id="8edda-141">**Note**  The maximum size of a differencing virtual disk is 2,040 GB.</span></span>

     

<span data-ttu-id="8edda-142">所有虛擬磁片類型的大小下限為 3 MB。</span><span class="sxs-lookup"><span data-stu-id="8edda-142">All virtual disk types have a minimum size of 3 MB.</span></span>

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="8edda-143"><span id="related_topics"></span>相關主題</span><span class="sxs-lookup"><span data-stu-id="8edda-143"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="8edda-144">關於 VDS</span><span class="sxs-lookup"><span data-stu-id="8edda-144">About VDS</span></span>](/windows/desktop/VDS/about-vds)

[<span data-ttu-id="8edda-145">VHD 參考</span><span class="sxs-lookup"><span data-stu-id="8edda-145">VHD Reference</span></span>](vhd-reference.md)

[<span data-ttu-id="8edda-146">虛擬硬碟映射格式規格</span><span class="sxs-lookup"><span data-stu-id="8edda-146">Virtual Hard Disk Image Format Specification</span></span>](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
