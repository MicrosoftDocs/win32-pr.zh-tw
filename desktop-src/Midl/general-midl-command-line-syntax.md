---
title: 一般 MIDL 命令列語法
description: MIDL 編譯器會處理 IDL 檔案和選擇性的應用程式佈建檔， (ACF) 以產生一組輸出檔。
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- 命令列參考 MIDL，一般語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840728"
---
# <a name="general-midl-command-line-syntax"></a><span data-ttu-id="482ae-104">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="482ae-104">General MIDL Command-line Syntax</span></span>

<span data-ttu-id="482ae-105">MIDL 編譯器會處理 IDL 檔案和選擇性的應用程式佈建檔， (ACF) 以產生一組輸出檔。</span><span class="sxs-lookup"><span data-stu-id="482ae-105">The MIDL compiler processes an IDL file and an optional application configuration file (ACF) to generate a set of output files.</span></span> <span data-ttu-id="482ae-106">IDL 檔案的介面屬性清單中指定的屬性，會決定編譯器是否要產生 RPC 介面的來源檔案，或自訂的 OLE 介面。</span><span class="sxs-lookup"><span data-stu-id="482ae-106">The attributes specified in the IDL file's interface attribute list determine whether the compiler generates source files for an RPC interface or for a custom OLE interface.</span></span>

## <a name="switch-options"></a><span data-ttu-id="482ae-107">切換選項</span><span class="sxs-lookup"><span data-stu-id="482ae-107">Switch Options</span></span>

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span data-ttu-id="482ae-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*命令列參數*</span><span class="sxs-lookup"><span data-stu-id="482ae-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*command-line-switch*</span></span>
</dt> <dd>

<span data-ttu-id="482ae-109">指定 MIDL 編譯器命令列參數。</span><span class="sxs-lookup"><span data-stu-id="482ae-109">Specifies MIDL compiler command-line switches.</span></span> <span data-ttu-id="482ae-110">參數可以依任何順序出現。</span><span class="sxs-lookup"><span data-stu-id="482ae-110">Switches can appear in any sequence.</span></span>

</dd> <dt>

<span data-ttu-id="482ae-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*切換-選項*</span><span class="sxs-lookup"><span data-stu-id="482ae-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*switch-options*</span></span>
</dt> <dd>

<span data-ttu-id="482ae-112">指定與每個參數相關聯的選項。</span><span class="sxs-lookup"><span data-stu-id="482ae-112">Specifies options associated with each switch.</span></span> <span data-ttu-id="482ae-113">有效的選項會在每個 MIDL 編譯器參數的參考專案中描述。</span><span class="sxs-lookup"><span data-stu-id="482ae-113">Valid options are described in the reference entry for each MIDL compiler switch.</span></span>

</dd> <dt>

<span data-ttu-id="482ae-114"><span id="filename"></span><span id="FILENAME"></span>*檔案名*</span><span class="sxs-lookup"><span data-stu-id="482ae-114"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="482ae-115">指定 IDL 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="482ae-115">Specifies the name of the IDL file.</span></span> <span data-ttu-id="482ae-116">這個檔案的副檔名通常是 .idl，但它可以有另一個或無。</span><span class="sxs-lookup"><span data-stu-id="482ae-116">This file usually has the extension .idl, but it can have another or none.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="482ae-117">備註</span><span class="sxs-lookup"><span data-stu-id="482ae-117">Remarks</span></span>

<span data-ttu-id="482ae-118">下列清單顯示為名為 idl 的 IDL 檔案所產生之檔案的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="482ae-118">The following lists show the default names of the files generated for an IDL file named Name.idl.</span></span> <span data-ttu-id="482ae-119">您可以使用命令列參數來覆寫這些預設名稱。</span><span class="sxs-lookup"><span data-stu-id="482ae-119">You can use command-line switches to override these default names.</span></span> <span data-ttu-id="482ae-120">請注意，IDL 檔案的名稱可以有 .idl 以外的副檔名，或完全沒有副檔名。</span><span class="sxs-lookup"><span data-stu-id="482ae-120">Note that the name of the IDL file can have an extension other than .idl, or no extension at all.</span></span>

<span data-ttu-id="482ae-121">依預設 (也就是，如果介面屬性清單未包含 [**物件**](object.md) 或 [**本機**](local.md) 屬性) ，則編譯器會為 [RPC 介面](files-generated-for-an-rpc-interface.md)產生下列檔案：</span><span class="sxs-lookup"><span data-stu-id="482ae-121">By default (that is, if the interface attribute list does not contain the [**object**](object.md) or [**local**](local.md) attribute), the compiler generates the following files for an [RPC interface](files-generated-for-an-rpc-interface.md):</span></span>

