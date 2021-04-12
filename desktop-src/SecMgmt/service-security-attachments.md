---
description: Microsoft Security Configuration tool 組是一組 Microsoft Management Console 的 (MMC) 工具，可簡化系統安全性的設定和分析。
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: 服務安全性附件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318212"
---
# <a name="service-security-attachments"></a><span data-ttu-id="ddbcc-103">服務安全性附件</span><span class="sxs-lookup"><span data-stu-id="ddbcc-103">Service Security Attachments</span></span>

<span data-ttu-id="ddbcc-104">Microsoft Security Configuration tool 組是一組 Microsoft Management Console 的 (MMC) 工具，可簡化系統安全性的設定和分析。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-104">The Microsoft Security Configuration tool set is a set of Microsoft Management Console (MMC) tools that simplify configuration and analysis of system security.</span></span> <span data-ttu-id="ddbcc-105">不過，有些服務具有特殊的設定需求，而不是標準工具組所提供的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-105">Some services, however, have specialized configuration needs that go beyond the security settings provided by the standard tool set.</span></span> <span data-ttu-id="ddbcc-106">若要處理這些需求，您可以撰寫可處理特定服務安全性工作的附件，以擴充工具集的功能。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-106">To handle those needs, you can extend the functionality of the tool set by writing an attachment that handles the service-specific security tasks.</span></span>

<span data-ttu-id="ddbcc-107">例如，多工緩衝處理器是一種 Windows NT 服務，用來定義需要保護的私用物件，例如印表機。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-107">For example, Spooler is a Windows NT service that defines private objects, which need to be secured, for example, printers.</span></span> <span data-ttu-id="ddbcc-108">標準工具組不會處理這項功能，因此需要附件來處理印表機物件的設定和分析。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-108">This functionality is not handled by the standard tool set and thus requires an attachment to handle configuration and analysis of printer objects.</span></span> <span data-ttu-id="ddbcc-109">一般安全性參數的設定（例如服務調用原則）仍由安全性設定工具集處理。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-109">Configuration of general security parameters, such as the service invocation policy, is still handled by the Security Configuration tool set.</span></span>

<span data-ttu-id="ddbcc-110">安全性服務附件會擴充安全性設定工具集的功能，以支援服務特定的設定。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-110">Security service attachments extend the functionality of the Security Configuration tool set to support service-specific configurations.</span></span>

<span data-ttu-id="ddbcc-111">附件有兩個元件：</span><span class="sxs-lookup"><span data-stu-id="ddbcc-111">An attachment has two components:</span></span>

-   <span data-ttu-id="ddbcc-112">一個 MMC 嵌入式管理單元延伸模組，可執行附件使用者介面。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-112">An MMC snap-in extension that implements the attachment user interface.</span></span>
-   <span data-ttu-id="ddbcc-113">處理服務特定安全性設定與分析工作的附件引擎。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-113">An attachment engine that processes service-specific security configuration and analysis tasks.</span></span>

<span data-ttu-id="ddbcc-114">附件嵌入式管理單元延伸是由安全性設定嵌入式管理單元所主控。這些是 MMC 嵌入式管理單元，可為使用者提供介面來設定及分析服務的一般安全性設定。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-114">The attachment snap-in extension is hosted by the Security Configuration snap-ins. These are MMC snap-ins that provide the user with interfaces to configure and analyze the general security settings for a service.</span></span> <span data-ttu-id="ddbcc-115">服務特定的設定是使用附件嵌入式管理單元擴充功能來設定。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-115">Service-specific settings are configured using the attachment snap-in extension.</span></span>

<span data-ttu-id="ddbcc-116">當使用者變更設定時，[安全性設定] 嵌入式管理單元會儲存新的資訊，然後將要求傳遞至安全性設定引擎。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-116">When the user changes a configuration setting, the Security Configuration snap-ins store the new information and then pass the request to the Security Configuration Engine.</span></span> <span data-ttu-id="ddbcc-117">引擎會處理要求，並將服務設定為新的設定。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-117">The Engine processes the request and sets the service to the new configuration.</span></span> <span data-ttu-id="ddbcc-118">如果要求會影響標準安全性設定，則會由引擎處理。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-118">If the request affects a standard security setting, it is handled by the Engine.</span></span> <span data-ttu-id="ddbcc-119">如果要求是服務特定的，引擎會呼叫適當的附件引擎來處理要求。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-119">If the request is service-specific, the Engine calls the appropriate attachment engine to handle the request.</span></span>

<span data-ttu-id="ddbcc-120">下圖顯示「附件引擎」和「嵌入式管理單元」延伸模組在安全性設定工具集的架構內的運作方式。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-120">The following illustration shows how the attachment engine and snap-in extension work within the framework of the Security Configuration tool set.</span></span>

![附件引擎和嵌入式管理單元](images/model1a.png)

<span data-ttu-id="ddbcc-122">如需使用 Microsoft 安全性設定工具集的詳細資訊，請使用您慣用的搜尋引擎來搜尋安全性設定。</span><span class="sxs-lookup"><span data-stu-id="ddbcc-122">For more information about using the Microsoft Security Configuration tool set, search for Security Configuration using your preferred search engine.</span></span>

 

 



