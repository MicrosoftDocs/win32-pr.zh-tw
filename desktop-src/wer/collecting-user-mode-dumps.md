---
title: 收集 User-Mode 傾印
description: 從 Windows Server 2008 和 Windows Vista （含 Service Pack 1） (SP1) 開始，Windows 錯誤報告 (WER) 可進行設定，以便在使用者模式應用程式損毀之後，收集完整的使用者模式傾印並儲存在本機。
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7b1e7850e84d9fa6c8d10953d23640b41b1bc6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842111"
---
# <a name="collecting-user-mode-dumps"></a><span data-ttu-id="356b8-103">收集 User-Mode 傾印</span><span class="sxs-lookup"><span data-stu-id="356b8-103">Collecting User-Mode Dumps</span></span>

<span data-ttu-id="356b8-104">從 Windows Server 2008 和 Windows Vista （含 Service Pack 1） (SP1) 開始，Windows 錯誤報告 (WER) 可進行設定，以便在使用者模式應用程式損毀之後，收集完整的使用者模式傾印並儲存在本機。</span><span class="sxs-lookup"><span data-stu-id="356b8-104">Starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1), Windows Error Reporting (WER) can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes.</span></span> <span data-ttu-id="356b8-105">這項功能不支援自行自訂損毀報告（包括 .NET 應用程式）的應用程式。</span><span class="sxs-lookup"><span data-stu-id="356b8-105">Applications that do their own custom crash reporting, including .NET applications, are not supported by this feature.</span></span>

