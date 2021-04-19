---
description: 瞭解如何使用標準使用者分析器 (SUA) tool 和 SUA Wizard 來測試您的應用程式，並偵測潛在的相容性問題。
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: 標準使用者分析器 (SUA) 工具和標準使用者分析器精靈 (SUA 精靈)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a897c603f185db775c059e4b3dd4a040cba9ad
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314581"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a><span data-ttu-id="36a65-103">標準使用者分析器 (SUA) 工具和標準使用者分析器精靈 (SUA 精靈)</span><span class="sxs-lookup"><span data-stu-id="36a65-103">Standard User Analyzer (SUA) Tool and Standard User Analyzer Wizard (SUA Wizard)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="36a65-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="36a65-104">Affected Platforms</span></span>

<span data-ttu-id="36a65-105">**用戶端：** Windows XP、Windows Vista、Windows 7</span><span class="sxs-lookup"><span data-stu-id="36a65-105">**Clients:** Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="36a65-106">**伺服器：** Windows Server 2003、Windows Server 2008、Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36a65-106">**Servers:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="36a65-107">描述</span><span class="sxs-lookup"><span data-stu-id="36a65-107">Description</span></span>

<span data-ttu-id="36a65-108">應用程式相容性工具組包含標準使用者分析器 (SUA) 工具和標準使用者分析器 Wizard (SUA Wizard) 。</span><span class="sxs-lookup"><span data-stu-id="36a65-108">The Application Compatibility Toolkit includes the Standard User Analyzer (SUA) tool and the Standard User Analyzer Wizard (SUA Wizard).</span></span> <span data-ttu-id="36a65-109">這些工具可讓您測試應用程式，並監視 API 呼叫，以便偵測由於 Windows 7 作業系統中的使用者帳戶控制 (UAC) 功能所造成的潛在相容性問題。</span><span class="sxs-lookup"><span data-stu-id="36a65-109">These tools enable you to test your applications and to monitor API calls in order to detect potential compatibility issues due to the User Account Control (UAC) feature in the Windows 7 operating system.</span></span>

<span data-ttu-id="36a65-110">UAC （先前稱為受限的使用者帳戶 (LUA) ）要求 (包括系統管理員群組成員的所有使用者) 以標準使用者身分執行，直到蓄意提高應用程式的許可權。</span><span class="sxs-lookup"><span data-stu-id="36a65-110">UAC, formerly known as Limited User Account (LUA), requires that all users (including members of the Administrator group) run as Standard Users by using the security prompt dialog box until the application is deliberately elevated.</span></span> <span data-ttu-id="36a65-111">不過，需要存取權的應用程式以及標準使用者無法使用之位置的許可權，無法正常執行標準使用者角色。</span><span class="sxs-lookup"><span data-stu-id="36a65-111">However, applications that require access and privileges for locations that are unavailable to a Standard User cannot run properly with the Standard User role.</span></span>

## <a name="usage"></a><span data-ttu-id="36a65-112">使用方式</span><span class="sxs-lookup"><span data-stu-id="36a65-112">Usage</span></span>

<span data-ttu-id="36a65-113">下列各節提供有關如何使用 SUA 和 SUA Wizard 工具的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="36a65-113">The following sections provide detailed information about how to use the SUA and SUA Wizard tools.</span></span>

<span data-ttu-id="36a65-114">**SUA 工具**</span><span class="sxs-lookup"><span data-stu-id="36a65-114">**SUA Tool**</span></span>

<span data-ttu-id="36a65-115">SUA 工具可讓您分析應用程式、查看有關 UAC 相關問題的詳細報告，然後套用建議和選取的應用程式緩和措施，如下列流程圖所示。</span><span class="sxs-lookup"><span data-stu-id="36a65-115">The SUA tool enables you to analyze an application, review a detailed report about the UAC-related issues, and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span>

![顯示 S U 工具的流程的圖表。](images/act-suaflowchart-appcookbook.gif)

<span data-ttu-id="36a65-117">*SUA 工具和虛擬化*</span><span class="sxs-lookup"><span data-stu-id="36a65-117">*SUA Tool and Virtualization*</span></span>

