---
title: " (功能表和其他資源的預處理器指示詞) "
description: 您可以視需要在資源腳本中使用下表所述的指示詞。 它們指示 RC 執行動作或指派值給名稱。
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- 資源編譯器，預處理器指示詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317072"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a><span data-ttu-id="e6f83-105"> (功能表和其他資源的預處理器指示詞) </span><span class="sxs-lookup"><span data-stu-id="e6f83-105">Preprocessor Directives (Menus and Other Resources)</span></span>

<span data-ttu-id="e6f83-106">您可以視需要在資源腳本中使用下表所述的指示詞。</span><span class="sxs-lookup"><span data-stu-id="e6f83-106">You can use the directives described in the following table as needed in your resource script.</span></span> <span data-ttu-id="e6f83-107">它們指示 RC 執行動作或指派值給名稱。</span><span class="sxs-lookup"><span data-stu-id="e6f83-107">They instruct RC to perform actions or to assign values to names.</span></span>



| <span data-ttu-id="e6f83-108">指示詞</span><span class="sxs-lookup"><span data-stu-id="e6f83-108">Directive</span></span>                     | <span data-ttu-id="e6f83-109">Description</span><span class="sxs-lookup"><span data-stu-id="e6f83-109">Description</span></span>                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="e6f83-110">**\#定義**</span><span class="sxs-lookup"><span data-stu-id="e6f83-110">**\#define**</span></span>](-define.md)   | <span data-ttu-id="e6f83-111">藉由將指定的值指派給指定的名稱，以定義指定的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6f83-111">Defines a specified name by assigning it a given value.</span></span>               |
| [<span data-ttu-id="e6f83-112">**\#elif**</span><span class="sxs-lookup"><span data-stu-id="e6f83-112">**\#elif**</span></span>](-elif.md)       | <span data-ttu-id="e6f83-113">標記條件式編譯區塊的選擇性子句。</span><span class="sxs-lookup"><span data-stu-id="e6f83-113">Marks an optional clause of a conditional-compilation block.</span></span>          |
| [<span data-ttu-id="e6f83-114">**\#else**</span><span class="sxs-lookup"><span data-stu-id="e6f83-114">**\#else**</span></span>](-else.md)       | <span data-ttu-id="e6f83-115">標記條件式編譯區塊的最後一個選擇性子句。</span><span class="sxs-lookup"><span data-stu-id="e6f83-115">Marks the last optional clause of a conditional-compilation block.</span></span>    |
| [<span data-ttu-id="e6f83-116">**\#endif**</span><span class="sxs-lookup"><span data-stu-id="e6f83-116">**\#endif**</span></span>](-endif.md)     | <span data-ttu-id="e6f83-117">標記條件式編譯區塊的結尾。</span><span class="sxs-lookup"><span data-stu-id="e6f83-117">Marks the end of a conditional-compilation block.</span></span>                     |
| [<span data-ttu-id="e6f83-118">**\#如果**</span><span class="sxs-lookup"><span data-stu-id="e6f83-118">**\#if**</span></span>](-if.md)           | <span data-ttu-id="e6f83-119">如果指定的運算式為 true，則會有條件地編譯腳本。</span><span class="sxs-lookup"><span data-stu-id="e6f83-119">Conditionally compiles the script if a specified expression is true.</span></span>  |
| [<span data-ttu-id="e6f83-120">**\#ifdef**</span><span class="sxs-lookup"><span data-stu-id="e6f83-120">**\#ifdef**</span></span>](-ifdef.md)     | <span data-ttu-id="e6f83-121">如果已定義指定的名稱，則會有條件地編譯腳本。</span><span class="sxs-lookup"><span data-stu-id="e6f83-121">Conditionally compiles the script if a specified name is defined.</span></span>     |
| [<span data-ttu-id="e6f83-122">**\#ifndef**</span><span class="sxs-lookup"><span data-stu-id="e6f83-122">**\#ifndef**</span></span>](-ifndef.md)   | <span data-ttu-id="e6f83-123">如果未定義指定的名稱，則會有條件地編譯腳本。</span><span class="sxs-lookup"><span data-stu-id="e6f83-123">Conditionally compiles the script if a specified name is not defined.</span></span> |
| [<span data-ttu-id="e6f83-124">**\#包括**</span><span class="sxs-lookup"><span data-stu-id="e6f83-124">**\#include**</span></span>](-include.md) | <span data-ttu-id="e6f83-125">將檔案的內容複寫到資源定義檔中。</span><span class="sxs-lookup"><span data-stu-id="e6f83-125">Copies the contents of a file into the resource-definition file.</span></span>      |
| [<span data-ttu-id="e6f83-126">**\#undef**</span><span class="sxs-lookup"><span data-stu-id="e6f83-126">**\#undef**</span></span>](-undef.md)     | <span data-ttu-id="e6f83-127">移除指定之名稱的定義。</span><span class="sxs-lookup"><span data-stu-id="e6f83-127">Removes the definition of the specified name.</span></span>                         |



 

<span data-ttu-id="e6f83-128">若要定義資源識別碼的符號，請使用 **\# define** 指示詞在標頭檔中定義符號。</span><span class="sxs-lookup"><span data-stu-id="e6f83-128">To define symbols for your resource identifiers, use the **\#define** directive to define them in a header file.</span></span> <span data-ttu-id="e6f83-129">在資源腳本和您的應用程式原始程式碼中包含此標頭。</span><span class="sxs-lookup"><span data-stu-id="e6f83-129">Include this header both in the resource script and your application source code.</span></span> <span data-ttu-id="e6f83-130">同樣地，您可以在資源腳本中包含 Windows .h 來定義資源屬性和樣式的值。</span><span class="sxs-lookup"><span data-stu-id="e6f83-130">Similarly, you define the values for resource attributes and styles by including Windows.h in the resource script.</span></span>

<span data-ttu-id="e6f83-131">RC 以特殊方式將檔案與 .c 和 .h 延伸。</span><span class="sxs-lookup"><span data-stu-id="e6f83-131">RC treats files with the .c and .h extensions in a special manner.</span></span> <span data-ttu-id="e6f83-132">它會假設具有其中一個擴充功能的檔案不包含資源。</span><span class="sxs-lookup"><span data-stu-id="e6f83-132">It assumes that a file with one of these extensions does not contain resources.</span></span> <span data-ttu-id="e6f83-133">如果檔案的副檔名為 .c 或 .h，RC 會忽略檔案中的所有行（預處理器指示詞除外）。</span><span class="sxs-lookup"><span data-stu-id="e6f83-133">If a file has the .c or .h file name extension, RC ignores all lines in the file except the preprocessor directives.</span></span> <span data-ttu-id="e6f83-134">因此，若要在另一個資源腳本中包含包含資源的檔案，請將檔案包含在 .c 或 .h 以外的副檔名。</span><span class="sxs-lookup"><span data-stu-id="e6f83-134">Therefore, to include a file that contains resources in another resource script, give the file to be included an extension other than .c or .h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6f83-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6f83-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6f83-136">Pragma 指示詞</span><span class="sxs-lookup"><span data-stu-id="e6f83-136">Pragma Directives</span></span>](pragma-directives.md)
</dt> </dl>

 

 




