---
description: 下表顯示已保留且不得使用的單字。
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: 保留字、標頭和批註
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8879d0dbb518f92f0d8a6c38793ab315ae48b73e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343653"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="ef90c-103">保留字、標頭和批註</span><span class="sxs-lookup"><span data-stu-id="ef90c-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="ef90c-104">下表顯示已保留且不得使用的單字。</span><span class="sxs-lookup"><span data-stu-id="ef90c-104">The table below shows which words are reserved and must not be used.</span></span>

| <span data-ttu-id="ef90c-105">保留字</span><span class="sxs-lookup"><span data-stu-id="ef90c-105">Reserved Words</span></span> | <span data-ttu-id="ef90c-106">保留字</span><span class="sxs-lookup"><span data-stu-id="ef90c-106">Reserved Words</span></span> | <span data-ttu-id="ef90c-107">保留字</span><span class="sxs-lookup"><span data-stu-id="ef90c-107">Reserved Words</span></span>|
|------------------|----------|-----------|
| <span data-ttu-id="ef90c-108">ARRAY</span><span class="sxs-lookup"><span data-stu-id="ef90c-108">ARRAY</span></span>            | <span data-ttu-id="ef90c-109">DWORD</span><span class="sxs-lookup"><span data-stu-id="ef90c-109">DWORD</span></span>    | <span data-ttu-id="ef90c-110">UCHAR</span><span class="sxs-lookup"><span data-stu-id="ef90c-110">UCHAR</span></span>     |
| <span data-ttu-id="ef90c-111">BINARY</span><span class="sxs-lookup"><span data-stu-id="ef90c-111">BINARY</span></span>           | <span data-ttu-id="ef90c-112">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ef90c-112">FLOAT</span></span>    | <span data-ttu-id="ef90c-113">ULONGLONG</span><span class="sxs-lookup"><span data-stu-id="ef90c-113">ULONGLONG</span></span> |
| <span data-ttu-id="ef90c-114">二進位 \_ 資源</span><span class="sxs-lookup"><span data-stu-id="ef90c-114">BINARY\_RESOURCE</span></span> | <span data-ttu-id="ef90c-115">SDWORD</span><span class="sxs-lookup"><span data-stu-id="ef90c-115">SDWORD</span></span>   | <span data-ttu-id="ef90c-116">UNICODE</span><span class="sxs-lookup"><span data-stu-id="ef90c-116">UNICODE</span></span>   |
| <span data-ttu-id="ef90c-117">CHAR</span><span class="sxs-lookup"><span data-stu-id="ef90c-117">CHAR</span></span>             | <span data-ttu-id="ef90c-118">STRING</span><span class="sxs-lookup"><span data-stu-id="ef90c-118">STRING</span></span>   | <span data-ttu-id="ef90c-119">WORD</span><span class="sxs-lookup"><span data-stu-id="ef90c-119">WORD</span></span>      |
| <span data-ttu-id="ef90c-120">CSTRING</span><span class="sxs-lookup"><span data-stu-id="ef90c-120">CSTRING</span></span>          | <span data-ttu-id="ef90c-121">SWORD</span><span class="sxs-lookup"><span data-stu-id="ef90c-121">SWORD</span></span>    |           |
| <span data-ttu-id="ef90c-122">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="ef90c-122">DOUBLE</span></span>           | <span data-ttu-id="ef90c-123">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="ef90c-123">TEMPLATE</span></span> |           |



 

<span data-ttu-id="ef90c-124">可變長度的標頭是強制的，且必須在資料流程的開頭。</span><span class="sxs-lookup"><span data-stu-id="ef90c-124">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="ef90c-125">標頭包含下列資料。</span><span class="sxs-lookup"><span data-stu-id="ef90c-125">The header contains the following data.</span></span>



