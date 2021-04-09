---
title: /Zp 參數
description: /Zp 參數與/pack 選項相同。
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- /Zp 參數 MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678307"
---
# <a name="zp-switch"></a><span data-ttu-id="cc49b-104">/Zp 參數</span><span class="sxs-lookup"><span data-stu-id="cc49b-104">/Zp switch</span></span>

<span data-ttu-id="cc49b-105">**/Zp** 參數與 [**/pack**](-pack.md)選項相同。</span><span class="sxs-lookup"><span data-stu-id="cc49b-105">The **/Zp** switch is the same as the [**/pack**](-pack.md) option.</span></span>

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a><span data-ttu-id="cc49b-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="cc49b-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="cc49b-107">*封裝 \_ 層級*</span><span class="sxs-lookup"><span data-stu-id="cc49b-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="cc49b-108">指定目標系統中結構的封裝層級。</span><span class="sxs-lookup"><span data-stu-id="cc49b-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="cc49b-109">封裝層級值可以設定為1、2、4或8。</span><span class="sxs-lookup"><span data-stu-id="cc49b-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc49b-110">備註</span><span class="sxs-lookup"><span data-stu-id="cc49b-110">Remarks</span></span>

<span data-ttu-id="cc49b-111">**/Zp** 參數會指定目標系統中結構的封裝層級。</span><span class="sxs-lookup"><span data-stu-id="cc49b-111">The **/Zp** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="cc49b-112">封裝層級值會對應到 Microsoft C/c + + 編譯器所使用的 **/Zp** 選項值。</span><span class="sxs-lookup"><span data-stu-id="cc49b-112">The packing-level value corresponds to the **/Zp** option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="cc49b-113">如需詳細資訊，請參閱 Microsoft C/c + + 程式設計檔。</span><span class="sxs-lookup"><span data-stu-id="cc49b-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="cc49b-114">當您叫用 MIDL 編譯器和 C 編譯器時，請指定相同的封裝層級。</span><span class="sxs-lookup"><span data-stu-id="cc49b-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="cc49b-115">未指定 **/Zp** 或 [**/pack**](-pack.md) 參數時，所使用的預設封裝層級在所有組建環境中都是8。</span><span class="sxs-lookup"><span data-stu-id="cc49b-115">The default packing level used when neither the **/Zp** nor [**/pack**](-pack.md) switch is specified is 8 in all build environments.</span></span>

> [!Note]  
> <span data-ttu-id="cc49b-116">請勿在 MIPS 或 Alpha 平臺上使用 **/Zp1** 或 **/Zp2** ，而且在16位平臺上請勿使用 **/Zp4** 或 **了/zp8** 。</span><span class="sxs-lookup"><span data-stu-id="cc49b-116">Do not use **/Zp1** or **/Zp2** on MIPS or Alpha platforms and do not use **/Zp4** or **/Zp8** on 16-bit platforms.</span></span> <span data-ttu-id="cc49b-117">視 C 編譯器在執行時間所指派的資料類型和記憶體位置而定，這可能會導致 MIPS 和 Alpha 平臺上發生資料不一致的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="cc49b-117">Depending on the data type and memory location assigned by the C compiler at run time, this can result in a data misalignment exception on MIPS and Alpha platforms.</span></span> <span data-ttu-id="cc49b-118">在 MS-DOS 平臺上，C 編譯器不會確定對齊4或8，因此應用程式可能會終止。</span><span class="sxs-lookup"><span data-stu-id="cc49b-118">On MS-DOS platforms, the C compiler will not ensure the alignment at 4 or 8, and so the application may terminate.</span></span>

 

## <a name="examples"></a><span data-ttu-id="cc49b-119">範例</span><span class="sxs-lookup"><span data-stu-id="cc49b-119">Examples</span></span>

<span data-ttu-id="cc49b-120">**midl/Zp4 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="cc49b-120">**midl /Zp4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="cc49b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc49b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc49b-122">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="cc49b-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="cc49b-123">**/pack**</span><span class="sxs-lookup"><span data-stu-id="cc49b-123">**/pack**</span></span>](-pack.md)
</dt> </dl>

 

 




