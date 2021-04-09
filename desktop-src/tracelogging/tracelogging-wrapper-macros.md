---
title: TraceLogging 包裝函式宏
description: 列出 TraceLogging 提供者的包裝函式宏。
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc28b3a35074089b1f5c613b041534b8b282423
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675635"
---
# <a name="tracelogging-wrapper-macros"></a><span data-ttu-id="d3234-103">TraceLogging 包裝函式宏</span><span class="sxs-lookup"><span data-stu-id="d3234-103">TraceLogging Wrapper Macros</span></span>

<span data-ttu-id="d3234-104">列出 TraceLogging 提供者的包裝函式宏。</span><span class="sxs-lookup"><span data-stu-id="d3234-104">Lists the wrapper macros for TraceLogging providers.</span></span>

<span data-ttu-id="d3234-105">若要使用 TraceLogging 提供者來記錄事件，您必須使用 TraceLogging 寫入宏 [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) 或 [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity)。</span><span class="sxs-lookup"><span data-stu-id="d3234-105">In order to record events using TraceLogging providers, you need to use the TraceLogging write macros [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) or [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span></span> <span data-ttu-id="d3234-106">這兩個宏都需要您將任何事件資料包裝在包裝函式宏中。</span><span class="sxs-lookup"><span data-stu-id="d3234-106">Both of these macros require you to wrap any event data in a wrapper macro.</span></span> <span data-ttu-id="d3234-107">不同的資料類型有幾個不同的包裝函式宏。</span><span class="sxs-lookup"><span data-stu-id="d3234-107">There are several different wrapper macros for different data types.</span></span> <span data-ttu-id="d3234-108">如需 TraceLogging 宏的完整清單，請參閱 [TraceLogging 宏](trace-logging-macros.md)。</span><span class="sxs-lookup"><span data-stu-id="d3234-108">For a complete list of TraceLogging macros, see [TraceLogging Macros](trace-logging-macros.md).</span></span>

<span data-ttu-id="d3234-109">除了上述的包裝函式宏之外，還提供數個宏供個別資料類型使用。</span><span class="sxs-lookup"><span data-stu-id="d3234-109">In addition to the wrapper macros above, several macros are available for individual data types.</span></span> <span data-ttu-id="d3234-110">所有這些宏都具有與 [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) 宏相同的格式。</span><span class="sxs-lookup"><span data-stu-id="d3234-110">All of these macros have the same format as the [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) macro.</span></span> <span data-ttu-id="d3234-111">您可以使用 TraceLoggingValue 宏來自動偵測要使用的適當包裝函式宏，或直接使用特定宏。</span><span class="sxs-lookup"><span data-stu-id="d3234-111">You can use the TraceLoggingValue macro to automatically detect the appropriate wrapper macro to use, or use the specific macro directly.</span></span>

-   [<span data-ttu-id="d3234-112">**TraceLoggingBinary**</span><span class="sxs-lookup"><span data-stu-id="d3234-112">**TraceLoggingBinary**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [<span data-ttu-id="d3234-113">**TraceLoggingChannel**</span><span class="sxs-lookup"><span data-stu-id="d3234-113">**TraceLoggingChannel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [<span data-ttu-id="d3234-114">**TraceLoggingCustomAttribute**</span><span class="sxs-lookup"><span data-stu-id="d3234-114">**TraceLoggingCustomAttribute**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [<span data-ttu-id="d3234-115">**TraceLoggingDescription**</span><span class="sxs-lookup"><span data-stu-id="d3234-115">**TraceLoggingDescription**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [<span data-ttu-id="d3234-116">**TraceLoggingEventTag**</span><span class="sxs-lookup"><span data-stu-id="d3234-116">**TraceLoggingEventTag**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [<span data-ttu-id="d3234-117">**TraceLoggingKeyword**</span><span class="sxs-lookup"><span data-stu-id="d3234-117">**TraceLoggingKeyword**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [<span data-ttu-id="d3234-118">**TraceLoggingLevel**</span><span class="sxs-lookup"><span data-stu-id="d3234-118">**TraceLoggingLevel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [<span data-ttu-id="d3234-119">**TraceLoggingOpcode**</span><span class="sxs-lookup"><span data-stu-id="d3234-119">**TraceLoggingOpcode**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [<span data-ttu-id="d3234-120">**TraceLoggingSocketAddress**</span><span class="sxs-lookup"><span data-stu-id="d3234-120">**TraceLoggingSocketAddress**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [<span data-ttu-id="d3234-121">**TraceLoggingStruct**</span><span class="sxs-lookup"><span data-stu-id="d3234-121">**TraceLoggingStruct**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [<span data-ttu-id="d3234-122">**TraceLoggingValue**</span><span class="sxs-lookup"><span data-stu-id="d3234-122">**TraceLoggingValue**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> <span data-ttu-id="d3234-123">**TraceLoggingOptionGroup** 專用於 TRACELOGGING \_ 定義提供者內的使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d3234-123">**TraceLoggingOptionGroup** is specifically for use inside of TRACELOGGING\_DEFINE\_PROVIDER.</span></span>
>
> -   [<span data-ttu-id="d3234-124">**TraceLoggingOptionGroup**</span><span class="sxs-lookup"><span data-stu-id="d3234-124">**TraceLoggingOptionGroup**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

<span data-ttu-id="d3234-125">以下是個別的包裝函式宏。</span><span class="sxs-lookup"><span data-stu-id="d3234-125">Here are the individual wrapper macros.</span></span>

-   <span data-ttu-id="d3234-126">TraceLoggingInt8</span><span class="sxs-lookup"><span data-stu-id="d3234-126">TraceLoggingInt8</span></span>

-   <span data-ttu-id="d3234-127">TraceLoggingUInt8</span><span class="sxs-lookup"><span data-stu-id="d3234-127">TraceLoggingUInt8</span></span>

-   <span data-ttu-id="d3234-128">TraceLoggingInt16</span><span class="sxs-lookup"><span data-stu-id="d3234-128">TraceLoggingInt16</span></span>

-   <span data-ttu-id="d3234-129">TraceLoggingUInt16</span><span class="sxs-lookup"><span data-stu-id="d3234-129">TraceLoggingUInt16</span></span>

-   <span data-ttu-id="d3234-130">TraceLoggingInt32</span><span class="sxs-lookup"><span data-stu-id="d3234-130">TraceLoggingInt32</span></span>

-   <span data-ttu-id="d3234-131">TraceLoggingUInt32</span><span class="sxs-lookup"><span data-stu-id="d3234-131">TraceLoggingUInt32</span></span>

-   <span data-ttu-id="d3234-132">TraceLoggingInt64</span><span class="sxs-lookup"><span data-stu-id="d3234-132">TraceLoggingInt64</span></span>

-   <span data-ttu-id="d3234-133">TraceLoggingUInt64</span><span class="sxs-lookup"><span data-stu-id="d3234-133">TraceLoggingUInt64</span></span>

-   <span data-ttu-id="d3234-134">TraceLoggingFloat32</span><span class="sxs-lookup"><span data-stu-id="d3234-134">TraceLoggingFloat32</span></span>

-   <span data-ttu-id="d3234-135">TraceLoggingFloat64</span><span class="sxs-lookup"><span data-stu-id="d3234-135">TraceLoggingFloat64</span></span>

-   <span data-ttu-id="d3234-136">TraceLoggingBool</span><span class="sxs-lookup"><span data-stu-id="d3234-136">TraceLoggingBool</span></span>

-   <span data-ttu-id="d3234-137">TraceLoggingFileTime</span><span class="sxs-lookup"><span data-stu-id="d3234-137">TraceLoggingFileTime</span></span>

-   <span data-ttu-id="d3234-138">TraceLoggingGuid</span><span class="sxs-lookup"><span data-stu-id="d3234-138">TraceLoggingGuid</span></span>

-   <span data-ttu-id="d3234-139">TraceLoggingPointer</span><span class="sxs-lookup"><span data-stu-id="d3234-139">TraceLoggingPointer</span></span>

-   <span data-ttu-id="d3234-140">TraceLoggingSystemTime</span><span class="sxs-lookup"><span data-stu-id="d3234-140">TraceLoggingSystemTime</span></span>

-   <span data-ttu-id="d3234-141">TraceLoggingHexInt8</span><span class="sxs-lookup"><span data-stu-id="d3234-141">TraceLoggingHexInt8</span></span>

-   <span data-ttu-id="d3234-142">TraceLoggingHexUInt8</span><span class="sxs-lookup"><span data-stu-id="d3234-142">TraceLoggingHexUInt8</span></span>

-   <span data-ttu-id="d3234-143">TraceLoggingHexInt32</span><span class="sxs-lookup"><span data-stu-id="d3234-143">TraceLoggingHexInt32</span></span>

-   <span data-ttu-id="d3234-144">TraceLoggingHexUInt32</span><span class="sxs-lookup"><span data-stu-id="d3234-144">TraceLoggingHexUInt32</span></span>

-   <span data-ttu-id="d3234-145">TraceLoggingHexInt64</span><span class="sxs-lookup"><span data-stu-id="d3234-145">TraceLoggingHexInt64</span></span>

-   <span data-ttu-id="d3234-146">TraceLoggingHexUInt64</span><span class="sxs-lookup"><span data-stu-id="d3234-146">TraceLoggingHexUInt64</span></span>

-   <span data-ttu-id="d3234-147">TraceLoggingWchar</span><span class="sxs-lookup"><span data-stu-id="d3234-147">TraceLoggingWchar</span></span>

-   <span data-ttu-id="d3234-148">TraceLoggingChar</span><span class="sxs-lookup"><span data-stu-id="d3234-148">TraceLoggingChar</span></span>

-   <span data-ttu-id="d3234-149">TraceLoggingIntPtr</span><span class="sxs-lookup"><span data-stu-id="d3234-149">TraceLoggingIntPtr</span></span>

-   <span data-ttu-id="d3234-150">TraceLoggingUIntPtr</span><span class="sxs-lookup"><span data-stu-id="d3234-150">TraceLoggingUIntPtr</span></span>

-   <span data-ttu-id="d3234-151">TraceLoggingBoolean</span><span class="sxs-lookup"><span data-stu-id="d3234-151">TraceLoggingBoolean</span></span>

-   <span data-ttu-id="d3234-152">TraceLoggingHexInt16</span><span class="sxs-lookup"><span data-stu-id="d3234-152">TraceLoggingHexInt16</span></span>

-   <span data-ttu-id="d3234-153">TraceLoggingHexUInt16</span><span class="sxs-lookup"><span data-stu-id="d3234-153">TraceLoggingHexUInt16</span></span>

-   <span data-ttu-id="d3234-154">TraceLoggingPid</span><span class="sxs-lookup"><span data-stu-id="d3234-154">TraceLoggingPid</span></span>

-   <span data-ttu-id="d3234-155">TraceLoggingTid</span><span class="sxs-lookup"><span data-stu-id="d3234-155">TraceLoggingTid</span></span>

-   <span data-ttu-id="d3234-156">TraceLoggingPort</span><span class="sxs-lookup"><span data-stu-id="d3234-156">TraceLoggingPort</span></span>

-   <span data-ttu-id="d3234-157">TraceLoggingWinError</span><span class="sxs-lookup"><span data-stu-id="d3234-157">TraceLoggingWinError</span></span>

-   <span data-ttu-id="d3234-158">TraceLoggingNTStatus</span><span class="sxs-lookup"><span data-stu-id="d3234-158">TraceLoggingNTStatus</span></span>

-   <span data-ttu-id="d3234-159">TraceLoggingHResult</span><span class="sxs-lookup"><span data-stu-id="d3234-159">TraceLoggingHResult</span></span>

-   <span data-ttu-id="d3234-160">TraceLoggingSocketAddress</span><span class="sxs-lookup"><span data-stu-id="d3234-160">TraceLoggingSocketAddress</span></span>

-   <span data-ttu-id="d3234-161">TraceLoggingSid</span><span class="sxs-lookup"><span data-stu-id="d3234-161">TraceLoggingSid</span></span>

-   <span data-ttu-id="d3234-162">TraceLoggingString</span><span class="sxs-lookup"><span data-stu-id="d3234-162">TraceLoggingString</span></span>

-   <span data-ttu-id="d3234-163">TraceLoggingWideString</span><span class="sxs-lookup"><span data-stu-id="d3234-163">TraceLoggingWideString</span></span>

-   <span data-ttu-id="d3234-164">TraceLoggingCountedString</span><span class="sxs-lookup"><span data-stu-id="d3234-164">TraceLoggingCountedString</span></span>

-   <span data-ttu-id="d3234-165">TraceLoggingCountedWideString</span><span class="sxs-lookup"><span data-stu-id="d3234-165">TraceLoggingCountedWideString</span></span>

-   <span data-ttu-id="d3234-166">TraceLoggingAnsiString</span><span class="sxs-lookup"><span data-stu-id="d3234-166">TraceLoggingAnsiString</span></span>

-   <span data-ttu-id="d3234-167">TraceLoggingUnicodeString</span><span class="sxs-lookup"><span data-stu-id="d3234-167">TraceLoggingUnicodeString</span></span>

-   <span data-ttu-id="d3234-168">TraceLoggingBinary (void \* 資料、資料大小（以位元組為單位）、 \[ 選擇性 \] 名稱 ) 這個宏的參數不同于上述的參數。</span><span class="sxs-lookup"><span data-stu-id="d3234-168">TraceLoggingBinary(void \*data, size of the data in bytes, \[optional\] name ) The parameters to this macro differ from those above.</span></span> <span data-ttu-id="d3234-169">如果指定 *name* 參數，它必須是字串常值， (不是變數) ，而且可能不包含任何內嵌的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="d3234-169">If the *name* parameter is specified, it must be a string literal (not a variable) and may not contain any embedded null characters.</span></span> <span data-ttu-id="d3234-170">如果未提供 *名稱* 參數，則會自動產生名稱。</span><span class="sxs-lookup"><span data-stu-id="d3234-170">If the *name* parameter is not provided, a name is generated automatically.</span></span>

<span data-ttu-id="d3234-171">TraceLogging API 也會為數組提供數個宏。</span><span class="sxs-lookup"><span data-stu-id="d3234-171">The TraceLogging API also makes several macros available for arrays.</span></span> <span data-ttu-id="d3234-172">這些陣列的長度可以是固定長度，也可以是可變長度的長度，視您選擇使用的包裝函式宏而定。</span><span class="sxs-lookup"><span data-stu-id="d3234-172">These arrays can either have a fixed length or be of a variable length, depending on the wrapper macro you choose to use.</span></span> <span data-ttu-id="d3234-173">所有這些包裝函式宏都遵循此格式。</span><span class="sxs-lookup"><span data-stu-id="d3234-173">All of these wrapper macros follow this format.</span></span>

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

<span data-ttu-id="d3234-174">參數 *pVals* 指向資料的陣列，而 *cVals* 指出陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d3234-174">The parameter *pVals* points to the array of data and *cVals* indicates the number of elements in the array.</span></span> <span data-ttu-id="d3234-175">*cVals* 必須是常數，而且不可以是變數。</span><span class="sxs-lookup"><span data-stu-id="d3234-175">*cVals* must be a constant and cannot be a variable.</span></span> <span data-ttu-id="d3234-176">如同單一值包裝函式宏， *name*、 **desc** 和 *tag* 是選擇性參數，且必須遵循與 **TraceLoggingValue** 宏所說明的相同限制。</span><span class="sxs-lookup"><span data-stu-id="d3234-176">As with the single value wrapper macros, *name*, **desc**, and *tags* are optional parameters and must follow the same restrictions as explained with the **TraceLoggingValue** macro.</span></span>

-   <span data-ttu-id="d3234-177">TraceLoggingInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-177">TraceLoggingInt8FixedArray</span></span>

-   <span data-ttu-id="d3234-178">TraceLoggingUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-178">TraceLoggingUInt8FixedArray</span></span>

-   <span data-ttu-id="d3234-179">TraceLoggingInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-179">TraceLoggingInt16FixedArray</span></span>

-   <span data-ttu-id="d3234-180">TraceLoggingUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-180">TraceLoggingUInt16FixedArray</span></span>

-   <span data-ttu-id="d3234-181">TraceLoggingInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-181">TraceLoggingInt32FixedArray</span></span>

-   <span data-ttu-id="d3234-182">TraceLoggingUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-182">TraceLoggingUInt32FixedArray</span></span>

-   <span data-ttu-id="d3234-183">TraceLoggingInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-183">TraceLoggingInt64FixedArray</span></span>

-   <span data-ttu-id="d3234-184">TraceLoggingUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-184">TraceLoggingUInt64FixedArray</span></span>

-   <span data-ttu-id="d3234-185">TraceLoggingFloat32FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-185">TraceLoggingFloat32FixedArray</span></span>

-   <span data-ttu-id="d3234-186">TraceLoggingFloat64FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-186">TraceLoggingFloat64FixedArray</span></span>

-   <span data-ttu-id="d3234-187">TraceLoggingBoolFixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-187">TraceLoggingBoolFixedArray</span></span>

-   <span data-ttu-id="d3234-188">TraceLoggingGuidFixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-188">TraceLoggingGuidFixedArray</span></span>

-   <span data-ttu-id="d3234-189">TraceLoggingPointerFixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-189">TraceLoggingPointerFixedArray</span></span>

-   <span data-ttu-id="d3234-190">TraceLoggingFileTimeFixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-190">TraceLoggingFileTimeFixedArray</span></span>

-   <span data-ttu-id="d3234-191">TraceLoggingSystemTimeFixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-191">TraceLoggingSystemTimeFixedArray</span></span>

-   <span data-ttu-id="d3234-192">TraceLoggingHexInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-192">TraceLoggingHexInt8FixedArray</span></span>

-   <span data-ttu-id="d3234-193">TraceLoggingHexUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-193">TraceLoggingHexUInt8FixedArray</span></span>

-   <span data-ttu-id="d3234-194">TraceLoggingHexInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-194">TraceLoggingHexInt32FixedArray</span></span>

-   <span data-ttu-id="d3234-195">TraceLoggingHexUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-195">TraceLoggingHexUInt32FixedArray</span></span>

-   <span data-ttu-id="d3234-196">TraceLoggingHexInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-196">TraceLoggingHexInt64FixedArray</span></span>

-   <span data-ttu-id="d3234-197">TraceLoggingHexUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-197">TraceLoggingHexUInt64FixedArray</span></span>

-   <span data-ttu-id="d3234-198">TraceLoggingWcharFixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-198">TraceLoggingWcharFixedArray</span></span>

-   <span data-ttu-id="d3234-199">TraceLoggingCharFixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-199">TraceLoggingCharFixedArray</span></span>

-   <span data-ttu-id="d3234-200">TraceLoggingIntPtrFixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-200">TraceLoggingIntPtrFixedArray</span></span>

-   <span data-ttu-id="d3234-201">TraceLoggingUIntPtrFixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-201">TraceLoggingUIntPtrFixedArray</span></span>

-   <span data-ttu-id="d3234-202">TraceLoggingBooleanFixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-202">TraceLoggingBooleanFixedArray</span></span>

-   <span data-ttu-id="d3234-203">TraceLoggingHexInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-203">TraceLoggingHexInt16FixedArray</span></span>

-   <span data-ttu-id="d3234-204">TraceLoggingHexUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="d3234-204">TraceLoggingHexUInt16FixedArray</span></span>

-   <span data-ttu-id="d3234-205">TraceLoggingInt8Array</span><span class="sxs-lookup"><span data-stu-id="d3234-205">TraceLoggingInt8Array</span></span>

-   <span data-ttu-id="d3234-206">TraceLoggingUInt8Array</span><span class="sxs-lookup"><span data-stu-id="d3234-206">TraceLoggingUInt8Array</span></span>

-   <span data-ttu-id="d3234-207">TraceLoggingInt16Array</span><span class="sxs-lookup"><span data-stu-id="d3234-207">TraceLoggingInt16Array</span></span>

-   <span data-ttu-id="d3234-208">TraceLoggingUInt16Array</span><span class="sxs-lookup"><span data-stu-id="d3234-208">TraceLoggingUInt16Array</span></span>

-   <span data-ttu-id="d3234-209">TraceLoggingInt32Array</span><span class="sxs-lookup"><span data-stu-id="d3234-209">TraceLoggingInt32Array</span></span>

-   <span data-ttu-id="d3234-210">TraceLoggingUInt32Array</span><span class="sxs-lookup"><span data-stu-id="d3234-210">TraceLoggingUInt32Array</span></span>

-   <span data-ttu-id="d3234-211">TraceLoggingInt64Array</span><span class="sxs-lookup"><span data-stu-id="d3234-211">TraceLoggingInt64Array</span></span>

-   <span data-ttu-id="d3234-212">TraceLoggingUInt64Array</span><span class="sxs-lookup"><span data-stu-id="d3234-212">TraceLoggingUInt64Array</span></span>

-   <span data-ttu-id="d3234-213">TraceLoggingFloat32Array</span><span class="sxs-lookup"><span data-stu-id="d3234-213">TraceLoggingFloat32Array</span></span>

-   <span data-ttu-id="d3234-214">TraceLoggingFloat64Array</span><span class="sxs-lookup"><span data-stu-id="d3234-214">TraceLoggingFloat64Array</span></span>

-   <span data-ttu-id="d3234-215">TraceLoggingBoolArray</span><span class="sxs-lookup"><span data-stu-id="d3234-215">TraceLoggingBoolArray</span></span>

-   <span data-ttu-id="d3234-216">TraceLoggingGuidArray</span><span class="sxs-lookup"><span data-stu-id="d3234-216">TraceLoggingGuidArray</span></span>

-   <span data-ttu-id="d3234-217">TraceLoggingPointerArray</span><span class="sxs-lookup"><span data-stu-id="d3234-217">TraceLoggingPointerArray</span></span>

-   <span data-ttu-id="d3234-218">TraceLoggingFileTimeArray</span><span class="sxs-lookup"><span data-stu-id="d3234-218">TraceLoggingFileTimeArray</span></span>

-   <span data-ttu-id="d3234-219">TraceLoggingSystemTimeArray</span><span class="sxs-lookup"><span data-stu-id="d3234-219">TraceLoggingSystemTimeArray</span></span>

-   <span data-ttu-id="d3234-220">TraceLoggingHexInt8Array</span><span class="sxs-lookup"><span data-stu-id="d3234-220">TraceLoggingHexInt8Array</span></span>

-   <span data-ttu-id="d3234-221">TraceLoggingHexUInt8Array</span><span class="sxs-lookup"><span data-stu-id="d3234-221">TraceLoggingHexUInt8Array</span></span>

-   <span data-ttu-id="d3234-222">TraceLoggingHexInt32Array</span><span class="sxs-lookup"><span data-stu-id="d3234-222">TraceLoggingHexInt32Array</span></span>

-   <span data-ttu-id="d3234-223">TraceLoggingHexUInt32Array</span><span class="sxs-lookup"><span data-stu-id="d3234-223">TraceLoggingHexUInt32Array</span></span>

-   <span data-ttu-id="d3234-224">TraceLoggingHexInt64Array</span><span class="sxs-lookup"><span data-stu-id="d3234-224">TraceLoggingHexInt64Array</span></span>

-   <span data-ttu-id="d3234-225">TraceLoggingHexUInt64Array</span><span class="sxs-lookup"><span data-stu-id="d3234-225">TraceLoggingHexUInt64Array</span></span>

-   <span data-ttu-id="d3234-226">TraceLoggingWcharArray</span><span class="sxs-lookup"><span data-stu-id="d3234-226">TraceLoggingWcharArray</span></span>

-   <span data-ttu-id="d3234-227">TraceLoggingCharArray</span><span class="sxs-lookup"><span data-stu-id="d3234-227">TraceLoggingCharArray</span></span>

-   <span data-ttu-id="d3234-228">TraceLoggingIntPtrArray</span><span class="sxs-lookup"><span data-stu-id="d3234-228">TraceLoggingIntPtrArray</span></span>

-   <span data-ttu-id="d3234-229">TraceLoggingUIntPtrArray</span><span class="sxs-lookup"><span data-stu-id="d3234-229">TraceLoggingUIntPtrArray</span></span>

-   <span data-ttu-id="d3234-230">TraceLoggingBooleanArray</span><span class="sxs-lookup"><span data-stu-id="d3234-230">TraceLoggingBooleanArray</span></span>

-   <span data-ttu-id="d3234-231">TraceLoggingHexInt16Array</span><span class="sxs-lookup"><span data-stu-id="d3234-231">TraceLoggingHexInt16Array</span></span>

-   <span data-ttu-id="d3234-232">TraceLoggingHexUInt16Array</span><span class="sxs-lookup"><span data-stu-id="d3234-232">TraceLoggingHexUInt16Array</span></span>

 

 




