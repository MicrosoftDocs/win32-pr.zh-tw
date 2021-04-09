---
title: " 在、字串和輸出中，字串原型"
description: 下列函式原型使用 \ in、string \ 參數和 out、string \ 參數的兩個參數。
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933554"
---
# <a name="in-string-and-out-string-prototype"></a><span data-ttu-id="dbaa3-103">\[在、字串 \] 和 \[ 輸出中，字串 \] 原型</span><span class="sxs-lookup"><span data-stu-id="dbaa3-103">\[in, string\] and \[out, string\] Prototype</span></span>

<span data-ttu-id="dbaa3-104">下列函數原型會使用兩個參數： \[ [**in**](/windows/desktop/Midl/in)、 [**string**](/windows/desktop/Midl/string) \] 參數和 \[ [**out**](/windows/desktop/Midl/out-idl)、 **string** \] 參數。</span><span class="sxs-lookup"><span data-stu-id="dbaa3-104">The following function prototype uses two parameters: an \[[**in**](/windows/desktop/Midl/in), [**string**](/windows/desktop/Midl/string)\] parameter and an \[[**out**](/windows/desktop/Midl/out-idl), **string**\] parameter.</span></span>

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

<span data-ttu-id="dbaa3-105">第一個參數只能 \[ [**是**](/windows/desktop/Midl/in) \] 。</span><span class="sxs-lookup"><span data-stu-id="dbaa3-105">The first parameter is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="dbaa3-106">此輸入字串只會從用戶端傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="dbaa3-106">This input string is only transmitted from the client to the server.</span></span> <span data-ttu-id="dbaa3-107">伺服器會使用它做為進一步處理的基礎。</span><span class="sxs-lookup"><span data-stu-id="dbaa3-107">The server uses it as the basis for further processing.</span></span> <span data-ttu-id="dbaa3-108">字串不會經過修改，而且用戶端不需要再次使用，因此不需要將它傳回至用戶端。</span><span class="sxs-lookup"><span data-stu-id="dbaa3-108">The string is not modified and is not required again by the client, so it does not have to be returned to the client.</span></span>

<span data-ttu-id="dbaa3-109">第二個參數（代表醫生的回應）只是 \[ [**輸出**](/windows/desktop/Midl/out-idl) \] 。</span><span class="sxs-lookup"><span data-stu-id="dbaa3-109">The second parameter, representing the doctor's response, is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="dbaa3-110">這個回應字串只會從伺服器傳送到用戶端。</span><span class="sxs-lookup"><span data-stu-id="dbaa3-110">This response string is only transmitted from the server to the client.</span></span> <span data-ttu-id="dbaa3-111">提供配置大小，讓伺服器存根可以為它配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="dbaa3-111">The allocation size is provided so that the server stubs can allocate memory for it.</span></span> <span data-ttu-id="dbaa3-112">因為 *pszOutput* 是 \[ [**ref**](/windows/desktop/Midl/ref) \] 指標，所以用戶端必須在呼叫之前配置足夠的記憶體給字串。</span><span class="sxs-lookup"><span data-stu-id="dbaa3-112">Since *pszOutput* is a \[[**ref**](/windows/desktop/Midl/ref)\] pointer, the client must have sufficient memory allocated for the string before the call.</span></span> <span data-ttu-id="dbaa3-113">當遠端程式傳回時，回應字串會寫入此記憶體區域中。</span><span class="sxs-lookup"><span data-stu-id="dbaa3-113">The response string is written into this area of memory when the remote procedure returns.</span></span>

 

 