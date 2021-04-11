---
description: 將硬碟封裝成單一檔案，以供作業系統作為虛擬磁片使用。 虛擬磁片可以作為開機磁片，並且可以將原生檔案系統裝載 (NTFS、FAT、exFAT 和 UDF) ，同時支援標準磁片和檔案作業。
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 虛擬磁碟
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044145f5d631b878b533bbd409fad5eda5b4863f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191356"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span data-ttu-id="a130a-104"><span id="vhd.portal"></span>虛擬磁碟</span><span class="sxs-lookup"><span data-stu-id="a130a-104"><span id="vhd.portal"></span>Virtual Disk</span></span>

## <a name="span-idpurposespanpurpose"></a><span data-ttu-id="a130a-105"><span id="purpose"></span>目的</span><span class="sxs-lookup"><span data-stu-id="a130a-105"><span id="purpose"></span>Purpose</span></span>

<span data-ttu-id="a130a-106">虛擬硬碟 (VHD) 格式是一種公開可用的映射格式規格，可指定封裝在單一檔案中的虛擬硬碟，而且能夠裝載原生檔案系統，同時支援標準磁片和檔案作業。</span><span class="sxs-lookup"><span data-stu-id="a130a-106">The Virtual Hard Disk (VHD) format is a publicly-available image format specification that specifies a virtual hard disk encapsulated in a single file, capable of hosting native file systems while supporting standard disk and file operations.</span></span> <span data-ttu-id="a130a-107">如何使用 VHD 檔案的範例是 Windows Server 2008、Virtual Server 和 Windows Virtual PC 中的 [hyper-v](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) 功能。</span><span class="sxs-lookup"><span data-stu-id="a130a-107">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="a130a-108">這些產品使用 Vhd 來包含虛擬機器用來作為其系統開機磁片的 Windows 作業系統映射。</span><span class="sxs-lookup"><span data-stu-id="a130a-108">These products use VHDs to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span data-ttu-id="a130a-109"><span id="developer_audience_heading"></span>開發人員對象</span><span class="sxs-lookup"><span data-stu-id="a130a-109"><span id="developer_audience_heading"></span>Developer audience</span></span>

<span data-ttu-id="a130a-110">Microsoft Windows 軟體開發套件 (SDK) 整合原生 VHD 支援以使用 Vhd，讓開發人員和系統管理員可以使用平臺 API 支援或管理工具，更輕鬆地在 Vhd 中建立、管理及部署 Windows 映像。</span><span class="sxs-lookup"><span data-stu-id="a130a-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with VHDs, making it easier for developers and administrators to create, manage, and deploy Windows images in VHDs using the platform API support or management tools.</span></span> <span data-ttu-id="a130a-111">不需要安裝個別的應用程式，也不需要執行 VHD 格式剖析器來啟用這些作業。</span><span class="sxs-lookup"><span data-stu-id="a130a-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="a130a-112">這些 Api 可讓您一般使用 Vhd，與任何其他虛擬化技術無關。</span><span class="sxs-lookup"><span data-stu-id="a130a-112">These APIs allow for generic use of VHDs independent of any other virtualization technologies.</span></span>

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span data-ttu-id="a130a-113"><span id="run_time_requirements_heading"></span>執行時間需求</span><span class="sxs-lookup"><span data-stu-id="a130a-113"><span id="run_time_requirements_heading"></span>Run-time requirements</span></span>

<span data-ttu-id="a130a-114">Windows 7 和 Windows Server 2008 R2 支援 VHD。</span><span class="sxs-lookup"><span data-stu-id="a130a-114">VHD is supported on Windows 7 and Windows Server 2008 R2.</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="a130a-115"><span id="in_this_section"></span>本節內容</span><span class="sxs-lookup"><span data-stu-id="a130a-115"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a130a-116">主題</span><span class="sxs-lookup"><span data-stu-id="a130a-116">Topic</span></span></th>
<th><span data-ttu-id="a130a-117">描述</span><span class="sxs-lookup"><span data-stu-id="a130a-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a130a-118"><a href="about-vhd.md">關於 VHD</a></span><span class="sxs-lookup"><span data-stu-id="a130a-118"><a href="about-vhd.md">About VHD</a></span></span></p></td>
<td><p><span data-ttu-id="a130a-119">描述具有 API 使用方式提示和建議的 VHD 格式。</span><span class="sxs-lookup"><span data-stu-id="a130a-119">Describes the VHD format with API usage tips and suggestions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a130a-120"><a href="vhd-reference.md">VHD 參考</a></span><span class="sxs-lookup"><span data-stu-id="a130a-120"><a href="vhd-reference.md">VHD Reference</a></span></span></p></td>
<td><p><span data-ttu-id="a130a-121">描述 VHD API 函數、結構和列舉。</span><span class="sxs-lookup"><span data-stu-id="a130a-121">Describes the VHD API functions, structures, and enumerations.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="a130a-122"><span id="related_topics"></span>相關主題</span><span class="sxs-lookup"><span data-stu-id="a130a-122"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="a130a-123">虛擬磁碟服務</span><span class="sxs-lookup"><span data-stu-id="a130a-123">Virtual Disk Service</span></span>](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
