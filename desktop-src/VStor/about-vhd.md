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
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span id="vhd.about_vhd"></span>關於 VHD

虛擬硬碟 (VHD) 格式是公開可用的映射格式 [規格](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) ，可將硬碟封裝成個別的檔案，以供作業系統作為 *虛擬磁片* 使用，方法與使用實體硬碟的方式相同。 這些虛擬磁片可以裝載原生檔案系統 (NTFS、FAT、exFAT 和 UDF) ，同時支援標準磁片和檔案作業。 VHD API 支援可讓您管理虛擬磁片。 使用 VHD API 建立的虛擬磁片可以作為開機磁片。

如何使用 VHD 檔案的範例是 Windows 7、Windows Server 2008、Virtual Server 和 Windows Virtual PC 中的 [hyper-v](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) 功能。 這些產品使用 VHD API 來包含虛擬機器用來作為其系統開機磁片的 Windows 作業系統映射。

Microsoft Windows 軟體開發套件 (SDK) 整合原生 VHD 支援以使用虛擬磁片，讓開發人員和系統管理員可以使用平臺 API 支援或管理工具，更輕鬆地在 VHD 檔案中建立、管理及部署 Windows 映像。 不需要安裝個別的應用程式，也不需要執行 VHD 格式剖析器來啟用這些作業。 這些 Api 可讓您一般使用虛擬磁片，而不受任何其他虛擬化技術的影響。

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>術語

「 *備份存放區* 」一詞是用來參考存在於實際硬碟的實體檔案。 備份存放區是以 *VHD 影像檔* 表示。

*動態*、*可擴充* 和 *稀疏* 這些詞彙通常會在參考動態可擴充的虛擬磁片時交替使用。 針對 VHD 技術，這些詞彙是相同的。

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>VHD 系統功能總覽

下圖顯示 VHD 功能及其關聯性的總覽。

![vhd 區塊圖表](images/vhd.png)

以下是先前所述功能的摘要說明。

使用者模式原生 Windows Api：

-   VirtDisk.dll-適用于 VHD 管理 Api 的通用程式庫。

使用者模式網域特定的管理包裝函式：

-   [VDS Vhd api](/windows/desktop/VDS/about-vds) -適用于 VHD Windows api 的 Vds 物件模型包裝函式。

核心模式驅動程式：

-   VDrvRoot.sys 根虛擬磁片磁碟機枚舉器。
-   FsDepends.sys 嵌套的磁片區相依性管理。
-   Vhdmp.sys-VHD 剖析器和相依性屬性提供者。

本節中的 SDK 檔涵蓋使用者模式原生 Windows VHD Api。

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>虛擬磁片類型

使用虛擬磁片以及可用的虛擬磁片類型有一些考慮：

-   已 **修正**-已在備份存放區上預先配置 VHD 映射檔案，以取得所要求的最大大小。
-   可 **展開**（又稱為「動態」、「動態可擴充」和「稀疏」）的 VHD 影像檔案，在儲存虛擬磁片目前包含的實際資料時，只會在備份存放區上使用多少空間。 當您建立這種類型的虛擬磁片時，VHD API 不會根據要求的大小上限來測試實體磁片上的可用空間，因此可以成功建立大小上限大於可用實體磁片可用空間的動態虛擬磁片。 如需詳細資訊，請參閱 [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk)。
    **注意**  動態虛擬磁片的大小上限為 2040 GB。

     

-   **差異**：使用父虛擬磁片做為此類型的基礎，且寫入虛擬磁片的任何後續寫入都與新的差異 vhd 映射檔案差異，而且不會修改父 VHD 映射檔案。 例如，如果您有一個全新安裝的系統開機作業系統虛擬磁片做為父系，並將差異虛擬磁片指定為系統要使用的目前虛擬磁片，則父虛擬磁片上的作業系統會保持其原始狀態以進行快速復原，或根據其他差異虛擬磁片快速建立更多開機映射。 如需詳細資訊，請參閱 [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk)。
    **注意**  差異虛擬磁片的大小上限為 2040 GB。

     

所有虛擬磁片類型的大小下限為 3 MB。

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>相關主題

[關於 VDS](/windows/desktop/VDS/about-vds)

[VHD 參考](vhd-reference.md)

[虛擬硬碟映射格式規格](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
