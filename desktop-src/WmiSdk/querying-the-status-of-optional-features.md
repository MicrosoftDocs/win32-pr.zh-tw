---
description: 在 Windows 7 中，WMI 已實作為 Win32 \_ OptionalFeature 類別。 此類別會抓取存在於電腦上之選用功能的狀態。
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: 查詢選用功能的狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecffe6ddbe9b860c6f49fe12d3fed500c169bef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476704"
---
# <a name="querying-the-status-of-optional-features"></a>查詢選用功能的狀態

在 Windows 7 中，WMI 已實作為 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)類別。 此類別會抓取存在於電腦上之選用功能的狀態。

您可以使用 Windows PowerShell Cmdlet 來查詢選用功能的狀態。 本主題中的所有範例都使用 Get-WmiObject Cmdlet。 如需詳細資訊，請參閱 [>get-wmiobject](/previous-versions//dd315295(v=technet.10))。

**取得電腦上所有選用功能的實例**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject Win32_OptionalFeature</code></pre> | 


    

**藉由指定功能名稱來查詢選用功能**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from Win32_OptionalFeature where name = 'TelnetClient'"</code></pre> | 


    

    > [!Note]  
    > The **name** property is case-sensitive.

     

**藉由指定安裝狀態來查詢選用功能**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from win32_optionalfeature where installstate= 1"</code></pre> | 


    

    For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
