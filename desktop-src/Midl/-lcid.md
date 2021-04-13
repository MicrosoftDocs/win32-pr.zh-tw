---
title: /lcid 參數
description: /Lcid MIDL 編譯器選項可讓您在輸入檔、檔案名和目錄路徑中使用國際字元。
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /lcid 參數 MIDL
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312950"
---
# <a name="lcid-switch"></a><span data-ttu-id="af1d3-104">/lcid 參數</span><span class="sxs-lookup"><span data-stu-id="af1d3-104">/lcid switch</span></span>

<span data-ttu-id="af1d3-105">**/Lcid** MIDL 編譯器選項可讓您在輸入檔、檔案名和目錄路徑中使用國際字元。</span><span class="sxs-lookup"><span data-stu-id="af1d3-105">The **/lcid** MIDL compiler option lets you use international characters in your input files, file names, and directory paths.</span></span>

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a><span data-ttu-id="af1d3-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="af1d3-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="af1d3-107">*localeID*</span><span class="sxs-lookup"><span data-stu-id="af1d3-107">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="af1d3-108">指定 Windows 國家語言支援中使用的32位地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="af1d3-108">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="af1d3-109">地區設定識別碼應以 decimal 指定。</span><span class="sxs-lookup"><span data-stu-id="af1d3-109">The locale identifier should be specified in decimal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af1d3-110">備註</span><span class="sxs-lookup"><span data-stu-id="af1d3-110">Remarks</span></span>

<span data-ttu-id="af1d3-111">在輸入檔案中，您可以使用當地語系化的批註、字串、helpstrings 和識別碼。</span><span class="sxs-lookup"><span data-stu-id="af1d3-111">Within the input files, you can use localized comments, strings, helpstrings and identifiers.</span></span> <span data-ttu-id="af1d3-112">尤其是， **/lcid** 參數提供完整的 DBCS 支援，以代表日文、中文和韓文等亞洲語言。</span><span class="sxs-lookup"><span data-stu-id="af1d3-112">In particular, the **/lcid** switch provides full DBCS support, to represent Asian languages such as Japanese, Chinese, and Korean.</span></span>

> [!Note]  
> <span data-ttu-id="af1d3-113">**/Lcid** 參數可搭配 MIDL 版本3.01.75 和更新版本使用。</span><span class="sxs-lookup"><span data-stu-id="af1d3-113">The **/lcid** switch is available with MIDL version 3.01.75 and later.</span></span>

 

## <a name="examples"></a><span data-ttu-id="af1d3-114">範例</span><span class="sxs-lookup"><span data-stu-id="af1d3-114">Examples</span></span>

<span data-ttu-id="af1d3-115">**midl/lcid 1041 iface .idl**</span><span class="sxs-lookup"><span data-stu-id="af1d3-115">**midl /lcid 1041 iface.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="af1d3-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af1d3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af1d3-117">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="af1d3-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="af1d3-118">**Lcid**</span><span class="sxs-lookup"><span data-stu-id="af1d3-118">**lcid**</span></span>](lcid.md)
</dt> </dl>

 

 




