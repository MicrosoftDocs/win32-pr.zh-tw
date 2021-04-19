---
description: 本節說明每個記錄相關權杖的記錄格式。 資訊分成下列各節。
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: 權杖記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991612"
---
# <a name="token-records"></a><span data-ttu-id="cbd65-104">權杖記錄</span><span class="sxs-lookup"><span data-stu-id="cbd65-104">Token Records</span></span>

<span data-ttu-id="cbd65-105">本節說明每個記錄相關權杖的記錄格式。</span><span class="sxs-lookup"><span data-stu-id="cbd65-105">This section describes the format of the records for each of the record-bearing tokens.</span></span> <span data-ttu-id="cbd65-106">資訊分成下列各節。</span><span class="sxs-lookup"><span data-stu-id="cbd65-106">Information is divided into the following sections.</span></span>

-   [<span data-ttu-id="cbd65-107">標記 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="cbd65-107">TOKEN\_NAME</span></span>](/windows)
-   [<span data-ttu-id="cbd65-108">標記 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="cbd65-108">TOKEN\_STRING</span></span>](/windows)
-   [<span data-ttu-id="cbd65-109">TOKEN \_ 整數</span><span class="sxs-lookup"><span data-stu-id="cbd65-109">TOKEN\_INTEGER</span></span>](/windows)
-   [<span data-ttu-id="cbd65-110">權杖 \_ GUID</span><span class="sxs-lookup"><span data-stu-id="cbd65-110">TOKEN\_GUID</span></span>](/windows)
-   [<span data-ttu-id="cbd65-111">TOKEN \_ 整數 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="cbd65-111">TOKEN\_INTEGER\_LIST</span></span>](/windows)
-   [<span data-ttu-id="cbd65-112">TOKEN \_ FLOAT \_ 清單</span><span class="sxs-lookup"><span data-stu-id="cbd65-112">TOKEN\_FLOAT\_LIST</span></span>](/windows)

## <a name="token_name"></a><span data-ttu-id="cbd65-113">標記 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="cbd65-113">TOKEN\_NAME</span></span>

<span data-ttu-id="cbd65-114">可變長度的記錄。</span><span class="sxs-lookup"><span data-stu-id="cbd65-114">A variable-length record.</span></span> <span data-ttu-id="cbd65-115">標記後面會接著一個計數值，指定 [名稱] 欄位中接下來的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="cbd65-115">The token is followed by a count value that specifies the number of bytes that follow in the name field.</span></span> <span data-ttu-id="cbd65-116">長度計數的 ASCII 名稱會完成記錄。</span><span class="sxs-lookup"><span data-stu-id="cbd65-116">An ASCII name of length count completes the record.</span></span>



| <span data-ttu-id="cbd65-117">欄位</span><span class="sxs-lookup"><span data-stu-id="cbd65-117">Field</span></span> | <span data-ttu-id="cbd65-118">類型</span><span class="sxs-lookup"><span data-stu-id="cbd65-118">Type</span></span>       | <span data-ttu-id="cbd65-119">大小 (位元組)</span><span class="sxs-lookup"><span data-stu-id="cbd65-119">Size (bytes)</span></span> | <span data-ttu-id="cbd65-120">目錄</span><span class="sxs-lookup"><span data-stu-id="cbd65-120">Contents</span></span>                       |
|-------|------------|--------------|--------------------------------|
| <span data-ttu-id="cbd65-121">token</span><span class="sxs-lookup"><span data-stu-id="cbd65-121">token</span></span> | <span data-ttu-id="cbd65-122">WORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-122">WORD</span></span>       | <span data-ttu-id="cbd65-123">2</span><span class="sxs-lookup"><span data-stu-id="cbd65-123">2</span></span>            | <span data-ttu-id="cbd65-124">標記 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="cbd65-124">token\_name</span></span>                    |
| <span data-ttu-id="cbd65-125">count</span><span class="sxs-lookup"><span data-stu-id="cbd65-125">count</span></span> | <span data-ttu-id="cbd65-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-126">DWORD</span></span>      | <span data-ttu-id="cbd65-127">4</span><span class="sxs-lookup"><span data-stu-id="cbd65-127">4</span></span>            | <span data-ttu-id="cbd65-128">名稱欄位的長度（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="cbd65-128">Length of name field, in bytes</span></span> |
| <span data-ttu-id="cbd65-129">NAME</span><span class="sxs-lookup"><span data-stu-id="cbd65-129">name</span></span>  | <span data-ttu-id="cbd65-130">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="cbd65-130">BYTE array</span></span> | <span data-ttu-id="cbd65-131">count</span><span class="sxs-lookup"><span data-stu-id="cbd65-131">count</span></span>        | <span data-ttu-id="cbd65-132">ASCII 名稱</span><span class="sxs-lookup"><span data-stu-id="cbd65-132">ASCII name</span></span>                     |



 

