---
description: 受保護的資源清單
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: 受保護的資源清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316a9bf9233283a7c0aba11f0d5fe8a09f38f1e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195064"
---
# <a name="protected-resource-list"></a><span data-ttu-id="f7f60-103">受保護的資源清單</span><span class="sxs-lookup"><span data-stu-id="f7f60-103">Protected Resource List</span></span>

<span data-ttu-id="f7f60-104">修改受 WRP 保護之資源的完整存取權，僅限 TrustedInstaller。</span><span class="sxs-lookup"><span data-stu-id="f7f60-104">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="f7f60-105">WRP 保護的資源只能使用 [支援的資源取代機制](supported-file-replacement-mechanisms.md) 搭配 Windows 模組安裝程式服務來變更。</span><span class="sxs-lookup"><span data-stu-id="f7f60-105">WRP-protected resources can be changed only using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span>

<span data-ttu-id="f7f60-106">WRP 會使用 Windows Server 2008 或 Windows Vista 所安裝的下列延伸模組來保護檔案： .dll、.exe、.ocx 和 sys。</span><span class="sxs-lookup"><span data-stu-id="f7f60-106">WRP protects files with the following extensions that are installed by Windows Server 2008 or Windows Vista: .dll, .exe, .ocx, and .sys.</span></span>

<span data-ttu-id="f7f60-107">WRP 可保護 Windows Server 2008 或 Windows Vista 所安裝的重要檔案，其副檔名如下： < a0/&gt; < a1/&gt;：.：..：.：..：.：.：.：.：..：... < a2/&gt; 應用程式、asa、.asp、.aspx、ax、bas、.bat、.cmd、.cer、. cnv、. com、cpl、cpx、.crt、. csh、.dll、. winspool.drv、mmc.exe、.exe、fxp、. grp、. h1s、.hlp、.hta、ime、.inf、.ins、. .jse、.lnk、regedit.exe、. ksh、maf、.. e d、. mag、。、mam、man、。 maq、mar、ma、. mau、. mav、. maw、mda、.mdb、.mde、mdt、. mdw、. mdz、services.msc、.msi、.msp、.mst、dsa.msc、. pcd、.msp、....、......、.msp、prf、.。 prg、.pst、.reg、scf、.scr、sct、. shb、shs、sys、.tlb、tsp、.url、.vb、vbe、.vbs、. vsmacros、.vss、vsw、wsc、.xsd、.xsd 和 .xsl.. w2kmiguser.wsf、.xsd、.、.xsd、.xsd 和 .xsl。</span><span class="sxs-lookup"><span data-stu-id="f7f60-107">WRP protects critical files that are installed by Windows Server 2008 or Windows Vista with the following extensions: .acm, .ade, .adp, .app, .asa, .asp, .aspx, .ax, .bas, .bat, .bin, .cer, .chm, .clb, .cmd, .cnt, .cnv, .com, .cpl, .cpx, .crt, .csh, .dll, .drv, .dtd, .exe, .fxp, .grp, .h1s, .hlp, .hta, .ime, .inf, .ins, .isp, .its, .js, .jse, .ksh, .lnk, .mad, .maf, .mag, .mam, .man, .maq, .mar, .mas, .mat, .mau, .mav, .maw, .mda, .mdb, .mde, .mdt, .mdw, .mdz, .msc, .msi, .msp, .mst, .mui, .nls, .ocx, .ops, .pal, .pcd, .pif, .prf, .prg, .pst, .reg, .scf, .scr, .sct, .shb, .shs, .sys, .tlb, .tsp, .url, .vb, .vbe, .vbs, .vsmacros, .vss, .vst, .vsw, .ws, .wsc, .wsf, .wsh, .xsd, and .xsl.</span></span>

<span data-ttu-id="f7f60-108">WRP 可保護重要資料夾。</span><span class="sxs-lookup"><span data-stu-id="f7f60-108">WRP protects critical folders.</span></span> <span data-ttu-id="f7f60-109">只包含受 WRP 保護之檔案的資料夾可能會遭到鎖定，因此只有 Windows 受信任的安裝程式才能在資料夾中建立檔案或子資料夾。</span><span class="sxs-lookup"><span data-stu-id="f7f60-109">A folder containing only WRP-protected files may be locked so that only the Windows trusted installer is able to create files or subfolders in the folder.</span></span> <span data-ttu-id="f7f60-110">資料夾可能已部分鎖定，可讓系統管理員在資料夾中建立檔案和子資料夾。</span><span class="sxs-lookup"><span data-stu-id="f7f60-110">A folder may be partially locked to enable Administrators to create files and subfolders in the folder.</span></span>

<span data-ttu-id="f7f60-111">WRP 可保護 Windows Server 2008 和 Windows Vista 所安裝的必要登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="f7f60-111">WRP protects essential registry keys installed by Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="f7f60-112">如果金鑰受 WRP 保護，則所有子機碼和值都可以受到保護。</span><span class="sxs-lookup"><span data-stu-id="f7f60-112">If a key is protected by WRP, all its subkeys and values can be protected.</span></span>

<span data-ttu-id="f7f60-113">WRP 會複製在位於% Windir% winsxs 備份的快取 *目錄* 中重新開機 Windows 所需的檔案 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="f7f60-113">WRP copies files that are needed to restart Windows in the *cache directory* located at %Windir%\\winsxs\\Backup.</span></span> <span data-ttu-id="f7f60-114">重新開機 Windows 所需的重要檔案不會複製到快取目錄。</span><span class="sxs-lookup"><span data-stu-id="f7f60-114">Critical files that are not needed to restart Windows are not copied to the cache directory.</span></span> <span data-ttu-id="f7f60-115">無法修改快取目錄的大小和複製到快取的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="f7f60-115">The size of the cache directory and the list of files copied to cache cannot be modified.</span></span>

