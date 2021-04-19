---
title: 標頭注釋
description: 標頭注釋描述函式如何使用其參數和傳回值。
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- Windows API，標頭檔批註
- 標頭檔批註
- Specstrings。h
- '標準批註語言 (SAL) '
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8535118383a97d6c48f19246ad24ce324e8bb528
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965444"
---
# <a name="header-annotations"></a><span data-ttu-id="c6b6d-117">標頭注釋</span><span class="sxs-lookup"><span data-stu-id="c6b6d-117">Header Annotations</span></span>

<span data-ttu-id="c6b6d-118">\[本主題說明 Windows 標頭透過 Windows 7 所支援的批註。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-118">\[This topic describes the annotations supported in the Windows headers through Windows 7.</span></span> <span data-ttu-id="c6b6d-119">如果您正在針對 Windows 8 進行開發，您應該使用 [SAL 注釋]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120))中所述的注釋。\]</span><span class="sxs-lookup"><span data-stu-id="c6b6d-119">If you are developing for Windows 8, you should use the annotations described in [SAL Annotations]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span></span>

<span data-ttu-id="c6b6d-120">標頭注釋描述函式如何使用其參數和傳回值。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-120">Header annotations describe how a function uses its parameters and return value.</span></span> <span data-ttu-id="c6b6d-121">這些批註已新增至許多 Windows 標頭檔，以協助您確定您正確地呼叫 Windows API。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-121">These annotations have been added to many of the Windows header files to help you ensure that you are calling the Windows API correctly.</span></span> <span data-ttu-id="c6b6d-122">如果您啟用程式碼分析（從 Visual Studio 2005 開始提供），則編譯器將會產生層級6000警告，如果您未根據批註所描述的使用方式來呼叫這些函式。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-122">If you enable code analysis, which is available starting with the Visual Studio 2005, the compiler will produce level 6000 warnings if you are not calling these functions per the usage described through the annotations.</span></span> <span data-ttu-id="c6b6d-123">您也可以在自己的程式碼中新增這些批註，以確保正確地呼叫它。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-123">You can also add these annotations in your own code to ensure that it is being called correctly.</span></span> <span data-ttu-id="c6b6d-124">若要在 Visual Studio 中啟用程式碼分析，請參閱 Visual Studio 版本的檔。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-124">To enable code analysis in Visual Studio, see the documentation for your version of Visual Studio.</span></span>

<span data-ttu-id="c6b6d-125">這些批註是在 Specstrings 中定義。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-125">These annotations are defined in Specstrings.h.</span></span> <span data-ttu-id="c6b6d-126">它們建置於屬於標準批註語言一部分的基本專案， (SAL) 並使用執行 `_declspec("SAL_*")` 。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-126">They are built on primitives that are part of the Standard Annotation Language (SAL) and implemented using `_declspec("SAL_*")`.</span></span>

<span data-ttu-id="c6b6d-127">注釋有兩種類別：緩衝區注釋和先進注釋。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-127">There are two classes of annotations: buffer annotations and advanced annotations.</span></span>

## <a name="buffer-annotations"></a><span data-ttu-id="c6b6d-128">緩衝區批註</span><span class="sxs-lookup"><span data-stu-id="c6b6d-128">Buffer Annotations</span></span>

<span data-ttu-id="c6b6d-129">緩衝區批註描述函式如何使用其指標，並可用於偵測緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-129">Buffer annotations describe how functions use their pointers and can be used to detect buffer overruns.</span></span> <span data-ttu-id="c6b6d-130">每個參數都可以使用零或一個緩衝區注釋。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-130">Each parameter may use zero or one buffer annotation.</span></span> <span data-ttu-id="c6b6d-131">緩衝區批註會以前置底線和下列各節所述的元件來建立。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-131">A buffer annotation is constructed with a leading underscore and the components described in the following sections.</span></span>



| <span data-ttu-id="c6b6d-132">緩衝區大小</span><span class="sxs-lookup"><span data-stu-id="c6b6d-132">Buffer size</span></span>                                                                                  | <span data-ttu-id="c6b6d-133">Description</span><span class="sxs-lookup"><span data-stu-id="c6b6d-133">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b6d-134"><span id="_size_"></span><span id="_SIZE_"></span> (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-134"><span id="_size_"></span><span id="_SIZE_"></span>(*size*)</span></span><br/>                        | <span data-ttu-id="c6b6d-135">指定緩衝區的總大小。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-135">Specifies the total size of the buffer.</span></span> <span data-ttu-id="c6b6d-136">搭配 \_ bcount 和 \_ ecount 使用; 請勿使用 with \_ 部分。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-136">Use with \_bcount and \_ecount; do not use with \_part.</span></span> <span data-ttu-id="c6b6d-137">此值是可存取的空間;它可能小於配置的空間。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-137">This value is the accessible space; it may be less than the allocated space.</span></span><br/> |
| <span data-ttu-id="c6b6d-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span> (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*size*,*length*)</span></span><br/> | <span data-ttu-id="c6b6d-139">指定緩衝區的總大小和初始化長度。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-139">Specifies the total size and initialized length of the buffer.</span></span> <span data-ttu-id="c6b6d-140">搭配 \_ bcount \_ 元件和 \_ ecount 部分使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-140">Use with \_bcount\_part and \_ecount\_part.</span></span> <span data-ttu-id="c6b6d-141">總大小可能小於配置的空間。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-141">The total size may be less than the allocated space.</span></span><br/>              |



 



| <span data-ttu-id="c6b6d-142">緩衝區大小單位</span><span class="sxs-lookup"><span data-stu-id="c6b6d-142">Buffer size units</span></span>                                                       | <span data-ttu-id="c6b6d-143">Description</span><span class="sxs-lookup"><span data-stu-id="c6b6d-143">Description</span></span>                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="c6b6d-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span><span class="sxs-lookup"><span data-stu-id="c6b6d-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span></span><br/> | <span data-ttu-id="c6b6d-145">緩衝區大小以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-145">The buffer size is in bytes.</span></span><br/>    |
| <span data-ttu-id="c6b6d-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span><span class="sxs-lookup"><span data-stu-id="c6b6d-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span></span><br/> | <span data-ttu-id="c6b6d-147">緩衝區大小是在元素中。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-147">The buffer size is in elements.</span></span><br/> |



 



| <span data-ttu-id="c6b6d-148">方向</span><span class="sxs-lookup"><span data-stu-id="c6b6d-148">Direction</span></span>                                                            | <span data-ttu-id="c6b6d-149">Description</span><span class="sxs-lookup"><span data-stu-id="c6b6d-149">Description</span></span>                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b6d-150"><span id="_in"></span><span id="_IN"></span>\_在</span><span class="sxs-lookup"><span data-stu-id="c6b6d-150"><span id="_in"></span><span id="_IN"></span>\_in</span></span><br/>          | <span data-ttu-id="c6b6d-151">函數會從緩衝區讀取。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-151">The function reads from the buffer.</span></span> <span data-ttu-id="c6b6d-152">呼叫端會提供緩衝區，並將其初始化。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-152">The caller provides the buffer and initializes it.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="c6b6d-153"><span id="_inout"></span><span id="_INOUT"></span>\_inout</span><span class="sxs-lookup"><span data-stu-id="c6b6d-153"><span id="_inout"></span><span id="_INOUT"></span>\_inout</span></span><br/> | <span data-ttu-id="c6b6d-154">函數會從緩衝區讀取和寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-154">The function both reads from and writes to buffer.</span></span> <span data-ttu-id="c6b6d-155">呼叫端會提供緩衝區，並將其初始化。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-155">The caller provides the buffer and initializes it.</span></span> <span data-ttu-id="c6b6d-156">如果與 deref 搭配使用 \_ ，緩衝區可能會由函式重新配置。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-156">If used with \_deref, the buffer may be reallocated by the function.</span></span><br/>                                      |
| <span data-ttu-id="c6b6d-157"><span id="_out"></span><span id="_OUT"></span>\_擴展</span><span class="sxs-lookup"><span data-stu-id="c6b6d-157"><span id="_out"></span><span id="_OUT"></span>\_out</span></span><br/>       | <span data-ttu-id="c6b6d-158">函數會寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-158">The function writes to the buffer.</span></span> <span data-ttu-id="c6b6d-159">如果用於傳回值或使用 \_ deref，則函式會提供緩衝區，並將其初始化。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-159">If used on the return value or with \_deref, the function provides the buffer and initializes it.</span></span> <span data-ttu-id="c6b6d-160">否則，呼叫端會提供緩衝區，而函式會將它初始化。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-160">Otherwise, the caller provides the buffer and the function initializes it.</span></span><br/> |



 



| <span data-ttu-id="c6b6d-161">間接</span><span class="sxs-lookup"><span data-stu-id="c6b6d-161">Indirection</span></span>                                                                       | <span data-ttu-id="c6b6d-162">Description</span><span class="sxs-lookup"><span data-stu-id="c6b6d-162">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b6d-163"><span id="_deref"></span><span id="_DEREF"></span>\_deref</span><span class="sxs-lookup"><span data-stu-id="c6b6d-163"><span id="_deref"></span><span id="_DEREF"></span>\_deref</span></span><br/>              | <span data-ttu-id="c6b6d-164">取值參數以取得緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-164">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="c6b6d-165">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-165">This parameter may not be **NULL**.</span></span><br/> |
| <span data-ttu-id="c6b6d-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref \_ opt</span><span class="sxs-lookup"><span data-stu-id="c6b6d-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref\_opt</span></span><br/> | <span data-ttu-id="c6b6d-167">取值參數以取得緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-167">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="c6b6d-168">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-168">This parameter can be **NULL**.</span></span><br/>     |



 



| <span data-ttu-id="c6b6d-169">初始化</span><span class="sxs-lookup"><span data-stu-id="c6b6d-169">Initialization</span></span>                                                    | <span data-ttu-id="c6b6d-170">Description</span><span class="sxs-lookup"><span data-stu-id="c6b6d-170">Description</span></span>                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b6d-171"><span id="_full"></span><span id="_FULL"></span>\_全</span><span class="sxs-lookup"><span data-stu-id="c6b6d-171"><span id="_full"></span><span id="_FULL"></span>\_full</span></span><br/> | <span data-ttu-id="c6b6d-172">函數會初始化整個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-172">The function initializes the entire buffer.</span></span> <span data-ttu-id="c6b6d-173">只能搭配輸出緩衝區使用。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-173">Use only with output buffers.</span></span><br/>                                     |
| <span data-ttu-id="c6b6d-174"><span id="_part"></span><span id="_PART"></span>\_部分</span><span class="sxs-lookup"><span data-stu-id="c6b6d-174"><span id="_part"></span><span id="_PART"></span>\_part</span></span><br/> | <span data-ttu-id="c6b6d-175">此函式會初始化緩衝區的一部分，並明確地指出有多少。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-175">The function initializes part of the buffer, and explicitly indicates how much.</span></span> <span data-ttu-id="c6b6d-176">只能搭配輸出緩衝區使用。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-176">Use only with output buffers.</span></span><br/> |



 



| <span data-ttu-id="c6b6d-177">必要或選擇性的緩衝區</span><span class="sxs-lookup"><span data-stu-id="c6b6d-177">Required or optional buffer</span></span>                                    | <span data-ttu-id="c6b6d-178">Description</span><span class="sxs-lookup"><span data-stu-id="c6b6d-178">Description</span></span>                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="c6b6d-179"><span id="_opt"></span><span id="_OPT"></span>\_選擇</span><span class="sxs-lookup"><span data-stu-id="c6b6d-179"><span id="_opt"></span><span id="_OPT"></span>\_opt</span></span><br/> | <span data-ttu-id="c6b6d-180">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-180">This parameter can be **NULL**.</span></span><br/> |



 

<span data-ttu-id="c6b6d-181">下列範例會顯示 **GetModuleFileName** 函式的附注。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-181">The following example shows the annotations for the **GetModuleFileName** function.</span></span> <span data-ttu-id="c6b6d-182">*HModule* 參數是選擇性的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-182">The *hModule* parameter is an optional input parameter .</span></span> <span data-ttu-id="c6b6d-183">*LpFilename* 參數是輸出參數;其大小（以字元為單位）是由 *nSize* 參數指定，其長度包括 **null** 終止字元。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-183">The *lpFilename* parameter is an output parameter; its size in characters is specified by the *nSize* parameter and its length includes the **null**-terminating character.</span></span> <span data-ttu-id="c6b6d-184">*NSize* 參數是輸入參數。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-184">The *nSize* parameter is an input parameter.</span></span>


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



<span data-ttu-id="c6b6d-185">以下是在 Specstrings 中定義的附注。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-185">The following are the annotations defined in Specstrings.h.</span></span> <span data-ttu-id="c6b6d-186">使用上述表格中的資訊來解讀其意義。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-186">Use the information in the tables above to interpret their meaning.</span></span>

<span data-ttu-id="c6b6d-187">__bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-187">__bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-188">__bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-188">__bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-189">__deref_bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-189">__deref_bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-190">__deref_bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-190">__deref_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-191">__deref_ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-191">__deref_ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-192">__deref_ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-192">__deref_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-193">__deref_in</span><span class="sxs-lookup"><span data-stu-id="c6b6d-193">__deref_in</span></span>  
<span data-ttu-id="c6b6d-194">__deref_in_bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-194">__deref_in_bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-195">__deref_in_bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-195">__deref_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-196">__deref_in_ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-196">__deref_in_ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-197">__deref_in_ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-197">__deref_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-198">__deref_in_opt</span><span class="sxs-lookup"><span data-stu-id="c6b6d-198">__deref_in_opt</span></span>  
<span data-ttu-id="c6b6d-199">__deref_inout</span><span class="sxs-lookup"><span data-stu-id="c6b6d-199">__deref_inout</span></span>  
<span data-ttu-id="c6b6d-200">__deref_inout_bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-200">__deref_inout_bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-201">__deref_inout_bcount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-201">__deref_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-202">__deref_inout_bcount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-202">__deref_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-203">__deref_inout_bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-203">__deref_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-204">__deref_inout_bcount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-204">__deref_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-205">__deref_inout_bcount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-205">__deref_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-206">__deref_inout_ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-206">__deref_inout_ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-207">__deref_inout_ecount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-207">__deref_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-208">__deref_inout_ecount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-208">__deref_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-209">__deref_inout_ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-209">__deref_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-210">__deref_inout_ecount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-210">__deref_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-211">__deref_inout_ecount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-211">__deref_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-212">__deref_inout_opt</span><span class="sxs-lookup"><span data-stu-id="c6b6d-212">__deref_inout_opt</span></span>  
<span data-ttu-id="c6b6d-213">__deref_opt_bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-213">__deref_opt_bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-214">__deref_opt_bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-214">__deref_opt_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-215">__deref_opt_ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-215">__deref_opt_ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-216">__deref_opt_ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-216">__deref_opt_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-217">__deref_opt_in</span><span class="sxs-lookup"><span data-stu-id="c6b6d-217">__deref_opt_in</span></span>  
<span data-ttu-id="c6b6d-218">__deref_opt_in_bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-218">__deref_opt_in_bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-219">__deref_opt_in_bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-219">__deref_opt_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-220">__deref_opt_in_ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-220">__deref_opt_in_ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-221">__deref_opt_in_ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-221">__deref_opt_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-222">__deref_opt_in_opt</span><span class="sxs-lookup"><span data-stu-id="c6b6d-222">__deref_opt_in_opt</span></span>  
<span data-ttu-id="c6b6d-223">__deref_opt_inout</span><span class="sxs-lookup"><span data-stu-id="c6b6d-223">__deref_opt_inout</span></span>  
<span data-ttu-id="c6b6d-224">__deref_opt_inout_bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-224">__deref_opt_inout_bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-225">__deref_opt_inout_bcount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-225">__deref_opt_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-226">__deref_opt_inout_bcount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-226">__deref_opt_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-227">__deref_opt_inout_bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-227">__deref_opt_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-228">__deref_opt_inout_bcount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-228">__deref_opt_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-229">__deref_opt_inout_bcount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-229">__deref_opt_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-230">__deref_opt_inout_ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-230">__deref_opt_inout_ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-231">__deref_opt_inout_ecount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-231">__deref_opt_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-232">__deref_opt_inout_ecount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-232">__deref_opt_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-233">__deref_opt_inout_ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-233">__deref_opt_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-234">__deref_opt_inout_ecount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-234">__deref_opt_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-235">__deref_opt_inout_ecount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-235">__deref_opt_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-236">__deref_opt_inout_opt</span><span class="sxs-lookup"><span data-stu-id="c6b6d-236">__deref_opt_inout_opt</span></span>  
<span data-ttu-id="c6b6d-237">__deref_opt_out</span><span class="sxs-lookup"><span data-stu-id="c6b6d-237">__deref_opt_out</span></span>  
<span data-ttu-id="c6b6d-238">__deref_opt_out_bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-238">__deref_opt_out_bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-239">__deref_opt_out_bcount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-239">__deref_opt_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-240">__deref_opt_out_bcount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-240">__deref_opt_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-241">__deref_opt_out_bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-241">__deref_opt_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-242">__deref_opt_out_bcount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-242">__deref_opt_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-243">__deref_opt_out_bcount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-243">__deref_opt_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-244">__deref_opt_out_ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-244">__deref_opt_out_ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-245">__deref_opt_out_ecount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-245">__deref_opt_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-246">__deref_opt_out_ecount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-246">__deref_opt_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-247">__deref_opt_out_ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-247">__deref_opt_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-248">__deref_opt_out_ecount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-248">__deref_opt_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-249">__deref_opt_out_ecount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-249">__deref_opt_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-250">__deref_opt_out_opt</span><span class="sxs-lookup"><span data-stu-id="c6b6d-250">__deref_opt_out_opt</span></span>  
<span data-ttu-id="c6b6d-251">__deref_out</span><span class="sxs-lookup"><span data-stu-id="c6b6d-251">__deref_out</span></span>  
<span data-ttu-id="c6b6d-252">__deref_out_bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-252">__deref_out_bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-253">__deref_out_bcount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-253">__deref_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-254">__deref_out_bcount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-254">__deref_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-255">__deref_out_bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-255">__deref_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-256">__deref_out_bcount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-256">__deref_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-257">__deref_out_bcount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-257">__deref_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-258">__deref_out_ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-258">__deref_out_ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-259">__deref_out_ecount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-259">__deref_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-260">__deref_out_ecount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-260">__deref_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-261">__deref_out_ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-261">__deref_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-262">__deref_out_ecount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-262">__deref_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-263">__deref_out_ecount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-263">__deref_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-264">__deref_out_opt</span><span class="sxs-lookup"><span data-stu-id="c6b6d-264">__deref_out_opt</span></span>  
<span data-ttu-id="c6b6d-265">__ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-265">__ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-266">__ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-266">__ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-267">__in</span><span class="sxs-lookup"><span data-stu-id="c6b6d-267">__in</span></span>  
<span data-ttu-id="c6b6d-268">__in_bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-268">__in_bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-269">__in_bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-269">__in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-270">__in_ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-270">__in_ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-271">__in_ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-271">__in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-272">__in_opt</span><span class="sxs-lookup"><span data-stu-id="c6b6d-272">__in_opt</span></span>  
<span data-ttu-id="c6b6d-273">__inout</span><span class="sxs-lookup"><span data-stu-id="c6b6d-273">__inout</span></span>  
<span data-ttu-id="c6b6d-274">__inout_bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-274">__inout_bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-275">__inout_bcount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-275">__inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-276">__inout_bcount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-276">__inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-277">__inout_bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-277">__inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-278">__inout_bcount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-278">__inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-279">__inout_bcount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-279">__inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-280">__inout_ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-280">__inout_ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-281">__inout_ecount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-281">__inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-282">__inout_ecount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-282">__inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-283">__inout_ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-283">__inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-284">__inout_ecount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-284">__inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-285">__inout_ecount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-285">__inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-286">__inout_opt</span><span class="sxs-lookup"><span data-stu-id="c6b6d-286">__inout_opt</span></span>  
<span data-ttu-id="c6b6d-287">__out</span><span class="sxs-lookup"><span data-stu-id="c6b6d-287">__out</span></span>  
<span data-ttu-id="c6b6d-288">__out_bcount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-288">__out_bcount(*size*)</span></span>  
<span data-ttu-id="c6b6d-289">__out_bcount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-289">__out_bcount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-290">__out_bcount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-290">__out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-291">__out_bcount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-291">__out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-292">__out_bcount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-292">__out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-293">__out_bcount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-293">__out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-294">__out_ecount (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-294">__out_ecount(*size*)</span></span>  
<span data-ttu-id="c6b6d-295">__out_ecount_full (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-295">__out_ecount_full(*size*)</span></span>  
<span data-ttu-id="c6b6d-296">__out_ecount_full_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-296">__out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-297">__out_ecount_opt (*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-297">__out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c6b6d-298">__out_ecount_part (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-298">__out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-299">__out_ecount_part_opt (*大小*，*長度*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-299">__out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c6b6d-300">__out_opt</span><span class="sxs-lookup"><span data-stu-id="c6b6d-300">__out_opt</span></span>  

## <a name="advanced-annotations"></a><span data-ttu-id="c6b6d-301">Advanced 批註</span><span class="sxs-lookup"><span data-stu-id="c6b6d-301">Advanced Annotations</span></span>

<span data-ttu-id="c6b6d-302">Advanced 批註提供參數或傳回值的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-302">Advanced annotations provide additional information about the parameter or return value.</span></span> <span data-ttu-id="c6b6d-303">每個參數或傳回值都可以使用零或一個 advanced 批註。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-303">Each parameter or return value may use zero or one advanced annotation.</span></span>



| <span data-ttu-id="c6b6d-304">Annotation</span><span class="sxs-lookup"><span data-stu-id="c6b6d-304">Annotation</span></span>                                                                                                                                               | <span data-ttu-id="c6b6d-305">Description</span><span class="sxs-lookup"><span data-stu-id="c6b6d-305">Description</span></span>                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b6d-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn (*資源*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn(*resource*)</span></span><br/> | <span data-ttu-id="c6b6d-307">函數會封鎖指定的資源。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-307">The functions blocks on the specified resource.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="c6b6d-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_回檔</span><span class="sxs-lookup"><span data-stu-id="c6b6d-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_callback</span></span><br/>                                                                        | <span data-ttu-id="c6b6d-309">函數可用來當做函式指標。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-309">The function can be used as a function pointer.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="c6b6d-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span><span class="sxs-lookup"><span data-stu-id="c6b6d-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span></span><br/>                               | <span data-ttu-id="c6b6d-311">呼叫端必須檢查傳回值。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-311">Callers must check the return value.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="c6b6d-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_格式 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="c6b6d-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_format\_string</span></span><br/>                                                        | <span data-ttu-id="c6b6d-313">參數是包含 printf 樣式% 標記的字串。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-313">The parameter is a string that contains printf-style % markers.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="c6b6d-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_在 \_ awcount (*運算式* 中，*大小*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in\_awcount(*expr*,*size*)</span></span><br/>                            | <span data-ttu-id="c6b6d-315">如果在結束時運算式為 true，則會指定輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-315">If the expression is true at exit, the size of the input buffer is specified in bytes.</span></span> <span data-ttu-id="c6b6d-316">如果運算式為 false，則會在元素中指定大小。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-316">If the expression is false, the size is specified in elements.</span></span><br/>                                                                                                                |
| <span data-ttu-id="c6b6d-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span><span class="sxs-lookup"><span data-stu-id="c6b6d-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span></span><br/>                                          | <span data-ttu-id="c6b6d-318">緩衝區最多可存取，包括兩個 **null** 字元或指標的第一個序列。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-318">The buffer may be accessed up to and including the first sequence of two **null** characters or pointers.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="c6b6d-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_nullterminated</span><span class="sxs-lookup"><span data-stu-id="c6b6d-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_nullterminated</span></span><br/>                                                      | <span data-ttu-id="c6b6d-320">緩衝區最多可存取，並包括第一個 **null** 字元或指標。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-320">The buffer may be accessed up to and including the first **null** character or pointer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="c6b6d-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount (*expr*，*size*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out\_awcount(*expr*,*size*)</span></span><br/>                         | <span data-ttu-id="c6b6d-322">如果在結束時運算式為 true，則會指定輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-322">If the expression is true at exit, the size of the output buffer is specified in bytes.</span></span> <span data-ttu-id="c6b6d-323">如果運算式為 false，則會在元素中指定大小。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-323">If the expression is false, the size is specified in elements.</span></span> <br/>                                                                                                              |
| <span data-ttu-id="c6b6d-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_覆蓋</span><span class="sxs-lookup"><span data-stu-id="c6b6d-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_override</span></span><br/>                                                                        | <span data-ttu-id="c6b6d-325">指定虛擬方法的 c # 樣式覆寫行為。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-325">Specifies C#-style override behavior for virtual methods.</span></span><br/>                                                                                                                                                                                                           |
| <span data-ttu-id="c6b6d-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_保留</span><span class="sxs-lookup"><span data-stu-id="c6b6d-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_reserved</span></span><br/>                                                                        | <span data-ttu-id="c6b6d-327">參數已保留供日後使用，且必須為零或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-327">The parameter is reserved for future use and must be zero or **NULL**.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="c6b6d-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_success (*expr*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_success(*expr*)</span></span><br/>                                                       | <span data-ttu-id="c6b6d-329">如果在結束時運算式為 true，則呼叫端可以依賴其他注釋所指定的所有保證。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-329">If the expression is true at exit, the caller can rely on all guarantees specified by other annotations.</span></span> <span data-ttu-id="c6b6d-330">如果運算式為 false，則呼叫端無法依賴保證。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-330">If the expression is false, the caller cannot rely on the guarantees.</span></span> <span data-ttu-id="c6b6d-331">這個批註會自動加入至傳回 **HRESULT** 值的函式。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-331">This annotation is automatically added to functions that return an **HRESULT** value.</span></span><br/> |
| <span data-ttu-id="c6b6d-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*ctype*) </span><span class="sxs-lookup"><span data-stu-id="c6b6d-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix(*ctype*)</span></span><br/>                                                    | <span data-ttu-id="c6b6d-333">將參數視為指定的型別，而不是其宣告的型別。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-333">Treat the parameter as the specified type rather than its declared type.</span></span><br/>                                                                                                                                                                                             |



 

<span data-ttu-id="c6b6d-334">下列範例顯示 [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer)、 [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)和 [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) 函數的緩衝區和先進注釋。</span><span class="sxs-lookup"><span data-stu-id="c6b6d-334">The following examples show the buffer and advanced annotations for the [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa), and [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) functions.</span></span>


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a><span data-ttu-id="c6b6d-335">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6b6d-335">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6b6d-336">SAL 注釋</span><span class="sxs-lookup"><span data-stu-id="c6b6d-336">SAL Annotations</span></span>](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="c6b6d-337">逐步解說：分析 C/C++ 程式碼的缺失</span><span class="sxs-lookup"><span data-stu-id="c6b6d-337">Walkthrough: Analyzing C/C++ Code for Defects</span></span>](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

