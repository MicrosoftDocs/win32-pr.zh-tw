---
title: /env 參數
description: /Env 參數會選取應用程式執行所在的環境。
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- /env 參數 MIDL
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375052"
---
# <a name="env-switch"></a><span data-ttu-id="1fdcc-104">/env 參數</span><span class="sxs-lookup"><span data-stu-id="1fdcc-104">/env switch</span></span>

<span data-ttu-id="1fdcc-105">**/Env** 參數會選取應用程式執行所在的環境。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-105">The **/env** switch selects the environment in which the application runs.</span></span>

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a><span data-ttu-id="1fdcc-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="1fdcc-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="1fdcc-107"><span id="win32"></span><span id="WIN32"></span>win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1fdcc-107"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1fdcc-108">指示 MIDL 編譯器產生32位環境的存根檔或類型程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-108">Directs the MIDL compiler to generate stub files, or a type library file, for a 32-bit environment.</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="1fdcc-109"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1fdcc-109"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1fdcc-110">指示 MIDL 編譯器為 Intel 架構64位 (IA64) 環境產生存根檔案或類型程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-110">Directs the MIDL compiler to generate stub files, or a type library file, for a Intel Architecture 64-bit (IA64) environment.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="1fdcc-111"><span id="amd64"></span><span id="AMD64"></span>amd64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1fdcc-111"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1fdcc-112">指示 MIDL 編譯器為 Advanced 微型裝置64位 (AMD64) 環境產生存根檔案或類型程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-112">Directs the MIDL compiler to generate stub files, or a type library file, for an Advanced Micro Devices 64-bit (AMD64) environment.</span></span>

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span data-ttu-id="1fdcc-113"><span id="win64"></span><span id="WIN64"></span>win64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1fdcc-113"><span id="win64"></span><span id="WIN64"></span>\*\*\*\*win64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1fdcc-114">與 *ia64* 相同的行為。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-114">Same behavior as *ia64*.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fdcc-115">備註</span><span class="sxs-lookup"><span data-stu-id="1fdcc-115">Remarks</span></span>

<span data-ttu-id="1fdcc-116">**/Env** 參數主要會影響在該環境中用於結構的封裝層級。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-116">The **/env** switch primarily affects the packing level used for structures in that environment.</span></span> <span data-ttu-id="1fdcc-117">請務必為 MIDL 編譯器和 C 編譯器指定相同的封裝層級設定。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-117">Be sure you specify the same packing-level setting for both the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="1fdcc-118">**/Env** 參數會決定封裝層級和其他設定，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1fdcc-118">The **/env** switch determines the packing level and other settings as follows:</span></span>

-   <span data-ttu-id="1fdcc-119">當您指定 **win32** 時，產生的存根會針對所有涉及遠端作業的類型使用 C-編譯器封裝層級8。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-119">When you specify **win32**, generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="1fdcc-120">[**Int**](int.md)資料類型都是32位。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-120">The [**int**](int.md) data types are both 32 bits.</span></span> <span data-ttu-id="1fdcc-121">指標是32位。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-121">Pointers are 32 bits.</span></span>
-   <span data-ttu-id="1fdcc-122">當您指定 **ia64** 或 **AMD64** 時，MIDL 編譯器會以跨編譯器模式執行，表示 (Intel 或 AMD) 64 位平臺。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-122">When you specify **ia64** or **amd64**, the MIDL compiler runs in a cross-compiler mode for the indicated (Intel or AMD) 64-bit platform.</span></span> <span data-ttu-id="1fdcc-123">產生的存根會針對所有涉及遠端作業的類型使用 C 編譯器封裝層級8。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-123">The generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="1fdcc-124">[**Long**](long.md)和 [**int**](int.md)資料類型是32位。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-124">The [**long**](long.md) and [**int**](int.md) data types are 32 bits.</span></span> <span data-ttu-id="1fdcc-125">指標是64位。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-125">Pointers are 64 bits.</span></span>

<span data-ttu-id="1fdcc-126">[**/Align**](-align.md)、 [**/pack**](-pack.md)和 [**/Zp**](-zp.md)參數的優先順序高於 **/env** 設定。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-126">The [**/align**](-align.md), [**/pack**](-pack.md), and [**/Zp**](-zp.md) switches take precedence over the **/env** settings.</span></span>

<span data-ttu-id="1fdcc-127">如需 MIDL 和 RPC 64 位支援的詳細資訊，請參閱 [設計64位相容的介面](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)。</span><span class="sxs-lookup"><span data-stu-id="1fdcc-127">For more information on 64 bit support for MIDL and RPC see [Designing 64-bit-Compatible Interfaces](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span></span>

## <a name="examples"></a><span data-ttu-id="1fdcc-128">範例</span><span class="sxs-lookup"><span data-stu-id="1fdcc-128">Examples</span></span>

<span data-ttu-id="1fdcc-129">**midl/env win32 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="1fdcc-129">**midl /env win32 filename.idl**</span></span>

<span data-ttu-id="1fdcc-130">**midl/env ia64 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="1fdcc-130">**midl /env ia64 filename.idl**</span></span>

<span data-ttu-id="1fdcc-131">**midl/env amd64 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="1fdcc-131">**midl /env amd64 filename.idl**</span></span>

<span data-ttu-id="1fdcc-132">**midl/env win64 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="1fdcc-132">**midl /env win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1fdcc-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fdcc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fdcc-134">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="1fdcc-134">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1fdcc-135">**/pack**</span><span class="sxs-lookup"><span data-stu-id="1fdcc-135">**/pack**</span></span>](-pack.md)
</dt> <dt>

[<span data-ttu-id="1fdcc-136">**/Zp**</span><span class="sxs-lookup"><span data-stu-id="1fdcc-136">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 