---
description: Winlogon、GINA 和網路提供者都是互動式登入模型的部分。
ms.assetid: d049d83f-b962-4c47-a79a-da556831e319
title: Winlogon 和 GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a683077f275dc9bf38efca6649cbd8131e0b9334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847928"
---
# <a name="winlogon-and-gina"></a><span data-ttu-id="24764-103">Winlogon 和 GINA</span><span class="sxs-lookup"><span data-stu-id="24764-103">Winlogon and GINA</span></span>

<span data-ttu-id="24764-104">[*Winlogon*](../secgloss/w-gly.md)、 [*GINA*](../secgloss/g-gly.md)和網路提供者都是互動式登入模型的部分。</span><span class="sxs-lookup"><span data-stu-id="24764-104">[*Winlogon*](../secgloss/w-gly.md), the [*GINA*](../secgloss/g-gly.md), and network providers are the parts of the interactive logon model.</span></span> <span data-ttu-id="24764-105">互動式登入程式通常是由 Winlogon、MSGina.dll 和網路提供者控制。</span><span class="sxs-lookup"><span data-stu-id="24764-105">The interactive logon procedure is normally controlled by Winlogon, MSGina.dll, and network providers.</span></span> <span data-ttu-id="24764-106">若要變更互動式登入程式，可以使用自訂的 GINA DLL 來取代 MSGina.dll。</span><span class="sxs-lookup"><span data-stu-id="24764-106">To change the interactive logon procedure, MSGina.dll can be replaced with a customized GINA DLL.</span></span>

<span data-ttu-id="24764-107">若要使用 Winlogon、GINA 和網路提供者，您應該對 Windows 安全性架構有公司的知識，特別是關於 [*權杖*](../secgloss/a-gly.md)、 [*驗證套件*](../secgloss/a-gly.md)和相關事項。</span><span class="sxs-lookup"><span data-stu-id="24764-107">To work with Winlogon, the GINA, and network providers, you should have a firm knowledge of the Windows security architecture, especially with regard to [*tokens*](../secgloss/a-gly.md), [*authentication packages*](../secgloss/a-gly.md), and related matters.</span></span>

> [!Note]  
> <span data-ttu-id="24764-108">在 Windows Vista 中會忽略 GINA Dll。</span><span class="sxs-lookup"><span data-stu-id="24764-108">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="24764-109">如需特定函數和結構的詳細資訊，請參閱 [驗證參考](authentication-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="24764-109">For information about specific functions and structures, see [Authentication Reference](authentication-reference.md).</span></span> <span data-ttu-id="24764-110">這個參考章節包含 GINA DLL 必須執行之函式的描述、GINA DLL 可呼叫的 Winlogon 支援函式，以及用來在 Winlogon 和 GINA 之間傳遞資訊的資料結構。</span><span class="sxs-lookup"><span data-stu-id="24764-110">This reference section includes descriptions of the functions that a GINA DLL must implement, the Winlogon support functions that the GINA DLL can call, and the data structures used to pass information between Winlogon and the GINA.</span></span>

<span data-ttu-id="24764-111">您可以在平臺軟體發展工具組 (SDK) 安全性範例中找到範例 GINA 程式碼。</span><span class="sxs-lookup"><span data-stu-id="24764-111">Sample GINA code can be found in the Platform Software Development Kit (SDK) Security samples.</span></span> <span data-ttu-id="24764-112">這些範例包含用來執行 GINA 存根和 GINA 掛勾的 C 程式碼。</span><span class="sxs-lookup"><span data-stu-id="24764-112">The samples contain C code for implementing a GINA stub and a GINA hook.</span></span> <span data-ttu-id="24764-113">如需有關自訂 GINA DLL 開發的詳細資訊，請將電子郵件訊息傳送至： ginareqs@microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="24764-113">For more information about custom GINA DLL development, send an email message to: ginareqs@microsoft.com.</span></span>

<span data-ttu-id="24764-114">如需 Windows 所支援之驗證模型的相關資訊，以及有關 [*本地安全機構*](../secgloss/l-gly.md) (LSA) 服務和 [*驗證封裝*](../secgloss/a-gly.md) 介面的詳細資訊，請參閱 [lsa 驗證](lsa-authentication.md)。</span><span class="sxs-lookup"><span data-stu-id="24764-114">For information about the authentication model supported by Windows and for details about the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) services and [*authentication package*](../secgloss/a-gly.md) interfaces, see [LSA Authentication](lsa-authentication.md).</span></span>

