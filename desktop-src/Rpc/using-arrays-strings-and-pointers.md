---
title: 使用陣列、字串和指標
description: 醫生計畫 (查看 \\ \\ \\ 平臺軟體發展工具組中的 RPC 醫生 (SDK) ) 是示範陣列和字串屬性相關設計取捨的應用程式範例。
ms.assetid: 9aea94a1-ae1f-4bd6-9dd3-146edf0b5fec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542a174b9ffd742ecf88de7231449a780be8dca9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092793"
---
# <a name="using-arrays-strings-and-pointers"></a><span data-ttu-id="11039-103">使用陣列、字串和指標</span><span class="sxs-lookup"><span data-stu-id="11039-103">Using Arrays, Strings, and Pointers</span></span>

<span data-ttu-id="11039-104">醫生計畫 (查看 \\ \\ \\ 平臺軟體發展工具組中的 RPC 醫生 (SDK) ) 是示範陣列和字串屬性相關設計取捨的應用程式範例。</span><span class="sxs-lookup"><span data-stu-id="11039-104">The Doctor program (see \\samples\\rpc\\doctor in the Platform Software Development Kit (SDK)) is a good example of an application that demonstrates the design trade-offs involved with array and string attributes.</span></span> <span data-ttu-id="11039-105">醫生計畫是由1960年代中 MIT 的人工智慧研究人員 Joseph Weizenbaum 所開發之較知名程式（Eliza）的小型範例版本。</span><span class="sxs-lookup"><span data-stu-id="11039-105">The Doctor program is a small sample version of a better-known program, Eliza, developed by artificial intelligence researcher Joseph Weizenbaum at MIT in the 1960s.</span></span> <span data-ttu-id="11039-106">程式會使用簡單的模式比對來模擬 therapist，以回應自然語言輸入。</span><span class="sxs-lookup"><span data-stu-id="11039-106">The program mimics a therapist by using simple pattern-matching to respond to natural language input.</span></span>

<span data-ttu-id="11039-107">Eliza 程式已記錄下列會話。</span><span class="sxs-lookup"><span data-stu-id="11039-107">The Eliza program recorded the following session.</span></span>



