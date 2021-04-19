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
# <a name="version-helper-functions"></a>版本 Helper 函數

您可以使用下列函式來判斷目前的作業系統版本，或識別它是 Windows 或 Windows Server 版本。 這些函式會提供簡單的測試，以使用 [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) 函式和建議的大於或等於比較，以確定作業系統版本的健全方法。

> [!Note]  
> 這些 Api 是由 Windows 8.1 軟體發展工具組 (SDK) 中包含的 **versionhelpers** 所定義。 這個檔案可以與其他 Microsoft Visual Studio 版本搭配使用，以在 Windows 8.1 之前，對 Windows 版本執行相同的功能。

<table>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows XP 版本。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows XP Service Pack 1 (SP1) 版本。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows XP Service Pack 2 (SP2) 版本。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows XP Service Pack 3 (SP3) 版本。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows Vista 版本。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows Vista （含 Service Pack 1） (SP1) 版本。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows Vista （含 Service Pack 2） (SP2) 版本。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows 7 版本。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows 7 Service Pack 1 (SP1) 版本。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows 8 版本。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows 8.1 版本。<br/> 針對 Windows 10，除非應用程式包含的資訊清單包含包含指定 Windows 8.1 和/或 Windows 10 之 Guid 的相容性區段，否則 <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> 會傳回 false。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></td>
<td>指出目前的作業系統版本是否符合或大於 Windows 10 版本。<br/> 針對 Windows 10，除非應用程式包含包含指定 Windows 10 之 GUID 的相容性區段的資訊清單，否則 <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> 會傳回 false。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></td>
<td>指出目前的作業系統是否為 Windows Server 版本。 需要區分伺服器和用戶端版本之 Windows 的應用程式應該呼叫此函式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></td>
<td>
<blockquote>如果其他提供的版本協助程式函式不符合您的案例，您應該只使用此函式。</blockquote>
<br/>指出目前的作業系統版本是否符合或大於提供的版本資訊。 當您確認未與用戶端版本共用版本號碼的 Windows Server 版本時，此功能很有用。
</td>
</tr>
</tbody>
</table>

## <a name="example"></a>範例

**VersionHelpers .h** 標頭檔中定義的內嵌函式可讓您在測試某個版本的 Windows 時，藉由傳回 **布林** 值來確認作業系統版本。

例如，如果您的應用程式需要 Windows 8 或更新版本，請使用下列測試。

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a>相關主題

- [OSVERSIONINFOEX](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
