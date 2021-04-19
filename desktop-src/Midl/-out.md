---
title: /out 參數
description: /Out 參數會指定 MIDL 編譯器寫入輸出檔的預設目錄。
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- /out 參數 MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966222"
---
# <a name="out-switch"></a><span data-ttu-id="fdf95-104">/out 參數</span><span class="sxs-lookup"><span data-stu-id="fdf95-104">/out switch</span></span>

<span data-ttu-id="fdf95-105">**/Out** 參數會指定 MIDL 編譯器寫入輸出檔的預設目錄。</span><span class="sxs-lookup"><span data-stu-id="fdf95-105">The **/out** switch specifies the default directory where the MIDL compiler writes output files.</span></span>

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a><span data-ttu-id="fdf95-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="fdf95-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="fdf95-107">*路徑規格*</span><span class="sxs-lookup"><span data-stu-id="fdf95-107">*path-specification*</span></span> 
</dt> <dd>

<span data-ttu-id="fdf95-108">指定要在其中產生存根、標頭和交換器檔案之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="fdf95-108">Specifies the path to the directory in which the stub, header, and switch files are generated.</span></span> <span data-ttu-id="fdf95-109">您可以指定磁片磁碟機規格、絕對目錄路徑或兩者。</span><span class="sxs-lookup"><span data-stu-id="fdf95-109">A drive specification, an absolute directory path, or both can be specified.</span></span> <span data-ttu-id="fdf95-110">您可以使用雙引號 ( ") 來明確地括住路徑，以防止 shell 解讀特殊字元。</span><span class="sxs-lookup"><span data-stu-id="fdf95-110">Paths can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdf95-111">備註</span><span class="sxs-lookup"><span data-stu-id="fdf95-111">Remarks</span></span>

<span data-ttu-id="fdf95-112">您可以使用磁碟機號、絕對路徑名稱或兩者來指定輸出目錄。</span><span class="sxs-lookup"><span data-stu-id="fdf95-112">The output directory can be specified with a drive letter, an absolute path name, or both.</span></span> <span data-ttu-id="fdf95-113">**/Out** 選項可以搭配任何啟用個別輸出檔規格的參數使用。</span><span class="sxs-lookup"><span data-stu-id="fdf95-113">The **/out** option can be used with any of the switches that enable individual output file specification.</span></span>

<span data-ttu-id="fdf95-114">未指定 **/out** 參數時，會將檔案寫入至目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="fdf95-114">When the **/out** switch is not specified, files are written to the current directory.</span></span>

<span data-ttu-id="fdf95-115">藉由指定為 [**/cstub**](-cstub.md)、 [**/header**](-header.md)、 [**/proxy**](-proxy.md)或 [**/sstub**](-sstub.md)參數一部分的明確路徑名稱，可覆寫 **/out** 參數指定的預設目錄。</span><span class="sxs-lookup"><span data-stu-id="fdf95-115">The default directory specified by the **/out** switch can be overridden by an explicit path name specified as part of the [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md), or [**/sstub**](-sstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="fdf95-116">範例</span><span class="sxs-lookup"><span data-stu-id="fdf95-116">Examples</span></span>

<span data-ttu-id="fdf95-117">**midl/out c： \\ mydir \\ mysubdir \\ subdir2 更深層的檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="fdf95-117">**midl /out c:\\mydir\\mysubdir\\subdir2 deeper filename.idl**</span></span>

<span data-ttu-id="fdf95-118">**midl/out c： filename .idl**</span><span class="sxs-lookup"><span data-stu-id="fdf95-118">**midl /out c: filename.idl**</span></span>

<span data-ttu-id="fdf95-119">**midl/out \\ mydir \\ mysubdir \\ 另一個檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="fdf95-119">**midl /out \\mydir\\mysubdir\\another filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="fdf95-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdf95-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdf95-121">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="fdf95-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="fdf95-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="fdf95-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="fdf95-123">**/header**</span><span class="sxs-lookup"><span data-stu-id="fdf95-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="fdf95-124">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="fdf95-124">**/proxy**</span></span>](-proxy.md)
</dt> <dt>

[<span data-ttu-id="fdf95-125">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="fdf95-125">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




