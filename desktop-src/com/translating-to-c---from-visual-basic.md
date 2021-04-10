---
title: 從 Visual Basic 轉換成 c + +
description: Visual Basic 會隱含地處理指標。 在 c + + 中，您的應用程式會負責執行任何必要的指標算術。
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183463"
---
# <a name="translating-to-c-from-visual-basic"></a><span data-ttu-id="97dce-104">從 Visual Basic 轉換成 c + +</span><span class="sxs-lookup"><span data-stu-id="97dce-104">Translating to C++ from Visual Basic</span></span>

<span data-ttu-id="97dce-105">Visual Basic 會隱含地處理指標。</span><span class="sxs-lookup"><span data-stu-id="97dce-105">Visual Basic handles pointers implicitly.</span></span> <span data-ttu-id="97dce-106">在 c + + 中，您的應用程式會負責執行任何必要的指標算術。</span><span class="sxs-lookup"><span data-stu-id="97dce-106">In C++, your application is responsible for performing any necessary pointer arithmetic.</span></span>

<span data-ttu-id="97dce-107">依預設，Visual Basic 會以傳址方式傳遞參數 (作為) 指標。</span><span class="sxs-lookup"><span data-stu-id="97dce-107">By default, Visual Basic passes parameters by reference (as pointers).</span></span> <span data-ttu-id="97dce-108">只以傳值方式傳遞的參數是由關鍵字 **ByVal** 指定。</span><span class="sxs-lookup"><span data-stu-id="97dce-108">Parameters that are meant to be passed by value only are specified by the keyword **ByVal**.</span></span> <span data-ttu-id="97dce-109">例如，Visual Basic 中的 **ByVal**- **整數** 參數相當於 c + + 中的 **short** 參數，而 Visual Basic 中的 **ByRef**- **整數** 參數相當於 **short \*** 參數。</span><span class="sxs-lookup"><span data-stu-id="97dce-109">For example, a **ByVal** Â  **Integer** parameter in Visual Basic is equivalent to a **short** parameter in C++, whereas a **ByRef** Â  **Integer** parameter in Visual Basic is equivalent to a **short\*** parameter.</span></span>

<span data-ttu-id="97dce-110">在 Visual Basic 中宣告 **為字串** 的參數會宣告為 c + + 中的 **BSTR** 指標。</span><span class="sxs-lookup"><span data-stu-id="97dce-110">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="97dce-111">在 c + + 中將字串指標設定為 **Null** ，相當於將字串設定為 Visual Basic 中的 **vbNullString** 常數。</span><span class="sxs-lookup"><span data-stu-id="97dce-111">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="97dce-112">將零長度的字串 ( "" ) 傳遞給設計用來接收 **Null** 的函式無法運作，因為這會將指標傳遞至長度為零的字串，而不是零指標。</span><span class="sxs-lookup"><span data-stu-id="97dce-112">Passing a zero-length string ("") to a function designed to receive **NULL** does not work, because this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="97dce-113">C + + 和 Visual Basic 在其代表屬性的方式上稍有不同。</span><span class="sxs-lookup"><span data-stu-id="97dce-113">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="97dce-114">在 c + + 中，屬性是以一組存取子函式來表示，其中一個設定屬性值，另一個則會抓取屬性值。</span><span class="sxs-lookup"><span data-stu-id="97dce-114">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="97dce-115">在 Visual Basic 中，屬性會以單一專案的形式表示，可用於抓取或設定屬性值。</span><span class="sxs-lookup"><span data-stu-id="97dce-115">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97dce-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="97dce-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97dce-117">轉換成 c + +</span><span class="sxs-lookup"><span data-stu-id="97dce-117">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 