## <a name="token_string"></a><span data-ttu-id="cbd65-133">標記 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="cbd65-133">TOKEN\_STRING</span></span>

<span data-ttu-id="cbd65-134">可變長度的記錄。</span><span class="sxs-lookup"><span data-stu-id="cbd65-134">A variable-length record.</span></span> <span data-ttu-id="cbd65-135">標記後面會接著一個計數值，此值會指定字串欄位中所遵循的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="cbd65-135">The token is followed by a count value that specifies the number of bytes that follow in the string field.</span></span> <span data-ttu-id="cbd65-136">長度計數的 ASCII 字串會繼續記錄，該記錄是由終止權杖所完成。</span><span class="sxs-lookup"><span data-stu-id="cbd65-136">An ASCII string of length count continues the record, which is completed by a terminating token.</span></span> <span data-ttu-id="cbd65-137">結束字元的選擇取決於其他地方所討論的語法問題。</span><span class="sxs-lookup"><span data-stu-id="cbd65-137">The choice of terminator is determined by syntax issues discussed elsewhere.</span></span>



| <span data-ttu-id="cbd65-138">欄位</span><span class="sxs-lookup"><span data-stu-id="cbd65-138">Field</span></span>      | <span data-ttu-id="cbd65-139">類型</span><span class="sxs-lookup"><span data-stu-id="cbd65-139">Type</span></span>       | <span data-ttu-id="cbd65-140">大小 (位元組)</span><span class="sxs-lookup"><span data-stu-id="cbd65-140">Size (bytes)</span></span> | <span data-ttu-id="cbd65-141">目錄</span><span class="sxs-lookup"><span data-stu-id="cbd65-141">Contents</span></span>                         |
|------------|------------|--------------|----------------------------------|
| <span data-ttu-id="cbd65-142">token</span><span class="sxs-lookup"><span data-stu-id="cbd65-142">token</span></span>      | <span data-ttu-id="cbd65-143">WORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-143">WORD</span></span>       | <span data-ttu-id="cbd65-144">2</span><span class="sxs-lookup"><span data-stu-id="cbd65-144">2</span></span>            | <span data-ttu-id="cbd65-145">標記 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="cbd65-145">token\_string</span></span>                    |
| <span data-ttu-id="cbd65-146">count</span><span class="sxs-lookup"><span data-stu-id="cbd65-146">count</span></span>      | <span data-ttu-id="cbd65-147">DWORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-147">DWORD</span></span>      | <span data-ttu-id="cbd65-148">4</span><span class="sxs-lookup"><span data-stu-id="cbd65-148">4</span></span>            | <span data-ttu-id="cbd65-149">字串欄位的長度（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="cbd65-149">Length of string field in bytes</span></span>  |
| <span data-ttu-id="cbd65-150">字串</span><span class="sxs-lookup"><span data-stu-id="cbd65-150">strinG</span></span>     | <span data-ttu-id="cbd65-151">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="cbd65-151">BYTE array</span></span> | <span data-ttu-id="cbd65-152">count</span><span class="sxs-lookup"><span data-stu-id="cbd65-152">count</span></span>        | <span data-ttu-id="cbd65-153">ASCII 字串</span><span class="sxs-lookup"><span data-stu-id="cbd65-153">ASCII string</span></span>                     |
| <span data-ttu-id="cbd65-154">終結</span><span class="sxs-lookup"><span data-stu-id="cbd65-154">terminator</span></span> | <span data-ttu-id="cbd65-155">DWORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-155">DWORD</span></span>      | <span data-ttu-id="cbd65-156">4</span><span class="sxs-lookup"><span data-stu-id="cbd65-156">4</span></span>            | <span data-ttu-id="cbd65-157">標記 \_ 分號或標記 \_ 逗號</span><span class="sxs-lookup"><span data-stu-id="cbd65-157">tOKEN\_SEMICOLON or TOKEN\_COMMA</span></span> |



 

## <a name="token_integer"></a><span data-ttu-id="cbd65-158">TOKEN \_ 整數</span><span class="sxs-lookup"><span data-stu-id="cbd65-158">TOKEN\_INTEGER</span></span>

