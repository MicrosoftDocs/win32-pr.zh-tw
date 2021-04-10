---
description: 如果資料是一致的，則會同步處理伺服器和所有用戶端上的資料。 有一種提供資料一致性的軟體系統，就是 (RCS) 的修訂控制系統。
ms.assetid: cd33d20e-bf25-4a50-9b20-344495554434
title: 資料一致性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f300296ff0fdc807beb95e2c03662814957bedb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851583"
---
# <a name="data-coherency"></a><span data-ttu-id="1c263-104">資料一致性</span><span class="sxs-lookup"><span data-stu-id="1c263-104">Data Coherency</span></span>

<span data-ttu-id="1c263-105">*一致* 的資料是網路上相同的資料。</span><span class="sxs-lookup"><span data-stu-id="1c263-105">Data that is *coherent* is data that is the same across the network.</span></span> <span data-ttu-id="1c263-106">換句話說，如果資料是一致的，則會同步處理伺服器和所有用戶端上的資料。</span><span class="sxs-lookup"><span data-stu-id="1c263-106">In other words, if data is coherent, data on the server and all the clients is synchronized.</span></span> <span data-ttu-id="1c263-107">有一種提供資料一致性的軟體系統，就是 (RCS) 的修訂控制系統。</span><span class="sxs-lookup"><span data-stu-id="1c263-107">One type of software system that provides data coherency is a revision control system (RCS).</span></span> <span data-ttu-id="1c263-108">這類系統通常相當簡單，只允許一位使用者一次修改指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="1c263-108">Such a system is usually fairly simple, with only one user allowed to modify a specified file at a time.</span></span> <span data-ttu-id="1c263-109">其他人可以讀取該檔案，但無法加以變更。</span><span class="sxs-lookup"><span data-stu-id="1c263-109">Others can read the file but cannot change it.</span></span>

<span data-ttu-id="1c263-110">可以變更檔案的使用者稱為已簽出。使用者接著會簽入修改過的檔案，讓其他人可以看到變更。</span><span class="sxs-lookup"><span data-stu-id="1c263-110">The user who can change a file is said to have checked it out. The user then checks in the modified file so that others may see the changes.</span></span> <span data-ttu-id="1c263-111">只有在使用者已簽回檔案之後，其他使用者才能簽出檔案。</span><span class="sxs-lookup"><span data-stu-id="1c263-111">Only after the user has checked a file back in can another user check it out.</span></span>

<span data-ttu-id="1c263-112">RCS 需要使用者的積極介入才能以實用的方式操作。</span><span class="sxs-lookup"><span data-stu-id="1c263-112">An RCS requires the active intervention of users to operate in a useful manner.</span></span> <span data-ttu-id="1c263-113">在網路上操作的檔案系統應該會自動處理此問題。</span><span class="sxs-lookup"><span data-stu-id="1c263-113">A file system that operates across a network should handle the problem automatically.</span></span>

<span data-ttu-id="1c263-114">當某個用戶端上有一個執行緒在一次存取整個網路上的檔案時，提供一致資料的本機快取相當簡單。</span><span class="sxs-lookup"><span data-stu-id="1c263-114">Providing local caching of coherent data is fairly simple when you have one thread on one client accessing a file across the network at a time.</span></span> <span data-ttu-id="1c263-115">不過，在大部分情況下，一或多部電腦上有許多不同的執行緒可能會讀取相同的檔案。</span><span class="sxs-lookup"><span data-stu-id="1c263-115">However, in most situations many different threads on one or more computers may be reading the same file.</span></span> <span data-ttu-id="1c263-116">這種情況仍相當簡單。</span><span class="sxs-lookup"><span data-stu-id="1c263-116">This situation is still fairly straightforward.</span></span> <span data-ttu-id="1c263-117">由於檔案中的資料是靜態的，因此每一部用戶端電腦都可以有自己的本機複本，而不會影響資料的一致性。</span><span class="sxs-lookup"><span data-stu-id="1c263-117">Because the data in the file is static, each client computer can have its own local copy with no implications for data coherency.</span></span>

<span data-ttu-id="1c263-118">較常見的情況是修改檔案的一個執行緒，還有許多其他的執行緒讀取。</span><span class="sxs-lookup"><span data-stu-id="1c263-118">A more common situation is one thread modifying the file, and a lot of other threads reading it.</span></span> <span data-ttu-id="1c263-119">寫入作業發生時，該檔案的所有本機快取都會淘汰。</span><span class="sxs-lookup"><span data-stu-id="1c263-119">The moment a write operation occurs, all of the local caches of that file are obsolete.</span></span> <span data-ttu-id="1c263-120">伺服器必須通知每個用戶端放棄其快取。</span><span class="sxs-lookup"><span data-stu-id="1c263-120">The server must notify each client to abandon its cache.</span></span> <span data-ttu-id="1c263-121">檔案的任何後續讀取作業都必須跨網路執行。</span><span class="sxs-lookup"><span data-stu-id="1c263-121">Any subsequent read operations for the file must be performed across the network.</span></span>

<span data-ttu-id="1c263-122">在另一種常見的情況下，一個或多個網路用戶端上的多個執行緒可能會嘗試寫入相同的檔案。</span><span class="sxs-lookup"><span data-stu-id="1c263-122">In another common situation, multiple threads on one or more network clients might try to write to the same file.</span></span> <span data-ttu-id="1c263-123">這種情況類似于多個 RCS 使用者都想要對相同的檔案進行變更。</span><span class="sxs-lookup"><span data-stu-id="1c263-123">This situation is similar to a one in which several RCS users all want to make changes to the same file.</span></span> <span data-ttu-id="1c263-124">順序中的每個使用者都必須簽出檔案、進行變更，然後再簽回檔案。</span><span class="sxs-lookup"><span data-stu-id="1c263-124">Each user in sequence must check out the file, make changes, and then check the file back in.</span></span> <span data-ttu-id="1c263-125">同樣地，在本機快取配置中，伺服器必須一次將寫入檔案的許可權移交給一個用戶端執行緒。</span><span class="sxs-lookup"><span data-stu-id="1c263-125">Similarly, in a local caching scheme the server must hand off the privilege of writing to a file to one client thread at a time.</span></span>

 

 



