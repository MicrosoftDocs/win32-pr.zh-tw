---
title: 類型格式字串
description: 格式字元代表 NDR 引擎感興趣的物件。
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021812"
---
# <a name="type-format-strings"></a><span data-ttu-id="9b045-103">類型格式字串</span><span class="sxs-lookup"><span data-stu-id="9b045-103">Type Format Strings</span></span>

<span data-ttu-id="9b045-104">格式字元代表 NDR 引擎感興趣的物件。</span><span class="sxs-lookup"><span data-stu-id="9b045-104">Format characters denote objects of interest to the NDR engine.</span></span> <span data-ttu-id="9b045-105">每個基本類型都有格式字元，適用于各種複雜類型，以及指標、封裝、對齊和其他其他物件的描述。</span><span class="sxs-lookup"><span data-stu-id="9b045-105">There is a format character for each basic type, for various complex types, and for descriptions of pointers, packing, alignment, and other miscellaneous objects.</span></span> <span data-ttu-id="9b045-106">如果是複合類型，則會根據其效能屬性來辨識結構和陣列的數個類別。</span><span class="sxs-lookup"><span data-stu-id="9b045-106">For compound types, several categories of structures and arrays are recognized based on their performance properties.</span></span> <span data-ttu-id="9b045-107">每個類別的格式字串都會以識別特定格式字串的 FC 權杖開頭。</span><span class="sxs-lookup"><span data-stu-id="9b045-107">A format string for each category starts with an FC token identifying the particular format string.</span></span> <span data-ttu-id="9b045-108">結構和陣列類別目錄的格式字元可能會在下表所示的開頭 FC 權杖名稱中共用修正。</span><span class="sxs-lookup"><span data-stu-id="9b045-108">Format characters for structures and arrays categories may share the in-fixes in the name of the leading FC token shown in the following table.</span></span>



| <span data-ttu-id="9b045-109">格式字元</span><span class="sxs-lookup"><span data-stu-id="9b045-109">Format character</span></span> | <span data-ttu-id="9b045-110">說明</span><span class="sxs-lookup"><span data-stu-id="9b045-110">Description</span></span>                                    |
|------------------|------------------------------------------------|
| <span data-ttu-id="9b045-111">C</span><span class="sxs-lookup"><span data-stu-id="9b045-111">C</span></span>                | <span data-ttu-id="9b045-112">表示類型中的一致性資訊。</span><span class="sxs-lookup"><span data-stu-id="9b045-112">Indicates conformance information in the type.</span></span> |
| <span data-ttu-id="9b045-113">V</span><span class="sxs-lookup"><span data-stu-id="9b045-113">V</span></span>                | <span data-ttu-id="9b045-114">表示類型中的差異資訊。</span><span class="sxs-lookup"><span data-stu-id="9b045-114">Indicates variance information in the type.</span></span>    |
| <span data-ttu-id="9b045-115">P</span><span class="sxs-lookup"><span data-stu-id="9b045-115">P</span></span>                | <span data-ttu-id="9b045-116">指出指標是類型的一部分。</span><span class="sxs-lookup"><span data-stu-id="9b045-116">Indicates pointers are a part of the type.</span></span>     |



 

<span data-ttu-id="9b045-117">例如，FC \_ CSTRUCT 和 fc \_ CARRAY 會分別識別符合標準的結構和一致的陣列描述項。</span><span class="sxs-lookup"><span data-stu-id="9b045-117">For example, FC\_CSTRUCT and FC\_CARRAY identify the conformant structure and conformant array descriptors, respectively.</span></span>

<span data-ttu-id="9b045-118">以下是具有特殊意義的格式字元。</span><span class="sxs-lookup"><span data-stu-id="9b045-118">The following are format characters with special meanings.</span></span>



| <span data-ttu-id="9b045-119">格式字元</span><span class="sxs-lookup"><span data-stu-id="9b045-119">Format character</span></span> | <span data-ttu-id="9b045-120">說明</span><span class="sxs-lookup"><span data-stu-id="9b045-120">Description</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9b045-121">FC \_ PP</span><span class="sxs-lookup"><span data-stu-id="9b045-121">FC\_PP</span></span>           | <span data-ttu-id="9b045-122">指出結構或陣列的指標描述區段開始。</span><span class="sxs-lookup"><span data-stu-id="9b045-122">Indicates the beginning of the pointer description section of a structure or array.</span></span> |



 

<span data-ttu-id="9b045-123">下列主題會更詳細地描述 RPC NDR 類型格式字串：</span><span class="sxs-lookup"><span data-stu-id="9b045-123">RPC NDR type format strings are described in more detail in the following topics:</span></span>

-   [<span data-ttu-id="9b045-124">簡單類型</span><span class="sxs-lookup"><span data-stu-id="9b045-124">Simple Types</span></span>](simple-types-tfs.md)
-   [<span data-ttu-id="9b045-125">指標</span><span class="sxs-lookup"><span data-stu-id="9b045-125">Pointers</span></span>](pointers-tfs.md)
-   [<span data-ttu-id="9b045-126">陣列</span><span class="sxs-lookup"><span data-stu-id="9b045-126">Arrays</span></span>](arrays-tfs.md)
-   [<span data-ttu-id="9b045-127">字串</span><span class="sxs-lookup"><span data-stu-id="9b045-127">Strings</span></span>](strings-tfs.md)
-   [<span data-ttu-id="9b045-128">相互關聯描述元</span><span class="sxs-lookup"><span data-stu-id="9b045-128">Correlation Descriptors</span></span>](correlation-descriptors-tfs.md)
-   [<span data-ttu-id="9b045-129">結構</span><span class="sxs-lookup"><span data-stu-id="9b045-129">Structures</span></span>](structures-tfs.md)
-   [<span data-ttu-id="9b045-130">指標版面配置</span><span class="sxs-lookup"><span data-stu-id="9b045-130">Pointer Layout</span></span>](pointer-layout-tfs.md)
-   [<span data-ttu-id="9b045-131">等位</span><span class="sxs-lookup"><span data-stu-id="9b045-131">Unions</span></span>](unions-tfs.md)
-   [<span data-ttu-id="9b045-132">傳送 \_ as 和表示 \_ 為</span><span class="sxs-lookup"><span data-stu-id="9b045-132">Transmit\_as and Represent\_as</span></span>](transmit-as-and-represent-as-tfs.md)
-   [<span data-ttu-id="9b045-133">使用者封送處理</span><span class="sxs-lookup"><span data-stu-id="9b045-133">User-marshal</span></span>](user-marshal-tfs.md)

 

 




