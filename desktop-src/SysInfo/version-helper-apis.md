---
description: 您可以使用下列函式來判斷目前的作業系統版本，或識別它是 Windows 或 Windows Server 版本。
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: 版本 Helper 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746e6488d949fe6512355d7ef9910c26aaf3b54b
ms.sourcegitcommit: 49df0f62429d21bca96d8704205048267ee0eb59
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2021
ms.locfileid: "106997758"
---
# <a name="version-helper-functions"></a><span data-ttu-id="9626a-103">版本 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="9626a-103">Version Helper functions</span></span>

<span data-ttu-id="9626a-104">您可以使用下列函式來判斷目前的作業系統版本，或識別它是 Windows 或 Windows Server 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-104">The following functions can be used to determine the current operating system version or identify whether it is a Windows or Windows Server release.</span></span> <span data-ttu-id="9626a-105">這些函式會提供簡單的測試，以使用 [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) 函式和建議的大於或等於比較，以確定作業系統版本的健全方法。</span><span class="sxs-lookup"><span data-stu-id="9626a-105">These functions provide simple tests that use the [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) function and the recommended greater than or equal to comparisons that are proven as a robust means to determine the operating system version.</span></span>

> [!Note]  
> <span data-ttu-id="9626a-106">這些 Api 是由 Windows 8.1 軟體發展工具組 (SDK) 中包含的 **versionhelpers** 所定義。</span><span class="sxs-lookup"><span data-stu-id="9626a-106">These APIs are defined by **versionhelpers.h**, which is included in the Windows 8.1 software development kit (SDK).</span></span> <span data-ttu-id="9626a-107">這個檔案可以與其他 Microsoft Visual Studio 版本搭配使用，以在 Windows 8.1 之前，對 Windows 版本執行相同的功能。</span><span class="sxs-lookup"><span data-stu-id="9626a-107">This file can be used with other Microsoft Visual Studio releases to implement the same functionality for Windows versions prior to Windows 8.1.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9626a-108">函式</span><span class="sxs-lookup"><span data-stu-id="9626a-108">Function</span></span></th>
<th><span data-ttu-id="9626a-109">描述</span><span class="sxs-lookup"><span data-stu-id="9626a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9626a-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-111">指出目前的作業系統版本是否符合或大於 Windows XP 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-111">Indicates if the current OS version matches, or is greater than, the Windows XP version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9626a-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-113">指出目前的作業系統版本是否符合或大於 Windows XP Service Pack 1 (SP1) 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-113">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9626a-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-115">指出目前的作業系統版本是否符合或大於 Windows XP Service Pack 2 (SP2) 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-115">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9626a-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-117">指出目前的作業系統版本是否符合或大於 Windows XP Service Pack 3 (SP3) 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-117">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 3 (SP3) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9626a-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-119">指出目前的作業系統版本是否符合或大於 Windows Vista 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-119">Indicates if the current OS version matches, or is greater than, the Windows Vista version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9626a-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-121">指出目前的作業系統版本是否符合或大於 Windows Vista （含 Service Pack 1） (SP1) 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-121">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9626a-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-123">指出目前的作業系統版本是否符合或大於 Windows Vista （含 Service Pack 2） (SP2) 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-123">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9626a-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-125">指出目前的作業系統版本是否符合或大於 Windows 7 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-125">Indicates if the current OS version matches, or is greater than, the Windows 7 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9626a-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-127">指出目前的作業系統版本是否符合或大於 Windows 7 Service Pack 1 (SP1) 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-127">Indicates if the current OS version matches, or is greater than, the Windows 7 with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9626a-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-129">指出目前的作業系統版本是否符合或大於 Windows 8 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-129">Indicates if the current OS version matches, or is greater than, the Windows 8 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9626a-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-131">指出目前的作業系統版本是否符合或大於 Windows 8.1 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-131">Indicates if the current OS version matches, or is greater than, the Windows 8.1 version.</span></span><br/> <span data-ttu-id="9626a-132">針對 Windows 10，除非應用程式包含的資訊清單包含包含指定 Windows 8.1 和/或 Windows 10 之 Guid 的相容性區段，否則 <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> 會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="9626a-132">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUIDs that designate Windows 8.1 and/or Windows 10.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9626a-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="9626a-134">指出目前的作業系統版本是否符合或大於 Windows 10 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-134">Indicates if the current OS version matches, or is greater than, the Windows 10 version.</span></span><br/> <span data-ttu-id="9626a-135">針對 Windows 10，除非應用程式包含包含指定 Windows 10 之 GUID 的相容性區段的資訊清單，否則 <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> 會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="9626a-135">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUID that designates Windows 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9626a-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span></span></td>
<td><span data-ttu-id="9626a-137">指出目前的作業系統是否為 Windows Server 版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-137">Indicates if the current OS is a Windows Server release.</span></span> <span data-ttu-id="9626a-138">需要區分伺服器和用戶端版本之 Windows 的應用程式應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="9626a-138">Applications that need to distinguish between server and client versions of Windows should call this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9626a-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="9626a-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span></span></td>
<td>
<blockquote><span data-ttu-id="9626a-140">如果其他提供的版本協助程式函式不符合您的案例，您應該只使用此函式。</span><span class="sxs-lookup"><span data-stu-id="9626a-140">You should only use this function if the other provided version helper functions do not fit your scenario.</span></span></blockquote>
<br/><span data-ttu-id="9626a-141">指出目前的作業系統版本是否符合或大於提供的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="9626a-141">Indicates if the current OS version matches, or is greater than, the provided version information.</span></span> <span data-ttu-id="9626a-142">當您確認未與用戶端版本共用版本號碼的 Windows Server 版本時，此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="9626a-142">This function is useful in confirming a version of Windows Server that doesn't share a version number with a client release.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="9626a-143">範例</span><span class="sxs-lookup"><span data-stu-id="9626a-143">Example</span></span>

<span data-ttu-id="9626a-144">**VersionHelpers .h** 標頭檔中定義的內嵌函式可讓您在測試某個版本的 Windows 時，藉由傳回 **布林** 值來確認作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="9626a-144">The inline functions defined in the **VersionHelpers.h** header file let you verify the operating system version by returning a **Boolean** value when testing for a version of Windows.</span></span>

<span data-ttu-id="9626a-145">例如，如果您的應用程式需要 Windows 8 或更新版本，請使用下列測試。</span><span class="sxs-lookup"><span data-stu-id="9626a-145">For example, if your application requires Windows 8 or later, use the following test.</span></span>

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a><span data-ttu-id="9626a-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="9626a-146">Related topics</span></span>

- [<span data-ttu-id="9626a-147">OSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="9626a-147">OSVERSIONINFOEX</span></span>](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
