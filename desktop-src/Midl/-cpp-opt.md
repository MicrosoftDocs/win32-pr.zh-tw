---
title: /cpp_opt 參數
description: /Cpp \_ opt 參數指定要傳遞至 c/c + + 預處理器的選項。
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt switch MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104383405"
---
# <a name="cpp_opt-switch"></a><span data-ttu-id="c6972-104">/cpp \_ opt 參數</span><span class="sxs-lookup"><span data-stu-id="c6972-104">/cpp\_opt switch</span></span>

<span data-ttu-id="c6972-105">**/Cpp \_ opt** 參數指定要傳遞至 c/c + + 預處理器的選項。</span><span class="sxs-lookup"><span data-stu-id="c6972-105">The **/cpp\_opt** switch specifies options to pass to the C/C++ preprocessor.</span></span>

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a><span data-ttu-id="c6972-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="c6972-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="c6972-107">*C \_ 預處理器 \_ 選項*</span><span class="sxs-lookup"><span data-stu-id="c6972-107">*C\_preprocessor\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="c6972-108">指定與叫用預處理器相關聯的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="c6972-108">Specifies command-line option associated with the invoked preprocessor.</span></span> 

<span data-ttu-id="c6972-109">**注意**：針對 Microsoft C/c + + 預處理器，您必須提供 `/E` 參數作為 *C \_ 預處理器 \_ 選項* 字串的一部分。</span><span class="sxs-lookup"><span data-stu-id="c6972-109">**Note**: For the Microsoft C/C++ preprocessors you must supply the `/E` switch as part of the *C\_preprocessor\_option* string.</span></span> 

<span data-ttu-id="c6972-110">使用一個以上的選項時，以及針對空格，都需要引號。</span><span class="sxs-lookup"><span data-stu-id="c6972-110">Quotes are required when more than one option is used, and for spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6972-111">備註</span><span class="sxs-lookup"><span data-stu-id="c6972-111">Remarks</span></span>

<span data-ttu-id="c6972-112">除非有特定原因需要這麼做，否則請勿使用此參數。</span><span class="sxs-lookup"><span data-stu-id="c6972-112">Do not use this switch unless there is a specific reason for doing so.</span></span> <span data-ttu-id="c6972-113">如需有關前置處理的重要資訊，請參閱 [MIDL 的 C 預處理器需求](c-preprocessor-requirements-for-midl.md) 。</span><span class="sxs-lookup"><span data-stu-id="c6972-113">Consult [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for important information regarding preprocessing.</span></span>

<span data-ttu-id="c6972-114">**/Cpp \_ opt** 參數可以搭配或不搭配 [**/cpp \_ cmd**](-cpp-cmd.md)參數使用。</span><span class="sxs-lookup"><span data-stu-id="c6972-114">The **/cpp\_opt** switch can be used with or without the [**/cpp\_cmd**](-cpp-cmd.md) switch.</span></span> <span data-ttu-id="c6972-115">請參閱 **/cpp \_ cmd** ，以取得在任一情況下如何建立預處理器命令列的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c6972-115">Consult **/cpp\_cmd** for details of how the preprocessor command line is constructed in either case.</span></span>

<span data-ttu-id="c6972-116">**/Cpp \_ opt** 參數（如果有指定）必須一律包含，才能 `/E` 正確運作。</span><span class="sxs-lookup"><span data-stu-id="c6972-116">The **/cpp\_opt** switch, if specified, must always include `/E` in order to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="c6972-117">範例</span><span class="sxs-lookup"><span data-stu-id="c6972-117">Examples</span></span>

<span data-ttu-id="c6972-118">**midl/cpp \_ cmd d： \\ nt \\ tools \\ IA64 \\cl.exe/DFLAG = TRUE/Ic： \\ inc. 名稱 .idl**</span><span class="sxs-lookup"><span data-stu-id="c6972-118">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="c6972-119">**midl/cpp \_ cmd "mycpp"/DFLAG = TRUE/Ic： \\ inc. 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="c6972-119">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="c6972-120">**midl/cpp \_ opt "/E/DFLAG = TRUE/Ic： \\ inc." 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="c6972-120">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="c6972-121">**midl/cpp \_ cmd "cl"/cpp \_ opt "/e/DFLAG = TRUE/Ic： \\ inc." 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="c6972-121">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c6972-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6972-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6972-123">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="c6972-123">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="c6972-124">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="c6972-124">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="c6972-125">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="c6972-125">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c6972-126">**/no \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="c6972-126">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="c6972-127">C-MIDL 的預處理器需求</span><span class="sxs-lookup"><span data-stu-id="c6972-127">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




