---
title: 函數傳回值
description: 函數傳回值類似于僅限 \t 參數，因為它們的資料不是由用戶端應用程式所提供。
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967918"
---
# <a name="function-return-values"></a><span data-ttu-id="b26ab-103">函數傳回值</span><span class="sxs-lookup"><span data-stu-id="b26ab-103">Function Return Values</span></span>

<span data-ttu-id="b26ab-104">函式傳回值類似于 **\[ out \]** 參數，因為它們的資料不是由用戶端應用程式所提供。</span><span class="sxs-lookup"><span data-stu-id="b26ab-104">Function return values are similar to **\[out\]**-only parameters because their data is not provided by the client application.</span></span> <span data-ttu-id="b26ab-105">不過，它們的管理方式不同。</span><span class="sxs-lookup"><span data-stu-id="b26ab-105">However they are managed differently.</span></span> <span data-ttu-id="b26ab-106">不同于僅限 **\[ out \]** 參數，它們不需要是指標。</span><span class="sxs-lookup"><span data-stu-id="b26ab-106">Unlike **\[out\]**-only parameters, they are not required to be pointers.</span></span> <span data-ttu-id="b26ab-107">除了參考指標和 nonencapsulated 等位之外，遠端程式可以傳回任何有效的資料類型。</span><span class="sxs-lookup"><span data-stu-id="b26ab-107">The remote procedure can return any valid data type except reference pointers and nonencapsulated unions.</span></span>

<span data-ttu-id="b26ab-108">不過，建議使用 **\[ out \]** 參數，而不是複雜資料類型的傳回值。</span><span class="sxs-lookup"><span data-stu-id="b26ab-108">However, using an **\[out\]** parameter instead of a return value for complex data types is recommended.</span></span> <span data-ttu-id="b26ab-109">當傳回復雜的資料類型時，MIDL 編譯器將會產生/Os 模式存根。</span><span class="sxs-lookup"><span data-stu-id="b26ab-109">While returning complex data types, the MIDL compiler will generate an /Os mode stub.</span></span> <span data-ttu-id="b26ab-110">因此，/robust 所提供的所有最近的錯誤檢查資訊都會遺失。</span><span class="sxs-lookup"><span data-stu-id="b26ab-110">As a result, all recent error-checking information provided by /robust is lost.</span></span>

<span data-ttu-id="b26ab-111">指標類型的函式傳回值是由用戶端存根配置，並且會呼叫 [midl \_ 使用者 \_ 配置](/windows/desktop/Midl/midl-user-allocate-1)。</span><span class="sxs-lookup"><span data-stu-id="b26ab-111">Function return values that are pointer types are allocated by the client stub with a call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="b26ab-112">因此，只有 unique 或 full 指標屬性可以套用至指標函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="b26ab-112">Accordingly, only the unique or full pointer attribute can be applied to a pointer function-return type.</span></span>

 

 