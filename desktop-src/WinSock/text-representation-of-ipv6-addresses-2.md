---
description: 此區段會從 &\# 0034; IPv6 定址架構&\# 0034; 由 R 複製。
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: IPv6 位址的文字標記法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df97c1c8933f3708fee56e34e05f918d531d2a13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978897"
---
# <a name="text-representation-of-ipv6-addresses"></a><span data-ttu-id="5bb15-103">IPv6 位址的文字標記法</span><span class="sxs-lookup"><span data-stu-id="5bb15-103">Text Representation of IPv6 Addresses</span></span>

<span data-ttu-id="5bb15-104">此區段是從「IPv6 定址架構」（Hinden 和 Deering）複製而來。</span><span class="sxs-lookup"><span data-stu-id="5bb15-104">This section is copied from "IPv6 Addressing Architecture" by R. Hinden and S. Deering.</span></span> <span data-ttu-id="5bb15-105">有三種傳統形式可將 IPv6 位址表示為文字字串：</span><span class="sxs-lookup"><span data-stu-id="5bb15-105">There are three conventional forms for representing IPv6 addresses as text strings:</span></span>

-   <span data-ttu-id="5bb15-106">慣用的表單是 x：x： x：x： x：x： x：x，其中 ' x ' 是位址之 8 16 位部分的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="5bb15-106">The preferred form is x:x:x:x:x:x:x:x, where the 'x's are the hexadecimal values of the eight 16-bit pieces of the address.</span></span>

    <span data-ttu-id="5bb15-107">範例：</span><span class="sxs-lookup"><span data-stu-id="5bb15-107">Examples:</span></span>

    <dl> <span data-ttu-id="5bb15-108">FEDC： BA98：7654：3210： FEDC： BA98：7654：3210</span><span class="sxs-lookup"><span data-stu-id="5bb15-108">FEDC:BA98:7654:3210:FEDC:BA98:7654:3210</span></span>  
    <span data-ttu-id="5bb15-109">1080：0：0：0：8：800：200C：417A</span><span class="sxs-lookup"><span data-stu-id="5bb15-109">1080:0:0:0:8:800:200C:417A</span></span>  
    </dl>

> [!Note]  
> <span data-ttu-id="5bb15-110">不需要在個別欄位中撰寫前置零，但每個欄位中必須至少有一個數位 (但第二個表單) 所述的案例除外。</span><span class="sxs-lookup"><span data-stu-id="5bb15-110">It is not necessary to write the leading zeros in an individual field, but there must be at least one numeral in every field (except for the case described in the second form).</span></span>

 

-   <span data-ttu-id="5bb15-111">由於配置了某些 IPv6 位址樣式的方法，因此位址通常會包含長度為零位的長字串。</span><span class="sxs-lookup"><span data-stu-id="5bb15-111">Due to the method of allocating certain styles of IPv6 addresses, it is common for addresses to contain long strings of zero bits.</span></span> <span data-ttu-id="5bb15-112">為了讓您更輕鬆地撰寫包含零位的位址，有一種特殊的語法可壓縮零。</span><span class="sxs-lookup"><span data-stu-id="5bb15-112">In order to make writing addresses containing zero bits easier, a special syntax is available to compress the zeros.</span></span> <span data-ttu-id="5bb15-113">使用雙冒號 ( "：：" ) 指出多個16位零的群組。</span><span class="sxs-lookup"><span data-stu-id="5bb15-113">The use of double colons ("::") indicates multiple groups of 16-bits of zeros.</span></span>

    <span data-ttu-id="5bb15-114">例如，多播位址</span><span class="sxs-lookup"><span data-stu-id="5bb15-114">For example, the multicast address</span></span>

    <dl> <span data-ttu-id="5bb15-115">FF01：0：0：0：0：0：0：43</span><span class="sxs-lookup"><span data-stu-id="5bb15-115">FF01:0:0:0:0:0:0:43</span></span>  
    </dl>

    <span data-ttu-id="5bb15-116">可能會表示為：</span><span class="sxs-lookup"><span data-stu-id="5bb15-116">may be represented as:</span></span>

    <dl> <span data-ttu-id="5bb15-117">FF01：：43</span><span class="sxs-lookup"><span data-stu-id="5bb15-117">FF01::43</span></span>  
    </dl>

    <span data-ttu-id="5bb15-118">雙引號 ( "：：" ) 只能在位址中出現一次。</span><span class="sxs-lookup"><span data-stu-id="5bb15-118">The double quotation marks ("::") can only appear once in an address.</span></span> <span data-ttu-id="5bb15-119">可以用來壓縮位址中的前置或尾端零。</span><span class="sxs-lookup"><span data-stu-id="5bb15-119">They can be used to compress leading or trailing zeros in an address.</span></span>

-   <span data-ttu-id="5bb15-120">在處理 IPv4 和 IPv6 節點的混合式環境時，可能更方便的替代形式是 x：x： x：x： x：x： d. d. d. d，其中 ' x ' 是位址中六個高序位16位部分的十六進位值，而 ' d ' 是位址 (標準 IPv4 表示) 的四個低序位8位部分的十進位值。</span><span class="sxs-lookup"><span data-stu-id="5bb15-120">An alternative form that may be more convenient when dealing with a mixed environment of IPv4 and IPv6 nodes is x:x:x:x:x:x:d.d.d.d, where the 'x's are the hexadecimal values of the six high-order 16-bit pieces of the address, and the 'd's are the decimal values of the four low-order 8-bit pieces of the address (standard IPv4 representation).</span></span>

    <span data-ttu-id="5bb15-121">範例：</span><span class="sxs-lookup"><span data-stu-id="5bb15-121">Examples:</span></span>

    <dl> <span data-ttu-id="5bb15-122">0：0：0：0：0：0：13.1.68。3</span><span class="sxs-lookup"><span data-stu-id="5bb15-122">0:0:0:0:0:0:13.1.68.3</span></span>  
    <span data-ttu-id="5bb15-123">0：0：0：0：0： FFFF：129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="5bb15-123">0:0:0:0:0:FFFF:129.144.52.38</span></span>  
    </dl>

    <span data-ttu-id="5bb15-124">或壓縮格式：</span><span class="sxs-lookup"><span data-stu-id="5bb15-124">or in compressed form:</span></span>

    <dl> <span data-ttu-id="5bb15-125">::13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="5bb15-125">::13.1.68.3</span></span>  
    <span data-ttu-id="5bb15-126">：： FFFF：129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="5bb15-126">::FFFF:129.144.52.38</span></span>  
    </dl>

 

 



