---
title: /D 參數
description: /D 參數會定義要傳遞給 C 預處理器的名稱和選擇性值，如同由 \ define 指示詞一樣。 命令列中可以使用多個/D 指示詞。
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D 參數 MIDL
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092398"
---
# <a name="d-switch"></a><span data-ttu-id="ec70f-105">/D 參數</span><span class="sxs-lookup"><span data-stu-id="ec70f-105">/D switch</span></span>

<span data-ttu-id="ec70f-106">**/D** 參數會定義要傳遞給 C 預處理器的名稱和選擇性的值，如同由 **\# 定義** 指示詞一樣。</span><span class="sxs-lookup"><span data-stu-id="ec70f-106">The **/D** switch defines a name and an optional value to be passed to the C preprocessor as if by a **\#define** directive.</span></span> <span data-ttu-id="ec70f-107">命令列中可以使用多個 **/d** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="ec70f-107">Multiple **/D** directives can be used in a command line.</span></span>

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a><span data-ttu-id="ec70f-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="ec70f-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="ec70f-109">*name*</span><span class="sxs-lookup"><span data-stu-id="ec70f-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="ec70f-110">指定已定義的名稱，此名稱會在 [**/cpp \_ cmd**](-cpp-cmd.md) 參數存在且未出現 [**/cpp \_ Opt**](-cpp-opt.md) 參數時傳遞給 C 預處理器。</span><span class="sxs-lookup"><span data-stu-id="ec70f-110">Specifies a defined name that is passed to the C preprocessor when the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not present.</span></span>

</dd> <dt>

<span data-ttu-id="ec70f-111">*definition*</span><span class="sxs-lookup"><span data-stu-id="ec70f-111">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="ec70f-112">指定與定義的名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="ec70f-112">Specifies a value associated with the defined name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec70f-113">備註</span><span class="sxs-lookup"><span data-stu-id="ec70f-113">Remarks</span></span>

<span data-ttu-id="ec70f-114">**/D** 參數和定義的名稱之間的空格是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ec70f-114">White space between the **/D** switch and the defined name is optional.</span></span>

<span data-ttu-id="ec70f-115">當 [**/cpp \_ cmd**](-cpp-cmd.md) 參數存在且 [**/cpp \_ opt**](-cpp-opt.md) 參數不是時，MIDL 編譯器會串連 **/cpp \_ cmd** 參數所指定的字串與 [**/i**](-i.md)、 **/d** 和 [**/U**](-u.md) 選項，並使用這個串連的字串來叫用每個 IDL 和 ACF 原始程式檔的 C 預處理器。</span><span class="sxs-lookup"><span data-stu-id="ec70f-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the [**/I**](-i.md), **/D**, and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span>

<span data-ttu-id="ec70f-116">當指定 MIDL 編譯器參數 [/no \_ cpp](-no-cpp-nocpp.md)或 [**/cpp \_ OPT**](-cpp-opt.md)時，會忽略 midl 編譯器參數 **/d** 。</span><span class="sxs-lookup"><span data-stu-id="ec70f-116">The MIDL compiler switch **/D** is ignored when the MIDL compiler switch [/no\_cpp](-no-cpp-nocpp.md) or [**/cpp\_opt**](-cpp-opt.md) is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="ec70f-117">範例</span><span class="sxs-lookup"><span data-stu-id="ec70f-117">Examples</span></span>

<span data-ttu-id="ec70f-118">**midl-DUNICODE filename .idl**</span><span class="sxs-lookup"><span data-stu-id="ec70f-118">**midl -DUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="ec70f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec70f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec70f-120">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="ec70f-120">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="ec70f-121">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="ec70f-121">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="ec70f-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="ec70f-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="ec70f-123">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="ec70f-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="ec70f-124">**/no \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="ec70f-124">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="ec70f-125">**U**</span><span class="sxs-lookup"><span data-stu-id="ec70f-125">**/U**</span></span>](-u.md)
</dt> </dl>

 

 




