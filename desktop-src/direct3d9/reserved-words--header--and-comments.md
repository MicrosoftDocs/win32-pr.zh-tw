---
description: 下表顯示已保留且不得使用的單字。
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: 保留字、標頭和批註
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2696aaf6e635f08124e28392d0a8faf63c39a85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509883"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="7ea30-103">保留字、標頭和批註</span><span class="sxs-lookup"><span data-stu-id="7ea30-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="7ea30-104">下表顯示已保留且不得使用的單字。</span><span class="sxs-lookup"><span data-stu-id="7ea30-104">The table below shows which words are reserved and must not be used.</span></span>



|                  |          |           |
|------------------|----------|-----------|
| <span data-ttu-id="7ea30-105">ARRAY</span><span class="sxs-lookup"><span data-stu-id="7ea30-105">ARRAY</span></span>            | <span data-ttu-id="7ea30-106">DWORD</span><span class="sxs-lookup"><span data-stu-id="7ea30-106">DWORD</span></span>    | <span data-ttu-id="7ea30-107">UCHAR</span><span class="sxs-lookup"><span data-stu-id="7ea30-107">UCHAR</span></span>     |
| <span data-ttu-id="7ea30-108">BINARY</span><span class="sxs-lookup"><span data-stu-id="7ea30-108">BINARY</span></span>           | <span data-ttu-id="7ea30-109">FLOAT</span><span class="sxs-lookup"><span data-stu-id="7ea30-109">FLOAT</span></span>    | <span data-ttu-id="7ea30-110">ULONGLONG</span><span class="sxs-lookup"><span data-stu-id="7ea30-110">ULONGLONG</span></span> |
| <span data-ttu-id="7ea30-111">二進位 \_ 資源</span><span class="sxs-lookup"><span data-stu-id="7ea30-111">BINARY\_RESOURCE</span></span> | <span data-ttu-id="7ea30-112">SDWORD</span><span class="sxs-lookup"><span data-stu-id="7ea30-112">SDWORD</span></span>   | <span data-ttu-id="7ea30-113">UNICODE</span><span class="sxs-lookup"><span data-stu-id="7ea30-113">UNICODE</span></span>   |
| <span data-ttu-id="7ea30-114">CHAR</span><span class="sxs-lookup"><span data-stu-id="7ea30-114">CHAR</span></span>             | <span data-ttu-id="7ea30-115">STRING</span><span class="sxs-lookup"><span data-stu-id="7ea30-115">STRING</span></span>   | <span data-ttu-id="7ea30-116">WORD</span><span class="sxs-lookup"><span data-stu-id="7ea30-116">WORD</span></span>      |
| <span data-ttu-id="7ea30-117">CSTRING</span><span class="sxs-lookup"><span data-stu-id="7ea30-117">CSTRING</span></span>          | <span data-ttu-id="7ea30-118">SWORD</span><span class="sxs-lookup"><span data-stu-id="7ea30-118">SWORD</span></span>    |           |
| <span data-ttu-id="7ea30-119">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="7ea30-119">DOUBLE</span></span>           | <span data-ttu-id="7ea30-120">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="7ea30-120">TEMPLATE</span></span> |           |



 

<span data-ttu-id="7ea30-121">可變長度的標頭是強制的，且必須在資料流程的開頭。</span><span class="sxs-lookup"><span data-stu-id="7ea30-121">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="7ea30-122">標頭包含下列資料。</span><span class="sxs-lookup"><span data-stu-id="7ea30-122">The header contains the following data.</span></span>



