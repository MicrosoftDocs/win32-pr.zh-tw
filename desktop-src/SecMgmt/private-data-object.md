---
description: 在每個系統上都可以使用有限數目的私用資料物件，目的是要以受保護、加密的方式儲存資訊。
ms.assetid: 927473d7-b5bc-4b6f-b303-8a0f8680731d
title: 私用資料物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccacd1334c9859495acf89075b77a0f10af4cb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112661"
---
# <a name="private-data-object"></a><span data-ttu-id="858bc-103">私用資料物件</span><span class="sxs-lookup"><span data-stu-id="858bc-103">Private Data Object</span></span>

<span data-ttu-id="858bc-104">在每個系統上都可以使用有限數目的私用資料物件，目的是要以受保護、加密的方式儲存資訊。</span><span class="sxs-lookup"><span data-stu-id="858bc-104">A limited number of private data objects are available on each system for the purpose of storing information in a protected, encrypted, fashion.</span></span>

<span data-ttu-id="858bc-105">私用資料物件主要是用來支援伺服器帳戶密碼的儲存。</span><span class="sxs-lookup"><span data-stu-id="858bc-105">Private data objects are provided primarily to support storage of server account passwords.</span></span> <span data-ttu-id="858bc-106">這適用于在特定帳戶中執行的伺服器。</span><span class="sxs-lookup"><span data-stu-id="858bc-106">This is useful for servers that run in a specific account.</span></span> <span data-ttu-id="858bc-107">伺服器帳戶的密碼是私用資料，應該受到保護，但需要用來登入伺服器。</span><span class="sxs-lookup"><span data-stu-id="858bc-107">The password of the server account is private data that should be secured but is needed to log the server on.</span></span>

<span data-ttu-id="858bc-108">私用資料物件可能是一般用途，也可能是以下三種特製化類型的其中一種：本機、全域和電腦。</span><span class="sxs-lookup"><span data-stu-id="858bc-108">Private data objects may be general purpose, or they may be one of three specialized types: local, global, and machine.</span></span>

<span data-ttu-id="858bc-109">本機私用資料物件只能從儲存物件的電腦讀取本機。</span><span class="sxs-lookup"><span data-stu-id="858bc-109">Local private data objects can only be read locally from the computer storing the object.</span></span> <span data-ttu-id="858bc-110">嘗試從遠端讀取它們會導致狀態 \_ 拒絕存取 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="858bc-110">Attempting to read them remotely results in a STATUS\_ACCESS\_DENIED error.</span></span> <span data-ttu-id="858bc-111">本機私用資料物件的索引鍵名稱開頭為 "L $" 前置詞。</span><span class="sxs-lookup"><span data-stu-id="858bc-111">Local private data objects have key names that begin with the prefix "L$".</span></span> <span data-ttu-id="858bc-112">除了您所建立的本機私用物件之外，作業系統也會定義下列本機私用物件： $machine. acc、SAC、SAI 和 SANSC。</span><span class="sxs-lookup"><span data-stu-id="858bc-112">In addition to the local private objects you create, the operating system defines the following local private objects: $machine.acc, SAC, SAI, and SANSC.</span></span>

<span data-ttu-id="858bc-113">全域私用資料物件是全域的，如果它們是在網域控制站上建立的，就會自動複寫到該網域中的所有網域控制站。</span><span class="sxs-lookup"><span data-stu-id="858bc-113">Global private data objects are global in the sense that if they are created on a domain controller, they will be automatically replicated to all domain controllers in that domain.</span></span> <span data-ttu-id="858bc-114">換句話說，該網域中的每個網域控制站都可以存取全域私用資料物件所包含的值。</span><span class="sxs-lookup"><span data-stu-id="858bc-114">In other words, each domain controller in that domain will have access to the values the global private data object contains.</span></span> <span data-ttu-id="858bc-115">相反地，在不是網域控制站的系統上建立的全域私用資料物件，以及 nonglobal 的私用資料物件則不會進行複寫。</span><span class="sxs-lookup"><span data-stu-id="858bc-115">In contrast, global private data objects created on a system that is not a domain controller, as well as nonglobal private data objects, are not replicated.</span></span> <span data-ttu-id="858bc-116">全域私用資料物件的索引鍵名稱是以 "G $" 開頭。</span><span class="sxs-lookup"><span data-stu-id="858bc-116">Global private data objects have key names beginning with "G$".</span></span>

<span data-ttu-id="858bc-117">只有作業系統才能存取電腦私用資料物件。</span><span class="sxs-lookup"><span data-stu-id="858bc-117">Machine private data objects can be accessed only by the operating system.</span></span> <span data-ttu-id="858bc-118">這些物件的索引鍵名稱以 "M $" 開頭。</span><span class="sxs-lookup"><span data-stu-id="858bc-118">These objects have key names that begin with "M$".</span></span>

<span data-ttu-id="858bc-119">**注意**  您可以設定，但無法取出電腦私用資料物件。</span><span class="sxs-lookup"><span data-stu-id="858bc-119">**Note**  You can set, but you cannot retrieve, machine private data objects.</span></span>

<span data-ttu-id="858bc-120">除了這些前置詞之外，下列值也會指出本機或電腦物件。</span><span class="sxs-lookup"><span data-stu-id="858bc-120">In addition to these prefixes, the following values also indicate local or machine objects.</span></span> <span data-ttu-id="858bc-121">為了回溯相容性支援這些值，當您建立新的本機或電腦物件時，不應使用這些值。</span><span class="sxs-lookup"><span data-stu-id="858bc-121">These values are supported for backward compatibility and should not be used when you create new local or machine objects.</span></span> <span data-ttu-id="858bc-122">本機私用資料物件的索引鍵名稱也可以開頭為 "RasDialParms" 或 "RasCredentials"。</span><span class="sxs-lookup"><span data-stu-id="858bc-122">The key name of local private data objects may also start with "RasDialParms" or "RasCredentials".</span></span> <span data-ttu-id="858bc-123">電腦物件的索引鍵名稱可能也會以 "NL $" 或 " \_ sc \_ " 開頭。</span><span class="sxs-lookup"><span data-stu-id="858bc-123">The key name for machine objects may also start with, "NL$" or "\_sc\_".</span></span>

<span data-ttu-id="858bc-124">非上述任何特製化類型中的私用資料物件使用不是以前置詞開頭的索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="858bc-124">Private data objects that are not one of the preceding specialized types use key names that do not start with a prefix.</span></span> <span data-ttu-id="858bc-125">這些物件不會進行複寫，而且可以在本機或遠端讀取應用程式。</span><span class="sxs-lookup"><span data-stu-id="858bc-125">These objects are not replicated and can be read either locally or remotely by applications.</span></span>

 

 



