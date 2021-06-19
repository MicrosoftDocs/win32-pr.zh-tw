---
title: " (RPC) 的帶正負號和不帶正負號的類型"
description: 瞭解 RPC 中的已簽署和不帶正負號的類型。 使用不同預設類型的編譯器可能會在您的分散式應用程式中造成軟體錯誤。
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c03010262c8492b6738d1e817e165e5ca8f839
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406541"
---
# <a name="signed-and-unsigned-types-rpc"></a><span data-ttu-id="92727-104"> (RPC) 的帶正負號和不帶正負號的類型</span><span class="sxs-lookup"><span data-stu-id="92727-104">Signed and Unsigned Types (RPC)</span></span>

<span data-ttu-id="92727-105">針對帶正負號和不帶正負號的類型使用不同預設值的編譯器可能會在分散式應用程式中造成軟體錯誤。</span><span class="sxs-lookup"><span data-stu-id="92727-105">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="92727-106">您可以明確地將您的字元類型宣告為 **帶正負** 號或不 **帶正負** 號，以避免這些問題。</span><span class="sxs-lookup"><span data-stu-id="92727-106">You can avoid these problems by explicitly declaring your character types as **signed** or **unsigned**.</span></span>

<span data-ttu-id="92727-107">MIDL 會定義要在目標 C 編譯器中採用與 **char** 類型相同之預設正負號的 [**小型**](/windows/desktop/Midl/small)型別。</span><span class="sxs-lookup"><span data-stu-id="92727-107">MIDL defines the [**small**](/windows/desktop/Midl/small) type to take the same default sign as the **char** type in the target C compiler.</span></span> <span data-ttu-id="92727-108">如果編譯器假設 **char** 未簽署，則 **小小** 部分也會定義為未簽署。</span><span class="sxs-lookup"><span data-stu-id="92727-108">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="92727-109">許多 C 編譯器可讓您將預設值變更為命令列選項。</span><span class="sxs-lookup"><span data-stu-id="92727-109">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="92727-110">例如，Microsoft C 編譯器 **/j** 命令列選項會將預設的 **char** 符號從 sign 變更為未簽署。</span><span class="sxs-lookup"><span data-stu-id="92727-110">For example, the Microsoft C compiler **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="92727-111">您也可以使用 MIDL 編譯器命令列參數 [**/char**](/windows/desktop/Midl/-char)來控制 **char** 和 **small** 類型變數的正負號。</span><span class="sxs-lookup"><span data-stu-id="92727-111">You can also control the sign of variables of type **char** and **small** with the MIDL compiler command-line switch [**/char**](/windows/desktop/Midl/-char).</span></span> <span data-ttu-id="92727-112">此參數可讓您指定編譯器所使用的預設符號。</span><span class="sxs-lookup"><span data-stu-id="92727-112">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="92727-113">MIDL 編譯器會在產生的標頭檔中明確宣告不符合 C 編譯器預設類型的所有 **char** 類型的正負號。</span><span class="sxs-lookup"><span data-stu-id="92727-113">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 
