---
title: /no_def_idir 參數
description: 使用/I 參數指定目錄時，/no \_ def \_ idir 參數會指示 MIDL 編譯器只搜尋以/i 參數指定的目錄。
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir switch MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841468"
---
# <a name="no_def_idir-switch"></a><span data-ttu-id="a64c6-104">/no \_ def \_ idir 參數</span><span class="sxs-lookup"><span data-stu-id="a64c6-104">/no\_def\_idir switch</span></span>

<span data-ttu-id="a64c6-105">使用 [**/i**](-i.md) 參數指定目錄時， **/no \_ def \_ idir** 參數會指示 MIDL 編譯器只搜尋以 **/i** 參數指定的目錄，並忽略目前的目錄以及 INCLUDE 環境變數所指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="a64c6-105">When directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the directories specified with the **/I** switch, ignoring the current directory as well as the directories specified by the INCLUDE environment variable.</span></span>

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a><span data-ttu-id="a64c6-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="a64c6-106">Switch Options</span></span>

<span data-ttu-id="a64c6-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a64c6-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a64c6-108">備註</span><span class="sxs-lookup"><span data-stu-id="a64c6-108">Remarks</span></span>

<span data-ttu-id="a64c6-109">使用 [**/i**](-i.md) 參數指定目錄時， **/no \_ def \_ idir** 參數會指示 MIDL 編譯器只搜尋目前目錄。</span><span class="sxs-lookup"><span data-stu-id="a64c6-109">When no directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="a64c6-110">範例</span><span class="sxs-lookup"><span data-stu-id="a64c6-110">Examples</span></span>

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a><span data-ttu-id="a64c6-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a64c6-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a64c6-112">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="a64c6-112">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="a64c6-113">**/acf**</span><span class="sxs-lookup"><span data-stu-id="a64c6-113">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="a64c6-114">**/I**</span><span class="sxs-lookup"><span data-stu-id="a64c6-114">**/I**</span></span>](-i.md)
</dt> </dl>

 

 




