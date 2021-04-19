---
description: 系統檔案檢查程式的 Sfc.exe，可讓系統管理員掃描所有受保護的資源，以驗證其版本。
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: 系統檔案檢查程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981218"
---
# <a name="system-file-checker"></a><span data-ttu-id="34764-103">系統檔案檢查程式</span><span class="sxs-lookup"><span data-stu-id="34764-103">System File Checker</span></span>

<span data-ttu-id="34764-104">系統檔案檢查程式的 Sfc.exe，可讓系統管理員掃描所有受保護的資源，以驗證其版本。</span><span class="sxs-lookup"><span data-stu-id="34764-104">The system file checker utility, Sfc.exe, allows administrators to scan all protected resources to verify their versions.</span></span>

<span data-ttu-id="34764-105">重新開機不符合預期 Windows 版本之 Windows 的重要檔案，可能會以正確的版本取代。</span><span class="sxs-lookup"><span data-stu-id="34764-105">Files critical to restart Windows that do not match the expected Windows version may be replaced with the correct versions.</span></span> <span data-ttu-id="34764-106">如果檔案已修復，則也會修復對應的登錄資料。</span><span class="sxs-lookup"><span data-stu-id="34764-106">If a file is repaired, the corresponding registry data is also repaired.</span></span> <span data-ttu-id="34764-107">未修復受保護的檔案不是重新開機 Windows 的關鍵。</span><span class="sxs-lookup"><span data-stu-id="34764-107">Protected files not critical to restart Windows are not repaired.</span></span>

## <a name="syntax"></a><span data-ttu-id="34764-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="34764-108">Syntax</span></span>

<span data-ttu-id="34764-109">以下是 Sfc 的命令列語法。</span><span class="sxs-lookup"><span data-stu-id="34764-109">The following is the command-line syntax for Sfc.</span></span>

<span data-ttu-id="34764-110">**SFC 選項 \[ = 完整檔案路徑\]**</span><span class="sxs-lookup"><span data-stu-id="34764-110">**SFC options \[=full file path\]**</span></span>

## <a name="options"></a><span data-ttu-id="34764-111">選項</span><span class="sxs-lookup"><span data-stu-id="34764-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="34764-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE =*x*</span><span class="sxs-lookup"><span data-stu-id="34764-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE=*x*</span></span>
</dt> <dd>

<span data-ttu-id="34764-113">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="34764-113">This value is not supported.</span></span>

<span data-ttu-id="34764-114">**Windows Server 2003 和 WINDOWS XP：** 設定檔案快取大小。</span><span class="sxs-lookup"><span data-stu-id="34764-114">**Windows Server 2003 and Windows XP:** Sets the file cache size.</span></span> <span data-ttu-id="34764-115">快取的預設大小為 0x32 (50 MB) 。</span><span class="sxs-lookup"><span data-stu-id="34764-115">The default size of the cache is 0x32 (50 MB).</span></span>

</dd> <dt>

<span data-ttu-id="34764-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span><span class="sxs-lookup"><span data-stu-id="34764-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="34764-117">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="34764-117">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="34764-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span><span class="sxs-lookup"><span data-stu-id="34764-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span></span>
</dt> <dd>

<span data-ttu-id="34764-119">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="34764-119">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="34764-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span><span class="sxs-lookup"><span data-stu-id="34764-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span></span>
</dt> <dd>

<span data-ttu-id="34764-121">確認或只修復檔案。</span><span class="sxs-lookup"><span data-stu-id="34764-121">Verify or repair only files.</span></span> <span data-ttu-id="34764-122">請勿確認或修復登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="34764-122">Do not verify or repair registry keys.</span></span>

<span data-ttu-id="34764-123">**WINDOWS XP：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="34764-123">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="34764-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span><span class="sxs-lookup"><span data-stu-id="34764-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span></span>
</dt> <dd>

<span data-ttu-id="34764-125">使用此選項可進行離線修復。</span><span class="sxs-lookup"><span data-stu-id="34764-125">Use this option for offline repairs.</span></span> <span data-ttu-id="34764-126">指定離線開機目錄的位置。</span><span class="sxs-lookup"><span data-stu-id="34764-126">Specify the location of the offline boot directory.</span></span>

<span data-ttu-id="34764-127">**WINDOWS XP：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="34764-127">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="34764-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span><span class="sxs-lookup"><span data-stu-id="34764-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span></span>
</dt> <dd>

<span data-ttu-id="34764-129">使用此選項可進行離線修復。</span><span class="sxs-lookup"><span data-stu-id="34764-129">Use this option for offline repairs.</span></span> <span data-ttu-id="34764-130">指定離線 Windows 目錄的位置。</span><span class="sxs-lookup"><span data-stu-id="34764-130">Specify the location of the offline Windows directory.</span></span>

<span data-ttu-id="34764-131">**WINDOWS XP：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="34764-131">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="34764-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span><span class="sxs-lookup"><span data-stu-id="34764-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span></span>
</dt> <dd>

<span data-ttu-id="34764-133">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="34764-133">This value is not supported.</span></span>

<span data-ttu-id="34764-134">**Windows Server 2003 和 WINDOWS XP：** 清空檔案快取，並掃描所有受保護的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="34764-134">**Windows Server 2003 and Windows XP:** Empties the file cache and scans all protected system files.</span></span>

</dd> <dt>

<span data-ttu-id="34764-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span><span class="sxs-lookup"><span data-stu-id="34764-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span></span>
</dt> <dd>

<span data-ttu-id="34764-136">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="34764-136">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="34764-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span><span class="sxs-lookup"><span data-stu-id="34764-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span></span>
</dt> <dd>