| <span data-ttu-id="ef90c-126">類型</span><span class="sxs-lookup"><span data-stu-id="ef90c-126">Type</span></span>           | <span data-ttu-id="ef90c-127">必要</span><span class="sxs-lookup"><span data-stu-id="ef90c-127">Required</span></span> | <span data-ttu-id="ef90c-128">大小 (以位元組為單位)</span><span class="sxs-lookup"><span data-stu-id="ef90c-128">Size (in bytes)</span></span> | <span data-ttu-id="ef90c-129">值</span><span class="sxs-lookup"><span data-stu-id="ef90c-129">Value</span></span> | <span data-ttu-id="ef90c-130">描述</span><span class="sxs-lookup"><span data-stu-id="ef90c-130">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="ef90c-131">魔術數位</span><span class="sxs-lookup"><span data-stu-id="ef90c-131">Magic Number</span></span>   | <span data-ttu-id="ef90c-132">x</span><span class="sxs-lookup"><span data-stu-id="ef90c-132">x</span></span>        | <span data-ttu-id="ef90c-133">4</span><span class="sxs-lookup"><span data-stu-id="ef90c-133">4</span></span>               | <span data-ttu-id="ef90c-134">xof</span><span class="sxs-lookup"><span data-stu-id="ef90c-134">xof</span></span>   |                              |
| <span data-ttu-id="ef90c-135">版本號碼</span><span class="sxs-lookup"><span data-stu-id="ef90c-135">Version Number</span></span> | <span data-ttu-id="ef90c-136">x</span><span class="sxs-lookup"><span data-stu-id="ef90c-136">x</span></span>        | <span data-ttu-id="ef90c-137">2</span><span class="sxs-lookup"><span data-stu-id="ef90c-137">2</span></span>               | <span data-ttu-id="ef90c-138">03</span><span class="sxs-lookup"><span data-stu-id="ef90c-138">03</span></span>    | <span data-ttu-id="ef90c-139">主要版本3</span><span class="sxs-lookup"><span data-stu-id="ef90c-139">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="ef90c-140">03</span><span class="sxs-lookup"><span data-stu-id="ef90c-140">03</span></span>    | <span data-ttu-id="ef90c-141">次要版本3</span><span class="sxs-lookup"><span data-stu-id="ef90c-141">Minor version 3</span></span>              |
| <span data-ttu-id="ef90c-142">格式類型</span><span class="sxs-lookup"><span data-stu-id="ef90c-142">Format Type</span></span>    | <span data-ttu-id="ef90c-143">x</span><span class="sxs-lookup"><span data-stu-id="ef90c-143">x</span></span>        | <span data-ttu-id="ef90c-144">4</span><span class="sxs-lookup"><span data-stu-id="ef90c-144">4</span></span>               | <span data-ttu-id="ef90c-145">txt</span><span class="sxs-lookup"><span data-stu-id="ef90c-145">txt</span></span>   | <span data-ttu-id="ef90c-146">文字檔</span><span class="sxs-lookup"><span data-stu-id="ef90c-146">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="ef90c-147">bin</span><span class="sxs-lookup"><span data-stu-id="ef90c-147">bin</span></span>   | <span data-ttu-id="ef90c-148">二進位檔案</span><span class="sxs-lookup"><span data-stu-id="ef90c-148">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="ef90c-149">tzip</span><span class="sxs-lookup"><span data-stu-id="ef90c-149">tzip</span></span>  | <span data-ttu-id="ef90c-150">MSZip 壓縮的文字檔</span><span class="sxs-lookup"><span data-stu-id="ef90c-150">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="ef90c-151">bzip</span><span class="sxs-lookup"><span data-stu-id="ef90c-151">bzip</span></span>  | <span data-ttu-id="ef90c-152">MSZip 壓縮的二進位檔案</span><span class="sxs-lookup"><span data-stu-id="ef90c-152">MSZip compressed binary file</span></span> |
| <span data-ttu-id="ef90c-153">浮點數大小</span><span class="sxs-lookup"><span data-stu-id="ef90c-153">Float Size</span></span>     | <span data-ttu-id="ef90c-154">x</span><span class="sxs-lookup"><span data-stu-id="ef90c-154">x</span></span>        | <span data-ttu-id="ef90c-155">0064</span><span class="sxs-lookup"><span data-stu-id="ef90c-155">0064</span></span>            |       | <span data-ttu-id="ef90c-156">64位浮點數</span><span class="sxs-lookup"><span data-stu-id="ef90c-156">64-bit floats</span></span>                |
|                | <span data-ttu-id="ef90c-157">x</span><span class="sxs-lookup"><span data-stu-id="ef90c-157">x</span></span>        | <span data-ttu-id="ef90c-158">"0032"</span><span class="sxs-lookup"><span data-stu-id="ef90c-158">"0032"</span></span>          |       | <span data-ttu-id="ef90c-159">32位浮點數</span><span class="sxs-lookup"><span data-stu-id="ef90c-159">32-bit floats</span></span>                |



 

<span data-ttu-id="ef90c-160">資料表中的值會以引號分隔，以呼叫每個值中的字元數。</span><span class="sxs-lookup"><span data-stu-id="ef90c-160">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="ef90c-161">具有4個位元組的那些字元包含四個字元，其中2個位元組的字元包含兩個字元。</span><span class="sxs-lookup"><span data-stu-id="ef90c-161">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="ef90c-162">批註只適用于文字檔。</span><span class="sxs-lookup"><span data-stu-id="ef90c-162">Comments are applicable only in text files.</span></span> <span data-ttu-id="ef90c-163">批註可以出現在資料流程中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="ef90c-163">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="ef90c-164">批註的開頭是 c + + 樣式的雙斜線 (//) ，或 () 的井字型大小 \# 。</span><span class="sxs-lookup"><span data-stu-id="ef90c-164">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="ef90c-165">批註會執行到下一個新行。</span><span class="sxs-lookup"><span data-stu-id="ef90c-165">The comment runs to the next new line.</span></span> <span data-ttu-id="ef90c-166">下列範例會顯示有效的批註。</span><span class="sxs-lookup"><span data-stu-id="ef90c-166">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="ef90c-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef90c-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef90c-168">文字編碼方式</span><span class="sxs-lookup"><span data-stu-id="ef90c-168">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



