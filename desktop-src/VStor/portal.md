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
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>虛擬磁碟

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>目的

虛擬硬碟 (VHD) 格式是一種公開可用的映射格式規格，可指定封裝在單一檔案中的虛擬硬碟，而且能夠裝載原生檔案系統，同時支援標準磁片和檔案作業。 如何使用 VHD 檔案的範例是 Windows Server 2008、Virtual Server 和 Windows Virtual PC 中的 [hyper-v](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) 功能。 這些產品使用 Vhd 來包含虛擬機器用來作為其系統開機磁片的 Windows 作業系統映射。

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>開發人員對象

Microsoft Windows 軟體開發套件 (SDK) 整合原生 VHD 支援以使用 Vhd，讓開發人員和系統管理員可以使用平臺 API 支援或管理工具，更輕鬆地在 Vhd 中建立、管理及部署 Windows 映像。 不需要安裝個別的應用程式，也不需要執行 VHD 格式剖析器來啟用這些作業。 這些 Api 可讓您一般使用 Vhd，與任何其他虛擬化技術無關。

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>執行時間需求

Windows 7 和 Windows Server 2008 R2 支援 VHD。

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>本節內容

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="about-vhd.md">關於 VHD</a></p></td>
<td><p>描述具有 API 使用方式提示和建議的 VHD 格式。</p></td>
</tr>
<tr class="even">
<td><p><a href="vhd-reference.md">VHD 參考</a></p></td>
<td><p>描述 VHD API 函數、結構和列舉。</p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>相關主題

[虛擬磁碟服務](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
