---
title: MIDL Command-Line 參考
description: 本節包含 Microsoft RPC MIDL 編譯器可辨識的每個命令列參數和切換選項的參考資訊。
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Microsoft 介面定義語言 MIDL，參考
- 命令列參考 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1569e29daf8a2976379576a5f1671f5117e7990c
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106969828"
---
# <a name="midl-command-line-reference"></a><span data-ttu-id="e4d0f-105">MIDL Command-Line 參考</span><span class="sxs-lookup"><span data-stu-id="e4d0f-105">MIDL Command-Line Reference</span></span>

<span data-ttu-id="e4d0f-106">本節包含 Microsoft RPC MIDL 編譯器可辨識的每個命令列參數和切換選項的參考資訊。</span><span class="sxs-lookup"><span data-stu-id="e4d0f-106">This section contains reference information for each command-line switch and switch option recognized by the Microsoft RPC MIDL compiler.</span></span> <span data-ttu-id="e4d0f-107">交換器專案會依字母順序排列。</span><span class="sxs-lookup"><span data-stu-id="e4d0f-107">Switch entries are arranged in alphabetical order.</span></span> <span data-ttu-id="e4d0f-108">[一般 MIDL 命令列語法](general-midl-command-line-syntax.md) 描述一般命令列語法。</span><span class="sxs-lookup"><span data-stu-id="e4d0f-108">[General MIDL Command-line Syntax](general-midl-command-line-syntax.md) describes the general command-line syntax.</span></span>

<dl>

