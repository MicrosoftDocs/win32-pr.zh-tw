---
title: /dlldata 參數
description: /Dlldata 參數是用來指定為 proxy DLL 產生之 dlldata.c 檔的檔案名。 如果未指定/dlldata 參數，則會使用預設檔案名 Dlldata.c。
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- /dlldata 參數 MIDL
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678660"
---
# <a name="dlldata-switch"></a><span data-ttu-id="abb8a-105">/dlldata 參數</span><span class="sxs-lookup"><span data-stu-id="abb8a-105">/dlldata switch</span></span>

<span data-ttu-id="abb8a-106">**/Dlldata** 參數是用來指定為 proxy DLL 產生之 dlldata.c 檔的檔案名。</span><span class="sxs-lookup"><span data-stu-id="abb8a-106">The **/dlldata** switch is used to specify the file name for the generated dlldata file for a proxy DLL.</span></span> <span data-ttu-id="abb8a-107">如果未指定 **/dlldata** 參數，則會使用預設檔案名 dlldata.c。</span><span class="sxs-lookup"><span data-stu-id="abb8a-107">The default file name Dlldata.c is used if the **/dlldata** switch is not specified.</span></span>

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a><span data-ttu-id="abb8a-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="abb8a-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="abb8a-109">*檔案名*</span><span class="sxs-lookup"><span data-stu-id="abb8a-109">*file-name*</span></span> 
</dt> <dd>

<span data-ttu-id="abb8a-110">MIDL 編譯器將為 proxy DLL 產生的 C 原始程式檔名稱。</span><span class="sxs-lookup"><span data-stu-id="abb8a-110">The name of the C source file the MIDL compiler will generate for the proxy DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abb8a-111">備註</span><span class="sxs-lookup"><span data-stu-id="abb8a-111">Remarks</span></span>

<span data-ttu-id="abb8a-112">*檔案名* 所指定的檔案必須連結至 proxy DLL。</span><span class="sxs-lookup"><span data-stu-id="abb8a-112">The file specified by *file-name* must be linked to the proxy DLL.</span></span> <span data-ttu-id="abb8a-113">Dlldata.c 檔案包含 proxy DLL 的 class factory 所需的進入點和資料結構。</span><span class="sxs-lookup"><span data-stu-id="abb8a-113">The dlldata file contains entry points and data structures required by the class factory for the proxy DLL.</span></span> <span data-ttu-id="abb8a-114">這些資料結構會指定 proxy DLL 中包含的物件介面。</span><span class="sxs-lookup"><span data-stu-id="abb8a-114">These data structures specify the object interfaces contained in the proxy DLL.</span></span> <span data-ttu-id="abb8a-115">Dlldata.c 檔案也會指定 proxy DLL 之 class factory 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="abb8a-115">The dlldata file also specifies the class identifier of the class factory for the proxy DLL.</span></span> <span data-ttu-id="abb8a-116">這一律是第一個 proxy 檔案的第一個介面 (IID) 的 UUID，)  (依字母順序排列。</span><span class="sxs-lookup"><span data-stu-id="abb8a-116">This is always the UUID (IID) of the first interface of the first proxy file (by alphabetical order).</span></span>

<span data-ttu-id="abb8a-117">在將進入特定 proxy DLL 的所有 IDL 檔案上叫用 MIDL 時，應指定相同的 dlldata.c 檔。</span><span class="sxs-lookup"><span data-stu-id="abb8a-117">The same dlldata file should be specified when invoking MIDL on all the IDL files that will go into a particular proxy DLL.</span></span> <span data-ttu-id="abb8a-118">Dlldata.c 檔案會在每個 MIDL 編譯期間建立或更新，以累加方式建立將進入 proxy DLL 的介面清單。</span><span class="sxs-lookup"><span data-stu-id="abb8a-118">The dlldata file is created or updated during each MIDL compilation, incrementally building a list of the interfaces that will go into the proxy DLL.</span></span>

## <a name="examples"></a><span data-ttu-id="abb8a-119">範例</span><span class="sxs-lookup"><span data-stu-id="abb8a-119">Examples</span></span>

<span data-ttu-id="abb8a-120">**midl/dlldata 資料 c。**</span><span class="sxs-lookup"><span data-stu-id="abb8a-120">**midl /dlldata data.c**</span></span>

## <a name="see-also"></a><span data-ttu-id="abb8a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abb8a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb8a-122">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="abb8a-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




