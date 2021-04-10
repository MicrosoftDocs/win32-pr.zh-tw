---
description: SID 元件
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: SID 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026319"
---
# <a name="sid-components"></a><span data-ttu-id="87cb9-103">SID 元件</span><span class="sxs-lookup"><span data-stu-id="87cb9-103">SID Components</span></span>

<span data-ttu-id="87cb9-104">SID 值包含的元件提供了可唯一識別受信任者之 [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) 結構和元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="87cb9-104">A SID value includes components that provide information about the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure and components that uniquely identify a trustee.</span></span> <span data-ttu-id="87cb9-105">SID 是由下列元件所組成：</span><span class="sxs-lookup"><span data-stu-id="87cb9-105">A SID consists of the following components:</span></span>

-   <span data-ttu-id="87cb9-106">[**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)結構的修訂層級</span><span class="sxs-lookup"><span data-stu-id="87cb9-106">The revision level of the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure</span></span>
-   <span data-ttu-id="87cb9-107">識別發行 SID 之授權單位的48位識別碼授權單位值</span><span class="sxs-lookup"><span data-stu-id="87cb9-107">A 48-bit identifier authority value that identifies the authority that issued the SID</span></span>
-   <span data-ttu-id="87cb9-108">Subauthority 或 [*相對識別碼*](/windows/desktop/SecGloss/r-gly) 的可變數 (RID) 值，可唯一識別信任者相對於發出 SID 的授權單位</span><span class="sxs-lookup"><span data-stu-id="87cb9-108">A variable number of subauthority or [*relative identifier*](/windows/desktop/SecGloss/r-gly) (RID) values that uniquely identify the trustee relative to the authority that issued the SID</span></span>

<span data-ttu-id="87cb9-109">識別碼授權單位值和 subauthority 值的組合可確保兩個 Sid 都不相同，即使兩個不同的 SID 發行授權單位發出相同的 RID 值組合也一樣。</span><span class="sxs-lookup"><span data-stu-id="87cb9-109">The combination of the identifier authority value and the subauthority values ensures that no two SIDs will be the same, even if two different SID-issuing authorities issue the same combination of RID values.</span></span> <span data-ttu-id="87cb9-110">每個 SID 發行授權單位只會發出一次指定的 RID。</span><span class="sxs-lookup"><span data-stu-id="87cb9-110">Each SID-issuing authority issues a given RID only once.</span></span>

<span data-ttu-id="87cb9-111">Sid 會以二進位格式儲存在 [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) 結構中。</span><span class="sxs-lookup"><span data-stu-id="87cb9-111">SIDs are stored in binary format in a [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure.</span></span> <span data-ttu-id="87cb9-112">若要顯示 SID，您可以呼叫 [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) 函式，將二進位 SID 轉換成字串格式。</span><span class="sxs-lookup"><span data-stu-id="87cb9-112">To display a SID, you can call the [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) function to convert a binary SID to string format.</span></span> <span data-ttu-id="87cb9-113">若要將 SID 字串轉換回有效的功能 SID，請呼叫 [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) 函數。</span><span class="sxs-lookup"><span data-stu-id="87cb9-113">To convert a SID string back to a valid, functional SID, call the [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) function.</span></span>

<span data-ttu-id="87cb9-114">這些函式會使用下列 Sid 的標準化字串標記法，讓您更輕鬆地將其元件視覺化：</span><span class="sxs-lookup"><span data-stu-id="87cb9-114">These functions use the following standardized string notation for SIDs, which makes it simpler to visualize their components:</span></span>

<span data-ttu-id="87cb9-115">S-*R* - *I* - *S*.。。</span><span class="sxs-lookup"><span data-stu-id="87cb9-115">S-*R*-*I*-*S*…</span></span>

<span data-ttu-id="87cb9-116">在這個標記法中，常值字元 "S" 會將一系列的數位識別為 SID， *R* 是修訂層級， *I* 是識別碼授權值，而 *S*.。。</span><span class="sxs-lookup"><span data-stu-id="87cb9-116">In this notation, the literal character "S" identifies the series of digits as a SID, *R* is the revision level, *I* is the identifier-authority value, and *S*…</span></span> <span data-ttu-id="87cb9-117">這是一或多個 subauthority 值。</span><span class="sxs-lookup"><span data-stu-id="87cb9-117">is one or more subauthority values.</span></span>

<span data-ttu-id="87cb9-118">下列範例會使用此標記法來顯示本機系統管理員群組已知的網域相對 SID：</span><span class="sxs-lookup"><span data-stu-id="87cb9-118">The following example uses this notation to display the well-known domain-relative SID of the local Administrators group:</span></span>

<span data-ttu-id="87cb9-119">S-1-5-32-544</span><span class="sxs-lookup"><span data-stu-id="87cb9-119">S-1-5-32-544</span></span>

<span data-ttu-id="87cb9-120">在此範例中，SID 具有下列元件。</span><span class="sxs-lookup"><span data-stu-id="87cb9-120">In this example, the SID has the following components.</span></span> <span data-ttu-id="87cb9-121">括弧中的常數是知名的識別碼授權單位和 Winnt 中定義的 [*RID*](/windows/desktop/SecGloss/r-gly) 值：</span><span class="sxs-lookup"><span data-stu-id="87cb9-121">The constants in parentheses are well-known identifier authority and [*RID*](/windows/desktop/SecGloss/r-gly) values defined in Winnt.h:</span></span>

-   <span data-ttu-id="87cb9-122">修訂層級1</span><span class="sxs-lookup"><span data-stu-id="87cb9-122">A revision level of 1</span></span>
-   <span data-ttu-id="87cb9-123">識別碼授權單位值為 5 (SECURITY \_ NT \_ 授權單位) </span><span class="sxs-lookup"><span data-stu-id="87cb9-123">An identifier-authority value of 5 (SECURITY\_NT\_AUTHORITY)</span></span>
-   <span data-ttu-id="87cb9-124">第一個 subauthority 值 32 (安全性內 \_ 建 \_ 網域 \_ RID) </span><span class="sxs-lookup"><span data-stu-id="87cb9-124">A first subauthority value of 32 (SECURITY\_BUILTIN\_DOMAIN\_RID)</span></span>
-   <span data-ttu-id="87cb9-125">第二個 subauthority 值 544 (網域 \_ 別名 \_ RID \_ 管理員) </span><span class="sxs-lookup"><span data-stu-id="87cb9-125">A second subauthority value of 544 (DOMAIN\_ALIAS\_RID\_ADMINS)</span></span>

 

 
