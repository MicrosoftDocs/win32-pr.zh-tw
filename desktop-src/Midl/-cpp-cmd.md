---
title: /cpp_cmd 參數
description: /Cpp \_ cmd 參數會指定 MIDL 編譯器用來前置處理輸入檔的預處理器。
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd switch MIDL
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678664"
---
# <a name="cpp_cmd-switch"></a><span data-ttu-id="980e6-104">/cpp \_ cmd 參數</span><span class="sxs-lookup"><span data-stu-id="980e6-104">/cpp\_cmd switch</span></span>

<span data-ttu-id="980e6-105">**/Cpp \_ cmd** 參數會指定 MIDL 編譯器用來前置處理輸入檔的預處理器。</span><span class="sxs-lookup"><span data-stu-id="980e6-105">The **/cpp\_cmd** switch specifies the preprocessor that the MIDL compiler uses to preprocess input files.</span></span>

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a><span data-ttu-id="980e6-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="980e6-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="980e6-107">*C \_ 預處理器 \_ 二進位檔*</span><span class="sxs-lookup"><span data-stu-id="980e6-107">*C\_preprocessor\_binary*</span></span> 
</dt> <dd>

<span data-ttu-id="980e6-108">指定叫用預處理器的命令。</span><span class="sxs-lookup"><span data-stu-id="980e6-108">Specifies the command that invokes the preprocessor.</span></span> <span data-ttu-id="980e6-109">此命令可讓開發人員覆寫預設的預處理器。</span><span class="sxs-lookup"><span data-stu-id="980e6-109">This command allows developers to override the default preprocessor.</span></span> <span data-ttu-id="980e6-110">根據預設，MIDL 會從組建電腦的組建環境叫用 Microsoft C/c + + 編譯器。</span><span class="sxs-lookup"><span data-stu-id="980e6-110">By default, MIDL invokes the Microsoft C/C++ compiler from the build machine's build environment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="980e6-111">備註</span><span class="sxs-lookup"><span data-stu-id="980e6-111">Remarks</span></span>

<span data-ttu-id="980e6-112">參數的 *C \_ 預處理器 \_ 二進位* 引數可以指定完整路徑; exe 尾碼和引號是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="980e6-112">The *C\_preprocessor\_binary* argument to the switch may specify the full path; the exe suffix and quotes are optional.</span></span> <span data-ttu-id="980e6-113">一般情況下，開發人員會使用參數來選擇特定版本的 Microsoft C/c + + 預處理器或組建環境中的對等專案。</span><span class="sxs-lookup"><span data-stu-id="980e6-113">Typically, developers use the switch to choose a particular version of the Microsoft C/C++ preprocessor or equivalent in the build environment.</span></span> <span data-ttu-id="980e6-114">在此情況下，不需要搭配 **/cpp \_ cmd** 使用 [**/cpp \_ opt**](-cpp-opt.md)參數。</span><span class="sxs-lookup"><span data-stu-id="980e6-114">In this case, it is not necessary to use the [**/cpp\_opt**](-cpp-opt.md) switch with **/cpp\_cmd**.</span></span>

