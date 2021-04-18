---
title: /sstub 參數
description: /Sstub 參數會指定 RPC 介面的伺服器 stub 檔案名。
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- /sstub 參數 MIDL
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965621"
---
# <a name="sstub-switch"></a><span data-ttu-id="6ef96-104">/sstub 參數</span><span class="sxs-lookup"><span data-stu-id="6ef96-104">/sstub switch</span></span>

<span data-ttu-id="6ef96-105">**/Sstub** 參數會指定 RPC 介面的伺服器 stub 檔案名。</span><span class="sxs-lookup"><span data-stu-id="6ef96-105">The **/sstub** switch specifies the name of the server stub file for an RPC interface.</span></span>

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="6ef96-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="6ef96-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="6ef96-107">*stub \_ 檔案名 \_*</span><span class="sxs-lookup"><span data-stu-id="6ef96-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="6ef96-108">指定覆寫預設伺服器 stub 檔案名的檔案名。</span><span class="sxs-lookup"><span data-stu-id="6ef96-108">Specifies a file name that overrides the default server stub file name.</span></span> <span data-ttu-id="6ef96-109">檔案名可以用雙引號括住 ( ") 來防止 shell 解讀特殊字元。</span><span class="sxs-lookup"><span data-stu-id="6ef96-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ef96-110">備註</span><span class="sxs-lookup"><span data-stu-id="6ef96-110">Remarks</span></span>

<span data-ttu-id="6ef96-111">指定的檔案名會取代預設的檔案名。</span><span class="sxs-lookup"><span data-stu-id="6ef96-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="6ef96-112">根據預設，檔案名是藉由將 \_ S. C 加入至 IDL 檔案的名稱取得。</span><span class="sxs-lookup"><span data-stu-id="6ef96-112">By default, the file name is obtained by adding \_S.C to the name of the IDL file.</span></span> <span data-ttu-id="6ef96-113">此參數不會影響 OLE 介面。</span><span class="sxs-lookup"><span data-stu-id="6ef96-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="6ef96-114">當您匯入檔案時，指定的檔案名只適用于一個存根檔案，也就是對應至命令列上指定之 IDL 檔案的存根檔案。</span><span class="sxs-lookup"><span data-stu-id="6ef96-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="6ef96-115">如果 *存根 \_ 檔案名 \_* 不包含明確路徑，則會將檔案寫入至目前目錄或 [**/out**](-out.md) 參數所指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="6ef96-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="6ef96-116">*存根檔案名中的明確 \_ \_* 路徑會覆寫 **/out** 參數規格。</span><span class="sxs-lookup"><span data-stu-id="6ef96-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="6ef96-117">**/Server** 無參數優先于 **/sstub** 參數。</span><span class="sxs-lookup"><span data-stu-id="6ef96-117">The **/server** none switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="6ef96-118">範例</span><span class="sxs-lookup"><span data-stu-id="6ef96-118">Examples</span></span>

<span data-ttu-id="6ef96-119">**midl/sstub my \_ sstub .c 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="6ef96-119">**midl /sstub my\_sstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6ef96-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ef96-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef96-121">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="6ef96-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6ef96-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="6ef96-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="6ef96-123">**/header**</span><span class="sxs-lookup"><span data-stu-id="6ef96-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="6ef96-124">**/out**</span><span class="sxs-lookup"><span data-stu-id="6ef96-124">**/out**</span></span>](-out.md)
</dt> </dl>

 

 




