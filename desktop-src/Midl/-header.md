---
title: /header 參數
description: /Header 參數會指定標頭檔的名稱。
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- /header 參數 MIDL
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373232"
---
# <a name="header-switch"></a><span data-ttu-id="3c46d-104">/header 參數</span><span class="sxs-lookup"><span data-stu-id="3c46d-104">/header switch</span></span>

<span data-ttu-id="3c46d-105">**/Header** 參數會指定標頭檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c46d-105">The **/header** switch specifies the name of the header file.</span></span>

``` syntax
midl /header filename
```

## <a name="switch-options"></a><span data-ttu-id="3c46d-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="3c46d-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="3c46d-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="3c46d-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="3c46d-108">指定覆寫預設標頭檔名稱的標頭檔名稱。</span><span class="sxs-lookup"><span data-stu-id="3c46d-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="3c46d-109">檔案名可以用雙引號括住 ( ") 來防止 shell 解讀特殊字元。</span><span class="sxs-lookup"><span data-stu-id="3c46d-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c46d-110">備註</span><span class="sxs-lookup"><span data-stu-id="3c46d-110">Remarks</span></span>

<span data-ttu-id="3c46d-111">指定的檔案名會取代預設的檔案名。</span><span class="sxs-lookup"><span data-stu-id="3c46d-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="3c46d-112">預設檔案名的取得方式是將 IDL 副檔名 (取代為副檔名 .h 的 idl) 。</span><span class="sxs-lookup"><span data-stu-id="3c46d-112">The default file name is obtained by replacing the IDL file name extension (usually .idl) with the file name extension .h.</span></span> <span data-ttu-id="3c46d-113">若為 OLE 介面， **/header** 參數會覆寫介面標頭檔案的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="3c46d-113">For OLE interfaces, the **/header** switch overrides the default name of the interface header file.</span></span>

<span data-ttu-id="3c46d-114">當您匯入檔案時，指定的檔案名只適用于一個標頭檔，也就是對應至命令列上指定之 IDL 檔案的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="3c46d-114">When you are importing files, the specified file name applies to only one header file — the header file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="3c46d-115">如果 *filename* 未包含明確路徑，則會將檔案寫入至目前目錄或 [**/out**](-out.md) 參數所指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="3c46d-115">If *filename* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="3c46d-116">*檔案名* 中的明確路徑會覆寫 **/out** 參數規格。</span><span class="sxs-lookup"><span data-stu-id="3c46d-116">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="3c46d-117">範例</span><span class="sxs-lookup"><span data-stu-id="3c46d-117">Examples</span></span>

<span data-ttu-id="3c46d-118">**midl/header "bar. h" 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="3c46d-118">**midl /header "bar.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="3c46d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c46d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c46d-120">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="3c46d-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="3c46d-121">**/h**</span><span class="sxs-lookup"><span data-stu-id="3c46d-121">**/h**</span></span>](-h.md)
</dt> <dt>

[<span data-ttu-id="3c46d-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="3c46d-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="3c46d-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="3c46d-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="3c46d-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="3c46d-124">**/sstub**</span></span>](-sstub.md)
</dt> <dt>

[<span data-ttu-id="3c46d-125">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="3c46d-125">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




