---
title: /prefix 參數
description: /Prefix 參數會指示 MIDL 編譯器將前置詞字串新增至用戶端和/或伺服器 stub 常式名稱。
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- /prefix 參數 MIDL
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507625"
---
# <a name="prefix-switch"></a><span data-ttu-id="de754-104">/prefix 參數</span><span class="sxs-lookup"><span data-stu-id="de754-104">/prefix switch</span></span>

<span data-ttu-id="de754-105">**/Prefix** 參數會指示 MIDL 編譯器將前置詞字串新增至用戶端和/或伺服器 stub 常式名稱。</span><span class="sxs-lookup"><span data-stu-id="de754-105">The **/prefix** switch directs the MIDL compiler to add prefix strings to the client and/or server stub routine names.</span></span> <span data-ttu-id="de754-106">這可以用來允許單一程式同時是相同介面的用戶端和伺服器，而不會讓用戶端和伺服器端常式名稱彼此衝突。</span><span class="sxs-lookup"><span data-stu-id="de754-106">This can be used to allow a single program to be both a client and server of the same interface, without having the client- and server-side routine names conflict with each other.</span></span>

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a><span data-ttu-id="de754-107">切換選項</span><span class="sxs-lookup"><span data-stu-id="de754-107">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span data-ttu-id="de754-108"><span id="client"></span><span id="CLIENT"></span>用戶端 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="de754-108"><span id="client"></span><span id="CLIENT"></span>\*\*\*\*client\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="de754-109">只會影響用戶端存根常式名稱。</span><span class="sxs-lookup"><span data-stu-id="de754-109">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span data-ttu-id="de754-110"><span id="cstub"></span><span id="CSTUB"></span>cstub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="de754-110"><span id="cstub"></span><span id="CSTUB"></span>\*\*\*\*cstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="de754-111">與 *用戶端* 相同。</span><span class="sxs-lookup"><span data-stu-id="de754-111">Same as *client*.</span></span> <span data-ttu-id="de754-112">只會影響用戶端存根常式名稱。</span><span class="sxs-lookup"><span data-stu-id="de754-112">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="de754-113"><span id="server"></span><span id="SERVER"></span>伺服器 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="de754-113"><span id="server"></span><span id="SERVER"></span>\*\*\*\*server\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="de754-114">只會影響伺服器 stub 常式所呼叫的常式名稱。</span><span class="sxs-lookup"><span data-stu-id="de754-114">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span data-ttu-id="de754-115"><span id="sstub"></span><span id="SSTUB"></span>sstub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="de754-115"><span id="sstub"></span><span id="SSTUB"></span>\*\*\*\*sstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="de754-116">與 *伺服器* 相同。</span><span class="sxs-lookup"><span data-stu-id="de754-116">Same as *server*.</span></span> <span data-ttu-id="de754-117">只會影響伺服器 stub 常式所呼叫的常式名稱。</span><span class="sxs-lookup"><span data-stu-id="de754-117">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="de754-118"><span id="switch"></span><span id="SWITCH"></span>切換 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="de754-118"><span id="switch"></span><span id="SWITCH"></span>\*\*\*\*switch\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="de754-119">會影響新增至標頭檔的額外原型。</span><span class="sxs-lookup"><span data-stu-id="de754-119">Affects an extra prototype added to the header file.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="de754-120"><span id="all"></span><span id="ALL"></span>全部 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="de754-120"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="de754-121">會影響用戶端和伺服器 stub 常式名稱。</span><span class="sxs-lookup"><span data-stu-id="de754-121">Affects both the client and server stub routine names.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de754-122">備註</span><span class="sxs-lookup"><span data-stu-id="de754-122">Remarks</span></span>

<span data-ttu-id="de754-123">如果用戶端常式的前置詞與伺服器端常式的前置詞不同，則產生的標頭檔會有用戶端常式原型和伺服器端常式原型。</span><span class="sxs-lookup"><span data-stu-id="de754-123">If the prefix for the client-side routines is different from the prefix for the server-side routines, the generated header file will have both client-side routine prototypes and server-side routine prototypes.</span></span>

<span data-ttu-id="de754-124">當單一標頭檔會與多個 MIDL 編譯器執行的存根搭配使用時， **/prefix** 參數會很有用。</span><span class="sxs-lookup"><span data-stu-id="de754-124">The **/prefix** switch is useful when a single header file will be used with stubs from multiple runs of the MIDL compiler.</span></span> <span data-ttu-id="de754-125">這會在標頭檔中強制執行其他常式原型。</span><span class="sxs-lookup"><span data-stu-id="de754-125">This forces additional routine prototypes in the header file.</span></span>

<span data-ttu-id="de754-126">在所有情況下，用戶端、伺服器和交換器前置詞都會覆寫所有前置詞。</span><span class="sxs-lookup"><span data-stu-id="de754-126">In all cases, the client, server, and switch prefixes will override an all prefix.</span></span>

## <a name="examples"></a><span data-ttu-id="de754-127">範例</span><span class="sxs-lookup"><span data-stu-id="de754-127">Examples</span></span>

<span data-ttu-id="de754-128">**midl/prefix 用戶端 "c \_ " 伺服器 "s \_ "**</span><span class="sxs-lookup"><span data-stu-id="de754-128">**midl /prefix client "c\_" server "s\_"**</span></span>

<span data-ttu-id="de754-129">**midl/prefix 所有 "moo \_ "**</span><span class="sxs-lookup"><span data-stu-id="de754-129">**midl /prefix all "moo\_"**</span></span>

<span data-ttu-id="de754-130">**midl/prefix 用戶端 "吠 \_ "**</span><span class="sxs-lookup"><span data-stu-id="de754-130">**midl /prefix client "bark\_"**</span></span>

## <a name="see-also"></a><span data-ttu-id="de754-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de754-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de754-132">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="de754-132">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




