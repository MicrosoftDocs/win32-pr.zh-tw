---
description: 密碼編譯和安全通訊的未來無法輕易地預測。
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: 擴充 CryptoAPI 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec079a9ba81d7b264d317664f3c6e971d521090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945196"
---
# <a name="extending-cryptoapi-functionality"></a><span data-ttu-id="bc6a0-103">擴充 CryptoAPI 功能</span><span class="sxs-lookup"><span data-stu-id="bc6a0-103">Extending CryptoAPI Functionality</span></span>

<span data-ttu-id="bc6a0-104">[*密碼*](../secgloss/c-gly.md)編譯和安全通訊的未來無法輕易地預測。</span><span class="sxs-lookup"><span data-stu-id="bc6a0-104">The future of [*cryptography*](../secgloss/c-gly.md) and secure communications cannot easily be predicted.</span></span> <span data-ttu-id="bc6a0-105">可能會出現新的憑證類型，不同的憑證延伸可能會發現常見的使用方式，而且可能會引進新的訊息類型。</span><span class="sxs-lookup"><span data-stu-id="bc6a0-105">New certificate types might emerge, various certificate extensions might find common usage, and new message types might be introduced.</span></span> <span data-ttu-id="bc6a0-106">基於這個原因，擴充性是關鍵 [*CryptoAPI*](../secgloss/c-gly.md) 函數設計的一部分。</span><span class="sxs-lookup"><span data-stu-id="bc6a0-106">Because of this, extensibility is part of the design of key [*CryptoAPI*](../secgloss/c-gly.md) functions.</span></span>

<span data-ttu-id="bc6a0-107">下列各節顯示使用 Oid 擴充 CryptoAPI 函式的總覽。</span><span class="sxs-lookup"><span data-stu-id="bc6a0-107">The following sections present overviews on the use of OIDs for extending CryptoAPI functions.</span></span>



| <span data-ttu-id="bc6a0-108">主題</span><span class="sxs-lookup"><span data-stu-id="bc6a0-108">Topic</span></span>                                                                              | <span data-ttu-id="bc6a0-109">目錄</span><span class="sxs-lookup"><span data-stu-id="bc6a0-109">Contents</span></span>                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc6a0-110">OID 總覽</span><span class="sxs-lookup"><span data-stu-id="bc6a0-110">OID Overview</span></span>](oid-overview.md)                                                   | <span data-ttu-id="bc6a0-111">OID 基本概念。</span><span class="sxs-lookup"><span data-stu-id="bc6a0-111">OID fundamental concepts.</span></span>                                                                                                           |
| [<span data-ttu-id="bc6a0-112">建立新功能</span><span class="sxs-lookup"><span data-stu-id="bc6a0-112">Creating the New Functionality</span></span>](creating-the-new-functionality.md)               | <span data-ttu-id="bc6a0-113">建立 Oid 和函式，以擴充現有 Api 的使用。</span><span class="sxs-lookup"><span data-stu-id="bc6a0-113">Creating OIDs and functions to extend the use of existing APIs.</span></span>                                                                     |
| [<span data-ttu-id="bc6a0-114">註冊新功能</span><span class="sxs-lookup"><span data-stu-id="bc6a0-114">Registering the New Functionality</span></span>](registering-the-new-functionality.md)         | <span data-ttu-id="bc6a0-115">設定新的 OID 相關函數。</span><span class="sxs-lookup"><span data-stu-id="bc6a0-115">Setting up new OID-related functions.</span></span>                                                                                               |
| [<span data-ttu-id="bc6a0-116">安裝新功能</span><span class="sxs-lookup"><span data-stu-id="bc6a0-116">Installing the New Functionality</span></span>](installing-the-new-functionality.md)           | <span data-ttu-id="bc6a0-117">將 OID 函數安裝至記憶體，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="bc6a0-117">Installing OID functions to memory to improve performance.</span></span>                                                                          |
| [<span data-ttu-id="bc6a0-118">擴充 CertOpenStore 功能</span><span class="sxs-lookup"><span data-stu-id="bc6a0-118">Extending CertOpenStore Functionality</span></span>](extending-certopenstore-functionality.md) | <span data-ttu-id="bc6a0-119">使用可安裝或已註冊的憑證存放區提供者功能來擴充 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) 功能。</span><span class="sxs-lookup"><span data-stu-id="bc6a0-119">Extending [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) functionality using installable or registered certificate-store-provider function.</span></span> |



 

 

 