<span data-ttu-id="980e6-115">使用非 Microsoft 預處理器時，尤其是當指定的預處理器未將輸出導向至 stdout 時，必須指定將輸出重新導向至 stdout 的 C 編譯器參數，做為 MIDL 編譯器 [**/cpp \_ opt**](-cpp-opt.md) 參數的一部分。</span><span class="sxs-lookup"><span data-stu-id="980e6-115">When using a non-Microsoft preprocessor, especially when the specified preprocessor does not direct its output to stdout, the C compiler switch that redirects output to stdout as part of the MIDL compiler [**/cpp\_opt**](-cpp-opt.md) switch must be specified.</span></span> <span data-ttu-id="980e6-116">如需詳細資料，請參閱[C-預處理器的 MIDL 需求](c-preprocessor-requirements-for-midl.md)</span><span class="sxs-lookup"><span data-stu-id="980e6-116">See [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for details</span></span>

<span data-ttu-id="980e6-117">預處理器是透過 **/cpp \_ cmd**、 [**/cpp \_ opt**](-cpp-opt.md)、 [**/d**](-d.md)、 [**/i**](-i.md)和 [**/u**](-u.md) 參數提供給 MIDL 編譯器的資訊所組成的命令字串來叫用。</span><span class="sxs-lookup"><span data-stu-id="980e6-117">The preprocessor is invoked by a command string that is formed from the information provided to the MIDL compiler by **/cpp\_cmd**, [**/cpp\_opt**](-cpp-opt.md), [**/D**](-d.md), [**/I**](-i.md), and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="980e6-118">下表摘要說明如何針對 **/cpp \_ cmd** 和 **/cpp \_ opt** 參數的每個組合來建立命令字串。</span><span class="sxs-lookup"><span data-stu-id="980e6-118">The following table summarizes how the command string is constructed for each combination of **/cpp\_cmd** and **/cpp\_opt** switches.</span></span>

<span data-ttu-id="980e6-119">未指定 **/cpp \_ cmd** 參數時，MIDL 編譯器會叫用 Microsoft C/c + + 編譯器。</span><span class="sxs-lookup"><span data-stu-id="980e6-119">When the **/cpp\_cmd** switch is not specified, the MIDL compiler invokes the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="980e6-120">MIDL 使用在組建環境中找到的 Cl.exe 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="980e6-120">MIDL uses a Cl.exe binary found in the build environment.</span></span>

<span data-ttu-id="980e6-121">當 [**/cpp \_ opt**](-cpp-opt.md) 參數不存在時，midl 編譯器會串連 **/cpp \_ cmd** 參數所指定的字串與 MIDL [**/i**](-i.md)、 [**/d**](-d.md) 和 [**/u**](-u.md) 選項所指定的資訊。</span><span class="sxs-lookup"><span data-stu-id="980e6-121">When the [**/cpp\_opt**](-cpp-opt.md) switch is not present, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the information specified by the MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) options.</span></span> <span data-ttu-id="980e6-122">字串/E 也會串連至 C 編譯器調用字串，表示 C/c + + 編譯器只應執行前置處理。</span><span class="sxs-lookup"><span data-stu-id="980e6-122">The string /E is also concatenated to the C-compiler invocation string to indicate that the C/C++ compiler should perform preprocessing only.</span></span> <span data-ttu-id="980e6-123">已新增 [**/nologo**](-nologo.md) 參數來隱藏 C/c + + 編譯器橫幅。</span><span class="sxs-lookup"><span data-stu-id="980e6-123">The [**/nologo**](-nologo.md) switch is added to suppress the C/C++ compiler banner.</span></span> <span data-ttu-id="980e6-124">MIDL 編譯器會使用串連的字串來叫用最上層 IDL 的 C 預處理器，以及匯入的 IDL 檔案，也會針對任何存在的對應 ACF 檔叫用。</span><span class="sxs-lookup"><span data-stu-id="980e6-124">The MIDL compiler uses the concatenated string to invoke the C preprocessor for top-level IDL as well as imported IDL files, and also for any present, corresponding ACF files.</span></span>

<span data-ttu-id="980e6-125">如果有 [**/cpp \_ opt**](-cpp-opt.md) 參數存在（這應該是目前32位和64位平臺的罕見案例），MIDL 編譯器會將 **/cpp \_ cmd** 參數所指定的字串與 **/cpp \_ opt** 參數所指定的字串串連在一起。</span><span class="sxs-lookup"><span data-stu-id="980e6-125">When the [**/cpp\_opt**](-cpp-opt.md) switch is present, which should be a rare case for the current 32-bit and 64-bit platforms, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the string specified by the **/cpp\_opt** switch.</span></span> <span data-ttu-id="980e6-126">MIDL 編譯器會使用串連的字串來叫用指定的預處理器二進位檔，以取代預設的預處理器。</span><span class="sxs-lookup"><span data-stu-id="980e6-126">The MIDL compiler uses the concatenated string to invoke the indicated preprocessor binary in place of the default preprocessor.</span></span> <span data-ttu-id="980e6-127">當 **/cpp \_ opt** 參數存在時， [**/I**](-i.md)、 [**/D**](-d.md)和 [**/U**](-u.md) 參數指定的 MIDL 編譯器選項和 C 編譯器參數/e 都不會與字串串連。</span><span class="sxs-lookup"><span data-stu-id="980e6-127">When the **/cpp\_opt** switch is present, neither the MIDL compiler options specified by the [**/I**](-i.md), [**/D**](-d.md), and [**/U**](-u.md) switches nor the C compiler switch /E is concatenated with the string.</span></span> <span data-ttu-id="980e6-128">您必須在字串中提供/E 選項或對等專案。</span><span class="sxs-lookup"><span data-stu-id="980e6-128">You must supply the /E option, or equivalent, as part of the string.</span></span>



