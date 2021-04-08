---
title: C-MIDL 的預處理器需求
description: 此頁面僅適用于具有特定原因的開發人員，以將 Microsoft C/c + + 預處理器取代為 MIDL 所使用的預處理器，或必須指定自訂預處理器參數的開發人員。
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- MIDL 編譯器 MIDL、C-預處理器、需求
- C-預處理器 MIDL，需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932441"
---
# <a name="c-preprocessor-requirements-for-midl"></a><span data-ttu-id="bf963-105">C-MIDL 的預處理器需求</span><span class="sxs-lookup"><span data-stu-id="bf963-105">C-Preprocessor Requirements for MIDL</span></span>

<span data-ttu-id="bf963-106">此頁面僅適用于具有特定原因的開發人員，以將 Microsoft C/c + + 預處理器取代為 MIDL 所使用的預處理器，或必須指定自訂預處理器參數的開發人員。</span><span class="sxs-lookup"><span data-stu-id="bf963-106">This page applies only to developers who have specific reasons to replace the Microsoft C/C++ preprocessor as the preprocessor used by MIDL, or to developers who must specify customized preprocessor switches.</span></span> <span data-ttu-id="bf963-107">MIDL 參數 [**/cpp \_ cmd**](-cpp-cmd.md)、 [**/cpp \_ opt**](-cpp-opt.md)和 [**/no \_ cpp**](-no-cpp-nocpp.md) 可用來覆寫編譯器的預設行為。</span><span class="sxs-lookup"><span data-stu-id="bf963-107">The MIDL switches [**/cpp\_cmd**](-cpp-cmd.md), [**/cpp\_opt**](-cpp-opt.md), and [**/no\_cpp**](-no-cpp-nocpp.md) are used to override the default behavior of the compiler.</span></span> <span data-ttu-id="bf963-108">通常不需要取代 Microsoft C/c + + 預處理器，也不需要指定自訂的預處理器參數。</span><span class="sxs-lookup"><span data-stu-id="bf963-108">There is typically no reason to replace the Microsoft C/C++ preprocessor, nor to specify customized preprocessor switches.</span></span>

<span data-ttu-id="bf963-109">MIDL 編譯器會在 IDL 檔案的初始處理期間使用 C 預處理器。</span><span class="sxs-lookup"><span data-stu-id="bf963-109">The MIDL compiler uses a C preprocessor during initial processing of the IDL file.</span></span> <span data-ttu-id="bf963-110">編譯 IDL 檔案時所使用的組建環境與預設的 C/c + + 預處理器相關聯。</span><span class="sxs-lookup"><span data-stu-id="bf963-110">The build environment used when compiling the IDL files is associated with a default C/C++ preprocessor.</span></span> <span data-ttu-id="bf963-111">如果要使用不同的預處理器，MIDL 編譯器參數 [**/cpp \_ cmd**](-cpp-cmd.md) 會啟用預設 C/c + + 預處理器名稱的覆寫：</span><span class="sxs-lookup"><span data-stu-id="bf963-111">If a different preprocessor is to be used, the MIDL compiler switch [**/cpp\_cmd**](-cpp-cmd.md) enables an override of the default C/C++-preprocessor name:</span></span>

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span data-ttu-id="bf963-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*預處理器 \_ 名稱*</span><span class="sxs-lookup"><span data-stu-id="bf963-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*preprocessor\_name*</span></span>
</dt> <dd>

<span data-ttu-id="bf963-113">指定 MIDL 要使用的預處理器名稱。</span><span class="sxs-lookup"><span data-stu-id="bf963-113">Specifies the name of the preprocessor to be used by MIDL.</span></span> <span data-ttu-id="bf963-114">可以使用二進位檔的路徑來指定。</span><span class="sxs-lookup"><span data-stu-id="bf963-114">May be specified with a path to the binary.</span></span> <span data-ttu-id="bf963-115">.Exe 副檔名是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="bf963-115">The .exe extension is optional.</span></span>

</dd> <dt>

<span data-ttu-id="bf963-116"><span id="filename"></span><span id="FILENAME"></span>*檔案名*</span><span class="sxs-lookup"><span data-stu-id="bf963-116"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="bf963-117">指定 IDL 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf963-117">Specifies the name of the IDL file.</span></span>

</dd> </dl>

