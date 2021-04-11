---
description: 在 Windows 7 中，WMI 已實作為 Win32 \_ OptionalFeature 類別。 此類別會抓取存在於電腦上之選用功能的狀態。
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: 查詢選用功能的狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c190b2a2143dae1e22c30b3e5e803908bcb4116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692344"
---
# <a name="querying-the-status-of-optional-features"></a><span data-ttu-id="130bc-104">查詢選用功能的狀態</span><span class="sxs-lookup"><span data-stu-id="130bc-104">Querying the Status of Optional Features</span></span>

<span data-ttu-id="130bc-105">在 Windows 7 中，WMI 已實作為 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) 類別。</span><span class="sxs-lookup"><span data-stu-id="130bc-105">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="130bc-106">此類別會抓取存在於電腦上之選用功能的狀態。</span><span class="sxs-lookup"><span data-stu-id="130bc-106">This class retrieves the status of the optional features that are present on a computer.</span></span>

<span data-ttu-id="130bc-107">您可以使用 Windows PowerShell Cmdlet 來查詢選用功能的狀態。</span><span class="sxs-lookup"><span data-stu-id="130bc-107">You can use Windows PowerShell cmdlets to query the status of optional features.</span></span> <span data-ttu-id="130bc-108">本主題中的所有範例都使用 Get-WmiObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="130bc-108">All of the examples in this topic use the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="130bc-109">如需詳細資訊，請參閱 [>get-wmiobject](/previous-versions//dd315295(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="130bc-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

<span data-ttu-id="130bc-110">**取得電腦上所有選用功能的實例**</span><span class="sxs-lookup"><span data-stu-id="130bc-110">**To retrieve all instances of optional features present on a computer**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="130bc-111">PowerShell</span><span class="sxs-lookup"><span data-stu-id="130bc-111">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

<span data-ttu-id="130bc-112">**藉由指定功能名稱來查詢選用功能**</span><span class="sxs-lookup"><span data-stu-id="130bc-112">**To query for an optional feature by specifying the feature name**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="130bc-113">PowerShell</span><span class="sxs-lookup"><span data-stu-id="130bc-113">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > <span data-ttu-id="130bc-114">**Name** 屬性會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="130bc-114">The **name** property is case-sensitive.</span></span>

     

<span data-ttu-id="130bc-115">**藉由指定安裝狀態來查詢選用功能**</span><span class="sxs-lookup"><span data-stu-id="130bc-115">**To query for optional features by specifying the install state**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="130bc-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="130bc-116">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    <span data-ttu-id="130bc-117">如需 **InstallState** 屬性可能值的詳細資訊，請參閱 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)。</span><span class="sxs-lookup"><span data-stu-id="130bc-117">For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span></span>

## <a name="related-topics"></a><span data-ttu-id="130bc-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="130bc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="130bc-119">**Win32 \_ OptionalFeature**</span><span class="sxs-lookup"><span data-stu-id="130bc-119">**Win32\_OptionalFeature**</span></span>](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