[<span data-ttu-id="e4d0f-109">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="e4d0f-109">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)  
[<span data-ttu-id="e4d0f-110">回應檔命令</span><span class="sxs-lookup"><span data-stu-id="e4d0f-110">The Response File Command</span></span>](the-response-file-command.md)  
[<span data-ttu-id="e4d0f-111">**/acf**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-111">**/acf**</span></span>](-acf.md)  
[<span data-ttu-id="e4d0f-112">**/align**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-112">**/align**</span></span>](-align.md)  
[<span data-ttu-id="e4d0f-113">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-113">**/amd64**</span></span>](-amd64.md)  
[<span data-ttu-id="e4d0f-114">**/app \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-114">**/app\_config**</span></span>](-app-config.md)  
[<span data-ttu-id="e4d0f-115">/backward \_ 相容性</span><span class="sxs-lookup"><span data-stu-id="e4d0f-115">/backward\_compat</span></span>](-backward-compat.md)  
[<span data-ttu-id="e4d0f-116">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-116">**/c\_ext**</span></span>](-c-ext.md)  
[<span data-ttu-id="e4d0f-117">**/caux**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-117">**/caux**</span></span>](-caux.md)  
[<span data-ttu-id="e4d0f-118">**/char**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-118">**/char**</span></span>](-char.md)  
[<span data-ttu-id="e4d0f-119">**/client**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-119">**/client**</span></span>](-client.md)  
[<span data-ttu-id="e4d0f-120">**/confirm**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-120">**/confirm**</span></span>](-confirm.md)  
[<span data-ttu-id="e4d0f-121">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-121">**/cpp\_cmd**</span></span>](-cpp-cmd.md)  
[<span data-ttu-id="e4d0f-122">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-122">**/cpp\_opt**</span></span>](-cpp-opt.md)  
<span data-ttu-id="e4d0f-123">[**/cstruct_out**](-cstruct-out.md) 
[ **/cstub**](-cstub.md)</span><span class="sxs-lookup"><span data-stu-id="e4d0f-123">[**/cstruct_out**](-cstruct-out.md)
[**/cstub**](-cstub.md)</span></span>  
[<span data-ttu-id="e4d0f-124">**/D**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-124">**/D**</span></span>](-d.md)  
[<span data-ttu-id="e4d0f-125">**/dlldata**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-125">**/dlldata**</span></span>](-dlldata.md)  
[<span data-ttu-id="e4d0f-126">**/env**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-126">**/env**</span></span>](-env.md)  
[<span data-ttu-id="e4d0f-127">**/error**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-127">**/error**</span></span>](-error.md)  
[<span data-ttu-id="e4d0f-128">**/error**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-128">**/error**</span></span>](-error.md)  
[<span data-ttu-id="e4d0f-129">**/h**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-129">**/h**</span></span>](-h.md)  
[<span data-ttu-id="e4d0f-130">**/header**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-130">**/header**</span></span>](-header.md)  
[<span data-ttu-id="e4d0f-131">**/help (/？ )**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-131">**/help (/?)**</span></span>](-help-.md)  
[<span data-ttu-id="e4d0f-132">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-132">**/ia64**</span></span>](-ia64.md)  
[<span data-ttu-id="e4d0f-133">**/I**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-133">**/I**</span></span>](-i.md)  
[<span data-ttu-id="e4d0f-134">**/iid**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-134">**/iid**</span></span>](-iid.md)  
[<span data-ttu-id="e4d0f-135">**/import**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-135">**/import**</span></span>](-import.md)  
[<span data-ttu-id="e4d0f-136">**/lcid**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-136">**/lcid**</span></span>](-lcid.md)  
[<span data-ttu-id="e4d0f-137">**/mktyplib203**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-137">**/mktyplib203**</span></span>](-mktyplib203.md)  
[<span data-ttu-id="e4d0f-138">**/ms \_ ext**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-138">**/ms\_ext**</span></span>](-ms-ext.md)  
[<span data-ttu-id="e4d0f-139">**/ms 聯 \_ 集**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-139">**/ms\_union**</span></span>](-ms-union.md)  
[<span data-ttu-id="e4d0f-140">**/msc \_ ver**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-140">**/msc\_ver**</span></span>](-msc-ver.md)  
[<span data-ttu-id="e4d0f-141">**/new**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-141">**/new**</span></span>](-new.md)  
[<span data-ttu-id="e4d0f-142">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-142">**/newtlb**</span></span>](-newtlb.md)  
[<span data-ttu-id="e4d0f-143">**/no \_ cpp、/nocpp**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-143">**/no\_cpp, /nocpp**</span></span>](-no-cpp-nocpp.md)  
[<span data-ttu-id="e4d0f-144">**/no \_ 預設 \_ epv**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-144">**/no\_default\_epv**</span></span>](-no-default-epv.md)  
[<span data-ttu-id="e4d0f-145">**/no \_ def \_ idir**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-145">**/no\_def\_idir**</span></span>](-no-def-idir.md)  
[<span data-ttu-id="e4d0f-146">**/no \_ 格式 \_ 選擇**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-146">**/no\_format\_opt**</span></span>](-no-format-opt.md)  
[<span data-ttu-id="e4d0f-147">**/no \_ 健全**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-147">**/no\_robust**</span></span>](-no-robust.md)  
[<span data-ttu-id="e4d0f-148">**/no \_ 警告**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-148">**/no\_warn**</span></span>](-no-warn.md)  
[<span data-ttu-id="e4d0f-149">**/nologo**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-149">**/nologo**</span></span>](-nologo.md)  
[<span data-ttu-id="e4d0f-150">**/notlb**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-150">**/notlb**</span></span>](-notlb.md)  
[<span data-ttu-id="e4d0f-151">**/o**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-151">**/o**</span></span>](-o.md)  
[<span data-ttu-id="e4d0f-152">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-152">**/Oi**</span></span>](-oi.md)  
[<span data-ttu-id="e4d0f-153">**/old**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-153">**/old**</span></span>](-old.md)  
[<span data-ttu-id="e4d0f-154">**/oldtlb**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-154">**/oldtlb**</span></span>](-oldtlb.md)  
[<span data-ttu-id="e4d0f-155">**/oldnames**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-155">**/oldnames**</span></span>](-oldnames.md)  
[<span data-ttu-id="e4d0f-156">**/Os**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-156">**/Os**</span></span>](-os.md)  
[<span data-ttu-id="e4d0f-157">**/osf**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-157">**/osf**</span></span>](-osf.md)  
[<span data-ttu-id="e4d0f-158">**/out**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-158">**/out**</span></span>](-out.md)  
[<span data-ttu-id="e4d0f-159">**/pack**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-159">**/pack**</span></span>](-pack.md)  
[<span data-ttu-id="e4d0f-160">**/prefix**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-160">**/prefix**</span></span>](-prefix.md)  
[<span data-ttu-id="e4d0f-161">**/protocol**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-161">**/protocol**</span></span>](-protocol.md)  
[<span data-ttu-id="e4d0f-162">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-162">**/proxy**</span></span>](-proxy.md)  
[<span data-ttu-id="e4d0f-163">**/robust**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-163">**/robust**</span></span>](-robust.md)  
[<span data-ttu-id="e4d0f-164">**/rpcss**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-164">**/rpcss**</span></span>](-rpcss.md)  
[<span data-ttu-id="e4d0f-165">**/sal**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-165">**/sal**</span></span>](-sal.md)  
[<span data-ttu-id="e4d0f-166">**/sal \_ 本機**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-166">**/sal\_local**</span></span>](-sal-local.md)  
[<span data-ttu-id="e4d0f-167">**/saux**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-167">**/saux**</span></span>](-saux.md)  
[<span data-ttu-id="e4d0f-168">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-168">**/savePP**</span></span>](-savepp.md)  
[<span data-ttu-id="e4d0f-169">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-169">**/sstub**</span></span>](-sstub.md)  
[<span data-ttu-id="e4d0f-170">**/syntax \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-170">**/syntax\_check**</span></span>](-syntax-check.md)  
[**/<system>**](-system-.md)  
[<span data-ttu-id="e4d0f-171">**/target**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-171">**/target**</span></span>](-target.md)  
[<span data-ttu-id="e4d0f-172">**/tlb**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-172">**/tlb**</span></span>](-tlb.md)  
[<span data-ttu-id="e4d0f-173">**U**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-173">**/U**</span></span>](-u.md)  
[<span data-ttu-id="e4d0f-174">**/use \_ epv**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-174">**/use\_epv**</span></span>](-use-epv.md)  
[<span data-ttu-id="e4d0f-175">**/version \_ 戳記**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-175">**/version\_stamp**</span></span>](-version-stamp.md)  
[<span data-ttu-id="e4d0f-176">**/W**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-176">**/W**</span></span>](-w.md)  
[<span data-ttu-id="e4d0f-177">**/warn**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-177">**/warn**</span></span>](-warn.md)  
[<span data-ttu-id="e4d0f-178">**/win32**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-178">**/win32**</span></span>](-win32.md)  
[<span data-ttu-id="e4d0f-179">**/win64**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-179">**/win64**</span></span>](-win64.md)  
[<span data-ttu-id="e4d0f-180">**/WX**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-180">**/WX**</span></span>](-wx.md)  
[<span data-ttu-id="e4d0f-181">**/Zp**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-181">**/Zp**</span></span>](-zp.md)  
[<span data-ttu-id="e4d0f-182">**/Zs**</span><span class="sxs-lookup"><span data-stu-id="e4d0f-182">**/Zs**</span></span>](-zs.md)  
</dl>

<span data-ttu-id="e4d0f-183">MIDL 編譯器可以針對不同的平臺和系統版本產生程式碼。</span><span class="sxs-lookup"><span data-stu-id="e4d0f-183">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="e4d0f-184">請參閱 [**/target**](-target.md) 參數，以深入瞭解建議的參數，以及如何產生針對特定版本優化的程式碼。</span><span class="sxs-lookup"><span data-stu-id="e4d0f-184">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a given release.</span></span>

<span data-ttu-id="e4d0f-185">請注意，負號 ( – ) 可能會取代所有 MIDL 命令列參數中以斜線 (/) 開頭的斜線 (/) 。</span><span class="sxs-lookup"><span data-stu-id="e4d0f-185">Note that the minus sign (–) may be substituted for the slash (/) in all MIDL command-line switches that begin with a slash (/).</span></span> <span data-ttu-id="e4d0f-186">下列範例將示範叫用 MIDL 編譯器時的等價。</span><span class="sxs-lookup"><span data-stu-id="e4d0f-186">The following example demonstrates their equivalence when invoking the MIDL compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="e4d0f-187">範例</span><span class="sxs-lookup"><span data-stu-id="e4d0f-187">Examples</span></span>

<span data-ttu-id="e4d0f-188">**midl/acf my \_ acf. acf** *filename \* \* \* .idl*\*</span><span class="sxs-lookup"><span data-stu-id="e4d0f-188">**midl /acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

<span data-ttu-id="e4d0f-189">**midl-acf my \_ acf. acf** *filename \* \* \* .idl*\*</span><span class="sxs-lookup"><span data-stu-id="e4d0f-189">**midl -acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

 

 