<span data-ttu-id="cbd65-159">固定長度記錄。</span><span class="sxs-lookup"><span data-stu-id="cbd65-159">A fixed length record.</span></span> <span data-ttu-id="cbd65-160">標記後面接著需要的整數值。</span><span class="sxs-lookup"><span data-stu-id="cbd65-160">The token is followed by the integer value required.</span></span>



| <span data-ttu-id="cbd65-161">欄位</span><span class="sxs-lookup"><span data-stu-id="cbd65-161">Field</span></span> | <span data-ttu-id="cbd65-162">類型</span><span class="sxs-lookup"><span data-stu-id="cbd65-162">Type</span></span>  | <span data-ttu-id="cbd65-163">大小 (位元組)</span><span class="sxs-lookup"><span data-stu-id="cbd65-163">Size (bytes)</span></span> | <span data-ttu-id="cbd65-164">目錄</span><span class="sxs-lookup"><span data-stu-id="cbd65-164">Contents</span></span>       |
|-------|-------|--------------|----------------|
| <span data-ttu-id="cbd65-165">token</span><span class="sxs-lookup"><span data-stu-id="cbd65-165">token</span></span> | <span data-ttu-id="cbd65-166">WORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-166">WORD</span></span>  | <span data-ttu-id="cbd65-167">2</span><span class="sxs-lookup"><span data-stu-id="cbd65-167">2</span></span>            | <span data-ttu-id="cbd65-168">tOKEN \_ 整數</span><span class="sxs-lookup"><span data-stu-id="cbd65-168">tOKEN\_INTEGER</span></span> |
| <span data-ttu-id="cbd65-169">價值</span><span class="sxs-lookup"><span data-stu-id="cbd65-169">valuE</span></span> | <span data-ttu-id="cbd65-170">DWORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-170">DWORD</span></span> | <span data-ttu-id="cbd65-171">4</span><span class="sxs-lookup"><span data-stu-id="cbd65-171">4</span></span>            | <span data-ttu-id="cbd65-172">單一整數</span><span class="sxs-lookup"><span data-stu-id="cbd65-172">Single integer</span></span> |



 

## <a name="token_guid"></a><span data-ttu-id="cbd65-173">權杖 \_ GUID</span><span class="sxs-lookup"><span data-stu-id="cbd65-173">TOKEN\_GUID</span></span>

<span data-ttu-id="cbd65-174">固定長度的記錄。</span><span class="sxs-lookup"><span data-stu-id="cbd65-174">A fixed-length record.</span></span> <span data-ttu-id="cbd65-175">權杖後面會接著憑證 DCE 標準所定義的四個資料欄位。</span><span class="sxs-lookup"><span data-stu-id="cbd65-175">The token is followed by the four data fields as defined by the OSF DCE standard.</span></span>



