---
description: 目前，使用者名稱和密碼認證是用來進行驗證的最常見認證。
ms.assetid: 1d810f71-9bf5-4c5c-a573-c35081f604cf
title: 處理密碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d3a5ab2bc034500159adb25dab02b47eb43bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980500"
---
# <a name="handling-passwords"></a><span data-ttu-id="c738c-103">處理密碼</span><span class="sxs-lookup"><span data-stu-id="c738c-103">Handling Passwords</span></span>

<span data-ttu-id="c738c-104">目前，使用者名稱和密碼認證是用來進行驗證的最常見認證。</span><span class="sxs-lookup"><span data-stu-id="c738c-104">Currently, user name and password credentials are the most common credentials used for authentication.</span></span> <span data-ttu-id="c738c-105">即使其他類型的認證（例如憑證和生物識別）開始在系統和網路的世界中找出其使用方式，但它們通常會以密碼進行備份。</span><span class="sxs-lookup"><span data-stu-id="c738c-105">Even though other types of credentials, such as certificates and biometrics, are starting to find their way into the world of systems and networking, they are often backed up by passwords.</span></span> <span data-ttu-id="c738c-106">而且，即使使用憑證，也必須保護其加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c738c-106">And, even where certificates are used, their encryption keys must be protected.</span></span> <span data-ttu-id="c738c-107">因此，使用者名稱和密碼將繼續用於可預見的未來的認證。</span><span class="sxs-lookup"><span data-stu-id="c738c-107">So, user names and passwords will continue to be used for credentials well into the foreseeable future.</span></span>

<span data-ttu-id="c738c-108">由於密碼和加密金鑰即將存在一段時間，因此軟體系統必須以安全的方式使用它們。</span><span class="sxs-lookup"><span data-stu-id="c738c-108">Given that passwords and encryption keys are going to be around a while, it is important that software systems use them in a secure fashion.</span></span> <span data-ttu-id="c738c-109">如果網路或電腦系統保持安全，則必須保護密碼免于受到入侵者的攻擊。</span><span class="sxs-lookup"><span data-stu-id="c738c-109">If a network or computer system is to remain secure, passwords must be protected from would-be intruders.</span></span> <span data-ttu-id="c738c-110">乍看之下，這可能很簡單。</span><span class="sxs-lookup"><span data-stu-id="c738c-110">This might, at first, seem trivial.</span></span> <span data-ttu-id="c738c-111">不過，在網路遭入侵之後系統和網路之後的系統，是因為攻擊者可以登出使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="c738c-111">However, system after system and network after network have been compromised because an attacker has been able to sniff out users' passwords.</span></span> <span data-ttu-id="c738c-112">這些問題的範圍包括將其密碼與某人共用的使用者，到可由攻擊者滲透的軟體。</span><span class="sxs-lookup"><span data-stu-id="c738c-112">The problems range from users sharing their passwords with someone, to software that can be penetrated by an attacker.</span></span>

<span data-ttu-id="c738c-113">以完全安全的方式將秘密資訊儲存在軟體中是不可能的。</span><span class="sxs-lookup"><span data-stu-id="c738c-113">It is impossible to store secret information in software in a completely secure fashion.</span></span> <span data-ttu-id="c738c-114">而且因為軟體系統中儲存密碼和加密金鑰絕對不會完全安全，建議您不要將密碼和加密金鑰儲存在軟體系統中。</span><span class="sxs-lookup"><span data-stu-id="c738c-114">And because storing passwords and encryption keys in a software system can never be completely secure, it is recommended that they not be stored in a software system.</span></span>

<span data-ttu-id="c738c-115">不過，當密碼必須儲存在軟體系統（通常是這種情況下）時，有一些預防措施可以採取。</span><span class="sxs-lookup"><span data-stu-id="c738c-115">However, when passwords must be stored in a software system, which is usually the case, there are precautions that can be taken.</span></span> <span data-ttu-id="c738c-116">主要的預防措施是讓入侵者更難探索密碼。</span><span class="sxs-lookup"><span data-stu-id="c738c-116">The primary precaution is to make it as difficult as possible for an intruder to discover a password.</span></span> <span data-ttu-id="c738c-117">就像鎖定您的房屋大門一樣，如果有人判斷中斷了，就幾乎不可能阻止他們這麼做。</span><span class="sxs-lookup"><span data-stu-id="c738c-117">Just like locking your house doors, if someone is determined to break in, it is nearly impossible to prevent them from doing so.</span></span> <span data-ttu-id="c738c-118">但希望您能夠更輕鬆地提高攻擊者的程度，而不會發現更容易受害者。</span><span class="sxs-lookup"><span data-stu-id="c738c-118">But hopefully, you will have raised the level of difficulty sufficiently that the would-be intruder would rather find easier prey.</span></span>

<span data-ttu-id="c738c-119">有許多方法可讓攻擊者更難探索密碼的作業。</span><span class="sxs-lookup"><span data-stu-id="c738c-119">There are many ways to make an attacker's job of discovering passwords harder.</span></span> <span data-ttu-id="c738c-120">不過，實際上可以完成的工作範圍通常是與網路或系統使用者願意使用的功能取捨。</span><span class="sxs-lookup"><span data-stu-id="c738c-120">However, the extent of what can actually be done is usually a trade-off with what the users of the network or system are willing to live with.</span></span> <span data-ttu-id="c738c-121">例如，採用「單一登入」未使用的情況，並在每次啟動應用程式時提示使用者輸入密碼。</span><span class="sxs-lookup"><span data-stu-id="c738c-121">For example, take the case where "single sign on" is not used, and the user is prompted for a password every time an application is started.</span></span> <span data-ttu-id="c738c-122">在大部分的情況下，這會對使用者造成大量的負擔，而且可能會抱怨。</span><span class="sxs-lookup"><span data-stu-id="c738c-122">In most cases, this would create a significant burden on the users, and they would probably complain.</span></span> <span data-ttu-id="c738c-123">但不只是這樣，但缺少單一登入沒有效率，也會降低使用者的生產力。</span><span class="sxs-lookup"><span data-stu-id="c738c-123">Not only that, but lack of a single sign on is inefficient and would degrade the productivity of the users.</span></span> <span data-ttu-id="c738c-124">因此，幾乎說的，使用者通常不會從使用者收集密碼，除非登入時間。</span><span class="sxs-lookup"><span data-stu-id="c738c-124">So, practically speaking, a password generally is not collected from a user except at the time of log on.</span></span>

<span data-ttu-id="c738c-125">由於密碼通常必須儲存在軟體系統上，因此請務必確保密碼盡可能保持安全，並維護使用者的便利性。</span><span class="sxs-lookup"><span data-stu-id="c738c-125">Given that passwords must usually be stored on the software system, it becomes important to ensure that passwords are kept as secure as possible and that convenience for users is maintained.</span></span> <span data-ttu-id="c738c-126">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="c738c-126">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="c738c-127">密碼威脅評估</span><span class="sxs-lookup"><span data-stu-id="c738c-127">Password Threat Assessment</span></span>](password-threat-assessment.md)
-   [<span data-ttu-id="c738c-128">威脅緩和技巧</span><span class="sxs-lookup"><span data-stu-id="c738c-128">Threat Mitigation Techniques</span></span>](threat-mitigation-techniques.md)

> [!Note]  
> <span data-ttu-id="c738c-129">當您完成使用應用程式中的密碼時，請呼叫 [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) 函式，以清除記憶體中的敏感資訊。</span><span class="sxs-lookup"><span data-stu-id="c738c-129">When you have finished using passwords in applications, clear the sensitive information from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span>

 

 

 