| <span data-ttu-id="11039-108">User</span><span class="sxs-lookup"><span data-stu-id="11039-108">User</span></span>                                                | <span data-ttu-id="11039-109">伊麗莎</span><span class="sxs-lookup"><span data-stu-id="11039-109">Eliza</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="11039-110">男性都很相似。</span><span class="sxs-lookup"><span data-stu-id="11039-110">Men are all alike.</span></span>                                  | <span data-ttu-id="11039-111">以何種方式？</span><span class="sxs-lookup"><span data-stu-id="11039-111">In what way?</span></span>                                              |
| <span data-ttu-id="11039-112">他們一律會困擾我們的內容。</span><span class="sxs-lookup"><span data-stu-id="11039-112">They're always bugging us about something or other.</span></span> | <span data-ttu-id="11039-113">您可以考慮特定範例嗎？</span><span class="sxs-lookup"><span data-stu-id="11039-113">Can you think of a specific example?</span></span>                      |
| <span data-ttu-id="11039-114">好了，我的男友變成了。</span><span class="sxs-lookup"><span data-stu-id="11039-114">Well, my boyfriend made me come here.</span></span>               | <span data-ttu-id="11039-115">您的男友會在這裡提出。</span><span class="sxs-lookup"><span data-stu-id="11039-115">Your boyfriend made you come here.</span></span>                        |
| <span data-ttu-id="11039-116">他說我的時間很長。</span><span class="sxs-lookup"><span data-stu-id="11039-116">He says I'm depressed much of the time.</span></span>             | <span data-ttu-id="11039-117">很抱歉聽到您已按下。</span><span class="sxs-lookup"><span data-stu-id="11039-117">I am sorry to hear that you are depressed.</span></span>                |
| <span data-ttu-id="11039-118">沒錯，我不太高興。</span><span class="sxs-lookup"><span data-stu-id="11039-118">It's true, I am unhappy.</span></span>                            | <span data-ttu-id="11039-119">您認為這裡有助您不太滿意嗎？</span><span class="sxs-lookup"><span data-stu-id="11039-119">Do you think coming here will help you not to be unhappy?</span></span> |
| <span data-ttu-id="11039-120">我需要一些協助;這看起來很有特定的。</span><span class="sxs-lookup"><span data-stu-id="11039-120">I need some help; that much seems certain.</span></span>          | <span data-ttu-id="11039-121">如果您獲得一些協助，這對您有何意義？</span><span class="sxs-lookup"><span data-stu-id="11039-121">What would it mean to you if you got some help?</span></span>           |
| <span data-ttu-id="11039-122">或許我可以瞭解如何與我的母親一起進行。</span><span class="sxs-lookup"><span data-stu-id="11039-122">Perhaps I could learn to get along with my mother.</span></span>  | <span data-ttu-id="11039-123">告訴我更多關於您家人的資訊。</span><span class="sxs-lookup"><span data-stu-id="11039-123">Tell me more about your family.</span></span>                           |
| <span data-ttu-id="11039-124">我的母親負責處理。</span><span class="sxs-lookup"><span data-stu-id="11039-124">My mother takes care of me.</span></span>                         | <span data-ttu-id="11039-125">您家人中的其他人會負責您？</span><span class="sxs-lookup"><span data-stu-id="11039-125">Who else in your family takes care of you?</span></span>                |
| <span data-ttu-id="11039-126">我父親。</span><span class="sxs-lookup"><span data-stu-id="11039-126">My father.</span></span>                                          | <span data-ttu-id="11039-127">你父親。</span><span class="sxs-lookup"><span data-stu-id="11039-127">Your father.</span></span>                                              |
| <span data-ttu-id="11039-128">你喜歡我的父親的部分方式。</span><span class="sxs-lookup"><span data-stu-id="11039-128">You are like my father in some ways.</span></span>                | <span data-ttu-id="11039-129">您看到什麼非常相似？</span><span class="sxs-lookup"><span data-stu-id="11039-129">What resemblance do you see?</span></span>                              |



 

<span data-ttu-id="11039-130">醫生計畫可以分割成用戶端和伺服器端應用程式。</span><span class="sxs-lookup"><span data-stu-id="11039-130">The Doctor program can be split into client-side and server-side applications.</span></span> <span data-ttu-id="11039-131">用戶端會提示患者輸入，並顯示醫生的回應。</span><span class="sxs-lookup"><span data-stu-id="11039-131">The client side prompts the patient for input and displays the doctor's response.</span></span> <span data-ttu-id="11039-132">伺服器端會處理患者輸入，並產生醫生的回應。</span><span class="sxs-lookup"><span data-stu-id="11039-132">The server side processes the patient input and generates the doctor's response.</span></span> <span data-ttu-id="11039-133">這是典型的用戶端-伺服器應用程式範例：用戶端會負責使用者互動，而伺服器會處理大量的計算負載。</span><span class="sxs-lookup"><span data-stu-id="11039-133">This is a classic example of a client-server application: the client is responsible for user interaction while the server handles the extensive computational load.</span></span> <span data-ttu-id="11039-134">由於資料可能需要大量的處理，因此它不會將資料傳遞給函式，也不會傳回資料，而是由伺服器處理。</span><span class="sxs-lookup"><span data-stu-id="11039-134">Not much data is passed to and returned by the function but, because the data can require a significant amount of processing, the server processes it.</span></span>

<span data-ttu-id="11039-135">醫生計畫使用字元陣列進行輸入，並傳回另一個字元陣列作為輸出。</span><span class="sxs-lookup"><span data-stu-id="11039-135">The Doctor program uses a character array for input and returns another character array as output.</span></span> <span data-ttu-id="11039-136">下表列出在用戶端和伺服器之間傳遞字元陣列的四種方式，以及執行每個方法所需的屬性和函式。</span><span class="sxs-lookup"><span data-stu-id="11039-136">The table below lists four ways to pass character arrays between the client and server, and the attributes and functions needed to implement each approach.</span></span>



