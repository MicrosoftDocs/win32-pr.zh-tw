---
title: Wire_marshal 和 user_marshal 屬性
description: 本節討論如何使用 MIDL \ 連接 \_ 封送處理 \ 和 \ 使用者 \_ 封送處理 \ 屬性來進行程式設計人員資料類型轉換。
ms.assetid: 0ee2ce86-cd14-4659-a69f-6336145359da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a789f11fa15a20eab0fcd468cc410bb5a7200717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023890"
---
# <a name="the-wire_marshal-and-user_marshal-attributes"></a><span data-ttu-id="87f63-103">網路 \_ 封送處理和使用者 \_ 封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="87f63-103">The wire\_marshal and user\_marshal Attributes</span></span>

<span data-ttu-id="87f63-104">本節討論使用 MIDL 連接 \[ [ \_ 封送](/windows/desktop/Midl/wire-marshal)處理 \] 和 \[ [使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理屬性進行程式設計人員資料類型轉換的執行 \] 。</span><span class="sxs-lookup"><span data-stu-id="87f63-104">This section discusses the implementation of programmer data type conversion using the MIDL \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="87f63-105">以下各節將提供此資訊：</span><span class="sxs-lookup"><span data-stu-id="87f63-105">The information is presented in the following sections:</span></span>

-   [<span data-ttu-id="87f63-106">有線 \_ 封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="87f63-106">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
-   [<span data-ttu-id="87f63-107">使用者 \_ 封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="87f63-107">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
-   [<span data-ttu-id="87f63-108">型別 \_ UserSize 函式</span><span class="sxs-lookup"><span data-stu-id="87f63-108">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
-   [<span data-ttu-id="87f63-109">型別 \_ UserMarshal 函式</span><span class="sxs-lookup"><span data-stu-id="87f63-109">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
-   [<span data-ttu-id="87f63-110">型別 \_ UserUnmarshal 函式</span><span class="sxs-lookup"><span data-stu-id="87f63-110">The type\_UserUnmarshal Function</span></span>](the-type-userunmarshal-function.md)
-   [<span data-ttu-id="87f63-111">型別 \_ UserFree 函式</span><span class="sxs-lookup"><span data-stu-id="87f63-111">The type\_UserFree Function</span></span>](the-type-userfree-function.md)
-   [<span data-ttu-id="87f63-112">封送處理使用者 \_ 封送處理和網路封送處理的規則 \_</span><span class="sxs-lookup"><span data-stu-id="87f63-112">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)

 

 