<span data-ttu-id="34764-138">返回預設設定。</span><span class="sxs-lookup"><span data-stu-id="34764-138">Return to default settings.</span></span>

<span data-ttu-id="34764-139">**Windows Server 2008 和 Windows Vista：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="34764-139">**Windows Server 2008 and Windows Vista:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="34764-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span><span class="sxs-lookup"><span data-stu-id="34764-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span></span>
</dt> <dd>

<span data-ttu-id="34764-141">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="34764-141">This value is not supported.</span></span>

<span data-ttu-id="34764-142">**Windows Server 2003 和 WINDOWS XP：** 每次開機時掃描所有受保護的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="34764-142">**Windows Server 2003 and Windows XP:** Scans all protected system files at every boot.</span></span>

</dd> <dt>

<span data-ttu-id="34764-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span><span class="sxs-lookup"><span data-stu-id="34764-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span></span>
</dt> <dd>

<span data-ttu-id="34764-144">掃描並修復位於指定完整路徑的檔案。</span><span class="sxs-lookup"><span data-stu-id="34764-144">Scans and repairs the file located at the specified full path.</span></span>

<span data-ttu-id="34764-145">**WINDOWS XP：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="34764-145">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="34764-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span><span class="sxs-lookup"><span data-stu-id="34764-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span></span>
</dt> <dd>

<span data-ttu-id="34764-147">立即掃描所有受保護的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="34764-147">Scans all protected system files immediately.</span></span>

</dd> <dt>

<span data-ttu-id="34764-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span><span class="sxs-lookup"><span data-stu-id="34764-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span></span>
</dt> <dd>

<span data-ttu-id="34764-149">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="34764-149">This value is not supported.</span></span>

<span data-ttu-id="34764-150">**Windows Server 2003 和 WINDOWS XP：** 在下一次開機時掃描所有受保護的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="34764-150">**Windows Server 2003 and Windows XP:** Scans all protected system files at the next boot.</span></span>

</dd> <dt>

<span data-ttu-id="34764-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span><span class="sxs-lookup"><span data-stu-id="34764-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span></span>
</dt> <dd>

<span data-ttu-id="34764-152">驗證位於指定完整路徑的檔案。</span><span class="sxs-lookup"><span data-stu-id="34764-152">Verifies the file at the specified full path.</span></span> <span data-ttu-id="34764-153">此選項不會修復檔案。</span><span class="sxs-lookup"><span data-stu-id="34764-153">This option does not repair the file.</span></span>

<span data-ttu-id="34764-154">**WINDOWS XP：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="34764-154">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="34764-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span><span class="sxs-lookup"><span data-stu-id="34764-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span></span>
</dt> <dd>

<span data-ttu-id="34764-156">掃描所有受保護的系統檔案，但不修復檔案。</span><span class="sxs-lookup"><span data-stu-id="34764-156">Scans all protected system files but does not repair files.</span></span>

<span data-ttu-id="34764-157">**WINDOWS XP：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="34764-157">**Windows XP:** Not supported.</span></span>

</dd> </dl>

<span data-ttu-id="34764-158">Sfc 會設定下列登錄值：</span><span class="sxs-lookup"><span data-stu-id="34764-158">Sfc sets the following registry value:</span></span>

 <span data-ttu-id="34764-159">= HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCScan</span><span class="sxs-lookup"><span data-stu-id="34764-159">= HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\SFCScan</span></span>

<span data-ttu-id="34764-160">如需詳細資訊，請參閱 [WFP 登錄值](wfp-registry-values.md)。</span><span class="sxs-lookup"><span data-stu-id="34764-160">For more information, see [WFP Registry Values](wfp-registry-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="34764-161">備註</span><span class="sxs-lookup"><span data-stu-id="34764-161">Remarks</span></span>

<span data-ttu-id="34764-162">在 Windows Vista 中，您可以將 **windows \_ 追蹤 \_** 記錄檔環境變數設為有效目錄的位置，以接收記錄檔。</span><span class="sxs-lookup"><span data-stu-id="34764-162">On Windows Vista only, you can set the **WINDOWS\_TRACING\_LOGFILE** environment variable to the location of a valid directory to receive a log file.</span></span>

## <a name="examples"></a><span data-ttu-id="34764-163">範例</span><span class="sxs-lookup"><span data-stu-id="34764-163">Examples</span></span>

<span data-ttu-id="34764-164">下列範例命令列是 sfc.exe 語法的範例。</span><span class="sxs-lookup"><span data-stu-id="34764-164">The following sample command lines are examples of sfc.exe syntax.</span></span>

<span data-ttu-id="34764-165">**sfc/SCANNOW**</span><span class="sxs-lookup"><span data-stu-id="34764-165">**sfc /SCANNOW**</span></span>

<span data-ttu-id="34764-166">**sfc/VERIFYFILE = c： \\ windows \\ system32 \\kernel32.dll**</span><span class="sxs-lookup"><span data-stu-id="34764-166">**sfc /VERIFYFILE=c:\\windows\\system32\\kernel32.dll**</span></span>

<span data-ttu-id="34764-167">**sfc/SCANFILE = d： \\ windows \\ system32 \\kernel32.dll/OFFBOOTDIR = d： \\ /OFFWINDIR = d： \\ windows**</span><span class="sxs-lookup"><span data-stu-id="34764-167">**sfc /SCANFILE=d:\\windows\\system32\\kernel32.dll /OFFBOOTDIR=d:\\ /OFFWINDIR=d:\\windows**</span></span>

<span data-ttu-id="34764-168">**sfc/VERIFYONLY/FILESONLY**</span><span class="sxs-lookup"><span data-stu-id="34764-168">**sfc /VERIFYONLY /FILESONLY**</span></span>

 

 



