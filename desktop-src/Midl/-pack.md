---
title: /pack 參數
description: /Pack 參數與/Zp 選項相同。
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- /pack 參數 MIDL
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022594"
---
# <a name="pack-switch"></a><span data-ttu-id="2e91d-104">/pack 參數</span><span class="sxs-lookup"><span data-stu-id="2e91d-104">/pack switch</span></span>

<span data-ttu-id="2e91d-105">**/Pack** 參數與 [**/Zp**](-zp.md)選項相同。</span><span class="sxs-lookup"><span data-stu-id="2e91d-105">The **/pack** switch is the same as the [**/Zp**](-zp.md) option.</span></span>

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a><span data-ttu-id="2e91d-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="2e91d-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="2e91d-107">*封裝 \_ 層級*</span><span class="sxs-lookup"><span data-stu-id="2e91d-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="2e91d-108">指定目標系統中結構的封裝層級。</span><span class="sxs-lookup"><span data-stu-id="2e91d-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="2e91d-109">封裝層級值可以設定為1、2、4或8。</span><span class="sxs-lookup"><span data-stu-id="2e91d-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e91d-110">備註</span><span class="sxs-lookup"><span data-stu-id="2e91d-110">Remarks</span></span>

<span data-ttu-id="2e91d-111">**/Pack** 參數會指定目標系統中結構的封裝層級。</span><span class="sxs-lookup"><span data-stu-id="2e91d-111">The **/pack** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="2e91d-112">封裝層級值會對應到 Microsoft C/c + + 7.0 版編譯器所使用的 [**/Zp**](-zp.md) 選項值。</span><span class="sxs-lookup"><span data-stu-id="2e91d-112">The packing-level value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ version 7.0 compiler.</span></span> <span data-ttu-id="2e91d-113">如需詳細資訊，請參閱 Microsoft C/c + + 程式設計檔。</span><span class="sxs-lookup"><span data-stu-id="2e91d-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="2e91d-114">當您叫用 MIDL 編譯器和 C 編譯器時，請指定相同的封裝層級。</span><span class="sxs-lookup"><span data-stu-id="2e91d-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span> <span data-ttu-id="2e91d-115">未指定 [**/Zp**](-zp.md) 或 **/pack** 參數時，所使用的預設封裝層級在這兩個組建環境中都是8。</span><span class="sxs-lookup"><span data-stu-id="2e91d-115">The default packing level used when neither the [**/Zp**](-zp.md) nor **/pack** switch is specified is 8, in both all build environments.</span></span>

<span data-ttu-id="2e91d-116">如需使用非標準封裝層級的潛在危險討論，請參閱 [**/Zp**](-zp.md) 說明主題。</span><span class="sxs-lookup"><span data-stu-id="2e91d-116">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="2e91d-117">範例</span><span class="sxs-lookup"><span data-stu-id="2e91d-117">Examples</span></span>

<span data-ttu-id="2e91d-118">**midl/pack 2 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="2e91d-118">**midl /pack 2 filename.idl**</span></span>

<span data-ttu-id="2e91d-119">**midl/pack 8 bar .idl**</span><span class="sxs-lookup"><span data-stu-id="2e91d-119">**midl /pack 8 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="2e91d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e91d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e91d-121">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="2e91d-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="2e91d-122">**/env**</span><span class="sxs-lookup"><span data-stu-id="2e91d-122">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="2e91d-123">**/Zp**</span><span class="sxs-lookup"><span data-stu-id="2e91d-123">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




