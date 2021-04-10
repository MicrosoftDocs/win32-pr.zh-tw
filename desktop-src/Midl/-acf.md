---
title: /acf 參數
description: /Acf 參數允許使用者提供明確的 ACF 檔案名。 參數也允許在 IDL 和 ACF 檔中使用不同的介面名稱。
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- /acf 參數 MIDL
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932739"
---
# <a name="acf-switch"></a><span data-ttu-id="d7c07-105">/acf 參數</span><span class="sxs-lookup"><span data-stu-id="d7c07-105">/acf switch</span></span>

<span data-ttu-id="d7c07-106">**/Acf** 參數允許使用者提供明確的 acf 檔案名。</span><span class="sxs-lookup"><span data-stu-id="d7c07-106">The **/acf** switch allows the user to supply an explicit ACF file name.</span></span> <span data-ttu-id="d7c07-107">參數也允許在 IDL 和 ACF 檔中使用不同的介面名稱。</span><span class="sxs-lookup"><span data-stu-id="d7c07-107">The switch also allows the use of different interface names in the IDL and ACF files.</span></span>

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a><span data-ttu-id="d7c07-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="d7c07-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="d7c07-109">*acf \_ 檔案名*</span><span class="sxs-lookup"><span data-stu-id="d7c07-109">*acf\_filename*</span></span> 
</dt> <dd>

<span data-ttu-id="d7c07-110">指定 ACF 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7c07-110">Specifies the name of the ACF.</span></span> <span data-ttu-id="d7c07-111">空白字元不一定會出現在 **/acf** 參數和檔案名之間。</span><span class="sxs-lookup"><span data-stu-id="d7c07-111">White space may or may not be present between the **/acf** switch and the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7c07-112">備註</span><span class="sxs-lookup"><span data-stu-id="d7c07-112">Remarks</span></span>

<span data-ttu-id="d7c07-113">根據預設，MIDL 編譯器會藉由將 IDL 副檔名 (（通常是使用 ACF 的) idl 來取代）來建立 ACF 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7c07-113">By default, the MIDL compiler constructs the name of the ACF by replacing the IDL file name extension (usually .idl) with .acf.</span></span> <span data-ttu-id="d7c07-114">當 **/acf** 參數存在時，acf 會從指定的檔案名取得其名稱。</span><span class="sxs-lookup"><span data-stu-id="d7c07-114">When the **/acf** switch is present, the ACF takes its name from the specified file name.</span></span> <span data-ttu-id="d7c07-115">**/Acf** 參數僅適用于 MIDL 編譯器命令列上指定的 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="d7c07-115">The **/acf** switch applies only to the IDL file specified on the MIDL compiler command line.</span></span> <span data-ttu-id="d7c07-116">它並不適用于匯入的檔案。</span><span class="sxs-lookup"><span data-stu-id="d7c07-116">It does not apply to imported files.</span></span>

<span data-ttu-id="d7c07-117">使用 **/acf** 參數時，acf 中的介面名稱不需要與 MIDL 介面名稱相符。</span><span class="sxs-lookup"><span data-stu-id="d7c07-117">When the **/acf** switch is used, the interface name in the ACF need not match the MIDL interface name.</span></span> <span data-ttu-id="d7c07-118">這項功能可讓介面共用 ACF 規格。</span><span class="sxs-lookup"><span data-stu-id="d7c07-118">This feature allows interfaces to share an ACF specification.</span></span>

<span data-ttu-id="d7c07-119">如果未指定 ACF 的絕對路徑，MIDL 編譯器會在目前的目錄中搜尋、由 [**/i**](-i.md) 選項提供的目錄，以及包含路徑中的目錄。</span><span class="sxs-lookup"><span data-stu-id="d7c07-119">When an absolute path to an ACF is not specified, the MIDL compiler searches in the current directory, directories supplied by the [**/I**](-i.md) option, and directories in the INCLUDE path.</span></span>

<span data-ttu-id="d7c07-120">如果找不到 ACF，MIDL 編譯器會假設這個介面沒有 ACF。</span><span class="sxs-lookup"><span data-stu-id="d7c07-120">If the ACF is not found, the MIDL compiler assumes there is no ACF for this interface.</span></span> <span data-ttu-id="d7c07-121">如需目錄順序的詳細資訊，請參閱 [**/i**](-i.md) 和 [**/no \_ def \_ idir**](-no-def-idir.md) 參數的參考專案。</span><span class="sxs-lookup"><span data-stu-id="d7c07-121">For more information about the sequence of directories, see the reference entries for the [**/I**](-i.md) and [**/no\_def\_idir**](-no-def-idir.md) switches.</span></span> <span data-ttu-id="d7c07-122">如需 **/acf** 的相關詳細資訊，請參閱 [) 檔案 (的 IDL 介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="d7c07-122">For more information relating to **/acf**, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d7c07-123">範例</span><span class="sxs-lookup"><span data-stu-id="d7c07-123">Examples</span></span>

<span data-ttu-id="d7c07-124">**midl/acf bar. acf filename .idl**</span><span class="sxs-lookup"><span data-stu-id="d7c07-124">**midl /acf bar.acf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="d7c07-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7c07-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c07-126">**/I**</span><span class="sxs-lookup"><span data-stu-id="d7c07-126">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="d7c07-127">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="d7c07-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d7c07-128">**/no \_ def \_ idir**</span><span class="sxs-lookup"><span data-stu-id="d7c07-128">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