| <span data-ttu-id="980e6-129">/cpp \_ cmd 存在嗎？</span><span class="sxs-lookup"><span data-stu-id="980e6-129">/cpp\_cmd present?</span></span> | <span data-ttu-id="980e6-130">/cpp \_ opt 存在嗎？</span><span class="sxs-lookup"><span data-stu-id="980e6-130">/cpp\_opt present?</span></span> | <span data-ttu-id="980e6-131">Description</span><span class="sxs-lookup"><span data-stu-id="980e6-131">Description</span></span>                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="980e6-132">無 (預設值)</span><span class="sxs-lookup"><span data-stu-id="980e6-132">No (default)</span></span>       | <span data-ttu-id="980e6-133">無 (預設值)</span><span class="sxs-lookup"><span data-stu-id="980e6-133">No (default)</span></span>       | <span data-ttu-id="980e6-134">使用從 MIDL [**/i**](-i.md)、 [**/d**](-d.md) 和 [**/u**](-u.md) 參數取得的設定，叫用預設的 Microsoft C/c + + 編譯器。</span><span class="sxs-lookup"><span data-stu-id="980e6-134">Invokes the default Microsoft C/C++ compiler with settings obtained from MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="980e6-135">新增預處理器參數/E 和 [**/nologo**](-nologo.md)。</span><span class="sxs-lookup"><span data-stu-id="980e6-135">Adds the preprocessor switches /E and [**/nologo**](-nologo.md).</span></span> |
| <span data-ttu-id="980e6-136">是</span><span class="sxs-lookup"><span data-stu-id="980e6-136">Yes</span></span>                | <span data-ttu-id="980e6-137">否</span><span class="sxs-lookup"><span data-stu-id="980e6-137">No</span></span>                 | <span data-ttu-id="980e6-138">使用與上述相同的參數叫用指定的預處理器二進位檔。</span><span class="sxs-lookup"><span data-stu-id="980e6-138">Invokes the indicated preprocessor binary with the same switches as above.</span></span>                                                                                                                                        |
| <span data-ttu-id="980e6-139">否</span><span class="sxs-lookup"><span data-stu-id="980e6-139">No</span></span>                 | <span data-ttu-id="980e6-140">是</span><span class="sxs-lookup"><span data-stu-id="980e6-140">Yes</span></span>                | <span data-ttu-id="980e6-141">使用指定的選項叫用 Microsoft C 編譯器。</span><span class="sxs-lookup"><span data-stu-id="980e6-141">Invokes the Microsoft C compiler with specified options.</span></span> <span data-ttu-id="980e6-142">不使用 MIDL [**/i**](-i.md)、 [**/d**](-d.md)、 [**/u**](-u.md) 選項。</span><span class="sxs-lookup"><span data-stu-id="980e6-142">Does not use MIDL [**/I**](-i.md), [**/D**](-d.md), [**/U**](-u.md) options.</span></span> <span data-ttu-id="980e6-143">您必須提供/E 作為 [**/cpp \_ opt**](-cpp-opt.md)的一部分。</span><span class="sxs-lookup"><span data-stu-id="980e6-143">You must supply /E as part of [**/cpp\_opt**](-cpp-opt.md).</span></span>             |
| <span data-ttu-id="980e6-144">是</span><span class="sxs-lookup"><span data-stu-id="980e6-144">Yes</span></span>                | <span data-ttu-id="980e6-145">是</span><span class="sxs-lookup"><span data-stu-id="980e6-145">Yes</span></span>                | <span data-ttu-id="980e6-146">只使用指定的選項叫用指定的預處理器二進位檔。</span><span class="sxs-lookup"><span data-stu-id="980e6-146">Invokes the specified preprocessor binary with specified options only.</span></span> <span data-ttu-id="980e6-147">您必須使用引號。</span><span class="sxs-lookup"><span data-stu-id="980e6-147">You must use quotes.</span></span>                                                                                                                       |



 

## <a name="examples"></a><span data-ttu-id="980e6-148">範例</span><span class="sxs-lookup"><span data-stu-id="980e6-148">Examples</span></span>

<span data-ttu-id="980e6-149">**midl/cpp \_ cmd d： \\ nt \\ tools \\ IA64 \\cl.exe/DFLAG = TRUE/Ic： \\ inc. 名稱 .idl**</span><span class="sxs-lookup"><span data-stu-id="980e6-149">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="980e6-150">**midl/cpp \_ cmd "mycpp"/DFLAG = TRUE/Ic： \\ inc. 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="980e6-150">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="980e6-151">**midl/cpp \_ opt "/E/DFLAG = TRUE/Ic： \\ inc." 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="980e6-151">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="980e6-152">**midl/cpp \_ cmd "cl"/cpp \_ opt "/e/DFLAG = TRUE/Ic： \\ inc." 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="980e6-152">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="980e6-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="980e6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980e6-154">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="980e6-154">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="980e6-155">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="980e6-155">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="980e6-156">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="980e6-156">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="980e6-157">**/no \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="980e6-157">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="980e6-158">C-MIDL 的預處理器需求</span><span class="sxs-lookup"><span data-stu-id="980e6-158">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




