---
description: WMI Windows PowerShell 命令類別的受控參考
ms.assetid: 30e77956-8428-4259-9218-b93f143fd987
ms.tgt_platform: multiple
title: WMI Windows PowerShell 命令類別的受控參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb309a9ca421a3966f84ba1ae825bd0c81eee8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997562"
---
# <a name="managed-reference-for-wmi-windows-powershell-command-classes"></a><span data-ttu-id="06fc6-103">WMI Windows PowerShell 命令類別的受控參考</span><span class="sxs-lookup"><span data-stu-id="06fc6-103">Managed Reference for WMI Windows PowerShell Command Classes</span></span>

<span data-ttu-id="06fc6-104">Windows PowerShell 透過一組 Cmdlet 來執行 Windows Management Instrumentation (WMI) 功能。</span><span class="sxs-lookup"><span data-stu-id="06fc6-104">Windows PowerShell implements Windows Management Instrumentation (WMI) functionality through a set of cmdlets.</span></span> <span data-ttu-id="06fc6-105">您可以使用這些 Cmdlet 來完成管理本機和遠端電腦所需的端對端工作。</span><span class="sxs-lookup"><span data-stu-id="06fc6-105">You can use these cmdlets to complete the end-to-end tasks that are necessary to manage local and remote computers.</span></span>

<span data-ttu-id="06fc6-106">如需詳細資訊，請參閱 [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) 。</span><span class="sxs-lookup"><span data-stu-id="06fc6-106">See [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) for more information.</span></span>

## <a name="wmi-powershell-classes"></a><span data-ttu-id="06fc6-107">WMI PowerShell 類別</span><span class="sxs-lookup"><span data-stu-id="06fc6-107">WMI PowerShell Classes</span></span>

<span data-ttu-id="06fc6-108">**命名空間**： Microsoft. 命令</span><span class="sxs-lookup"><span data-stu-id="06fc6-108">**Namespace**: Microsoft.PowerShell.Commands</span></span>

<span data-ttu-id="06fc6-109">**元件**： Microsoft. 命令. 管理</span><span class="sxs-lookup"><span data-stu-id="06fc6-109">**Assembly**: Microsoft.PowerShell.Commands.Management</span></span>

<span data-ttu-id="06fc6-110">**DLL**： Microsoft.PowerShell.Commands.Management.dll</span><span class="sxs-lookup"><span data-stu-id="06fc6-110">**DLL**: Microsoft.PowerShell.Commands.Management.dll</span></span>

<span data-ttu-id="06fc6-111">這些 WMI 命令類別是由 Windows PowerShell 所執行。</span><span class="sxs-lookup"><span data-stu-id="06fc6-111">These WMI command classes are implemented by Windows PowerShell.</span></span> <span data-ttu-id="06fc6-112">這些類別包含在此軟體發展工具組中， (SDK) 僅供完整性之用。</span><span class="sxs-lookup"><span data-stu-id="06fc6-112">These classes are included in this software development kit (SDK) for completeness only.</span></span> <span data-ttu-id="06fc6-113">這些類別的成員不能直接使用，也不能用來衍生其他類別。</span><span class="sxs-lookup"><span data-stu-id="06fc6-113">The members of these classes cannot be used directly, nor should they be used to derive other classes.</span></span>



| <span data-ttu-id="06fc6-114">類別</span><span class="sxs-lookup"><span data-stu-id="06fc6-114">Class</span></span>                   | <span data-ttu-id="06fc6-115">描述</span><span class="sxs-lookup"><span data-stu-id="06fc6-115">Description</span></span>                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06fc6-116">GetWmiObjectCommand</span><span class="sxs-lookup"><span data-stu-id="06fc6-116">GetWmiObjectCommand</span></span>     | <span data-ttu-id="06fc6-117">取得 WMI 類別的實例或可用類別的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="06fc6-117">Gets instances of WMI classes or information about the available classes.</span></span><br/> <span data-ttu-id="06fc6-118">如需有關參數的範例和詳細資訊，請參閱 [>get-wmiobject](/previous-versions//dd315295(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06fc6-118">See the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/> |
| <span data-ttu-id="06fc6-119">InvokeWmiMethod</span><span class="sxs-lookup"><span data-stu-id="06fc6-119">InvokeWmiMethod</span></span>         | <span data-ttu-id="06fc6-120">呼叫 WMI 方法。</span><span class="sxs-lookup"><span data-stu-id="06fc6-120">Calls WMI methods.</span></span><br/> <span data-ttu-id="06fc6-121">如需有關參數的範例和詳細資訊，請參閱 [>invoke-wmimethod](/previous-versions//dd315300(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06fc6-121">See the [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                                     |
| <span data-ttu-id="06fc6-122">RegisterWmiEventCommand</span><span class="sxs-lookup"><span data-stu-id="06fc6-122">RegisterWmiEventCommand</span></span> | <span data-ttu-id="06fc6-123">訂閱 WMI 事件。</span><span class="sxs-lookup"><span data-stu-id="06fc6-123">Subscribes to a WMI event.</span></span><br/> <span data-ttu-id="06fc6-124">如需有關參數的範例和詳細資訊，請參閱 [>register-wmievent](/previous-versions//dd315242(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06fc6-124">See the [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                            |
| <span data-ttu-id="06fc6-125">RemoveWmiObject</span><span class="sxs-lookup"><span data-stu-id="06fc6-125">RemoveWmiObject</span></span>         | <span data-ttu-id="06fc6-126">刪除現有 WMI 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="06fc6-126">Deletes an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="06fc6-127">如需有關參數的範例和詳細資訊，請參閱 [>get-wmiobject](/previous-versions//dd347605(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06fc6-127">See the [Remove-WmiObject](/previous-versions//dd347605(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                          |
| <span data-ttu-id="06fc6-128">SetWmiInstance</span><span class="sxs-lookup"><span data-stu-id="06fc6-128">SetWmiInstance</span></span>          | <span data-ttu-id="06fc6-129">建立或更新現有 WMI 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="06fc6-129">Creates or updates an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="06fc6-130">如需有關參數的範例和詳細資訊，請參閱 [set-wmiinstance](/previous-versions//dd315391(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06fc6-130">See the [Set-WmiInstance](/previous-versions//dd315391(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                |



 

 

