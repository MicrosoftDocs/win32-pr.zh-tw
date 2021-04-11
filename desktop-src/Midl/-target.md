---
title: /target 參數
description: /Target 參數可讓 MIDL 編譯器只啟用最新 Windows 版本的優化功能。 /Target 參數會自動啟用額外的參數。
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- /target 參數 MIDL
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104027620"
---
# <a name="target-switch"></a><span data-ttu-id="ebc13-105">/target 參數</span><span class="sxs-lookup"><span data-stu-id="ebc13-105">/target switch</span></span>

<span data-ttu-id="ebc13-106">**/Target** 參數可讓 MIDL 編譯器只啟用最新 Windows 版本的優化功能。</span><span class="sxs-lookup"><span data-stu-id="ebc13-106">The **/target** switch enables the MIDL compiler to enable optimizations available only on recent versions of Windows.</span></span> <span data-ttu-id="ebc13-107">**/Target** 參數會自動啟用額外的參數。</span><span class="sxs-lookup"><span data-stu-id="ebc13-107">The **/target** switch automatically activates additional switches.</span></span>

``` syntax
midl /target level
```

## <a name="switch-options"></a><span data-ttu-id="ebc13-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="ebc13-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="ebc13-109">*level*</span><span class="sxs-lookup"><span data-stu-id="ebc13-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="ebc13-110">指定目標層級，例如 NT50、NT51、NT60、NT61、NT62 或 NT100。</span><span class="sxs-lookup"><span data-stu-id="ebc13-110">Specifies the target level, such as NT50, NT51, NT60, NT61, NT62, or NT100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebc13-111">備註</span><span class="sxs-lookup"><span data-stu-id="ebc13-111">Remarks</span></span>

<span data-ttu-id="ebc13-112">**/Target** 參數會根據下表所指定的作業系統，自動啟用其他參數：</span><span class="sxs-lookup"><span data-stu-id="ebc13-112">The **/target** switch automatically activates additional switches, based on the operating system, as specified in the following table:</span></span>



| <span data-ttu-id="ebc13-113">作業系統</span><span class="sxs-lookup"><span data-stu-id="ebc13-113">Operating system</span></span> | <span data-ttu-id="ebc13-114">/target 層級</span><span class="sxs-lookup"><span data-stu-id="ebc13-114">/target level</span></span> | <span data-ttu-id="ebc13-115">啟用的開關</span><span class="sxs-lookup"><span data-stu-id="ebc13-115">Switches Activated</span></span>                     |
|------------------|---------------|----------------------------------------|
| <span data-ttu-id="ebc13-116">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ebc13-116">Windows 2000</span></span>     | <span data-ttu-id="ebc13-117">NT50</span><span class="sxs-lookup"><span data-stu-id="ebc13-117">NT50</span></span>          | <span data-ttu-id="ebc13-118">/Oicf/error all/robust</span><span class="sxs-lookup"><span data-stu-id="ebc13-118">/Oicf /error all /robust</span></span>               |
| <span data-ttu-id="ebc13-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ebc13-119">Windows XP</span></span>       | <span data-ttu-id="ebc13-120">NT51</span><span class="sxs-lookup"><span data-stu-id="ebc13-120">NT51</span></span>          | <span data-ttu-id="ebc13-121">/Oicf/error all/robust/protocol all</span><span class="sxs-lookup"><span data-stu-id="ebc13-121">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="ebc13-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebc13-122">Windows Vista</span></span>    | <span data-ttu-id="ebc13-123">NT60</span><span class="sxs-lookup"><span data-stu-id="ebc13-123">NT60</span></span>          | <span data-ttu-id="ebc13-124">/Oicf/error all/robust/protocol all</span><span class="sxs-lookup"><span data-stu-id="ebc13-124">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="ebc13-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ebc13-125">Windows 7</span></span>        | <span data-ttu-id="ebc13-126">NT61</span><span class="sxs-lookup"><span data-stu-id="ebc13-126">NT61</span></span>          | <span data-ttu-id="ebc13-127">/Oicf/error all/robust/protocol all</span><span class="sxs-lookup"><span data-stu-id="ebc13-127">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="ebc13-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ebc13-128">Windows 8</span></span>        | <span data-ttu-id="ebc13-129">NT62</span><span class="sxs-lookup"><span data-stu-id="ebc13-129">NT62</span></span>          | <span data-ttu-id="ebc13-130">/Oicf/error all/robust/protocol all</span><span class="sxs-lookup"><span data-stu-id="ebc13-130">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="ebc13-131">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ebc13-131">Windows 10</span></span>       | <span data-ttu-id="ebc13-132">NT100</span><span class="sxs-lookup"><span data-stu-id="ebc13-132">NT100</span></span>         | <span data-ttu-id="ebc13-133">/Oicf/error all/robust/protocol all</span><span class="sxs-lookup"><span data-stu-id="ebc13-133">/Oicf /error all /robust /protocol all</span></span> |
 

<span data-ttu-id="ebc13-134">為了確保在 **/target** 參數所指定的系統上執行存根，MIDL 會在有較新版本的 Windows 上提供的功能存在時發出錯誤。</span><span class="sxs-lookup"><span data-stu-id="ebc13-134">To ensure a stub runs on the system specified by the **/target** switch, MIDL issues an error when a feature available only on a more recent version of Windows is present.</span></span> <span data-ttu-id="ebc13-135">下表指定啟用此功能所需的最小 **/target** 層級。</span><span class="sxs-lookup"><span data-stu-id="ebc13-135">The following table specifies the minimum **/target** level required to enable the feature.</span></span> <span data-ttu-id="ebc13-136">較高的目標層級包含來自較低目標層級的所有功能。</span><span class="sxs-lookup"><span data-stu-id="ebc13-136">Higher target levels include all features from lower target levels.</span></span>



