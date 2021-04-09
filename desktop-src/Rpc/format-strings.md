---
title: 格式字串
description: 格式字串是 NDR 引擎可理解的已轉譯標記。 格式字串通常稱為 MOPs;本檔會在整個中使用詞彙格式字串。
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563dd9e4145a7d83b2e49f180329c05c1d55155d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673819"
---
# <a name="format-strings"></a><span data-ttu-id="40982-104">格式字串</span><span class="sxs-lookup"><span data-stu-id="40982-104">Format Strings</span></span>

<span data-ttu-id="40982-105">格式字串是 NDR 引擎可理解的已轉譯標記。</span><span class="sxs-lookup"><span data-stu-id="40982-105">A format string is an interpreted token that the NDR engine understands.</span></span> <span data-ttu-id="40982-106">格式字串通常稱為 MOPs;本檔會在整個中使用詞彙格式字串。</span><span class="sxs-lookup"><span data-stu-id="40982-106">Format strings are often referred to as MOPs; this documentation uses the term format string throughout.</span></span>

<span data-ttu-id="40982-107">為了更加精確，格式字元是個別 (不可部分完成的) 可解譯 token。</span><span class="sxs-lookup"><span data-stu-id="40982-107">To be more precise, a format character is an individual (atomic) interpretable token.</span></span> <span data-ttu-id="40982-108">每個格式字元都是大小的一個位元組。</span><span class="sxs-lookup"><span data-stu-id="40982-108">Each format character is one byte in size.</span></span> <span data-ttu-id="40982-109">格式字串是格式化字元或格式字元和數值資料的序列。</span><span class="sxs-lookup"><span data-stu-id="40982-109">A format string is a sequence of format characters or format characters and numerical data.</span></span> <span data-ttu-id="40982-110">詞彙描述項也用於命名通用序列;例如，參數格式字串或參數描述項是用來描述常式參數的格式字串。</span><span class="sxs-lookup"><span data-stu-id="40982-110">The term descriptor is also used for naming common sequences; for example, a parameter format string or a parameter descriptor is a format string used to describe a parameter of a routine.</span></span>

<span data-ttu-id="40982-111">格式字元具有如 FC \_ LONG 或 fc 結構之類的暗示符號名稱 \_ 。</span><span class="sxs-lookup"><span data-stu-id="40982-111">Format characters have suggestive symbolic names like FC\_LONG or FC\_STRUCT.</span></span> <span data-ttu-id="40982-112">MIDL 和 NDR 引擎使用的所有格式字串字元都定義于 Ndrtypes .h 檔案中。</span><span class="sxs-lookup"><span data-stu-id="40982-112">All format string characters used by MIDL and the NDR engine are defined in the Ndrtypes.h file.</span></span>

## <a name="format-string-tables"></a><span data-ttu-id="40982-113">格式化字串資料表</span><span class="sxs-lookup"><span data-stu-id="40982-113">Format String Tables</span></span>

<span data-ttu-id="40982-114">引擎會使用兩個主要格式字串資料表：程式格式字串資料表、 **\_ \_ midl \_ ProcFormatString**、保留程式描述項，以及保留資料類型描述元的類型格式字串資料表 **\_ \_ midl \_ TypeFormatString**。</span><span class="sxs-lookup"><span data-stu-id="40982-114">Two primary format string tables are used by the engine: the procedure format string table, **\_\_MIDL\_ProcFormatString**, that keeps the procedure descriptors; and the type format string table, **\_\_MIDL\_TypeFormatString**, that keeps the data type descriptors.</span></span> <span data-ttu-id="40982-115">編譯器會在主要存根檔案中同時產生 (\* \_ c. c、 \* \_ s. c \* \_) 。</span><span class="sxs-lookup"><span data-stu-id="40982-115">The compiler generates both into the main stub files (\*\_c.c, \*\_s.c, \*\_p.c).</span></span> <span data-ttu-id="40982-116">程式格式字串表大多使用於各種解譯器，但它也會用於緩衝區轉換，不論編譯器模式為何。</span><span class="sxs-lookup"><span data-stu-id="40982-116">The procedure format string table is used mostly by various interpreters but it is also used for the buffer conversion regardless of the compiler mode.</span></span> <span data-ttu-id="40982-117">在呼叫核心 NDR 引擎來指出要處理的特定資料類型時，會使用類型格式字串表。</span><span class="sxs-lookup"><span data-stu-id="40982-117">The type format string table is used when calling the core NDR engine to indicate specific data types to be worked on.</span></span>