<span data-ttu-id="24764-115">如需有關與安全性原則管理相關之本地安全機構的各方面的資訊，包括與其他電腦和網域的信任關係、許可權指派、審核產生控制、系統協助工具，以及其他類似的主題，請參閱 [LSA 原則](../secmgmt/lsa-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="24764-115">For information about the aspects of the Local Security Authority that relate to the administration of security policy, which includes trust relationships with other computers and domains, assignment of privileges, audit generation control, system accessibility, and other similar topics, see [LSA Policy](../secmgmt/lsa-policy.md).</span></span>

<span data-ttu-id="24764-116">如需 Winlogon 和 GINA 的相關資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="24764-116">For information about Winlogon and GINA, see the following topics.</span></span>



| <span data-ttu-id="24764-117">主題</span><span class="sxs-lookup"><span data-stu-id="24764-117">Topic</span></span>                                                                              | <span data-ttu-id="24764-118">描述</span><span class="sxs-lookup"><span data-stu-id="24764-118">Description</span></span>                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24764-119">Winlogon</span><span class="sxs-lookup"><span data-stu-id="24764-119">Winlogon</span></span>](winlogon.md)                                                           | <span data-ttu-id="24764-120">Winlogon 針對 GINA DLL 提供一組支援功能。</span><span class="sxs-lookup"><span data-stu-id="24764-120">Winlogon provides a set of support functions for the GINA DLL.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="24764-121">吉娜</span><span class="sxs-lookup"><span data-stu-id="24764-121">GINA</span></span>](gina.md)                                                                   | <span data-ttu-id="24764-122">GINA DLL 提供可自訂的使用者識別和驗證程式。</span><span class="sxs-lookup"><span data-stu-id="24764-122">A GINA DLL provides customizable user identification and authentication procedures.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="24764-123">終端機服務 GINA 函式</span><span class="sxs-lookup"><span data-stu-id="24764-123">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)           | <span data-ttu-id="24764-124">啟用終端機服務時，GINA 必須呼叫 Winlogon 支援函式來完成數個工作。</span><span class="sxs-lookup"><span data-stu-id="24764-124">When Terminal Services are enabled, the GINA must call Winlogon support functions to complete several tasks.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="24764-125">與網路提供者的互動</span><span class="sxs-lookup"><span data-stu-id="24764-125">Interaction with Network Providers</span></span>](interaction-with-network-providers.md)       | <span data-ttu-id="24764-126">您可以將系統設定為支援零個或更多的網路提供者。</span><span class="sxs-lookup"><span data-stu-id="24764-126">You can configure a system to support zero or more network providers.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="24764-127">責任和功能</span><span class="sxs-lookup"><span data-stu-id="24764-127">Responsibilities and Features</span></span>](responsibilities-and-features.md)                 | <span data-ttu-id="24764-128">互動式登入程式的每個部分都有一組責任。</span><span class="sxs-lookup"><span data-stu-id="24764-128">Each part of the interactive logon process has a set of responsibilities.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="24764-129">Winlogon 與 GINA 之間的互動</span><span class="sxs-lookup"><span data-stu-id="24764-129">Interaction Between Winlogon and GINA</span></span>](interaction-between-winlogon-and-gina.md) | <span data-ttu-id="24764-130">Winlogon 的狀態會決定呼叫哪個 GINA 函式來處理任何指定的 [*安全注意順序*](../secgloss/s-gly.md) (SAS) 事件。</span><span class="sxs-lookup"><span data-stu-id="24764-130">The state of Winlogon determines which GINA function is called to process any given [*secure attention sequence*](../secgloss/s-gly.md) (SAS) event.</span></span><br/> |
| [<span data-ttu-id="24764-131">Winlogon 通知套件</span><span class="sxs-lookup"><span data-stu-id="24764-131">Winlogon Notification Packages</span></span>](winlogon-notification-packages.md)               | <span data-ttu-id="24764-132">您可以執行通知套件來監視及回應 Winlogon 事件。</span><span class="sxs-lookup"><span data-stu-id="24764-132">You can implement a notification package to monitor and respond to Winlogon events.</span></span><br/>                                                                                                                                            |



 

 

 
