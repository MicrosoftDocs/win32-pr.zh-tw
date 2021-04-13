---
title: /client 參數
description: /Client 參數會指示 MIDL 編譯器產生 RPC 介面的用戶端 C 來源檔案。
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- /client 參數 MIDL
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312962"
---
# <a name="client-switch"></a><span data-ttu-id="6fefe-104">/client 參數</span><span class="sxs-lookup"><span data-stu-id="6fefe-104">/client switch</span></span>

<span data-ttu-id="6fefe-105">**/Client** 參數會指示 MIDL 編譯器產生 RPC 介面的用戶端 C 來源檔案。</span><span class="sxs-lookup"><span data-stu-id="6fefe-105">The **/client** switch directs the MIDL compiler to generate client-side C source files for an RPC interface.</span></span>

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="6fefe-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="6fefe-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="6fefe-107"><span id="stub"></span><span id="STUB"></span>stub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="6fefe-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="6fefe-108">產生用戶端檔案。</span><span class="sxs-lookup"><span data-stu-id="6fefe-108">Generates the client-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="6fefe-109"><span id="none"></span><span id="NONE"></span>無 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="6fefe-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="6fefe-110">不會產生任何用戶端檔案。</span><span class="sxs-lookup"><span data-stu-id="6fefe-110">Does not generate any client-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fefe-111">備註</span><span class="sxs-lookup"><span data-stu-id="6fefe-111">Remarks</span></span>

<span data-ttu-id="6fefe-112">未指定 **/client** 參數時，MIDL 編譯器會產生用戶端存根檔案。</span><span class="sxs-lookup"><span data-stu-id="6fefe-112">When the **/client** switch is not specified, the MIDL compiler generates the client stub file.</span></span> <span data-ttu-id="6fefe-113">此參數不會影響 OLE 介面。</span><span class="sxs-lookup"><span data-stu-id="6fefe-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="6fefe-114">**/Client** 參數優先于 [**/cstub**](-cstub.md)參數。</span><span class="sxs-lookup"><span data-stu-id="6fefe-114">The **/client** switch takes precedence over the [**/cstub**](-cstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="6fefe-115">範例</span><span class="sxs-lookup"><span data-stu-id="6fefe-115">Examples</span></span>

<span data-ttu-id="6fefe-116">**midl/client 無檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="6fefe-116">**midl /client none filename.idl**</span></span>

<span data-ttu-id="6fefe-117">**midl/client stub 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="6fefe-117">**midl /client stub filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6fefe-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6fefe-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fefe-119">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="6fefe-119">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="6fefe-120">**/server**</span><span class="sxs-lookup"><span data-stu-id="6fefe-120">**/server**</span></span>](-server.md)
</dt> <dt>

[<span data-ttu-id="6fefe-121">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="6fefe-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




