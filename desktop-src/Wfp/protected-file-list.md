---
description: 受保護的資源清單
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: 受保護的資源清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c221068d9185c289d601f53c6b76df9677d8bc213b44f3dc13dbf5b66a0df446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760118"
---
# <a name="protected-resource-list"></a>受保護的資源清單

修改受 WRP 保護之資源的完整存取權，僅限 TrustedInstaller。 WRP 保護的資源只能使用[支援的資源取代機制](supported-file-replacement-mechanisms.md)搭配 Windows 模組安裝程式服務來變更。

WRP 會使用 Windows Server 2008 或 Windows Vista 所安裝的下列延伸模組來保護檔案： .dll、.exe、.ocx 和 .sys。

WRP 可保護 Windows Server 2008 或 Windows Vista 安裝的重要檔案，其副檔名如下：。 cnv、.com、.aspx、ax、bas、.bat、bin、.cer、.chm、、.com、.cpl、. cpx、.crt、. csh、.dll、winspool.drv、. <./、、.、. （.）的.。 dtd、.exe、fxp、. grp、. h1s、.hlp、.hta、ime、.inf、.ins、.、. .jse、ksh、.lnk、.lnk、maf、. mag、mam、man、. maq、. mar、... .js ma、mau、. mav、. maw、mda、.mdb、.mde、mdt、mdw、mdz、services.msc、.msi、.msp、.mst、mui、nls、.ocx、.ops、pal、. pcd、pif、....... prg、.pst、.reg、scf、.scr、sct、. shb、shs、.sys、.tlb、tsp、.url、.vb、vbe、.vbs、. vsmacros、.vss、vsw、. wsc、. ws、. w2kmiguser.wsf、.、wsh、 .xsd 和 .xsl。

WRP 可保護重要資料夾。 只包含受 WRP 保護之檔案的資料夾可能會遭到鎖定，因此只有 Windows 信任的安裝程式才能在資料夾中建立檔案或子資料夾。 資料夾可能已部分鎖定，可讓系統管理員在資料夾中建立檔案和子資料夾。

WRP 可保護 Windows Server 2008 和 Windows Vista 所安裝的必要登錄機碼。 如果金鑰受 WRP 保護，則所有子機碼和值都可以受到保護。

WRP 會複製在位於% Windir% winsxs 備份的快取 *目錄* 中重新開機 Windows 所需的檔案 \\ \\ 。 不需要重新開機 Windows 的重要檔案不會複製到快取目錄。 無法修改快取目錄的大小和複製到快取的檔案清單。

* * Windows Server 2003 和 Windows XP： * *

Windows檔案保護 (WFP) 之前 WRP。

WFP 會保護 Windows 安裝的檔案，其副檔名如下： .dll、.exe、.ocx 和 .sys。 此外，也會保護 TrueType 字型 Micross. ttf、Tahoma. ttf 和 Tahomabd. ttf。

在 Windows 安裝結束時，WFP 會執行所有受保護檔案的掃描，以確保這些檔案不會被透過自動安裝所安裝的應用程式修改。 WFP 也會將這些系統檔案的已驗證版本複製到快取目錄。 當應用程式嘗試取代受保護的檔案時，WFP 可以從快取目錄還原原始檔案。

預設值為% systemroot% \\ system32 \\ dllcache。 若要指定不同的快取位置，請建立下列登錄值： **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**

這必須是本機路徑。 使用網路路徑可為快取檔案建立單一的共用網路來源，前提是所有使用該共用的用戶端都執行相同的 service pack 和修補程式。

快取的預設大小是無限制的。 若要變更快取的大小，請使用下列登錄設定： **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCQuota**

如果值是 SFC \_ 配額 \_ 所有檔案 \_ ，則會在快取目錄中快取所有系統檔案。

由於磁碟空間的考慮，您可能不需要維護快取目錄中所有系統檔案的快取版本。 根據快取的大小，WFP 會將已驗證的檔案版本儲存在系統硬碟的快取目錄中。 WFP 會將檔案新增至快取，直到快取目錄的大小達到指定的限制為止。

當應用程式嘗試取代不在快取中的受保護檔案時，WFP 會嘗試從安裝來源還原原始檔案，必要時也會提示使用者。

 

 