<span data-ttu-id="f7f60-116">\* \* Windows Server 2003 和 Windows XP： \* \*</span><span class="sxs-lookup"><span data-stu-id="f7f60-116">\*\*Windows Server 2003 and Windows XP:  \*\*</span></span>

<span data-ttu-id="f7f60-117">Windows 檔案保護 (WFP) 之前 WRP。</span><span class="sxs-lookup"><span data-stu-id="f7f60-117">Windows File Protection (WFP) preceded WRP.</span></span>

<span data-ttu-id="f7f60-118">WFP 會保護 Windows 所安裝的檔案，其副檔名如下： .dll、.exe、.ocx 和 sys。</span><span class="sxs-lookup"><span data-stu-id="f7f60-118">WFP protects files that are installed by Windows with the following extensions: .dll, .exe, .ocx, and .sys.</span></span> <span data-ttu-id="f7f60-119">此外，也會保護 TrueType 字型 Micross. ttf、Tahoma. ttf 和 Tahomabd. ttf。</span><span class="sxs-lookup"><span data-stu-id="f7f60-119">In addition, the TrueType fonts Micross.ttf, Tahoma.ttf, and Tahomabd.ttf are also protected.</span></span>

<span data-ttu-id="f7f60-120">在 Windows 安裝結束時，WFP 會執行所有受保護檔案的掃描，以確保這些檔案不會被透過自動安裝所安裝的應用程式修改。</span><span class="sxs-lookup"><span data-stu-id="f7f60-120">At the end of the Windows installation, WFP runs a scan of all protected files to ensure they have not been modified by applications installed through unattended installation.</span></span> <span data-ttu-id="f7f60-121">WFP 也會將這些系統檔案的已驗證版本複製到快取目錄。</span><span class="sxs-lookup"><span data-stu-id="f7f60-121">WFP also copies verified versions of these system files to the cache directory.</span></span> <span data-ttu-id="f7f60-122">當應用程式嘗試取代受保護的檔案時，WFP 可以從快取目錄還原原始檔案。</span><span class="sxs-lookup"><span data-stu-id="f7f60-122">When an application attempts to replace a protected file, WFP can restore the original file from the cache directory.</span></span>

<span data-ttu-id="f7f60-123">預設值為% systemroot% \\ system32 \\ dllcache。</span><span class="sxs-lookup"><span data-stu-id="f7f60-123">The default value is %systemroot%\\system32\\dllcache.</span></span> <span data-ttu-id="f7f60-124">若要指定不同的快取位置，請建立下列登錄值： **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**</span><span class="sxs-lookup"><span data-stu-id="f7f60-124">To specify a different location for the cache, create the following registry value: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\SFCDllCacheDir**</span></span>

<span data-ttu-id="f7f60-125">這必須是本機路徑。</span><span class="sxs-lookup"><span data-stu-id="f7f60-125">This must be a local path.</span></span> <span data-ttu-id="f7f60-126">使用網路路徑可為快取檔案建立單一的共用網路來源，前提是所有使用該共用的用戶端都執行相同的 service pack 和修補程式。</span><span class="sxs-lookup"><span data-stu-id="f7f60-126">Using a network path creates a single shared network source for cache files, provided all clients using the share are running the same service packs and hotfixes.</span></span>

<span data-ttu-id="f7f60-127">快取的預設大小是無限制的。</span><span class="sxs-lookup"><span data-stu-id="f7f60-127">The default size of the cache is unlimited.</span></span> <span data-ttu-id="f7f60-128">若要變更快取的大小，請使用下列登錄設定： **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCQuota**</span><span class="sxs-lookup"><span data-stu-id="f7f60-128">To change the size of the cache, use the following registry setting: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\SFCQuota**</span></span>

<span data-ttu-id="f7f60-129">如果值是 SFC \_ 配額 \_ 所有檔案 \_ ，則會在快取目錄中快取所有系統檔案。</span><span class="sxs-lookup"><span data-stu-id="f7f60-129">If the value is SFC\_QUOTA\_ALL\_FILES, all system files will be cached in the cache directory.</span></span>

<span data-ttu-id="f7f60-130">由於磁碟空間的考慮，您可能不需要維護快取目錄中所有系統檔案的快取版本。</span><span class="sxs-lookup"><span data-stu-id="f7f60-130">Due to disk space considerations, it may not be desirable to maintain cached versions of all system files in the cache directory.</span></span> <span data-ttu-id="f7f60-131">根據快取的大小，WFP 會將已驗證的檔案版本儲存在系統硬碟的快取目錄中。</span><span class="sxs-lookup"><span data-stu-id="f7f60-131">Depending on the size of the cache, WFP will store verified file versions in the cache directory on the system hard drive.</span></span> <span data-ttu-id="f7f60-132">WFP 會將檔案新增至快取，直到快取目錄的大小達到指定的限制為止。</span><span class="sxs-lookup"><span data-stu-id="f7f60-132">WFP will add files to the cache until the size of the cache directory reaches the specified limit.</span></span>

<span data-ttu-id="f7f60-133">當應用程式嘗試取代不在快取中的受保護檔案時，WFP 會嘗試從安裝來源還原原始檔案，必要時也會提示使用者。</span><span class="sxs-lookup"><span data-stu-id="f7f60-133">When an application attempts to replace a protected file that is not in the cache, WFP attempts to restore the original file from the installation source, prompting the user if necessary.</span></span>

 

 



