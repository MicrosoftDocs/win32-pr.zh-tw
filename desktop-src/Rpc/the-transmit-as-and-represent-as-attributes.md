---
title: Transmit_as 和 represent_as 屬性
description: 本節將討論如何使用 MIDL \ 傳輸 \_ 作為 \ 和 \ 表示為 \ 屬性，以進行程式設計人員資料類型轉換 \_ 。
ms.assetid: 2e1af786-f507-453f-bb10-74805ef6b1a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16760091479a306b9dc9c815c7f3a41b25012ca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842403"
---
# <a name="the-transmit_as-and-represent_as-attributes"></a><span data-ttu-id="6bd06-103">傳送 \_ as 和表示 \_ 為屬性</span><span class="sxs-lookup"><span data-stu-id="6bd06-103">The transmit\_as and represent\_as Attributes</span></span>

<span data-ttu-id="6bd06-104">本節將討論使用 MIDL **\[** [**傳輸 \_ as**](/windows/desktop/Midl/transmit-as) **\]** 和 **\[** [**表示 \_ 為**](/windows/desktop/Midl/represent-as)屬性之程式設計人員資料類型轉換的實作為 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="6bd06-104">This section discusses the implementation of programmer data type conversion using the MIDL **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** and **\[**[**represent\_as**](/windows/desktop/Midl/represent-as)**\]** attributes.</span></span> <span data-ttu-id="6bd06-105">下列各節會提供討論：</span><span class="sxs-lookup"><span data-stu-id="6bd06-105">The discussion is presented in the following sections:</span></span>

-   [<span data-ttu-id="6bd06-106">**傳輸 \_ 為** 屬性</span><span class="sxs-lookup"><span data-stu-id="6bd06-106">The **transmit\_as** Attribute</span></span>](the-transmit-as-attribute.md)
-   [<span data-ttu-id="6bd06-107">**\_ 要 \_ xmit 的型** 別函數</span><span class="sxs-lookup"><span data-stu-id="6bd06-107">The **type\_to\_xmit** Function</span></span>](the-type-to-xmit-function.md)
-   [<span data-ttu-id="6bd06-108">**\_ \_ Xmit** 函式中的型別</span><span class="sxs-lookup"><span data-stu-id="6bd06-108">The **type\_from\_xmit** Function</span></span>](the-type-from-xmit-function.md)
-   [<span data-ttu-id="6bd06-109">**Type \_ free \_ xmit** 函式</span><span class="sxs-lookup"><span data-stu-id="6bd06-109">The **type\_free\_xmit** Function</span></span>](the-type-free-xmit-function.md)
-   [<span data-ttu-id="6bd06-110">**Type \_ free \_ inst** 函式</span><span class="sxs-lookup"><span data-stu-id="6bd06-110">The **type\_free\_inst** Function</span></span>](the-type-free-inst-function.md)
-   [<span data-ttu-id="6bd06-111">**表示 \_ 為** 屬性</span><span class="sxs-lookup"><span data-stu-id="6bd06-111">The **represent\_as** Attribute</span></span>](the-represent-as-attribute.md)
-   [<span data-ttu-id="6bd06-112">區域函式 **\_ \_ 中 \_ 的命名類型**</span><span class="sxs-lookup"><span data-stu-id="6bd06-112">The **named\_type\_from\_local** Function</span></span>](the-named-type-from-local-function.md)
-   [<span data-ttu-id="6bd06-113">**\_ \_ \_ 區域** 函式的命名類型</span><span class="sxs-lookup"><span data-stu-id="6bd06-113">The **named\_type\_to\_local** Function</span></span>](the-named-type-to-local-function.md)
-   [<span data-ttu-id="6bd06-114">**指名 \_ 型別的 \_ free \_ 區域** 函數</span><span class="sxs-lookup"><span data-stu-id="6bd06-114">The **named\_type\_free\_local** Function</span></span>](the-named-type-free-local-function.md)
-   [<span data-ttu-id="6bd06-115">**指名 \_ 型別 \_ free \_ inst** 函式</span><span class="sxs-lookup"><span data-stu-id="6bd06-115">The **named\_type\_free\_inst** Function</span></span>](the-named-type-free-inst-function.md)

 

 