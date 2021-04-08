---
title: /server 參數
description: /Server 參數會導向 MIDL 編譯器，以產生 RPC 介面的伺服器端 C 來源檔案。
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- /server 參數 MIDL
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022492"
---
# <a name="server-switch"></a><span data-ttu-id="04bc9-104">/server 參數</span><span class="sxs-lookup"><span data-stu-id="04bc9-104">/server switch</span></span>

<span data-ttu-id="04bc9-105">**/Server** 參數會導向 MIDL 編譯器，以產生 RPC 介面的伺服器端 C 來源檔案。</span><span class="sxs-lookup"><span data-stu-id="04bc9-105">The **/server** switch directs the MIDL compiler to generate server-side C source files for an RPC interface.</span></span>

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="04bc9-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="04bc9-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="04bc9-107"><span id="stub"></span><span id="STUB"></span>stub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="04bc9-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="04bc9-108">產生伺服器端檔案。</span><span class="sxs-lookup"><span data-stu-id="04bc9-108">Generates the server-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="04bc9-109"><span id="none"></span><span id="NONE"></span>無 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="04bc9-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="04bc9-110">不會產生伺服器端檔案。</span><span class="sxs-lookup"><span data-stu-id="04bc9-110">Does not generate server-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04bc9-111">備註</span><span class="sxs-lookup"><span data-stu-id="04bc9-111">Remarks</span></span>

<span data-ttu-id="04bc9-112">如果未指定 **/server** 參數，MIDL 編譯器會產生伺服器存根檔案。</span><span class="sxs-lookup"><span data-stu-id="04bc9-112">When the **/server** switch is not specified, the MIDL compiler generates the server stub file.</span></span> <span data-ttu-id="04bc9-113">此參數不會影響 OLE 介面。</span><span class="sxs-lookup"><span data-stu-id="04bc9-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="04bc9-114">[ **無** ] 選項不會產生任何檔案。</span><span class="sxs-lookup"><span data-stu-id="04bc9-114">The **none** option causes no files to be generated.</span></span>

<span data-ttu-id="04bc9-115">**/Server** 參數優先于 **/sstub** 參數。</span><span class="sxs-lookup"><span data-stu-id="04bc9-115">The **/server** switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="04bc9-116">範例</span><span class="sxs-lookup"><span data-stu-id="04bc9-116">Examples</span></span>

<span data-ttu-id="04bc9-117">**midl/server 無**</span><span class="sxs-lookup"><span data-stu-id="04bc9-117">**midl /server none**</span></span>

<span data-ttu-id="04bc9-118">**midl/server 存根**</span><span class="sxs-lookup"><span data-stu-id="04bc9-118">**midl /server stub**</span></span>

## <a name="see-also"></a><span data-ttu-id="04bc9-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04bc9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04bc9-120">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="04bc9-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="04bc9-121">**/client**</span><span class="sxs-lookup"><span data-stu-id="04bc9-121">**/client**</span></span>](-client.md)
</dt> <dt>

[<span data-ttu-id="04bc9-122">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="04bc9-122">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




