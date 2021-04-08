---
title: 名稱語法
description: 遠端程序呼叫 (RPC) 和名稱語法。
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d024130a5b8a873c6bfbb2194542344953625d5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932397"
---
# <a name="name-syntax"></a><span data-ttu-id="f1569-103">名稱語法</span><span class="sxs-lookup"><span data-stu-id="f1569-103">Name Syntax</span></span>

<span data-ttu-id="f1569-104">Microsoft RPC 接受符合下列語法的名稱：</span><span class="sxs-lookup"><span data-stu-id="f1569-104">Microsoft RPC accepts names that conform to the following syntax:</span></span>

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a><span data-ttu-id="f1569-105">參數</span><span class="sxs-lookup"><span data-stu-id="f1569-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1569-106"><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="f1569-106"><span id="name"></span><span id="NAME"></span>name</span></span>
</dt> <dd>

<span data-ttu-id="f1569-107">指定可包含任何字元的識別碼，除分隔斜線 (/) 字元以外。</span><span class="sxs-lookup"><span data-stu-id="f1569-107">Specifies an identifier that can contain any character except the delimiting slash (/) character.</span></span>

</dd> <dt>

<span data-ttu-id="f1569-108"><span id="domainname"></span><span id="DOMAINNAME"></span>domainname</span><span class="sxs-lookup"><span data-stu-id="f1569-108"><span id="domainname"></span><span id="DOMAINNAME"></span>domainname</span></span>
</dt> <dd>

<span data-ttu-id="f1569-109">指定網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1569-109">Specifies the name of the domain.</span></span>

</dd> </dl>

<span data-ttu-id="f1569-110">選取名稱-語法類型的參數，以及指定名稱的字串，會提供給許多名稱服務介面 (NSI) RPC 函數。</span><span class="sxs-lookup"><span data-stu-id="f1569-110">A parameter that selects the name-syntax type and the string that specifies the name are supplied to many of the name service interface (NSI) RPC functions.</span></span>

<span data-ttu-id="f1569-111">Microsoft RPC 只支援一個名稱語法類型，如常數 RPC \_ C \_ NS \_ 語法 DCE 所指定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1569-111">Only one name-syntax type is supported by Microsoft RPC, as specified by the constant RPC\_C\_NS\_SYNTAX\_DCE.</span></span> <span data-ttu-id="f1569-112">這個常數定義在標頭檔 RPCNSI 中。</span><span class="sxs-lookup"><span data-stu-id="f1569-112">This constant is defined in the header file RPCNSI.H.</span></span>

<span data-ttu-id="f1569-113">RPC \_ C NS 語法 DCE 指定的名稱語法 \_ \_ \_ 是憑證 \_ DCE Cell Directory 服務 (cd) 名稱語法的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f1569-113">The name syntax specified by RPC\_C\_NS\_SYNTAX\_DCE is an extension of the OSF\_DCE Cell Directory Service (CDS) name syntax.</span></span> <span data-ttu-id="f1569-114">指定功能變數名稱的能力代表該語法的延伸。</span><span class="sxs-lookup"><span data-stu-id="f1569-114">The ability to specify a domain name represents an extension to that syntax.</span></span> <span data-ttu-id="f1569-115">只要整個字串小於256個字元，就能以斜線字元分隔的名稱沒有絕對限制。</span><span class="sxs-lookup"><span data-stu-id="f1569-115">There is no absolute limit on the number of names that can be separated by slash characters as long as the overall string is less than 256 characters.</span></span>

<span data-ttu-id="f1569-116">斜線可讓您指定名稱的邏輯結構，但不會對應至物件本身中的邏輯結構。</span><span class="sxs-lookup"><span data-stu-id="f1569-116">The slashes allow you to specify a logical structure to the name, but they do not correspond to a logical structure in the objects themselves.</span></span>

 

 




