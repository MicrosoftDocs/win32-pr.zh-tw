---
title: /iid 參數
description: /Iid 參數會指定 COM 介面之介面識別碼檔案的名稱，並覆寫將 \_ i. c 加入至 IDL 檔案名所取得的預設名稱。
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- /iid 參數 MIDL
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373228"
---
# <a name="iid-switch"></a><span data-ttu-id="3ac19-104">/iid 參數</span><span class="sxs-lookup"><span data-stu-id="3ac19-104">/iid switch</span></span>

<span data-ttu-id="3ac19-105">**/Iid** 參數會指定 COM 介面之介面識別碼檔案的名稱，並覆寫將 \_ i. c 加入至 IDL 檔案名所取得的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac19-105">The **/iid** switch specifies the name of the interface identifier file for a COM interface, overriding the default name obtained by adding \_i.c to the IDL file name.</span></span>

``` syntax
midl /iid filename
```

## <a name="switch-options"></a><span data-ttu-id="3ac19-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="3ac19-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="3ac19-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="3ac19-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="3ac19-108">指定介面識別碼檔案名，此名稱會覆寫 COM 介面的預設介面識別碼檔案名。</span><span class="sxs-lookup"><span data-stu-id="3ac19-108">Specifies an interface identifier file name that overrides the default interface identifier file name for a COM interface.</span></span> <span data-ttu-id="3ac19-109">檔案名可以用雙引號括住 ( ") 來防止 shell 解讀特殊字元。</span><span class="sxs-lookup"><span data-stu-id="3ac19-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ac19-110">備註</span><span class="sxs-lookup"><span data-stu-id="3ac19-110">Remarks</span></span>

<span data-ttu-id="3ac19-111">**/Iid** 參數不會影響 RPC 介面。</span><span class="sxs-lookup"><span data-stu-id="3ac19-111">The **/iid** switch does not affect RPC interfaces.</span></span>

<span data-ttu-id="3ac19-112">如果 *filename* 未包含明確路徑，則會將檔案寫入至目前目錄或 [**/out**](-out.md) 參數所指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="3ac19-112">If *filename* does not include an explicit path, the file is written to the current directory or to the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="3ac19-113">*檔案名* 中的明確路徑會覆寫 **/out** 參數規格。</span><span class="sxs-lookup"><span data-stu-id="3ac19-113">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="3ac19-114">範例</span><span class="sxs-lookup"><span data-stu-id="3ac19-114">Examples</span></span>

<span data-ttu-id="3ac19-115">**midl/iid "my \_ iid .c" 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="3ac19-115">**midl /iid "my\_iid.c" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="3ac19-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ac19-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac19-117">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="3ac19-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="3ac19-118">**/header**</span><span class="sxs-lookup"><span data-stu-id="3ac19-118">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="3ac19-119">**/out**</span><span class="sxs-lookup"><span data-stu-id="3ac19-119">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="3ac19-120">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="3ac19-120">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




