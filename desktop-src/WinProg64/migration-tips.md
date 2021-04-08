---
title: 移轉提示
description: 將您的程式碼移植到64位 Windows 時，請務必考慮定址計算和指標算術。
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- 64位 Windows 程式設計指南64位 Windows 程式設計，遷移秘訣
- 遷移秘訣 64-位 Windows 程式設計
- 相容性64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674007"
---
# <a name="migration-tips"></a><span data-ttu-id="cb264-106">移轉提示</span><span class="sxs-lookup"><span data-stu-id="cb264-106">Migration Tips</span></span>

<span data-ttu-id="cb264-107">檢查程式碼是否有64位相容時，有兩個主要的考慮區域如下：</span><span class="sxs-lookup"><span data-stu-id="cb264-107">The two primary areas of concern when examining your code for 64-bit compatibility are as follows:</span></span>

-   <span data-ttu-id="cb264-108">位址計算</span><span class="sxs-lookup"><span data-stu-id="cb264-108">Address calculations</span></span>
-   <span data-ttu-id="cb264-109">指標算術</span><span class="sxs-lookup"><span data-stu-id="cb264-109">Pointer arithmetic</span></span>

<span data-ttu-id="cb264-110">基於許多原因，開發人員會以 **ULONG** 值的形式儲存位址。</span><span class="sxs-lookup"><span data-stu-id="cb264-110">For many reasons, developers have stored addresses as a **ULONG** value.</span></span> <span data-ttu-id="cb264-111">畢竟，在32位的 Windows 上，位址、指標和 **ULONG** 值全都是32位長。</span><span class="sxs-lookup"><span data-stu-id="cb264-111">After all, on 32-bit Windows, an address, a pointer, and a **ULONG** value are all 32 bits long.</span></span> <span data-ttu-id="cb264-112">不過，在64位的 Windows 上，位址和 **ULONG** 的長度不相同。</span><span class="sxs-lookup"><span data-stu-id="cb264-112">However, on 64-bit Windows, an address and a **ULONG** are not the same length.</span></span> <span data-ttu-id="cb264-113">雖然 **ULONG** 保持為32位值，但所有指標現在都是64位值。</span><span class="sxs-lookup"><span data-stu-id="cb264-113">While a **ULONG** remains a 32-bit value, all pointers are now 64-bit values.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cb264-114">本章節內容</span><span class="sxs-lookup"><span data-stu-id="cb264-114">In this Section</span></span>

-   [<span data-ttu-id="cb264-115">一般移植指導方針</span><span class="sxs-lookup"><span data-stu-id="cb264-115">General Porting Guidelines</span></span>](general-porting-guidelines.md)
-   [<span data-ttu-id="cb264-116">儲存64位值</span><span class="sxs-lookup"><span data-stu-id="cb264-116">Storing a 64-bit Value</span></span>](storing-a-64-bit-value.md)
-   [<span data-ttu-id="cb264-117">常見的編譯器錯誤</span><span class="sxs-lookup"><span data-stu-id="cb264-117">Common Compiler Errors</span></span>](common-compiler-errors.md)
-   [<span data-ttu-id="cb264-118">其他考慮</span><span class="sxs-lookup"><span data-stu-id="cb264-118">Additional Considerations</span></span>](additional-considerations.md)

 

 




