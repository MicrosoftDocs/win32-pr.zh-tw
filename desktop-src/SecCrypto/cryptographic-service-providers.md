---
description: 重要的是這個 API 已被取代。
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: 密碼編譯服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386149"
---
# <a name="cryptographic-service-providers"></a><span data-ttu-id="0d943-103">密碼編譯服務提供者</span><span class="sxs-lookup"><span data-stu-id="0d943-103">Cryptographic Service Providers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d943-104">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="0d943-104">This API is deprecated.</span></span> <span data-ttu-id="0d943-105">新的和現有的軟體應該開始使用 [新一代密碼編譯 api。](/windows/desktop/SecCNG/cng-portal)</span><span class="sxs-lookup"><span data-stu-id="0d943-105">New and existing software should start using [Cryptography Next Generation APIs.](/windows/desktop/SecCNG/cng-portal)</span></span> <span data-ttu-id="0d943-106">Microsoft 可能會在未來的版本中移除此 API。</span><span class="sxs-lookup"><span data-stu-id="0d943-106">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="0d943-107">[*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 包含密碼編譯標準和演算法的實施。</span><span class="sxs-lookup"><span data-stu-id="0d943-107">A [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) contains implementations of cryptographic standards and algorithms.</span></span> <span data-ttu-id="0d943-108">CSP 至少包含 [*動態連結程式庫*](../secgloss/d-gly.md) (DLL) ，可在 [*CryptoSPI*](../secgloss/c-gly.md) ([*系統程式介面*](../secgloss/s-gly.md)) 中執行函式。</span><span class="sxs-lookup"><span data-stu-id="0d943-108">At a minimum, a CSP consists of a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements the functions in [*CryptoSPI*](../secgloss/c-gly.md) (a [*system program interface*](../secgloss/s-gly.md)).</span></span> <span data-ttu-id="0d943-109">大部分的 Csp 都包含所有自己的函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="0d943-109">Most CSPs contain the implementation of all of their own functions.</span></span> <span data-ttu-id="0d943-110">不過，某些 Csp 會在 Windows 服務控制管理員所管理的 Windows 型服務程式中，執行其功能。</span><span class="sxs-lookup"><span data-stu-id="0d943-110">Some CSPs, however, implement their functions mainly in a Windows-based service program managed by the Windows service control manager.</span></span> <span data-ttu-id="0d943-111">其他人會在硬體中執行功能，例如 [*智慧卡*](../secgloss/s-gly.md) 或安全的副處理器。</span><span class="sxs-lookup"><span data-stu-id="0d943-111">Others implement functions in hardware, such as a [*smart card*](../secgloss/s-gly.md) or secure coprocessor.</span></span> <span data-ttu-id="0d943-112">如果 CSP 未執行自己的函式，則 DLL 會作為傳遞層，以加速作業系統與實際 CSP 實行之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="0d943-112">If a CSP does not implement its own functions, the DLL acts as a pass-through layer, facilitating the communication between the operating system and the actual CSP implementation.</span></span>

<span data-ttu-id="0d943-113">本節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="0d943-113">This section includes the following topics.</span></span>



| <span data-ttu-id="0d943-114">主題</span><span class="sxs-lookup"><span data-stu-id="0d943-114">Topic</span></span>                                                                                      | <span data-ttu-id="0d943-115">目錄</span><span class="sxs-lookup"><span data-stu-id="0d943-115">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d943-116">密碼編譯提供者類型</span><span class="sxs-lookup"><span data-stu-id="0d943-116">Cryptographic Provider Types</span></span>](cryptographic-provider-types.md)                           | <span data-ttu-id="0d943-117">密碼編譯提供者類型是共用資料格式和密碼編譯通訊協定的密碼編譯服務提供者系列。</span><span class="sxs-lookup"><span data-stu-id="0d943-117">Cryptographic provider types are families of cryptographic services providers that share data formats and cryptographic protocols.</span></span> <span data-ttu-id="0d943-118">資料格式包括演算法 [*填補*](../secgloss/p-gly.md) 配置、 [*金鑰長度*](../secgloss/k-gly.md)和預設模式。</span><span class="sxs-lookup"><span data-stu-id="0d943-118">Data formats include algorithms [*padding*](../secgloss/p-gly.md) schemes, [*key lengths*](../secgloss/k-gly.md), and default modes.</span></span> |
| [<span data-ttu-id="0d943-119">Microsoft 密碼編譯服務提供者</span><span class="sxs-lookup"><span data-stu-id="0d943-119">Microsoft Cryptographic Service Providers</span></span>](microsoft-cryptographic-service-providers.md) | <span data-ttu-id="0d943-120">Microsoft 目前提供之 Csp 的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0d943-120">Detailed information about CSPs currently available from Microsoft.</span></span>                                                                                                                                                                                                                                                                                       |



 

 

 
