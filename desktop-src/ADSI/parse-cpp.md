---
title: 解析。Cpp
description: 在範例提供者元件中，目錄服務路徑剖析器的程式碼範例位於 Parse. .cpp 中。
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- 剖析 .cpp ADSI
- 路徑剖析器 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ee4df5c1c709fde724385fdf5d5cddbafef338
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931833"
---
# <a name="parsecpp"></a><span data-ttu-id="82785-105">解析。Cpp</span><span class="sxs-lookup"><span data-stu-id="82785-105">PARSE.CPP</span></span>

<span data-ttu-id="82785-106">在範例提供者元件中，目錄服務路徑剖析器的程式碼範例位於 Parse. .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="82785-106">In the example provider component, a code example of the directory service path parser is in Parse.cpp.</span></span> <span data-ttu-id="82785-107">路徑剖析器是 ADs 提供者元件中的重要元件。</span><span class="sxs-lookup"><span data-stu-id="82785-107">The path parser is a key component in ADs provider components.</span></span> <span data-ttu-id="82785-108">它會驗證傳遞給此提供者的 ADs 路徑語法是否有效。</span><span class="sxs-lookup"><span data-stu-id="82785-108">It verifies the syntactic validity of an ADs path passed to this provider.</span></span> <span data-ttu-id="82785-109">如果語法有效，則會建立 **OBJECTINFO** 結構，其中包含這個物件之 ADspath 的元件化版本。</span><span class="sxs-lookup"><span data-stu-id="82785-109">If the syntax is valid, an **OBJECTINFO** structure is constructed, which contains a componentized version of the ADspath for this object.</span></span>

<span data-ttu-id="82785-110">請注意，這只是語法驗證。</span><span class="sxs-lookup"><span data-stu-id="82785-110">Be aware that this is only a syntax verification.</span></span> <span data-ttu-id="82785-111">所有路徑驗證都必須符合剖析器所建立的文法規則，而不是特殊案例的每個新反復專案。</span><span class="sxs-lookup"><span data-stu-id="82785-111">Rather than special-case every new iteration of path, all path verification must conform to the grammar rules established by the parser.</span></span>

<span data-ttu-id="82785-112">下表列出在 Parse 中實作為函式和方法。</span><span class="sxs-lookup"><span data-stu-id="82785-112">The following table lists the functions and methods implemented in Parse.cpp.</span></span>



