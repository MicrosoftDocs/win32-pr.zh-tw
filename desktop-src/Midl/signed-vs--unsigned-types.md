---
title: " (MIDL) 的帶正負號和不帶正負號類型"
description: 針對帶正負號和不帶正負號的類型使用不同預設值的編譯器可能會在分散式應用程式中造成軟體錯誤。
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- 資料類型 MIDL、帶正負號和不帶正負號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e38fbe1dc27eebae7c7933db1d699600370d960
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383550"
---
# <a name="signed-and-unsigned-types-midl"></a><span data-ttu-id="8d10f-104"> (MIDL) 的帶正負號和不帶正負號類型</span><span class="sxs-lookup"><span data-stu-id="8d10f-104">Signed and Unsigned Types (MIDL)</span></span>

<span data-ttu-id="8d10f-105">針對帶正負號和不帶正負號的類型使用不同預設值的編譯器可能會在分散式應用程式中造成軟體錯誤。</span><span class="sxs-lookup"><span data-stu-id="8d10f-105">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="8d10f-106">您可以明確地將您的字元類型宣告為帶正負號或不帶正負號，以避免這些問題。</span><span class="sxs-lookup"><span data-stu-id="8d10f-106">You can avoid these problems by explicitly declaring your character types as signed or unsigned.</span></span> <span data-ttu-id="8d10f-107">請注意，DCE IDL 編譯器無法辨識關鍵字 [**簽署**](signed.md)。</span><span class="sxs-lookup"><span data-stu-id="8d10f-107">Note that DCE IDL compilers do not recognize the keyword [**signed**](signed.md).</span></span> <span data-ttu-id="8d10f-108">因此，當您使用 MIDL 編譯器/**憑證** 參數時，就無法使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="8d10f-108">Therefore, this feature is not available when you use the MIDL compiler /**osf** switch.</span></span>

<span data-ttu-id="8d10f-109">MIDL 會定義要在目標 C 編譯器中採用與 [**char**](char-idl.md)類型相同之預設正負號的 [**小型**](small.md)型別。</span><span class="sxs-lookup"><span data-stu-id="8d10f-109">MIDL defines the [**small**](small.md) type to take the same default sign as the [**char**](char-idl.md) type in the target C compiler.</span></span> <span data-ttu-id="8d10f-110">如果編譯器假設 **char** 未簽署，則 **小小** 部分也會定義為未簽署。</span><span class="sxs-lookup"><span data-stu-id="8d10f-110">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="8d10f-111">許多 C 編譯器可讓您將預設值變更為命令列選項。</span><span class="sxs-lookup"><span data-stu-id="8d10f-111">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="8d10f-112">例如，在 Microsoft Visual C++ 開發環境中， **/j** 命令列選項會將預設的 **char** 符號從 [已簽署] 變更為 [未簽署]。</span><span class="sxs-lookup"><span data-stu-id="8d10f-112">For example, in the Microsoft Visual C++ development environment, the **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="8d10f-113">您也可以使用 MIDL 編譯器命令列參數 [**/char**](-char.md)來控制 [**char**](char-idl.md)和 [**small**](small.md)類型變數的正負號。</span><span class="sxs-lookup"><span data-stu-id="8d10f-113">You can also control the sign of variables of type [**char**](char-idl.md) and [**small**](small.md) with the MIDL compiler command-line switch [**/char**](-char.md).</span></span> <span data-ttu-id="8d10f-114">此參數可讓您指定編譯器所使用的預設符號。</span><span class="sxs-lookup"><span data-stu-id="8d10f-114">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="8d10f-115">MIDL 編譯器會在產生的標頭檔中明確宣告不符合 C 編譯器預設類型的所有 **char** 類型的正負號。</span><span class="sxs-lookup"><span data-stu-id="8d10f-115">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 




