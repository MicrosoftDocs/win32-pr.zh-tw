---
title: /U 參數
description: /U 參數會藉由將名稱傳遞到 C 預處理器來移除任何先前的名稱定義，如同由取消定義的指示詞。
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U 參數 MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092375"
---
# <a name="u-switch"></a><span data-ttu-id="6a1b8-104">/U 參數</span><span class="sxs-lookup"><span data-stu-id="6a1b8-104">/U switch</span></span>

<span data-ttu-id="6a1b8-105">**/U** 參數會藉由將名稱傳遞到 C 預處理器來移除任何先前的名稱定義，如同由未 **\# 定義** 的指示詞。</span><span class="sxs-lookup"><span data-stu-id="6a1b8-105">The **/U** switch removes any previous definition of a name by passing the name to the C preprocessor as if by a **\#undefine** directive.</span></span>

``` syntax
midl /U name
```

## <a name="switch-options"></a><span data-ttu-id="6a1b8-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="6a1b8-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="6a1b8-107">*name*</span><span class="sxs-lookup"><span data-stu-id="6a1b8-107">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="6a1b8-108">指定要傳遞到 C 預處理器的定義的名稱，如同由未 **\# 定義** 的指示詞一樣。</span><span class="sxs-lookup"><span data-stu-id="6a1b8-108">Specifies a defined name to be passed to the C preprocessor as if by a **\#undefine** directive.</span></span> <span data-ttu-id="6a1b8-109">名稱是由 C 預處理器預先定義，或由使用者先前定義。</span><span class="sxs-lookup"><span data-stu-id="6a1b8-109">The name is predefined by the C preprocessor or previously defined by the user.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a1b8-110">備註</span><span class="sxs-lookup"><span data-stu-id="6a1b8-110">Remarks</span></span>

<span data-ttu-id="6a1b8-111">命令列中可以使用多個 **/u** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="6a1b8-111">Multiple **/U** directives can be used in a command line.</span></span> <span data-ttu-id="6a1b8-112">**/U** 參數與未定義名稱之間的空格是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6a1b8-112">White space between the **/U** switch and the undefined name is optional.</span></span>

<span data-ttu-id="6a1b8-113">當 [**/cpp \_ cmd**](-cpp-cmd.md) 參數存在且 [**/cpp \_ opt**](-cpp-opt.md) 參數不是時，MIDL 編譯器會串連/cpp cmd 參數所指定的字串 \_ 與 [**/i**](-i.md)、 [**/d**](-d.md)和 **/u** 選項，並使用這個串連的字串來叫用每個 IDL 和 ACF 原始程式檔的 C 預處理器。</span><span class="sxs-lookup"><span data-stu-id="6a1b8-113">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the /cpp\_cmd switch with the [**/I**](-i.md), [**/D**](-d.md), and **/U** options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="6a1b8-114">當指定 MIDL 編譯器參數 **/no \_ cpp** 或 **/cpp \_ OPT** 時，會忽略 midl 編譯器參數 **/u** 。</span><span class="sxs-lookup"><span data-stu-id="6a1b8-114">The MIDL compiler switch **/U** is ignored when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="6a1b8-115">範例</span><span class="sxs-lookup"><span data-stu-id="6a1b8-115">Examples</span></span>

<span data-ttu-id="6a1b8-116">**midl/UUNICODE 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="6a1b8-116">**midl /UUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6a1b8-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a1b8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1b8-118">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="6a1b8-118">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6a1b8-119">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="6a1b8-119">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="6a1b8-120">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="6a1b8-120">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="6a1b8-121">**/D**</span><span class="sxs-lookup"><span data-stu-id="6a1b8-121">**/D**</span></span>](-d.md)
</dt> <dt>

[<span data-ttu-id="6a1b8-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="6a1b8-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="6a1b8-123">**/no \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="6a1b8-123">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




