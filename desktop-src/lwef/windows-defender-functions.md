---
title: Windows Defender 函式
description: 應用程式所呼叫的函式，可要求掃描、簽章更新或 Windows Defender 的資訊。
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374286"
---
# <a name="windows-defender-functions"></a>Windows Defender 函式

應用程式所呼叫的函式，可要求掃描、簽章更新或 Windows Defender 的資訊。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></td>
<td>根據錯誤碼傳回格式化的錯誤訊息。<br/></td>
</tr>
<tr class="even">
<td><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></td>
<td>釋出 malware protection manager 的記憶體。<br/></td>
</tr>
<tr class="odd">
<td><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></td>
<td>關閉 <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>、 <a href="mpscanstart.md"><strong>MpScanStart</strong></a>、 <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>或 <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>所傳回的控制碼。<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></td>
<td>在本機電腦上建立與惡意程式碼防護管理員的連接。<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></td>
<td><strong>不支援。</strong> 傳回惡意程式碼防護管理員各元件的相關狀態資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></td>
<td>傳回惡意程式碼防護管理員各元件的相關狀態資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></td>
<td>傳回惡意程式碼防護管理員各元件的版本資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></td>
<td>允許透過 <a href="mpscanstart.md"><strong>MpScanStart</strong></a>以非同步方式起始的掃描控制。<br/></td>
</tr>
<tr class="odd">
<td><a href="mpscanstart.md"><strong>MpScanStart</strong></a></td>
<td>啟動掃描工作。<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></td>
<td>傳回列舉清單中下一個威脅的相關資訊。 您可以重複呼叫這個函式，直到所有威脅的列舉都完成為止。<br/></td>
</tr>
<tr class="odd">
<td><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></td>
<td>針對取得威脅的目的，傳回列舉控制碼。 這項功能可用來開啟特定掃描偵測到的威脅、系統中的所有作用中威脅、威脅消毒的歷程記錄，或簽章資料庫中出現的所有威脅。<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></td>
<td>用來查詢靜態 (（例如嚴重性和類別）) 或當地語系化的 (例如類別描述和建議) 特定威脅的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></td>
<td>允許透過 <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>以非同步方式啟動的簽章更新作業控制。<br/></td>
</tr>
<tr class="even">
<td><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></td>
<td>開始簽名更新作業。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></td>
<td>將 Windows Defender 狀態變更為開啟或關閉。<br/>
<blockquote>
[!Note]<br />
從 Windows 10、1607版和 Windows Server 2016 開始， <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> 函數一律會傳回 <strong>E_NOTIMPL</strong>。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></td>
<td>傳回 Windows Defender 的目前狀態。<br/></td>
</tr>
</tbody>
</table>



 

 

 





