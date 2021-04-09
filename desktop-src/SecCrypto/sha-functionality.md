---
description: 原始的基底提供者錯誤地報告了 SHA 雜湊演算法，其會呼叫 CryptGetProvParam 並指定參數 PP ENUMALGS 來列舉演算法 \_ 。
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: SHA 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689456"
---
# <a name="sha-functionality"></a><span data-ttu-id="4f427-103">SHA 功能</span><span class="sxs-lookup"><span data-stu-id="4f427-103">SHA Functionality</span></span>

<span data-ttu-id="4f427-104">原始的基底提供者錯誤地報告了 [*SHA*](../secgloss/s-gly.md) 雜湊演算法，其會呼叫 [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) 並指定參數 PP ENUMALGS 來列舉演算法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4f427-104">The original Base Provider incorrectly reported that the [*SHA*](../secgloss/s-gly.md) hash algorithm enumerating algorithms by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with parameter PP\_ENUMALGS specified.</span></span> <span data-ttu-id="4f427-105">這已在基底提供者中修正。</span><span class="sxs-lookup"><span data-stu-id="4f427-105">This has been fixed in the Base Provider.</span></span> <span data-ttu-id="4f427-106">修訂的基底提供者和延伸的提供者，現在都能正確地報告 SHA-1。</span><span class="sxs-lookup"><span data-stu-id="4f427-106">Both the revised Base Provider and the Extended Provider and now correctly report SHA-1.</span></span>

<span data-ttu-id="4f427-107">已將已定義的 CALG \_ SHA1 常數新增至 Wincrypt，其值與 CALG SHA 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4f427-107">A defined CALG\_SHA1 constant has been added to Wincrypt.h with the same value as CALG\_SHA.</span></span>

 

 
