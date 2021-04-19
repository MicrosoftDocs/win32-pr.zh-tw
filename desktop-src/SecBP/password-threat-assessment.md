---
description: 在實施保護密碼的程式碼之前，最好先分析您的特定環境，以瞭解攻擊者可能嘗試滲透軟體防禦的方式。
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: 密碼威脅評估
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48a79d44bda9714083c5dd1085e9d09497e7341
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987401"
---
# <a name="password-threat-assessment"></a><span data-ttu-id="51041-103">密碼威脅評估</span><span class="sxs-lookup"><span data-stu-id="51041-103">Password Threat Assessment</span></span>

<span data-ttu-id="51041-104">在實施保護密碼的程式碼之前，最好先分析您的特定環境，以瞭解攻擊者可能嘗試滲透軟體防禦的方式。</span><span class="sxs-lookup"><span data-stu-id="51041-104">Before implementing code that protects passwords, it is best to analyze your particular environment for ways that an attacker might try to penetrate software defenses.</span></span>

<span data-ttu-id="51041-105">從分析您的網路或系統架構開始。</span><span class="sxs-lookup"><span data-stu-id="51041-105">Start by analyzing your network or system architecture.</span></span> <span data-ttu-id="51041-106">以下是一些範例：</span><span class="sxs-lookup"><span data-stu-id="51041-106">Here are some examples:</span></span>

-   <span data-ttu-id="51041-107">必須保護的密碼數目。</span><span class="sxs-lookup"><span data-stu-id="51041-107">The number of passwords that must be protected.</span></span> <span data-ttu-id="51041-108">需要密碼才能登入本機電腦嗎？</span><span class="sxs-lookup"><span data-stu-id="51041-108">Is a password required to log on to the local computer?</span></span> <span data-ttu-id="51041-109">用來登入網路的密碼是否相同？</span><span class="sxs-lookup"><span data-stu-id="51041-109">Is the same password used to log on to the network?</span></span> <span data-ttu-id="51041-110">密碼是否會傳播到網路上的一部以上的伺服器？</span><span class="sxs-lookup"><span data-stu-id="51041-110">Are passwords propagated to more than one server on the network?</span></span> <span data-ttu-id="51041-111">必須容納多少密碼？</span><span class="sxs-lookup"><span data-stu-id="51041-111">How many passwords must be accommodated?</span></span>
-   <span data-ttu-id="51041-112">如果將使用任何) ，網路 (的種類。</span><span class="sxs-lookup"><span data-stu-id="51041-112">The kind of network (if any) that will be used.</span></span> <span data-ttu-id="51041-113">使用公司目錄系統執行的網路 (例如 LDAP) ，是否使用其密碼架構？</span><span class="sxs-lookup"><span data-stu-id="51041-113">Is the network implemented using a corporate directory system (such as LDAP), and is its password architecture used?</span></span> <span data-ttu-id="51041-114">是否有任何物件儲存未加密的密碼？</span><span class="sxs-lookup"><span data-stu-id="51041-114">Are any objects storing unencrypted passwords?</span></span>
-   <span data-ttu-id="51041-115">開啟與關閉的網路。</span><span class="sxs-lookup"><span data-stu-id="51041-115">Open versus closed network.</span></span> <span data-ttu-id="51041-116">網路是獨立的，還是在外部開啟？</span><span class="sxs-lookup"><span data-stu-id="51041-116">Is the network self-contained or is it open to the outside?</span></span> <span data-ttu-id="51041-117">若是如此，它是否受到防火牆保護？</span><span class="sxs-lookup"><span data-stu-id="51041-117">If so, is it protected by a firewall?</span></span>
-   <span data-ttu-id="51041-118">遠端存取。</span><span class="sxs-lookup"><span data-stu-id="51041-118">Remote access.</span></span> <span data-ttu-id="51041-119">使用者是否需要從遠端位置存取網路？</span><span class="sxs-lookup"><span data-stu-id="51041-119">Will users need to access the network from a remote location?</span></span>

<span data-ttu-id="51041-120">分析您的系統或網路架構之後，您就可以開始分析攻擊者可能嘗試攻擊的方式。</span><span class="sxs-lookup"><span data-stu-id="51041-120">After you have analyzed your system or network architecture, then you can start to analyze how an attacker might try to attack it.</span></span> <span data-ttu-id="51041-121">以下是一些可能性：</span><span class="sxs-lookup"><span data-stu-id="51041-121">Here are some possibilities:</span></span>

-   <span data-ttu-id="51041-122">從電腦的登錄讀取未加密的密碼。</span><span class="sxs-lookup"><span data-stu-id="51041-122">Read an unencrypted password from a computer's registry.</span></span>
-   <span data-ttu-id="51041-123">讀取軟體中硬式編碼的未加密密碼。</span><span class="sxs-lookup"><span data-stu-id="51041-123">Read an unencrypted password that is hard-coded in the software.</span></span>
-   <span data-ttu-id="51041-124">從電腦的已交換程式字碼頁面讀取未加密的密碼。</span><span class="sxs-lookup"><span data-stu-id="51041-124">Read an unencrypted password from a computer's swapped-out code page.</span></span>
-   <span data-ttu-id="51041-125">從程式的事件記錄檔讀取密碼。</span><span class="sxs-lookup"><span data-stu-id="51041-125">Read a password from a program's event log.</span></span>
-   <span data-ttu-id="51041-126">從具有包含純文字密碼之物件的擴充 Microsoft Active Directory 目錄服務架構中，讀取密碼。</span><span class="sxs-lookup"><span data-stu-id="51041-126">Read a password from an extended Microsoft Active Directory directory service schema that has objects that contain a plaintext password.</span></span>
-   <span data-ttu-id="51041-127">在需要密碼的程式上執行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="51041-127">Run a debugger on a program that requires a password.</span></span>
-   <span data-ttu-id="51041-128">猜測密碼。</span><span class="sxs-lookup"><span data-stu-id="51041-128">Guess a password.</span></span> <span data-ttu-id="51041-129">您可以使用任何一種技術。</span><span class="sxs-lookup"><span data-stu-id="51041-129">Any of several techniques might be used.</span></span> <span data-ttu-id="51041-130">例如，攻擊者可能知道使用者的一些個人資訊，並嘗試從該資訊中猜出密碼 (例如，配偶/夥伴或子) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="51041-130">For example, the attacker might know some personal information about a user and try to guess a password from that information (for example, the name of a spouse/partner or child).</span></span> <span data-ttu-id="51041-131">或者，可能會嘗試暴力密碼破解方法，在此方法中只會嘗試字母、數位和標點符號的所有組合 (只有在使用短密碼) 的情況下才可行。</span><span class="sxs-lookup"><span data-stu-id="51041-131">Or, a brute-force method might be tried, where all combinations of letters, numbers, and punctuation are tried (only feasible where short passwords are used).</span></span>

<span data-ttu-id="51041-132">比較可能的攻擊方法與系統或網路架構可能會顯示安全性風險。</span><span class="sxs-lookup"><span data-stu-id="51041-132">Comparing the possible attack methodologies with system or network architecture will likely reveal security risks.</span></span> <span data-ttu-id="51041-133">屆時，可以為每個風險建立風險因素，而且風險因素可以用來將修正程式分類。</span><span class="sxs-lookup"><span data-stu-id="51041-133">At that point, a risk factor can be established for each risk, and the risk factors can be used to triage fixes.</span></span>

 

 



