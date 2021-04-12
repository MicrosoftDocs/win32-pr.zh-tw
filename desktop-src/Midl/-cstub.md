---
title: /cstub 參數
description: /Cstub 參數會指定 RPC 介面的用戶端 stub 檔案名。
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- /cstub 參數 MIDL
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312957"
---
# <a name="cstub-switch"></a><span data-ttu-id="c1249-104">/cstub 參數</span><span class="sxs-lookup"><span data-stu-id="c1249-104">/cstub switch</span></span>

<span data-ttu-id="c1249-105">**/Cstub** 參數會指定 RPC 介面的用戶端 stub 檔案名。</span><span class="sxs-lookup"><span data-stu-id="c1249-105">The **/cstub** switch specifies the name of the client stub file for an RPC interface.</span></span>

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="c1249-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="c1249-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="c1249-107">*stub \_ 檔案名 \_*</span><span class="sxs-lookup"><span data-stu-id="c1249-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="c1249-108">指定覆寫預設用戶端 stub 檔案名的檔案名。</span><span class="sxs-lookup"><span data-stu-id="c1249-108">Specifies a file name that overrides the default client stub file name.</span></span> <span data-ttu-id="c1249-109">檔案名可以用雙引號括住 ( ") 來防止 shell 解讀特殊字元。</span><span class="sxs-lookup"><span data-stu-id="c1249-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1249-110">備註</span><span class="sxs-lookup"><span data-stu-id="c1249-110">Remarks</span></span>

<span data-ttu-id="c1249-111">指定的檔案名會取代預設的檔案名。</span><span class="sxs-lookup"><span data-stu-id="c1249-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="c1249-112">根據預設，檔案名是藉由將副檔名 \_ c. 新增至 IDL 檔案的名稱取得。</span><span class="sxs-lookup"><span data-stu-id="c1249-112">By default, the file name is obtained by adding the extension \_c.c to the name of the IDL file.</span></span> <span data-ttu-id="c1249-113">此參數不會影響 OLE 介面。</span><span class="sxs-lookup"><span data-stu-id="c1249-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="c1249-114">當您匯入檔案時，指定的檔案名只適用于一個存根檔案，也就是對應至命令列上指定之 IDL 檔案的存根檔案。</span><span class="sxs-lookup"><span data-stu-id="c1249-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="c1249-115">如果 *存根 \_ 檔案名 \_* 不包含明確路徑，則會將檔案寫入至目前目錄或 [**/out**](-out.md) 參數所指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="c1249-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="c1249-116">*存根檔案名中的明確 \_ \_* 路徑會覆寫 **/out** 參數規格。</span><span class="sxs-lookup"><span data-stu-id="c1249-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="c1249-117">**/Client** none 參數優先于 **/cstub** 參數。</span><span class="sxs-lookup"><span data-stu-id="c1249-117">The **/client** none switch takes precedence over the **/cstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="c1249-118">範例</span><span class="sxs-lookup"><span data-stu-id="c1249-118">Examples</span></span>

<span data-ttu-id="c1249-119">**midl/cstub my \_ cstub .c 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="c1249-119">**midl /cstub my\_cstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c1249-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1249-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1249-121">**/header**</span><span class="sxs-lookup"><span data-stu-id="c1249-121">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="c1249-122">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="c1249-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c1249-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="c1249-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="c1249-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="c1249-124">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




