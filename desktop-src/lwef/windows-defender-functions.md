---
title: Windows Defender功能
description: 應用程式所呼叫的函式，可要求掃描、簽章更新或 Windows Defender 的資訊。
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ecfa00a38c2263fe1db1b996bb3ec052f8caef1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483124"
---
# <a name="windows-defender-functions"></a>Windows Defender功能

應用程式所呼叫的函式，可要求掃描、簽章更新或 Windows Defender 的資訊。




| 函式 | 描述 | 
|----------|-------------|
| <a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a> | 根據錯誤碼傳回格式化的錯誤訊息。<br /> | 
| <a href="mpfreememory.md"><strong>MpFreeMemory</strong></a> | 釋出 malware protection manager 的記憶體。<br /> | 
| <a href="mphandleclose.md"><strong>MpHandleClose</strong></a> | 關閉 <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>、 <a href="mpscanstart.md"><strong>MpScanStart</strong></a>、 <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>或 <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>所傳回的控制碼。<br /> | 
| <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a> | 在本機電腦上建立與惡意程式碼防護管理員的連接。<br /> | 
| <a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a> | <strong>不支援。</strong> 傳回惡意程式碼防護管理員各元件的相關狀態資訊。<br /> | 
| <a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a> | 傳回惡意程式碼防護管理員各元件的相關狀態資訊。<br /> | 
| <a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a> | 傳回惡意程式碼防護管理員各元件的版本資訊。<br /> | 
| <a href="mpscancontrol.md"><strong>MpScanControl</strong></a> | 允許透過 <a href="mpscanstart.md"><strong>MpScanStart</strong></a>以非同步方式起始的掃描控制。<br /> | 
| <a href="mpscanstart.md"><strong>MpScanStart</strong></a> | 啟動掃描工作。<br /> | 
| <a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a> | 傳回列舉清單中下一個威脅的相關資訊。 您可以重複呼叫這個函式，直到所有威脅的列舉都完成為止。<br /> | 
| <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a> | 針對取得威脅的目的，傳回列舉控制碼。 這項功能可用來開啟特定掃描偵測到的威脅、系統中的所有作用中威脅、威脅消毒的歷程記錄，或簽章資料庫中出現的所有威脅。<br /> | 
| <a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a> | 用來查詢靜態 (（例如嚴重性和類別）) 或當地語系化的 (例如類別描述和建議) 特定威脅的相關資訊。<br /> | 
| <a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a> | 允許透過 <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>以非同步方式啟動的簽章更新作業控制。<br /> | 
| <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a> | 開始簽名更新作業。<br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> | 將 Windows Defender 狀態變更為開啟或關閉。<br /><blockquote>[!Note]<br />從 Windows 10，1607版和 Windows Server 2016 開始， <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a>函式一律會傳回<strong>E_NOTIMPL</strong>。</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a> | 傳回 Windows Defender 的目前狀態。<br /> | 




 

 

 