## <a name="format-string-notation"></a><span data-ttu-id="40982-118">格式字串標記法</span><span class="sxs-lookup"><span data-stu-id="40982-118">Format String Notation</span></span>

<span data-ttu-id="40982-119">本檔中使用的標記法會遵循常見的程式設計描述指導方針，並使用橫條 ( \| ) 用來表示替代的結構和方括弧 ( \[ \] ) 用來表示選擇性元素。</span><span class="sxs-lookup"><span data-stu-id="40982-119">The notation used in this document follows common programming description guidelines, with a bar ( \| ) used to denote alternative constructs and square brackets ( \[ \] ) used to indicate optional elements.</span></span> <span data-ttu-id="40982-120">格式字串通常會堆疊以提供可讀性 (責任) 。</span><span class="sxs-lookup"><span data-stu-id="40982-120">Format strings are frequently stacked up for readability (accountability).</span></span> <span data-ttu-id="40982-121">在本檔中，FC 代表單一格式字元。</span><span class="sxs-lookup"><span data-stu-id="40982-121">Throughout this document, FC denotes a single format character.</span></span> <span data-ttu-id="40982-122">格式字元使用其實際的符號名稱，以全部大寫顯示。</span><span class="sxs-lookup"><span data-stu-id="40982-122">Format characters are presented in all CAPS, using their actual symbolic names.</span></span> <span data-ttu-id="40982-123">其他任意欄位會以名稱和大小表示。</span><span class="sxs-lookup"><span data-stu-id="40982-123">Other arbitrary fields are represented by a name and a size.</span></span>

<span data-ttu-id="40982-124">角括弧 ( <> ) 用來表示描述項的大小。</span><span class="sxs-lookup"><span data-stu-id="40982-124">Angle brackets ( <> ) are used to denote sizes of the descriptors.</span></span> <span data-ttu-id="40982-125">採用下表所示的慣例。</span><span class="sxs-lookup"><span data-stu-id="40982-125">The conventions shown in the following table are employed.</span></span>



| <span data-ttu-id="40982-126">表示法</span><span class="sxs-lookup"><span data-stu-id="40982-126">Notation</span></span>     | <span data-ttu-id="40982-127">意義</span><span class="sxs-lookup"><span data-stu-id="40982-127">Meaning</span></span>                                                   |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="40982-128"><*n-1*></span><span class="sxs-lookup"><span data-stu-id="40982-128"><*n*></span></span>  | <span data-ttu-id="40982-129">描述項的大小為 n 個位元組。</span><span class="sxs-lookup"><span data-stu-id="40982-129">The size of descriptor is n bytes.</span></span>                        |
| <>     | <span data-ttu-id="40982-130">描述項的大小會有所不同。</span><span class="sxs-lookup"><span data-stu-id="40982-130">The size of descriptor varies.</span></span>                            |
| <span data-ttu-id="40982-131">{<>}\*</span><span class="sxs-lookup"><span data-stu-id="40982-131">{<>}\*</span></span> | <span data-ttu-id="40982-132">描述項會重複任意次數 (0、1、2 ... ) 。</span><span class="sxs-lookup"><span data-stu-id="40982-132">The descriptor is repeated any number of times (0,1,2 …).</span></span> |



 

<span data-ttu-id="40982-133">下列格式字元具有特殊意義。</span><span class="sxs-lookup"><span data-stu-id="40982-133">The following format characters have a special meaning.</span></span>



| <span data-ttu-id="40982-134">字元</span><span class="sxs-lookup"><span data-stu-id="40982-134">Character</span></span> | <span data-ttu-id="40982-135">意義</span><span class="sxs-lookup"><span data-stu-id="40982-135">Meaning</span></span>                                   |
|-----------|-------------------------------------------|
| <span data-ttu-id="40982-136">FC \_ 端</span><span class="sxs-lookup"><span data-stu-id="40982-136">FC\_END</span></span>   | <span data-ttu-id="40982-137">指出某些格式字串的結尾。</span><span class="sxs-lookup"><span data-stu-id="40982-137">Indicates the end of some format strings.</span></span> |
| <span data-ttu-id="40982-138">FC \_ 板</span><span class="sxs-lookup"><span data-stu-id="40982-138">FC\_PAD</span></span>   | <span data-ttu-id="40982-139">未解釋的填補字元。</span><span class="sxs-lookup"><span data-stu-id="40982-139">Uninterpreted pad character.</span></span>              |



 

 

 