| <span data-ttu-id="11039-137">方法</span><span class="sxs-lookup"><span data-stu-id="11039-137">Approach</span></span>                       | <span data-ttu-id="11039-138">屬性或函數</span><span class="sxs-lookup"><span data-stu-id="11039-138">Attributes or functions</span></span>                                                                                                        |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11039-139">計算的字元陣列</span><span class="sxs-lookup"><span data-stu-id="11039-139">Counted character arrays</span></span>       | <span data-ttu-id="11039-140">\[[大小 \_ 為](/windows/desktop/Midl/size-is) \] ， \[ [長度 \_ 為](/windows/desktop/Midl/length-is) \] ， \[ [參考](/windows/desktop/Midl/ref)\]</span><span class="sxs-lookup"><span data-stu-id="11039-140">\[ [size\_is](/windows/desktop/Midl/size-is)\], \[ [length\_is](/windows/desktop/Midl/length-is)\], \[ [ref](/windows/desktop/Midl/ref)\]</span></span>                                         |
| <span data-ttu-id="11039-141">Stub 管理的字串</span><span class="sxs-lookup"><span data-stu-id="11039-141">Stub-managed strings</span></span>           | <span data-ttu-id="11039-142">\[[](/windows/desktop/Midl/string) \] \[ [](/windows/desktop/Midl/ref) \] 伺服器上的字串、ref、 [midl \_ 使用者 \_ 配置](/windows/desktop/Midl/midl-user-allocate-1)</span><span class="sxs-lookup"><span data-stu-id="11039-142">\[ [string](/windows/desktop/Midl/string)\], \[ [ref](/windows/desktop/Midl/ref)\], [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1) on server</span></span>                  |
| <span data-ttu-id="11039-143">Stub 管理的字串</span><span class="sxs-lookup"><span data-stu-id="11039-143">Stub-managed strings</span></span>           | <span data-ttu-id="11039-144">\[[](/windows/desktop/Midl/string) \] \[ [](/windows/desktop/Midl/unique) \] 用戶端和伺服器上的字串、唯一、 [midl \_ 使用者 \_ 配置](/windows/desktop/Midl/midl-user-allocate-1)</span><span class="sxs-lookup"><span data-stu-id="11039-144">\[ [string](/windows/desktop/Midl/string)\], \[ [unique](/windows/desktop/Midl/unique)\], [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1) on client and server</span></span> |
| <span data-ttu-id="11039-145">傳回字串的函式</span><span class="sxs-lookup"><span data-stu-id="11039-145">Function that returns a string</span></span> | <span data-ttu-id="11039-146">\[[唯一](/windows/desktop/Midl/unique)\]</span><span class="sxs-lookup"><span data-stu-id="11039-146">\[ [unique](/windows/desktop/Midl/unique)\]</span></span>                                                                                                     |



 

<span data-ttu-id="11039-147">在與這些屬性組合相關聯的條件約束中，有其他方式可將一個字元陣列從用戶端傳送到伺服器，並將另一個字元陣列從伺服器傳回至用戶端。</span><span class="sxs-lookup"><span data-stu-id="11039-147">Within the constraints associated with these combinations of attributes, there are alternative ways of sending one character array from client to server and of returning another character array from server to client.</span></span>

<span data-ttu-id="11039-148">下列主題示範可管理這些參數的各種介面之間的設計取捨。</span><span class="sxs-lookup"><span data-stu-id="11039-148">The following topics demonstrate the design trade-offs between the various interfaces that can manage these parameters.</span></span>

-   [<span data-ttu-id="11039-149">計算的字元陣列</span><span class="sxs-lookup"><span data-stu-id="11039-149">Counted Character Arrays</span></span>](counted-character-arrays.md)
-   [<span data-ttu-id="11039-150">字串</span><span class="sxs-lookup"><span data-stu-id="11039-150">Strings</span></span>](strings.md)
-   [<span data-ttu-id="11039-151">多個指標層級</span><span class="sxs-lookup"><span data-stu-id="11039-151">Multiple Levels of Pointers</span></span>](multiple-levels-of-pointers.md)

 

 