<span data-ttu-id="36a65-118">只有 SUA 工具可讓您開啟和關閉虛擬化功能。</span><span class="sxs-lookup"><span data-stu-id="36a65-118">Only the SUA tool enables you to turn on and off the virtualization feature.</span></span> <span data-ttu-id="36a65-119">藉由關閉虛擬化功能，經過測試的應用程式在 Windows XP 作業系統上運作時的行為就會更類似。</span><span class="sxs-lookup"><span data-stu-id="36a65-119">By turning off the virtualization feature, the tested application will behave more like when it is functioning on the Windows XP operating system.</span></span>

<span data-ttu-id="36a65-120">*SUA 工具和更高的許可權*</span><span class="sxs-lookup"><span data-stu-id="36a65-120">*SUA Tool and Elevated Privileges*</span></span>

<span data-ttu-id="36a65-121">只有 SUA 工具可讓您開啟和關閉 **啟動較高** 的功能。</span><span class="sxs-lookup"><span data-stu-id="36a65-121">Only the SUA tool enables you to turn on and off the **Launch Elevated** feature.</span></span> <span data-ttu-id="36a65-122">啟動提高許可權功能可讓選取的應用程式以系統管理員或標準使用者身分執行。</span><span class="sxs-lookup"><span data-stu-id="36a65-122">The Launch Elevated feature enables the selected application to run as an Administrator or as a Standard User.</span></span> <span data-ttu-id="36a65-123">根據您的選擇，您會找到與 UAC 相關的不同類型問題。</span><span class="sxs-lookup"><span data-stu-id="36a65-123">Depending on your selection, you will locate different types of UAC-related issues.</span></span> <span data-ttu-id="36a65-124">如果您清除 [提高 **許可權啟動** ] 核取方塊，您的應用程式將會以完整系統管理員許可權執行，這可讓 SUA 預測標準使用者可能發生的問題。</span><span class="sxs-lookup"><span data-stu-id="36a65-124">If you clear the **Launch Elevated** check box, your application will run with full Administrator privileges, which enables SUA to predict the issues that might occur for a Standard User.</span></span> <span data-ttu-id="36a65-125">如果您選取 [提高許可權啟動] 核取方塊，您將會看到應用程式實際執行和產生錯誤所導致的錯誤。</span><span class="sxs-lookup"><span data-stu-id="36a65-125">If you select the Launch Elevated check box, you will see errors that result from the application actually running and generating errors.</span></span>

<span data-ttu-id="36a65-126">**SUA Wizard**</span><span class="sxs-lookup"><span data-stu-id="36a65-126">**SUA Wizard**</span></span>

<span data-ttu-id="36a65-127">SUA Wizard 可讓您遵循引導式逐步程式，讓您分析應用程式，然後套用建議和選取的應用程式緩和措施，如下列流程圖所示。</span><span class="sxs-lookup"><span data-stu-id="36a65-127">The SUA Wizard enables you to follow a guided, step-by-step process by which you can analyze an application and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span> <span data-ttu-id="36a65-128">與 SUA 工具不同的是，嚮導不會啟用有關 UAC 相關問題的評論。</span><span class="sxs-lookup"><span data-stu-id="36a65-128">Unlike the SUA tool, the wizard does not enable a review of the detailed UAC-related issues.</span></span>

![顯示 S U Wizard 流程的圖表。](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a><span data-ttu-id="36a65-130">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="36a65-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="36a65-131">應用程式相容性工具組下載</span><span class="sxs-lookup"><span data-stu-id="36a65-131">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="36a65-132">[瞭解標準使用者分析器工具](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="36a65-132">[Understanding the Standard User Analyzer Tools](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span></span>
-   <span data-ttu-id="36a65-133">[標準使用者分析器技術參考](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="36a65-133">[Standard User Analyzer Technical Reference](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span></span>
-   <span data-ttu-id="36a65-134">[使用開發工具測試和緩和問題](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="36a65-134">[Testing and Mitigating Issues by Using the Development Tools](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span></span>
-   [<span data-ttu-id="36a65-135">應用程式相容性與使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="36a65-135">Application Compatibility and User Account Control</span></span>](/previous-versions/windows/)

> [!Note]  
> <span data-ttu-id="36a65-136">這些資源可能無法在某些語言及國家/地區中使用。</span><span class="sxs-lookup"><span data-stu-id="36a65-136">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