-   <span data-ttu-id="482ae-122">用戶端 stub (名稱 \_ c.) </span><span class="sxs-lookup"><span data-stu-id="482ae-122">Client stub (name\_c.c)</span></span>
-   <span data-ttu-id="482ae-123">伺服器 stub (名稱 \_ s. c) </span><span class="sxs-lookup"><span data-stu-id="482ae-123">Server stub (name\_s.c)</span></span>
-   <span data-ttu-id="482ae-124">標頭檔 (名稱 .h) </span><span class="sxs-lookup"><span data-stu-id="482ae-124">Header file (name.h)</span></span>

<span data-ttu-id="482ae-125">當 [**物件**](object.md) 屬性出現在 [介面屬性] 清單中時，編譯器會產生 COM 介面的下列檔案：</span><span class="sxs-lookup"><span data-stu-id="482ae-125">When the [**object**](object.md) attribute appears in the interface attribute list, the compiler generates the following files for a COM interface:</span></span>

-   <span data-ttu-id="482ae-126">介面 proxy 檔案 (名稱 \_ p. c) </span><span class="sxs-lookup"><span data-stu-id="482ae-126">Interface proxy file (name\_p.c)</span></span>
-   <span data-ttu-id="482ae-127">介面標頭檔 (名稱 .h) </span><span class="sxs-lookup"><span data-stu-id="482ae-127">Interface header file (name.h)</span></span>
-   <span data-ttu-id="482ae-128">介面 UUID 檔案 (名稱 \_ I .c) </span><span class="sxs-lookup"><span data-stu-id="482ae-128">Interface UUID file (name\_I.c)</span></span>

<span data-ttu-id="482ae-129">當 [**本機**](local.md) 屬性出現在介面屬性清單中時，編譯器只會產生介面標頭檔名稱 .h。</span><span class="sxs-lookup"><span data-stu-id="482ae-129">When the [**local**](local.md) attribute appears in the interface attribute list, the compiler generates only the interface header file, Name.h.</span></span>

<span data-ttu-id="482ae-130">Microsoft RPC 提供的 MIDL 編譯器會視需要叫用 C 預處理器來處理 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="482ae-130">The MIDL compiler provided with Microsoft RPC invokes the C preprocessor as needed to process the IDL file.</span></span> <span data-ttu-id="482ae-131">它不會自動叫用 C 編譯器來編譯產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="482ae-131">It does not automatically invoke the C compiler to compile generated files.</span></span>

> [!Note]  
> <span data-ttu-id="482ae-132">Microsoft RPC 提供的 MIDL 編譯器所使用的命令列語法與 DCE IDL 編譯器不同。</span><span class="sxs-lookup"><span data-stu-id="482ae-132">The MIDL compiler provided with Microsoft RPC uses a different command-line syntax than the DCE IDL compiler.</span></span>

 

<span data-ttu-id="482ae-133">MIDL 編譯器會將 [**/env**](-env.md)、 [**/server**](-server.md)、 [**/sstub**](-sstub.md)和 [**/out**](-out.md) 切換為伺服器 stub 檔案。</span><span class="sxs-lookup"><span data-stu-id="482ae-133">The MIDL compiler switches [**/env**](-env.md), [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

<span data-ttu-id="482ae-134">從 MIDL 版本6.0.359 開始，MIDL 編譯器的預設命令列選項是 [**/Oicf**](-oi.md)- [**/robust**](-robust.md)。</span><span class="sxs-lookup"><span data-stu-id="482ae-134">Starting with MIDL version 6.0.359, the default command line option for the MIDL compiler is [**/Oicf**](-oi.md)Â  [**/robust**](-robust.md).</span></span> <span data-ttu-id="482ae-135">若要停用/robust，請指定 [**/no \_ 健全**](-no-robust.md) 的選項。</span><span class="sxs-lookup"><span data-stu-id="482ae-135">To disable /robust, specify the [**/no\_robust**](-no-robust.md) option.</span></span>

## <a name="the-header-file"></a><span data-ttu-id="482ae-136">標頭檔</span><span class="sxs-lookup"><span data-stu-id="482ae-136">The Header File</span></span>

<span data-ttu-id="482ae-137">標頭檔包含 IDL 檔案中宣告之所有資料類型和作業的定義。</span><span class="sxs-lookup"><span data-stu-id="482ae-137">The header file contains definitions of all the data types and operations declared in the IDL file.</span></span> <span data-ttu-id="482ae-138">所有呼叫已定義作業的應用程式模組都必須包含標頭檔、執行定義的作業，或操作已定義的類型。</span><span class="sxs-lookup"><span data-stu-id="482ae-138">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="482ae-139">MIDL 編譯器參數 [**/header**](-header.md) 和 [**/out**](-out.md) 會影響標頭檔。</span><span class="sxs-lookup"><span data-stu-id="482ae-139">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