| <span data-ttu-id="82785-113">項目</span><span class="sxs-lookup"><span data-stu-id="82785-113">Item</span></span>                      | <span data-ttu-id="82785-114">描述</span><span class="sxs-lookup"><span data-stu-id="82785-114">Description</span></span>                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82785-115">**ADsObject**</span><span class="sxs-lookup"><span data-stu-id="82785-115">**ADsObject**</span></span>             | <span data-ttu-id="82785-116">剖析傳遞給它的 ADspath。</span><span class="sxs-lookup"><span data-stu-id="82785-116">Parses the ADspath passed to it.</span></span> <span data-ttu-id="82785-117">此函數會遵循下列文法規則： <ADsObject>  ->  <ProviderName><SampleDSObject></span><span class="sxs-lookup"><span data-stu-id="82785-117">This function follows the following grammar rules: <ADsObject> -> <ProviderName> <SampleDSObject></span></span><br/>     |
| <span data-ttu-id="82785-118">**SampleDSObject**</span><span class="sxs-lookup"><span data-stu-id="82785-118">**SampleDSObject**</span></span>        | <span data-ttu-id="82785-119">剖析下列文法規則： <SampleDSObject> -> " \\ \\ " <identifier> " \\ "<Pathname></span><span class="sxs-lookup"><span data-stu-id="82785-119">Parses the following grammar rules: <SampleDSObject> -> "\\\\" <identifier> "\\" <Pathname></span></span><br/>                                            |
| <span data-ttu-id="82785-120">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="82785-120">**ProviderName**</span></span>          | <span data-ttu-id="82785-121">在語法正確的提供者名稱中加入（如果沒有的話）。</span><span class="sxs-lookup"><span data-stu-id="82785-121">Adds in the syntactically correct provider name if not there.</span></span>                                                                                                          |
| <span data-ttu-id="82785-122">**PathName**</span><span class="sxs-lookup"><span data-stu-id="82785-122">**PathName**</span></span>              | <span data-ttu-id="82785-123">剖析下列文法規則： <Pathname>  ->  <Component> " \\ \\ " <Pathname> 或</span><span class="sxs-lookup"><span data-stu-id="82785-123">Parses the following grammar rules: <Pathname> -> <Component> "\\\\" <Pathname> OR</span></span><br/> <Pathname> -> <Component><br/> |
| <span data-ttu-id="82785-124">**元件**</span><span class="sxs-lookup"><span data-stu-id="82785-124">**Component**</span></span>             | <span data-ttu-id="82785-125">剖析下列文法規則： <Identifier> 或</span><span class="sxs-lookup"><span data-stu-id="82785-125">Parses the following grammar rules: <Identifier> OR</span></span><br/> <span data-ttu-id="82785-126"><Identifier> "=" <Identifier></span><span class="sxs-lookup"><span data-stu-id="82785-126"><Identifier> "=" <Identifier></span></span><br/>                                              |
| <span data-ttu-id="82785-127">**CLexer::CLexer**</span><span class="sxs-lookup"><span data-stu-id="82785-127">**CLexer::CLexer**</span></span>        | <span data-ttu-id="82785-128">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="82785-128">Standard constructor.</span></span>                                                                                                                                                  |
| <span data-ttu-id="82785-129">**CLexer：： ~ CLexer**</span><span class="sxs-lookup"><span data-stu-id="82785-129">**CLexer::~CLexer**</span></span>       | <span data-ttu-id="82785-130">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="82785-130">Standard destructor.</span></span>                                                                                                                                                   |
| <span data-ttu-id="82785-131">**CLexer::GetNextToken**</span><span class="sxs-lookup"><span data-stu-id="82785-131">**CLexer::GetNextToken**</span></span>  | <span data-ttu-id="82785-132">權杖化工具。</span><span class="sxs-lookup"><span data-stu-id="82785-132">Tokenizer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="82785-133">**CLexer::NextChar**</span><span class="sxs-lookup"><span data-stu-id="82785-133">**CLexer::NextChar**</span></span>      | <span data-ttu-id="82785-134">抓取下一個單一字元。</span><span class="sxs-lookup"><span data-stu-id="82785-134">Retrieves next single character.</span></span>                                                                                                                                       |
| <span data-ttu-id="82785-135">**CLexer：:P ushBackToken**</span><span class="sxs-lookup"><span data-stu-id="82785-135">**CLexer::PushBackToken**</span></span> | <span data-ttu-id="82785-136">備份到最後一個 token 的開頭。</span><span class="sxs-lookup"><span data-stu-id="82785-136">Backs up to the start of the last token.</span></span>                                                                                                                               |
| <span data-ttu-id="82785-137">**CLexer：:P ushbackChar**</span><span class="sxs-lookup"><span data-stu-id="82785-137">**CLexer::PushbackChar**</span></span>  | <span data-ttu-id="82785-138">備份一個字元。</span><span class="sxs-lookup"><span data-stu-id="82785-138">Backs up one character.</span></span>                                                                                                                                                |
| <span data-ttu-id="82785-139">**CLexer::IsKeyword**</span><span class="sxs-lookup"><span data-stu-id="82785-139">**CLexer::IsKeyword**</span></span>     | <span data-ttu-id="82785-140">驗證關鍵字清單。</span><span class="sxs-lookup"><span data-stu-id="82785-140">Verifies keyword list.</span></span> <span data-ttu-id="82785-141">在 Globals) 中定義。</span><span class="sxs-lookup"><span data-stu-id="82785-141">Defined in Globals.h).</span></span>                                                                                                                          |
| <span data-ttu-id="82785-142">**AddComponent**</span><span class="sxs-lookup"><span data-stu-id="82785-142">**AddComponent**</span></span>          | <span data-ttu-id="82785-143">將這個元件加入元件陣列中。</span><span class="sxs-lookup"><span data-stu-id="82785-143">Adds this component to the component array.</span></span>                                                                                                                            |
| <span data-ttu-id="82785-144">**AddProviderName**</span><span class="sxs-lookup"><span data-stu-id="82785-144">**AddProviderName**</span></span>       | <span data-ttu-id="82785-145">將語法正確的提供者名稱加入至 **OBJECTINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="82785-145">Adds a syntactically correct provider name to the **OBJECTINFO** structure.</span></span>                                                                                            |
| <span data-ttu-id="82785-146">**AddRootRDN**</span><span class="sxs-lookup"><span data-stu-id="82785-146">**AddRootRDN**</span></span>            | <span data-ttu-id="82785-147">將語法正確的根相對辨別名稱 (RDN) 名稱加入至 **OBJECTINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="82785-147">Adds the syntactically correct root relative distinguished name (RDN) name to the **OBJECTINFO** structure.</span></span>                                                            |
| <span data-ttu-id="82785-148">**>advanced.field.settype**</span><span class="sxs-lookup"><span data-stu-id="82785-148">**SetType**</span></span>               | <span data-ttu-id="82785-149">設定物件的類型。</span><span class="sxs-lookup"><span data-stu-id="82785-149">Sets the type of the object.</span></span>                                                                                                                                           |
| <span data-ttu-id="82785-150">**型別**</span><span class="sxs-lookup"><span data-stu-id="82785-150">**Type**</span></span>                  | <span data-ttu-id="82785-151">剖析類型-> "user" \| "group" 等等。</span><span class="sxs-lookup"><span data-stu-id="82785-151">Parses Type-> "user" \| "group" and so on.</span></span>                                                                                                                          |



 

 

 





