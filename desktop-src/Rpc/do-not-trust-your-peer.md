---
title: 不要信任您的對等
description: '\ 0034; 請勿信任您的對等 \ 0034;是基本安全性規則，但通常會被忽略。'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c5c7ba3760e14a66fb4765000c7a6698599b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672843"
---
# <a name="do-not-trust-your-peer"></a><span data-ttu-id="a00f7-103">不要信任您的對等</span><span class="sxs-lookup"><span data-stu-id="a00f7-103">Do Not Trust Your Peer</span></span>

<span data-ttu-id="a00f7-104">「請勿信任您的對等」是基本安全性規則，但通常會被忽略。</span><span class="sxs-lookup"><span data-stu-id="a00f7-104">"Do not trust your peer" is a basic security rule, but it is often overlooked.</span></span> <span data-ttu-id="a00f7-105">請勿假設通訊中的另一方會正常運作，而且不會假設您的對等會傳遞您預期的資料。</span><span class="sxs-lookup"><span data-stu-id="a00f7-105">Do not assume the other party in a communication will behave properly, and do not assume your peer will pass the data you expect.</span></span> <span data-ttu-id="a00f7-106">MIDL 和 RPC 會代表您執行一些檢查，但不會檢查所有的檢查。</span><span class="sxs-lookup"><span data-stu-id="a00f7-106">MIDL and RPC perform some checks on your behalf, but not all checks.</span></span>

<span data-ttu-id="a00f7-107">知道哪些是 MIDL 或 RPC 驗證的參數層面，以及您必須自行驗證的層面。</span><span class="sxs-lookup"><span data-stu-id="a00f7-107">Know which aspect of the parameters are verified by MIDL or RPC, and which aspects you must verify yourself.</span></span> <span data-ttu-id="a00f7-108">例如，對於 in/out 內容控制碼，RPC 會確認內容控制碼不是不正確非 null 值。</span><span class="sxs-lookup"><span data-stu-id="a00f7-108">For example, for in/out context handles, RPC verifies the context handle is not an invalid non-null value.</span></span> <span data-ttu-id="a00f7-109">它允許 null 值和有效值，但許多開發人員並不知道 null 值是否為 let。</span><span class="sxs-lookup"><span data-stu-id="a00f7-109">It allows null values and valid values, but many developers are not aware that null values are let through.</span></span> <span data-ttu-id="a00f7-110">這是要檢查的內容。</span><span class="sxs-lookup"><span data-stu-id="a00f7-110">This is something to check for.</span></span>

<span data-ttu-id="a00f7-111">即使您通常信任對等，也請務必不要導入遭到入侵的機器或主體帳戶可以攻擊其他電腦的新路徑。</span><span class="sxs-lookup"><span data-stu-id="a00f7-111">Even if you generally trust your peer, be sure not to introduce new paths by which a compromised machine or principal account can attack other machines.</span></span> <span data-ttu-id="a00f7-112">假設使用者選擇他的生日做為密碼，並被攻擊者猜得到。</span><span class="sxs-lookup"><span data-stu-id="a00f7-112">Imagine that a user chooses his birthday as his password, and it is guessed by an attacker.</span></span> <span data-ttu-id="a00f7-113">即使在使用者的要求經過驗證並存取其資料的情況下，仍請確定可利用的攻擊弱點並不存在，例如，可能會讓攻擊者控制您伺服器的堆疊溢位，並延長安全性缺口。</span><span class="sxs-lookup"><span data-stu-id="a00f7-113">Even after requests from the user are authenticated and access to his data is allowed, make sure exploitable vulnerabilities do not exist, such stack overruns that may allow an attacker to take control of your server and extend the security breach.</span></span>

 

 