| <span data-ttu-id="cbd65-176">欄位</span><span class="sxs-lookup"><span data-stu-id="cbd65-176">Field</span></span> | <span data-ttu-id="cbd65-177">類型</span><span class="sxs-lookup"><span data-stu-id="cbd65-177">Type</span></span>       | <span data-ttu-id="cbd65-178">大小 (位元組)</span><span class="sxs-lookup"><span data-stu-id="cbd65-178">Size (bytes)</span></span> | <span data-ttu-id="cbd65-179">目錄</span><span class="sxs-lookup"><span data-stu-id="cbd65-179">Contents</span></span>          |
|-------|------------|--------------|-------------------|
| <span data-ttu-id="cbd65-180">token</span><span class="sxs-lookup"><span data-stu-id="cbd65-180">token</span></span> | <span data-ttu-id="cbd65-181">WORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-181">WORD</span></span>       | <span data-ttu-id="cbd65-182">2</span><span class="sxs-lookup"><span data-stu-id="cbd65-182">2</span></span>            | <span data-ttu-id="cbd65-183">權杖 \_ GUID</span><span class="sxs-lookup"><span data-stu-id="cbd65-183">tOKEN\_GUID</span></span>       |
| <span data-ttu-id="cbd65-184">Data1</span><span class="sxs-lookup"><span data-stu-id="cbd65-184">Data1</span></span> | <span data-ttu-id="cbd65-185">DWORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-185">DWORD</span></span>      | <span data-ttu-id="cbd65-186">4</span><span class="sxs-lookup"><span data-stu-id="cbd65-186">4</span></span>            | <span data-ttu-id="cbd65-187">UUID 資料欄位1</span><span class="sxs-lookup"><span data-stu-id="cbd65-187">UUID data field 1</span></span> |
| <span data-ttu-id="cbd65-188">Data2</span><span class="sxs-lookup"><span data-stu-id="cbd65-188">Data2</span></span> | <span data-ttu-id="cbd65-189">WORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-189">WORD</span></span>       | <span data-ttu-id="cbd65-190">2</span><span class="sxs-lookup"><span data-stu-id="cbd65-190">2</span></span>            | <span data-ttu-id="cbd65-191">UUID 資料欄位2</span><span class="sxs-lookup"><span data-stu-id="cbd65-191">UUID data field 2</span></span> |
| <span data-ttu-id="cbd65-192">Data3</span><span class="sxs-lookup"><span data-stu-id="cbd65-192">Data3</span></span> | <span data-ttu-id="cbd65-193">WORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-193">WORD</span></span>       | <span data-ttu-id="cbd65-194">2</span><span class="sxs-lookup"><span data-stu-id="cbd65-194">2</span></span>            | <span data-ttu-id="cbd65-195">UUID 資料欄位3</span><span class="sxs-lookup"><span data-stu-id="cbd65-195">UUID data field 3</span></span> |
| <span data-ttu-id="cbd65-196">Data4</span><span class="sxs-lookup"><span data-stu-id="cbd65-196">Data4</span></span> | <span data-ttu-id="cbd65-197">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="cbd65-197">BYTE array</span></span> | <span data-ttu-id="cbd65-198">8</span><span class="sxs-lookup"><span data-stu-id="cbd65-198">8</span></span>            | <span data-ttu-id="cbd65-199">UUID 資料欄位4</span><span class="sxs-lookup"><span data-stu-id="cbd65-199">UUID data field 4</span></span> |



 

## <a name="token_integer_list"></a><span data-ttu-id="cbd65-200">TOKEN \_ 整數 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="cbd65-200">TOKEN\_INTEGER\_LIST</span></span>

<span data-ttu-id="cbd65-201">可變長度的記錄。</span><span class="sxs-lookup"><span data-stu-id="cbd65-201">A variable-length record.</span></span> <span data-ttu-id="cbd65-202">標記後面會接著一個計數值，指定清單欄位中的整數數目。</span><span class="sxs-lookup"><span data-stu-id="cbd65-202">The token is followed by a count value that specifies the number of integers that follow in the list field.</span></span> <span data-ttu-id="cbd65-203">為了提高效率，連續的整數清單應複合成單一清單。</span><span class="sxs-lookup"><span data-stu-id="cbd65-203">For efficiency, consecutive integer lists should be compounded into a single list.</span></span>



| <span data-ttu-id="cbd65-204">欄位</span><span class="sxs-lookup"><span data-stu-id="cbd65-204">Field</span></span> | <span data-ttu-id="cbd65-205">類型</span><span class="sxs-lookup"><span data-stu-id="cbd65-205">Type</span></span>  | <span data-ttu-id="cbd65-206">大小 (位元組)</span><span class="sxs-lookup"><span data-stu-id="cbd65-206">Size (bytes)</span></span> | <span data-ttu-id="cbd65-207">目錄</span><span class="sxs-lookup"><span data-stu-id="cbd65-207">Contents</span></span>                         |
|-------|-------|--------------|----------------------------------|
| <span data-ttu-id="cbd65-208">token</span><span class="sxs-lookup"><span data-stu-id="cbd65-208">token</span></span> | <span data-ttu-id="cbd65-209">WORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-209">WORD</span></span>  | <span data-ttu-id="cbd65-210">2</span><span class="sxs-lookup"><span data-stu-id="cbd65-210">2</span></span>            | <span data-ttu-id="cbd65-211">tOKEN \_ 整數 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="cbd65-211">tOKEN\_INTEGER\_LISt</span></span>             |
| <span data-ttu-id="cbd65-212">count</span><span class="sxs-lookup"><span data-stu-id="cbd65-212">count</span></span> | <span data-ttu-id="cbd65-213">DWORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-213">DWORD</span></span> | <span data-ttu-id="cbd65-214">4</span><span class="sxs-lookup"><span data-stu-id="cbd65-214">4</span></span>            | <span data-ttu-id="cbd65-215">清單欄位中的整數數目</span><span class="sxs-lookup"><span data-stu-id="cbd65-215">Number of integers in list field</span></span> |
| <span data-ttu-id="cbd65-216">list</span><span class="sxs-lookup"><span data-stu-id="cbd65-216">list</span></span>  | <span data-ttu-id="cbd65-217">DWORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-217">DWORD</span></span> | <span data-ttu-id="cbd65-218">4 x 計數</span><span class="sxs-lookup"><span data-stu-id="cbd65-218">4 x count</span></span>    | <span data-ttu-id="cbd65-219">整數清單</span><span class="sxs-lookup"><span data-stu-id="cbd65-219">Integer list</span></span>                     |



 