-   <span data-ttu-id="bf963-118">MIDL 編譯器預期任何預處理器都必須遵守下列慣例：</span><span class="sxs-lookup"><span data-stu-id="bf963-118">The MIDL compiler expects any preprocessor to observe the following conventions:</span></span>
-   <span data-ttu-id="bf963-119">輸入檔會指定為命令列上的最後一個引數。</span><span class="sxs-lookup"><span data-stu-id="bf963-119">The input file is specified as the last argument on the command line.</span></span>
-   <span data-ttu-id="bf963-120">預處理器必須將輸出重新導向至標準輸出裝置（stdout）。</span><span class="sxs-lookup"><span data-stu-id="bf963-120">The preprocessor must redirect output to the standard output device, stdout.</span></span>
-   <span data-ttu-id="bf963-121">在預處理器的輸出資料流程中，會出現 **\# 行** 指示詞，以啟用更佳的診斷訊息。</span><span class="sxs-lookup"><span data-stu-id="bf963-121">In the output stream of the preprocessor, the **\#line** directives are present to enable better diagnostic messages.</span></span>
-   <span data-ttu-id="bf963-122">Line 指示詞是輸出資料流程中唯一的預處理器指示詞。</span><span class="sxs-lookup"><span data-stu-id="bf963-122">The line directives are the only preprocessor directives in the output stream.</span></span>

<span data-ttu-id="bf963-123">MIDL 假設衍生的預處理器已從編譯器的輸入資料流程中移除所有預處理器指示詞，但在編譯器訊息中指出來源位置所需的行指示詞除外。</span><span class="sxs-lookup"><span data-stu-id="bf963-123">MIDL assumes that the spawned preprocessor has removed all preprocessor directives from the input stream of the compiler, with the exception of the occurrences of the line directive necessary for pinpointing source location in compiler messages.</span></span> <span data-ttu-id="bf963-124">當指出不同于 Microsoft C/c + + 預處理器的預處理器，或使用 [**/cpp \_ opt**](-cpp-opt.md) 參數指定預處理器選項時，必須指定適當的預處理器選項，以在編譯器的輸入資料流程中放置行指示詞。</span><span class="sxs-lookup"><span data-stu-id="bf963-124">When indicating a preprocessor different from the Microsoft C/C++ preprocessor, or when specifying preprocessor options with the [**/cpp\_opt**](-cpp-opt.md) switch, specifying an appropriate preprocessor option that puts the line directives in the input stream of the compiler is required.</span></span> <span data-ttu-id="bf963-125">例如，針對 Microsoft C/c + + 預處理器，必須使用 **/e** 選項：</span><span class="sxs-lookup"><span data-stu-id="bf963-125">For example, for the Microsoft C/C++ preprocessor the **/E** option would have to be used:</span></span>

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

<span data-ttu-id="bf963-126">MIDL 會接受下列其中一種形式的 **\# 行** 指示詞：</span><span class="sxs-lookup"><span data-stu-id="bf963-126">The **\#line** directive is accepted by MIDL in one of the following forms:</span></span>

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

<span data-ttu-id="bf963-127">如需直線指示詞和其他預處理器指示詞的完整說明，請參閱所使用之 C 編譯器的檔。</span><span class="sxs-lookup"><span data-stu-id="bf963-127">For a complete description of the line directive and other preprocessor directives, see the documentation for the C-compiler being used.</span></span>

<span data-ttu-id="bf963-128">MIDL 只接受行預處理器指示詞。</span><span class="sxs-lookup"><span data-stu-id="bf963-128">MIDL accepts only the line preprocessor directive.</span></span> <span data-ttu-id="bf963-129">因此，如果使用 [**/no \_ cpp**](-no-cpp-nocpp.md) 參數，則輸入檔案不能有其他的預處理器指示詞，或者輸入檔必須在叫用 MIDL 之前經過處理。</span><span class="sxs-lookup"><span data-stu-id="bf963-129">Therefore, if the [**/no\_cpp**](-no-cpp-nocpp.md) switch is used, the input file must not have other preprocessor directives, or the input file must have been processed prior to invoking MIDL.</span></span>

<span data-ttu-id="bf963-130">如需詳細資訊，請參閱 [處理 \# IDL 檔案中的定義](dealing-with-defines-in-idl-files-2.md)。</span><span class="sxs-lookup"><span data-stu-id="bf963-130">For more information, see [Dealing with \#defines in IDL Files](dealing-with-defines-in-idl-files-2.md).</span></span>

 

 




