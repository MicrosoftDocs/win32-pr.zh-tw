---
description: Windows 7 和 Windows Server 2008 R2 中的 AppInit_DLLs
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: Windows 7 中的 AppInit_DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820fcb9840bbec139ff78f3c6cc082b2dca4eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088706"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="14142-103">\_在 windows 7 和 Windows Server 2008 R2 中 AppInit dll</span><span class="sxs-lookup"><span data-stu-id="14142-103">AppInit\_DLLs in Windows 7 and Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="14142-104">平台</span><span class="sxs-lookup"><span data-stu-id="14142-104">Platform</span></span>

<span data-ttu-id="14142-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="14142-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="14142-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14142-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="14142-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="14142-107">Feature Impact</span></span>

 <span data-ttu-id="14142-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="14142-108">**Severity** - Low</span></span>  
<span data-ttu-id="14142-109">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="14142-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="14142-110">Description</span><span class="sxs-lookup"><span data-stu-id="14142-110">Description</span></span>

<span data-ttu-id="14142-111">AppInit \_ dll 是一種機制，可讓您將任意 dll 清單載入系統上的每個使用者模式進程。</span><span class="sxs-lookup"><span data-stu-id="14142-111">AppInit\_DLLs is a mechanism that allows an arbitrary list of DLLs to be loaded into each user mode process on the system.</span></span> <span data-ttu-id="14142-112">Microsoft 正在修改 Windows 7 和 Windows Server 2008 R2 中的 AppInit Dll 功能，以加入新的程式碼簽署需求。</span><span class="sxs-lookup"><span data-stu-id="14142-112">Microsoft is modifying the AppInit DLLs facility in Windows 7 and Windows Server 2008 R2 to add a new code-signing requirement.</span></span> <span data-ttu-id="14142-113">這將有助於改善系統的可靠性和效能，以及改善軟體來源的可見度。</span><span class="sxs-lookup"><span data-stu-id="14142-113">This will help improve the system reliability and performance, as well as improve visibility into the origin of software.</span></span>

## <a name="configuration"></a><span data-ttu-id="14142-114">組態</span><span class="sxs-lookup"><span data-stu-id="14142-114">Configuration</span></span>

<span data-ttu-id="14142-115">儲存在 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft Windows NT CurrentVersion Windows 機碼下的值會 \\ \\ \\ 決定 AppInit \_ dll 基礎結構的行為。</span><span class="sxs-lookup"><span data-stu-id="14142-115">Values stored under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion \\Windows key in the registry determine the behavior of the AppInit\_DLLs infrastructure.</span></span> <span data-ttu-id="14142-116">下表描述這些登錄值：</span><span class="sxs-lookup"><span data-stu-id="14142-116">The table below describes these registry values:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="14142-117">值</span><span class="sxs-lookup"><span data-stu-id="14142-117">Value</span></span></th>
<th><span data-ttu-id="14142-118">描述</span><span class="sxs-lookup"><span data-stu-id="14142-118">Description</span></span></th>
<th><span data-ttu-id="14142-119">範例值</span><span class="sxs-lookup"><span data-stu-id="14142-119">Sample Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="14142-120">LoadAppInit_DLLs (REG_DWORD) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="14142-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="14142-121">全域啟用或停用 AppInit_DLLs。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="14142-121">Globally enables or disables AppInit_DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="14142-122">0x0 – AppInit_DLLs 已停用。</span><span class="sxs-lookup"><span data-stu-id="14142-122">0x0 – AppInit_DLLs are disabled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14142-123">0x1 –已啟用 AppInit_DLLs。</span><span class="sxs-lookup"><span data-stu-id="14142-123">0x1 – AppInit_DLLs are enabled.</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="14142-124">AppInit_DLLs (REG_SZ) </span><span class="sxs-lookup"><span data-stu-id="14142-124">AppInit_DLLs (REG_SZ)</span></span></td>
<td><span data-ttu-id="14142-125">要載入之 Dll 的空格或逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="14142-125">Space or comma delimited list of DLLs to load.</span></span> <span data-ttu-id="14142-126">DLL 的完整路徑應該使用簡短名稱來指定。</span><span class="sxs-lookup"><span data-stu-id="14142-126">The complete path to the DLL should be specified using Short Names.</span></span></td>
<td><span data-ttu-id="14142-127">C：\PROGRA ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</span><span class="sxs-lookup"><span data-stu-id="14142-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="14142-128">RequireSignedAppInit_DLLs (REG_DWORD) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="14142-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="14142-129">僅載入程式碼簽署的 Dll。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="14142-129">Only load code-signed DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="14142-130">0x0 –載入任何 Dll。</span><span class="sxs-lookup"><span data-stu-id="14142-130">0x0 – Load any DLLs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14142-131">0x1 –僅載入程式碼簽署的 Dll。</span><span class="sxs-lookup"><span data-stu-id="14142-131">0x1 – Load only code-signed DLLs.</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="14142-132">**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="14142-132">**Windows 7**</span></span>

<span data-ttu-id="14142-133">AppInit dll 基礎結構載入的所有 Dll 都 \_ 應進行程式碼簽署。</span><span class="sxs-lookup"><span data-stu-id="14142-133">All DLLs that are loaded by the AppInit\_DLLs infrastructure should be code-signed.</span></span> <span data-ttu-id="14142-134">在應用程式相容性方面，Windows 7 作業系統會載入所有的 AppInit Dll。</span><span class="sxs-lookup"><span data-stu-id="14142-134">In the interests of application compatibility, the Windows 7 Operating System will load all AppInit DLLs.</span></span> <span data-ttu-id="14142-135">不過，Microsoft 建議所有應用程式開發人員對其 Dll 進行程式碼簽署，以協助改善 Windows 的可靠性，並準備好在未來的 Windows 版本中強制執行程式碼簽署。</span><span class="sxs-lookup"><span data-stu-id="14142-135">However, Microsoft recommends that all application developers code-sign their DLLs to help improve the reliability of Windows and prepare for code-signing enforcement in future versions of Windows.</span></span> <span data-ttu-id="14142-136">RequireSignedAppInit \_ dll 登錄機碼可控制這項行為，而在 Windows 7 上的值預設會設定為0。</span><span class="sxs-lookup"><span data-stu-id="14142-136">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows 7 is set to 0 by default.</span></span>

<span data-ttu-id="14142-137">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="14142-137">**Windows Server 2008 R2**</span></span>

<span data-ttu-id="14142-138">AppInit dll 基礎結構載入的所有 Dll 都 \_ 必須以程式碼簽署。</span><span class="sxs-lookup"><span data-stu-id="14142-138">All DLLs that are loaded by the AppInit\_DLLs infrastructure must be code-signed.</span></span> <span data-ttu-id="14142-139">RequireSignedAppInit \_ dll 登錄機碼可控制這個行為，而在 Windows Server 2008 R2 上的值預設會設定為1。</span><span class="sxs-lookup"><span data-stu-id="14142-139">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows Server 2008 R2 is set to 1 by default.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="14142-140">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="14142-140">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="14142-141">在 Windows 7 和 Windows Server 2008 R2 中 AppInit Dll</span><span class="sxs-lookup"><span data-stu-id="14142-141">AppInit DLLs in Windows 7 and Windows Server 2008 R2</span></span>](/windows-hardware/drivers/install/)  
</dl>

 

 