| <span data-ttu-id="7ea30-123">類型</span><span class="sxs-lookup"><span data-stu-id="7ea30-123">Type</span></span>           | <span data-ttu-id="7ea30-124">必要</span><span class="sxs-lookup"><span data-stu-id="7ea30-124">Required</span></span> | <span data-ttu-id="7ea30-125">大小 (以位元組為單位)</span><span class="sxs-lookup"><span data-stu-id="7ea30-125">Size (in bytes)</span></span> | <span data-ttu-id="7ea30-126">值</span><span class="sxs-lookup"><span data-stu-id="7ea30-126">Value</span></span> | <span data-ttu-id="7ea30-127">描述</span><span class="sxs-lookup"><span data-stu-id="7ea30-127">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="7ea30-128">魔術數位</span><span class="sxs-lookup"><span data-stu-id="7ea30-128">Magic Number</span></span>   | <span data-ttu-id="7ea30-129">x</span><span class="sxs-lookup"><span data-stu-id="7ea30-129">x</span></span>        | <span data-ttu-id="7ea30-130">4</span><span class="sxs-lookup"><span data-stu-id="7ea30-130">4</span></span>               | <span data-ttu-id="7ea30-131">xof</span><span class="sxs-lookup"><span data-stu-id="7ea30-131">xof</span></span>   |                              |
| <span data-ttu-id="7ea30-132">版本號碼</span><span class="sxs-lookup"><span data-stu-id="7ea30-132">Version Number</span></span> | <span data-ttu-id="7ea30-133">x</span><span class="sxs-lookup"><span data-stu-id="7ea30-133">x</span></span>        | <span data-ttu-id="7ea30-134">2</span><span class="sxs-lookup"><span data-stu-id="7ea30-134">2</span></span>               | <span data-ttu-id="7ea30-135">03</span><span class="sxs-lookup"><span data-stu-id="7ea30-135">03</span></span>    | <span data-ttu-id="7ea30-136">主要版本3</span><span class="sxs-lookup"><span data-stu-id="7ea30-136">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="7ea30-137">03</span><span class="sxs-lookup"><span data-stu-id="7ea30-137">03</span></span>    | <span data-ttu-id="7ea30-138">次要版本3</span><span class="sxs-lookup"><span data-stu-id="7ea30-138">Minor version 3</span></span>              |
| <span data-ttu-id="7ea30-139">格式類型</span><span class="sxs-lookup"><span data-stu-id="7ea30-139">Format Type</span></span>    | <span data-ttu-id="7ea30-140">x</span><span class="sxs-lookup"><span data-stu-id="7ea30-140">x</span></span>        | <span data-ttu-id="7ea30-141">4</span><span class="sxs-lookup"><span data-stu-id="7ea30-141">4</span></span>               | <span data-ttu-id="7ea30-142">txt</span><span class="sxs-lookup"><span data-stu-id="7ea30-142">txt</span></span>   | <span data-ttu-id="7ea30-143">文字檔</span><span class="sxs-lookup"><span data-stu-id="7ea30-143">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="7ea30-144">bin</span><span class="sxs-lookup"><span data-stu-id="7ea30-144">bin</span></span>   | <span data-ttu-id="7ea30-145">二進位檔案</span><span class="sxs-lookup"><span data-stu-id="7ea30-145">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="7ea30-146">tzip</span><span class="sxs-lookup"><span data-stu-id="7ea30-146">tzip</span></span>  | <span data-ttu-id="7ea30-147">MSZip 壓縮的文字檔</span><span class="sxs-lookup"><span data-stu-id="7ea30-147">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="7ea30-148">bzip</span><span class="sxs-lookup"><span data-stu-id="7ea30-148">bzip</span></span>  | <span data-ttu-id="7ea30-149">MSZip 壓縮的二進位檔案</span><span class="sxs-lookup"><span data-stu-id="7ea30-149">MSZip compressed binary file</span></span> |
| <span data-ttu-id="7ea30-150">浮點數大小</span><span class="sxs-lookup"><span data-stu-id="7ea30-150">Float Size</span></span>     | <span data-ttu-id="7ea30-151">x</span><span class="sxs-lookup"><span data-stu-id="7ea30-151">x</span></span>        | <span data-ttu-id="7ea30-152">0064</span><span class="sxs-lookup"><span data-stu-id="7ea30-152">0064</span></span>            |       | <span data-ttu-id="7ea30-153">64位浮點數</span><span class="sxs-lookup"><span data-stu-id="7ea30-153">64-bit floats</span></span>                |
|                | <span data-ttu-id="7ea30-154">x</span><span class="sxs-lookup"><span data-stu-id="7ea30-154">x</span></span>        | <span data-ttu-id="7ea30-155">"0032"</span><span class="sxs-lookup"><span data-stu-id="7ea30-155">"0032"</span></span>          |       | <span data-ttu-id="7ea30-156">32位浮點數</span><span class="sxs-lookup"><span data-stu-id="7ea30-156">32-bit floats</span></span>                |



 

<span data-ttu-id="7ea30-157">資料表中的值會以引號分隔，以呼叫每個值中的字元數。</span><span class="sxs-lookup"><span data-stu-id="7ea30-157">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="7ea30-158">具有4個位元組的那些字元包含四個字元，其中2個位元組的字元包含兩個字元。</span><span class="sxs-lookup"><span data-stu-id="7ea30-158">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="7ea30-159">批註只適用于文字檔。</span><span class="sxs-lookup"><span data-stu-id="7ea30-159">Comments are applicable only in text files.</span></span> <span data-ttu-id="7ea30-160">批註可以出現在資料流程中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="7ea30-160">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="7ea30-161">批註的開頭是 c + + 樣式的雙斜線 (//) ，或 () 的井字型大小 \# 。</span><span class="sxs-lookup"><span data-stu-id="7ea30-161">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="7ea30-162">批註會執行到下一個新行。</span><span class="sxs-lookup"><span data-stu-id="7ea30-162">The comment runs to the next new line.</span></span> <span data-ttu-id="7ea30-163">下列範例會顯示有效的批註。</span><span class="sxs-lookup"><span data-stu-id="7ea30-163">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="7ea30-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="7ea30-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ea30-165">文字編碼方式</span><span class="sxs-lookup"><span data-stu-id="7ea30-165">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



