---
title: /h 參數
description: /H 選項的功能相當於/header 選項。
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h 參數 MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022571"
---
# <a name="h-switch"></a><span data-ttu-id="bead0-104">/h 參數</span><span class="sxs-lookup"><span data-stu-id="bead0-104">/h switch</span></span>

<span data-ttu-id="bead0-105">**/H** 選項的功能相當於 [**/header**](-header.md)選項。</span><span class="sxs-lookup"><span data-stu-id="bead0-105">The **/h** option is functionally equivalent to the [**/header**](-header.md) option.</span></span>

``` syntax
midl /h filename
```

## <a name="switch-options"></a><span data-ttu-id="bead0-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="bead0-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="bead0-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="bead0-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="bead0-108">指定覆寫預設標頭檔名稱的標頭檔名稱。</span><span class="sxs-lookup"><span data-stu-id="bead0-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="bead0-109">檔案名可以用雙引號括住 ( ") 來防止 shell 解讀特殊字元。</span><span class="sxs-lookup"><span data-stu-id="bead0-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bead0-110">備註</span><span class="sxs-lookup"><span data-stu-id="bead0-110">Remarks</span></span>

<span data-ttu-id="bead0-111">**/H** 參數指定 *檔案名* 作為標頭檔的名稱，其中包含 idl 檔案中包含的所有定義，而不含 idl 語法。</span><span class="sxs-lookup"><span data-stu-id="bead0-111">The **/h** switch specifies *filename* as the name for a header file that contains all the definitions contained in the IDL file, without the IDL syntax.</span></span> <span data-ttu-id="bead0-112">這個檔案可以用來做為 C 或 c + + 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="bead0-112">This file can be used as a C or C++ header file.</span></span>

## <a name="examples"></a><span data-ttu-id="bead0-113">範例</span><span class="sxs-lookup"><span data-stu-id="bead0-113">Examples</span></span>

<span data-ttu-id="bead0-114">**midl/h tlibhead .h 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="bead0-114">**midl /h tlibhead.h filename.idl**</span></span>

<span data-ttu-id="bead0-115">**midl/h "midl .h" 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="bead0-115">**midl /h "midl.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="bead0-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bead0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bead0-117">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="bead0-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="bead0-118">**/header**</span><span class="sxs-lookup"><span data-stu-id="bead0-118">**/header**</span></span>](-header.md)
</dt> </dl>

 

 




