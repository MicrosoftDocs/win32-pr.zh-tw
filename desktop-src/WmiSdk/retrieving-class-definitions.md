---
description: 架構查詢是要求類別定義的 WQL 語句，以及架構關聯的相關資訊。
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: 正在抓取類別定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114896"
---
# <a name="retrieving-class-definitions"></a><span data-ttu-id="44b52-103">正在抓取類別定義</span><span class="sxs-lookup"><span data-stu-id="44b52-103">Retrieving Class Definitions</span></span>

<span data-ttu-id="44b52-104">架構查詢是要求類別定義的 WQL 語句，以及 [架構關聯](schema-associations.md)的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="44b52-104">Schema queries are WQL statements that request class definitions and information about [schema associations](schema-associations.md).</span></span> <span data-ttu-id="44b52-105">類別提供者會在其 [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md)類別的實例中使用架構查詢，以指定它們在向 WMI 註冊時所支援的類別。</span><span class="sxs-lookup"><span data-stu-id="44b52-105">Class providers use schema queries in their instances of the [**\_\_ClassProviderRegistration**](--classproviderregistration.md) class to specify the classes that they support when they register with WMI.</span></span> <span data-ttu-id="44b52-106">架構查詢位於 **\_ \_ ClassProviderRegistration** 實例的 **ResultSetQueries**、 **ReferencedSetQueries** 和 **UnsupportedQueries** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="44b52-106">Schema queries are placed in the **ResultSetQueries**, **ReferencedSetQueries**, and **UnsupportedQueries** properties of the **\_\_ClassProviderRegistration** instance.</span></span>

<span data-ttu-id="44b52-107">架構查詢與資料查詢類似，因為它們支援下列 WQL 語句：</span><span class="sxs-lookup"><span data-stu-id="44b52-107">Schema queries are similar to data queries in that they support the following WQL statements:</span></span>

-   [<span data-ttu-id="44b52-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="44b52-108">SELECT</span></span>](select-statement-for-schema-queries.md)
-   [<span data-ttu-id="44b52-109">ASSOCIATORS OF</span><span class="sxs-lookup"><span data-stu-id="44b52-109">ASSOCIATORS OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="44b52-110">的參考</span><span class="sxs-lookup"><span data-stu-id="44b52-110">REFERENCES OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="44b52-111">ISA</span><span class="sxs-lookup"><span data-stu-id="44b52-111">ISA</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="44b52-112">架構查詢類似于指定 **ClassDefsOnly** 關鍵字的資料查詢 [參考](references-of-statement.md);換句話說，它會傳回類別定義物件的結果集，而非關聯類別的實際實例。</span><span class="sxs-lookup"><span data-stu-id="44b52-112">A schema query is similar to a [REFERENCES OF](references-of-statement.md) data query that specifies the **ClassDefsOnly** keyword; in other words, that returns a result set of class definition objects rather than actual instances of association classes.</span></span> <span data-ttu-id="44b52-113">但是，的參考只有在有實例存在時才會傳回類別定義。</span><span class="sxs-lookup"><span data-stu-id="44b52-113">However, REFERENCES OF returns class definitions only if there are instances present.</span></span> <span data-ttu-id="44b52-114">架構查詢會傳回類別定義，無論實例是否存在。</span><span class="sxs-lookup"><span data-stu-id="44b52-114">A schema query returns class definitions whether or not instances are present.</span></span>

 

 