<span data-ttu-id="356b8-106">預設不會啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="356b8-106">This feature is not enabled by default.</span></span> <span data-ttu-id="356b8-107">啟用此功能需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="356b8-107">Enabling the feature requires administrator privileges.</span></span> <span data-ttu-id="356b8-108">若要啟用並設定此功能，請使用 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ Windows 錯誤報告 \\ LocalDumps** 機碼底下的下列登錄值。</span><span class="sxs-lookup"><span data-stu-id="356b8-108">To enable and configure the feature, use the following registry values under the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** key.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="356b8-109">值</span><span class="sxs-lookup"><span data-stu-id="356b8-109">Value</span></span></th>
<th><span data-ttu-id="356b8-110">描述</span><span class="sxs-lookup"><span data-stu-id="356b8-110">Description</span></span></th>
<th><span data-ttu-id="356b8-111">類型</span><span class="sxs-lookup"><span data-stu-id="356b8-111">Type</span></span></th>
<th><span data-ttu-id="356b8-112">預設值</span><span class="sxs-lookup"><span data-stu-id="356b8-112">Default value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="356b8-113"><strong>DumpFolder</strong></span><span class="sxs-lookup"><span data-stu-id="356b8-113"><strong>DumpFolder</strong></span></span></td>
<td><span data-ttu-id="356b8-114">要儲存傾印檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="356b8-114">The path where the dump files are to be stored.</span></span> <span data-ttu-id="356b8-115">如果您未使用預設路徑，請確定該資料夾包含允許損毀進程將資料寫入資料夾的 Acl。</span><span class="sxs-lookup"><span data-stu-id="356b8-115">If you do not use the default path, then make sure that the folder contains ACLs that allow the crashing process to write data to the folder.</span></span> <span data-ttu-id="356b8-116">針對服務損毀，會根據所使用的服務帳戶，將傾印寫入服務特定的設定檔資料夾。</span><span class="sxs-lookup"><span data-stu-id="356b8-116">For service crashes, the dump is written to service specific profile folders depending on the service account used.</span></span> <span data-ttu-id="356b8-117">例如，系統服務的設定檔資料夾是%WINDIR%\System32\Config\SystemProfile。</span><span class="sxs-lookup"><span data-stu-id="356b8-117">For example, the profile folder for System services is %WINDIR%\System32\Config\SystemProfile.</span></span> <span data-ttu-id="356b8-118">針對網路和本機服務，此資料夾為%WINDIR%\ServiceProfiles。</span><span class="sxs-lookup"><span data-stu-id="356b8-118">For Network and Local Services, the folder is %WINDIR%\ServiceProfiles.</span></span><br/></td>
<td><span data-ttu-id="356b8-119"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="356b8-119">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="356b8-120">%LOCALAPPDATA%\CrashDumps</span><span class="sxs-lookup"><span data-stu-id="356b8-120">%LOCALAPPDATA%\CrashDumps</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="356b8-121"><strong>DumpCount</strong></span><span class="sxs-lookup"><span data-stu-id="356b8-121"><strong>DumpCount</strong></span></span></td>
<td><span data-ttu-id="356b8-122">資料夾中傾印檔案的最大數目。</span><span class="sxs-lookup"><span data-stu-id="356b8-122">The maximum number of dump files in the folder.</span></span> <span data-ttu-id="356b8-123">當超過最大值時，資料夾中最舊的傾印檔案將會取代為新的傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="356b8-123">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span></td>
<td><span data-ttu-id="356b8-124">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="356b8-124">REG_DWORD</span></span></td>
<td><span data-ttu-id="356b8-125">10</span><span class="sxs-lookup"><span data-stu-id="356b8-125">10</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="356b8-126"><strong>DumpType</strong></span><span class="sxs-lookup"><span data-stu-id="356b8-126"><strong>DumpType</strong></span></span></td>
<td><span data-ttu-id="356b8-127">指定下列其中一種傾印類型：</span><span class="sxs-lookup"><span data-stu-id="356b8-127">Specify one of the following dump types:</span></span>
<ul>
<li><span data-ttu-id="356b8-128">0：自訂傾印</span><span class="sxs-lookup"><span data-stu-id="356b8-128">0: Custom dump</span></span></li>
<li><span data-ttu-id="356b8-129">1：迷你傾印</span><span class="sxs-lookup"><span data-stu-id="356b8-129">1: Mini dump</span></span></li>
<li><span data-ttu-id="356b8-130">2：完整傾印</span><span class="sxs-lookup"><span data-stu-id="356b8-130">2: Full dump</span></span></li>
</ul></td>
<td><span data-ttu-id="356b8-131">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="356b8-131">REG_DWORD</span></span></td>
<td><span data-ttu-id="356b8-132">1</span><span class="sxs-lookup"><span data-stu-id="356b8-132">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="356b8-133"><strong>CustomDumpFlags</strong></span><span class="sxs-lookup"><span data-stu-id="356b8-133"><strong>CustomDumpFlags</strong></span></span></td>
<td><span data-ttu-id="356b8-134">要使用的自訂傾印選項。</span><span class="sxs-lookup"><span data-stu-id="356b8-134">The custom dump options to be used.</span></span> <span data-ttu-id="356b8-135">只有當 <strong>DumpType</strong> 設為0時，才會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="356b8-135">This value is used only when <strong>DumpType</strong> is set to 0.</span></span><br/> <span data-ttu-id="356b8-136">這些選項是 <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> 列舉值的位元組合。</span><span class="sxs-lookup"><span data-stu-id="356b8-136">The options are a bitwise combination of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeration values.</span></span><br/></td>
<td><span data-ttu-id="356b8-137">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="356b8-137">REG_DWORD</span></span></td>
<td><code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData.</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> <span data-ttu-id="356b8-138">當您 [為 **應用程式**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes)損毀設定自動偵測時，不會收集損毀傾印。</span><span class="sxs-lookup"><span data-stu-id="356b8-138">A crash dump is not collected when you set [automatic debugging for **application** crashes](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span></span> 

<span data-ttu-id="356b8-139">這些登錄值代表全域設定。</span><span class="sxs-lookup"><span data-stu-id="356b8-139">These registry values represent the global settings.</span></span> <span data-ttu-id="356b8-140">您也可以提供覆寫全域設定的每個應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="356b8-140">You can also provide per-application settings that override the global settings.</span></span> <span data-ttu-id="356b8-141">若要建立每個應用程式的設定，請在 [ **HKEY \_ local \_ machine \\ software \\ microsoft \\ windows \\ Windows 錯誤報告 (\\ LocalDumps** ] 下，為您的應用程式建立新的金鑰，例如 **HKEY \_ local \_ machine \\ software \\ microsoft \\ windows \\ Windows 錯誤報告 \\ LocalDumps \\MyApplication.exe**) 。</span><span class="sxs-lookup"><span data-stu-id="356b8-141">To create a per-application setting, create a new key for your application under **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** (for example, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps\\MyApplication.exe**).</span></span> <span data-ttu-id="356b8-142">在 **MyApplication.exe** 機碼下新增傾印設定。</span><span class="sxs-lookup"><span data-stu-id="356b8-142">Add your dump settings under the **MyApplication.exe** key.</span></span> <span data-ttu-id="356b8-143">如果您的應用程式當機，則 WER 會先讀取全域設定，然後使用您的應用程式特定設定來覆寫任何設定。</span><span class="sxs-lookup"><span data-stu-id="356b8-143">If your application crashes, WER will first read the global settings, and then will override any of the settings with your application-specific settings.</span></span>

<span data-ttu-id="356b8-144">當應用程式損毀並在終止之前，系統會檢查登錄設定，以判斷是否要收集本機傾印。</span><span class="sxs-lookup"><span data-stu-id="356b8-144">After an application crashes and prior to its termination, the system will check the registry settings to determine whether a local dump is to be collected.</span></span> <span data-ttu-id="356b8-145">傾印收集完成後，應用程式就可以正常終止。</span><span class="sxs-lookup"><span data-stu-id="356b8-145">After the dump collection has completed, the application will be allowed to terminate normally.</span></span> <span data-ttu-id="356b8-146">如果應用程式支援復原，則在呼叫復原回呼之前，會先收集本機傾印。</span><span class="sxs-lookup"><span data-stu-id="356b8-146">If the application supports recovery, the local dump is collected before the recovery callback is called.</span></span>

<span data-ttu-id="356b8-147">這些傾印會獨立于 WER 基礎結構的其餘部分來設定和控制。</span><span class="sxs-lookup"><span data-stu-id="356b8-147">These dumps are configured and controlled independently of the rest of the WER infrastructure.</span></span> <span data-ttu-id="356b8-148">即使已停用 WER 或使用者取消 WER 報表，您也可以使用本機傾印集合。</span><span class="sxs-lookup"><span data-stu-id="356b8-148">You can make use of the local dump collection even if WER is disabled or if the user cancels WER reporting.</span></span> <span data-ttu-id="356b8-149">本機傾印可能不同于傳送給 Microsoft 的傾印。</span><span class="sxs-lookup"><span data-stu-id="356b8-149">The local dump can be different than the dump sent to Microsoft.</span></span>

 