| <span data-ttu-id="ebc13-137">至少需要/target 層級</span><span class="sxs-lookup"><span data-stu-id="ebc13-137">Minimum required /target level</span></span> | <span data-ttu-id="ebc13-138">功能</span><span class="sxs-lookup"><span data-stu-id="ebc13-138">Features</span></span>                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc13-139">NT50</span><span class="sxs-lookup"><span data-stu-id="ebc13-139">NT50</span></span>                           | <span data-ttu-id="ebc13-140">/robust</span><span class="sxs-lookup"><span data-stu-id="ebc13-140">/robust</span></span><br/> <span data-ttu-id="ebc13-141">\[message\]</span><span class="sxs-lookup"><span data-stu-id="ebc13-141">\[message\]</span></span><br/> <span data-ttu-id="ebc13-142">\[async\]</span><span class="sxs-lookup"><span data-stu-id="ebc13-142">\[async\]</span></span><br/> <span data-ttu-id="ebc13-143">\[非同步 \_ uuid\]</span><span class="sxs-lookup"><span data-stu-id="ebc13-143">\[async\_uuid\]</span></span><br/> <span data-ttu-id="ebc13-144">\[\]在/Oicf 模式中通知</span><span class="sxs-lookup"><span data-stu-id="ebc13-144">\[notify\] in /Oicf mode</span></span><br/> <span data-ttu-id="ebc13-145">\[\] \[ \] 在/Oicf 模式中進行編碼或解碼</span><span class="sxs-lookup"><span data-stu-id="ebc13-145">\[encode\] or \[decode\] in /Oicf mode</span></span><br/>                   |
| <span data-ttu-id="ebc13-146">NT51</span><span class="sxs-lookup"><span data-stu-id="ebc13-146">NT51</span></span>                           | <span data-ttu-id="ebc13-147">/protocol 64 位支援</span><span class="sxs-lookup"><span data-stu-id="ebc13-147">/protocol 64-bit support</span></span><br/> <span data-ttu-id="ebc13-148">\[部分 \_ 忽略\]</span><span class="sxs-lookup"><span data-stu-id="ebc13-148">\[partial\_ignore\]</span></span><br/> <span data-ttu-id="ebc13-149">\[強制 \_ 配置\]</span><span class="sxs-lookup"><span data-stu-id="ebc13-149">\[force\_allocate\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="ebc13-150">NT60</span><span class="sxs-lookup"><span data-stu-id="ebc13-150">NT60</span></span>                           | <span data-ttu-id="ebc13-151">強制複雜結構封送處理</span><span class="sxs-lookup"><span data-stu-id="ebc13-151">Forced complex structure marshalling</span></span><br/> <span data-ttu-id="ebc13-152">陣列或結構中的內容控制碼</span><span class="sxs-lookup"><span data-stu-id="ebc13-152">Context handles in an array or structure</span></span><br/> <span data-ttu-id="ebc13-153">\[\]可變大小字串的範圍支援</span><span class="sxs-lookup"><span data-stu-id="ebc13-153">\[range\] support for unsized strings</span></span><br/> <span data-ttu-id="ebc13-154">\[輸入 \_ strict \_ 內容 \_ 控制碼\]</span><span class="sxs-lookup"><span data-stu-id="ebc13-154">\[type\_strict\_context\_handle\]</span></span><br/> |
| <span data-ttu-id="ebc13-155">NT61</span><span class="sxs-lookup"><span data-stu-id="ebc13-155">NT61</span></span>                           | <span data-ttu-id="ebc13-156">具有小於32方法之介面的直接 COM stub 呼叫需要連結具有 **OLE32.DLL** 的 com 存根。</span><span class="sxs-lookup"><span data-stu-id="ebc13-156">Direct COM stub calls for interfaces with less than 32 methods requires linking COM stubs with **OLE32.DLL**.</span></span><br/>                                                                          |
| <span data-ttu-id="ebc13-157">NT62</span><span class="sxs-lookup"><span data-stu-id="ebc13-157">NT62</span></span>                           | <span data-ttu-id="ebc13-158">ARM 支援</span><span class="sxs-lookup"><span data-stu-id="ebc13-158">ARM support</span></span><br/> <span data-ttu-id="ebc13-159">WinRT 支援</span><span class="sxs-lookup"><span data-stu-id="ebc13-159">WinRT support</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="ebc13-160">NT100</span><span class="sxs-lookup"><span data-stu-id="ebc13-160">NT100</span></span>                          | <span data-ttu-id="ebc13-161">\[system_handle \] 支援</span><span class="sxs-lookup"><span data-stu-id="ebc13-161">\[system_handle\] support</span></span><br /> |


 

## <a name="examples"></a><span data-ttu-id="ebc13-162">範例</span><span class="sxs-lookup"><span data-stu-id="ebc13-162">Examples</span></span>

<span data-ttu-id="ebc13-163">**midl/target NT50**</span><span class="sxs-lookup"><span data-stu-id="ebc13-163">**midl /target NT50**</span></span>

## <a name="see-also"></a><span data-ttu-id="ebc13-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebc13-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc13-165">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="ebc13-165">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="ebc13-166">**/osf**</span><span class="sxs-lookup"><span data-stu-id="ebc13-166">**/osf**</span></span>](-osf.md)
</dt> </dl>
