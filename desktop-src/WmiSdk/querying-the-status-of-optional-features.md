---
description: 在 Windows 7 中，WMI 已實作為 Win32 \_ OptionalFeature 類別。 此類別會抓取存在於電腦上之選用功能的狀態。
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: 查詢選用功能的狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec27457336adcc5c358aad0a5e139c1c7c07f6bcb72335ec549f9ca98cc1e5a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996028"
---
# <a name="querying-the-status-of-optional-features"></a>查詢選用功能的狀態

在 Windows 7 中，WMI 已實作為 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)類別。 此類別會抓取存在於電腦上之選用功能的狀態。

您可以使用 Windows PowerShell Cmdlet 來查詢選用功能的狀態。 本主題中的所有範例都使用 Get-WmiObject Cmdlet。 如需詳細資訊，請參閱 [>get-wmiobject](/previous-versions//dd315295(v=technet.10))。

**取得電腦上所有選用功能的實例**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

**藉由指定功能名稱來查詢選用功能**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > **Name** 屬性會區分大小寫。

     

**藉由指定安裝狀態來查詢選用功能**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    如需 **InstallState** 屬性可能值的詳細資訊，請參閱 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
