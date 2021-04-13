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
# <a name="windows-defender-functions"></a><span data-ttu-id="27748-103">Windows Defender 函式</span><span class="sxs-lookup"><span data-stu-id="27748-103">Windows Defender Functions</span></span>

<span data-ttu-id="27748-104">應用程式所呼叫的函式，可要求掃描、簽章更新或 Windows Defender 的資訊。</span><span class="sxs-lookup"><span data-stu-id="27748-104">Functions called by apps to request scans, signature updates, or information from Windows Defender.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27748-105">函式</span><span class="sxs-lookup"><span data-stu-id="27748-105">Function</span></span></th>
<th><span data-ttu-id="27748-106">描述</span><span class="sxs-lookup"><span data-stu-id="27748-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27748-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span></span></td>
<td><span data-ttu-id="27748-108">根據錯誤碼傳回格式化的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="27748-108">Returns a formatted error message based on an error code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27748-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span></span></td>
<td><span data-ttu-id="27748-110">釋出 malware protection manager 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="27748-110">Frees memory for the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27748-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span></span></td>
<td><span data-ttu-id="27748-112">關閉 <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>、 <a href="mpscanstart.md"><strong>MpScanStart</strong></a>、 <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>或 <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="27748-112">Closes the handle returned by <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>, or <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27748-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span></span></td>
<td><span data-ttu-id="27748-114">在本機電腦上建立與惡意程式碼防護管理員的連接。</span><span class="sxs-lookup"><span data-stu-id="27748-114">Establishes a connection to the malware protection manager on the local computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27748-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span></span></td>
<td><span data-ttu-id="27748-116"><strong>不支援。</strong></span><span class="sxs-lookup"><span data-stu-id="27748-116"><strong>Not supported.</strong></span></span> <span data-ttu-id="27748-117">傳回惡意程式碼防護管理員各元件的相關狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="27748-117">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27748-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span></span></td>
<td><span data-ttu-id="27748-119">傳回惡意程式碼防護管理員各元件的相關狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="27748-119">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27748-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span></span></td>
<td><span data-ttu-id="27748-121">傳回惡意程式碼防護管理員各元件的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="27748-121">Returns version information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27748-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span></span></td>
<td><span data-ttu-id="27748-123">允許透過 <a href="mpscanstart.md"><strong>MpScanStart</strong></a>以非同步方式起始的掃描控制。</span><span class="sxs-lookup"><span data-stu-id="27748-123">Allows the control of a scan that was asynchronously initiated via <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27748-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span></span></td>
<td><span data-ttu-id="27748-125">啟動掃描工作。</span><span class="sxs-lookup"><span data-stu-id="27748-125">Starts a scanning operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27748-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span></span></td>
<td><span data-ttu-id="27748-127">傳回列舉清單中下一個威脅的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="27748-127">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="27748-128">您可以重複呼叫這個函式，直到所有威脅的列舉都完成為止。</span><span class="sxs-lookup"><span data-stu-id="27748-128">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27748-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span></span></td>
<td><span data-ttu-id="27748-130">針對取得威脅的目的，傳回列舉控制碼。</span><span class="sxs-lookup"><span data-stu-id="27748-130">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="27748-131">這項功能可用來開啟特定掃描偵測到的威脅、系統中的所有作用中威脅、威脅消毒的歷程記錄，或簽章資料庫中出現的所有威脅。</span><span class="sxs-lookup"><span data-stu-id="27748-131">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27748-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span></span></td>
<td><span data-ttu-id="27748-133">用來查詢靜態 (（例如嚴重性和類別）) 或當地語系化的 (例如類別描述和建議) 特定威脅的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="27748-133">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27748-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span></span></td>
<td><span data-ttu-id="27748-135">允許透過 <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>以非同步方式啟動的簽章更新作業控制。</span><span class="sxs-lookup"><span data-stu-id="27748-135">Allows the control of a signature update operation that was asynchronously initiated via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27748-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span></span></td>
<td><span data-ttu-id="27748-137">開始簽名更新作業。</span><span class="sxs-lookup"><span data-stu-id="27748-137">Starts a signature update operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27748-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span></span></td>
<td><span data-ttu-id="27748-139">將 Windows Defender 狀態變更為開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="27748-139">Changes Windows Defender status to on or off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="27748-140">從 Windows 10、1607版和 Windows Server 2016 開始， <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> 函數一律會傳回 <strong>E_NOTIMPL</strong>。</span><span class="sxs-lookup"><span data-stu-id="27748-140">Beginning in Windows 10, version 1607 and Windows Server 2016, the <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> function always returns <strong>E_NOTIMPL</strong>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27748-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="27748-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span></span></td>
<td><span data-ttu-id="27748-142">傳回 Windows Defender 的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="27748-142">Returns the current status of Windows Defender.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





