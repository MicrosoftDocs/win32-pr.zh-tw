---
title: BITS PowerShell 命令的受管理參考
description: 背景智慧型傳送服務 (位) 4.0 可以使用 Windows PowerShell Cmdlet 來管理傳送作業。
ms.assetid: 2c151dfe-4f89-41ea-a533-21ffcf0aa39e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bd195d2202849c2bf2df580d159ee401911c51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842523"
---
# <a name="managed-reference-for-bits-powershell-commands"></a><span data-ttu-id="a7075-103">BITS PowerShell 命令的受管理參考</span><span class="sxs-lookup"><span data-stu-id="a7075-103">Managed Reference for BITS PowerShell Commands</span></span>

<span data-ttu-id="a7075-104">背景智慧型傳送服務 (位) 4.0 可以使用 Windows PowerShell Cmdlet 來建立和管理檔案下載和上傳傳送作業。</span><span class="sxs-lookup"><span data-stu-id="a7075-104">Background Intelligent Transfer Service (BITS) 4.0 can use Windows PowerShell cmdlets to create and manage file download and upload transfer jobs.</span></span>

```PowerShell
Import-Module BitsTransfer
mkdir -force c:\temp\BITSFILES
Start-BitsTransfer -Source https://aka.ms/WinServ16/StndPDF -Destination c:\temp\BITSFILES\WindowsServer2016.pdf
```

<span data-ttu-id="a7075-105">適用于 BITS 的 Windows PowerShell Cmdlet 提供許多與 bitsadmin 命令列公用程式相同的功能。</span><span class="sxs-lookup"><span data-stu-id="a7075-105">Windows PowerShell cmdlets for BITS provide much of the same functionality as the bitsadmin command-line utility.</span></span> <span data-ttu-id="a7075-106">不過，Windows PowerShell 也會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="a7075-106">However, Windows PowerShell also does the following:</span></span>

-   <span data-ttu-id="a7075-107">使用可延伸和管理導向的指令碼語言來自動化 BITS 工作。</span><span class="sxs-lookup"><span data-stu-id="a7075-107">Automates BITS tasks in an extensible and management-oriented scripting language.</span></span>
-   <span data-ttu-id="a7075-108">提供適用于所有作業相關工作的單一工具。</span><span class="sxs-lookup"><span data-stu-id="a7075-108">Provides a single tool for all job-related tasks.</span></span>