## <a name="token_float_list"></a><span data-ttu-id="cbd65-220">TOKEN \_ FLOAT \_ 清單</span><span class="sxs-lookup"><span data-stu-id="cbd65-220">TOKEN\_FLOAT\_LIST</span></span>

<span data-ttu-id="cbd65-221">可變長度的記錄。</span><span class="sxs-lookup"><span data-stu-id="cbd65-221">A variable-length record.</span></span> <span data-ttu-id="cbd65-222">標記後面會接著一個計數值，可指定清單欄位中接下來的浮點數或雙精度浮點數。</span><span class="sxs-lookup"><span data-stu-id="cbd65-222">The token is followed by a count value that specifies the number of floats or doubles that follow in the list field.</span></span> <span data-ttu-id="cbd65-223">浮點數 (float 或 double) 的大小是由檔案標頭中的 float sizespecified 值所決定。</span><span class="sxs-lookup"><span data-stu-id="cbd65-223">The size of the floating point value (float or double) is determined by the value of float sizespecified in the file header.</span></span> <span data-ttu-id="cbd65-224">為了提高效率，連續的 TOKEN \_ FLOAT \_ 清單應複合成單一清單。</span><span class="sxs-lookup"><span data-stu-id="cbd65-224">For efficiency, consecutive TOKEN\_FLOAT\_LISTs should be compounded into a single list.</span></span>



| <span data-ttu-id="cbd65-225">欄位</span><span class="sxs-lookup"><span data-stu-id="cbd65-225">Field</span></span> | <span data-ttu-id="cbd65-226">類型</span><span class="sxs-lookup"><span data-stu-id="cbd65-226">Type</span></span>               | <span data-ttu-id="cbd65-227">大小 (位元組)</span><span class="sxs-lookup"><span data-stu-id="cbd65-227">Size (bytes)</span></span>   | <span data-ttu-id="cbd65-228">目錄</span><span class="sxs-lookup"><span data-stu-id="cbd65-228">Contents</span></span>                                  |
|-------|--------------------|----------------|-------------------------------------------|
| <span data-ttu-id="cbd65-229">token</span><span class="sxs-lookup"><span data-stu-id="cbd65-229">token</span></span> | <span data-ttu-id="cbd65-230">WORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-230">WORD</span></span>               | <span data-ttu-id="cbd65-231">2</span><span class="sxs-lookup"><span data-stu-id="cbd65-231">2</span></span>              | <span data-ttu-id="cbd65-232">tOKEN \_ FLOAT \_ 清單</span><span class="sxs-lookup"><span data-stu-id="cbd65-232">tOKEN\_FLOAT\_LISt</span></span>                        |
| <span data-ttu-id="cbd65-233">count</span><span class="sxs-lookup"><span data-stu-id="cbd65-233">count</span></span> | <span data-ttu-id="cbd65-234">DWORD</span><span class="sxs-lookup"><span data-stu-id="cbd65-234">DWORD</span></span>              | <span data-ttu-id="cbd65-235">4</span><span class="sxs-lookup"><span data-stu-id="cbd65-235">4</span></span>              | <span data-ttu-id="cbd65-236">清單欄位中的浮點數或雙精度浮點數</span><span class="sxs-lookup"><span data-stu-id="cbd65-236">Number of floats or doubles in list field</span></span> |
| <span data-ttu-id="cbd65-237">list</span><span class="sxs-lookup"><span data-stu-id="cbd65-237">list</span></span>  | <span data-ttu-id="cbd65-238">float/double 陣列</span><span class="sxs-lookup"><span data-stu-id="cbd65-238">float/double array</span></span> | <span data-ttu-id="cbd65-239">4或 8 x 計數</span><span class="sxs-lookup"><span data-stu-id="cbd65-239">4 or 8 x count</span></span> | <span data-ttu-id="cbd65-240">Float 或 double 清單</span><span class="sxs-lookup"><span data-stu-id="cbd65-240">Float or double list</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="cbd65-241">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbd65-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbd65-242">二進位編碼方式</span><span class="sxs-lookup"><span data-stu-id="cbd65-242">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 