> [!Note]  
> <span data-ttu-id="a7075-109">若要使用這些命令，您必須先使用命令匯入 BITS PowerShell 模組 `Import-Module BitsTransfer` 。</span><span class="sxs-lookup"><span data-stu-id="a7075-109">To use these commands, you must first import the BITS PowerShell module, using the `Import-Module BitsTransfer` command.</span></span> <span data-ttu-id="a7075-110">如需詳細資訊，請參閱下列 [TechNet 文章](/previous-versions/technet-magazine/ff382721(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="a7075-110">For more information, see the following [TechNet article](/previous-versions/technet-magazine/ff382721(v=msdn.10)).</span></span>

 

<span data-ttu-id="a7075-111">如需有關使用 Windows Powershell 的詳細資訊，請參閱 [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="a7075-111">For more information on using Windows Powershell, see [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).</span></span>

## <a name="bits-powershell-classes"></a><span data-ttu-id="a7075-112">BITS PowerShell 類別</span><span class="sxs-lookup"><span data-stu-id="a7075-112">BITS PowerShell Classes</span></span>

<span data-ttu-id="a7075-113">**命名空間**： Microsoft. BackgroundIntelligentTransfer. 管理</span><span class="sxs-lookup"><span data-stu-id="a7075-113">**Namespace**: Microsoft.BackgroundIntelligentTransfer.Management</span></span>

<span data-ttu-id="a7075-114">**元件**： System. Management. Automation</span><span class="sxs-lookup"><span data-stu-id="a7075-114">**Assembly**: System.Management.Automation</span></span>

<span data-ttu-id="a7075-115">這些位命令類別是由 Windows PowerShell 所執行。</span><span class="sxs-lookup"><span data-stu-id="a7075-115">These BITS command classes are implemented by Windows PowerShell.</span></span> <span data-ttu-id="a7075-116">這些類別包含在此軟體發展工具組中， (SDK) 僅供完整性之用。</span><span class="sxs-lookup"><span data-stu-id="a7075-116">These classes are included in this software development kit (SDK) for completeness only.</span></span> <span data-ttu-id="a7075-117">這些類別的成員不能直接使用，也不能用來衍生其他類別。</span><span class="sxs-lookup"><span data-stu-id="a7075-117">The members of these classes cannot be used directly, nor should they be used to derive other classes.</span></span>



| <span data-ttu-id="a7075-118">類別</span><span class="sxs-lookup"><span data-stu-id="a7075-118">Class</span></span>                           | <span data-ttu-id="a7075-119">描述</span><span class="sxs-lookup"><span data-stu-id="a7075-119">Description</span></span>                                                                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7075-120">**AddBitsFileCommand**</span><span class="sxs-lookup"><span data-stu-id="a7075-120">**AddBitsFileCommand**</span></span>          | <span data-ttu-id="a7075-121">將一或多個檔案新增至現有的 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="a7075-121">Adds one or more files to an existing BITS transfer job.</span></span><br/> <span data-ttu-id="a7075-122">如需有關參數的詳細資訊和範例，請參閱 [add-bitsfile](/previous-versions//dd347701(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7075-122">See the [Add-BitsFile](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                       |
| <span data-ttu-id="a7075-123">**ClearBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="a7075-123">**ClearBitsTransferCommand**</span></span>    | <span data-ttu-id="a7075-124">取消 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="a7075-124">Cancels a BITS transfer job.</span></span><br/> <span data-ttu-id="a7075-125">如需參數的詳細資訊和範例，請參閱 [BitsTransfer]( /previous-versions//dd347701(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7075-125">See the [Clear-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                          |
| <span data-ttu-id="a7075-126">**CompleteBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="a7075-126">**CompleteBitsTransferCommand**</span></span> | <span data-ttu-id="a7075-127">完成 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="a7075-127">Completes a BITS transfer job.</span></span><br/> <span data-ttu-id="a7075-128">如需參數的詳細資訊和範例，請參閱 [BitsTransfer]( /previous-versions//dd347701(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7075-128">See the [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                     |
| <span data-ttu-id="a7075-129">**GetBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="a7075-129">**GetBitsTransferCommand**</span></span>      | <span data-ttu-id="a7075-130">抓取現有 BITS 傳送工作的相關聯 BitsJob 物件。</span><span class="sxs-lookup"><span data-stu-id="a7075-130">Retrieves the associated BitsJob object for an existing BITS transfer job.</span></span><br/> <span data-ttu-id="a7075-131">如需參數的詳細資訊和範例，請參閱 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7075-131">See the [Get-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/> |
| <span data-ttu-id="a7075-132">**NewBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="a7075-132">**NewBitsTransferCommand**</span></span>      | <span data-ttu-id="a7075-133">建立新的 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="a7075-133">Creates a new BITS transfer job.</span></span><br/> <span data-ttu-id="a7075-134">如需參數的詳細資訊和範例，請參閱 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7075-134">See the [New-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                           |
| <span data-ttu-id="a7075-135">**ResumeBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="a7075-135">**ResumeBitsTransferCommand**</span></span>   | <span data-ttu-id="a7075-136">繼續 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="a7075-136">Resumes a BITS transfer job.</span></span><br/> <span data-ttu-id="a7075-137">如需參數的詳細資訊和範例，請參閱 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7075-137">See the [Resume-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                            |
| <span data-ttu-id="a7075-138">**SetBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="a7075-138">**SetBitsTransferCommand**</span></span>      | <span data-ttu-id="a7075-139">修改現有 BITS 傳送工作的屬性。</span><span class="sxs-lookup"><span data-stu-id="a7075-139">Modifies the properties of an existing BITS transfer job.</span></span><br/> <span data-ttu-id="a7075-140">如需參數的詳細資訊和範例，請參閱 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7075-140">See the [Set-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                  |
| <span data-ttu-id="a7075-141">**SuspendBitsTransferCommand**</span><span class="sxs-lookup"><span data-stu-id="a7075-141">**SuspendBitsTransferCommand**</span></span>  | <span data-ttu-id="a7075-142">暫停 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="a7075-142">Suspends a BITS transfer job.</span></span><br/> <span data-ttu-id="a7075-143">如需有關參數的詳細資訊和範例，請參閱 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7075-143">See the [Suspend-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                          |



 

 

