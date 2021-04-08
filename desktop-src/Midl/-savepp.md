---
title: /savePP 參數
description: 指定/savePP 指示詞時，MIDL 編譯器不會刪除 C/c + + 預處理器的輸出。
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- /savePP 參數 MIDL
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022493"
---
# <a name="savepp-switch"></a><span data-ttu-id="a9a5a-104">/savePP 參數</span><span class="sxs-lookup"><span data-stu-id="a9a5a-104">/savePP switch</span></span>

<span data-ttu-id="a9a5a-105">指定 **/savePP** 指示詞時，MIDL 編譯器不會刪除 C/c + + 預處理器的輸出。</span><span class="sxs-lookup"><span data-stu-id="a9a5a-105">When the **/savePP** directive is specified, the MIDL compiler does not delete the output of the C/C++ preprocessor.</span></span>

``` syntax
midl /savePP
```

## <a name="switch-options"></a><span data-ttu-id="a9a5a-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="a9a5a-106">Switch Options</span></span>

<span data-ttu-id="a9a5a-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a9a5a-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9a5a-108">備註</span><span class="sxs-lookup"><span data-stu-id="a9a5a-108">Remarks</span></span>

<span data-ttu-id="a9a5a-109">此參數可讓開發人員分辨 MIDL 編譯器所剖析的內容，而且對進行調試很有用。</span><span class="sxs-lookup"><span data-stu-id="a9a5a-109">This switch enables developers to discern what is being parsed by the MIDL compiler, and is useful for debugging.</span></span> <span data-ttu-id="a9a5a-110">預處理器的輸出會寫入 TEMP 環境變數所指定之目錄中的一或多個暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="a9a5a-110">The output of the preprocessor is written to one or more temporary files in the directory indicated by the TEMP environment variable.</span></span> <span data-ttu-id="a9a5a-111">輸出檔或檔案的名稱，會遵循中間 .tmp 的命名慣例 \* 。</span><span class="sxs-lookup"><span data-stu-id="a9a5a-111">The name of the output file, or files, follows a naming convention of MID\*.tmp.</span></span> <span data-ttu-id="a9a5a-112">請注意，單一編譯可能會產生數個前置處理的輸入資料流程;這是因為匯入 IDL 檔案（而不是使用 **\# include**）會導致個別的預處理器執行。</span><span class="sxs-lookup"><span data-stu-id="a9a5a-112">Note that a single compile may generate several preprocessed input streams; this is because importing an IDL file, as opposed to using **\#include**, causes a separate preprocessor run.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9a5a-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9a5a-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a5a-114">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="a9a5a-114">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="a9a5a-115">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="a9a5a-115">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="a9a5a-116">/no \_ cpp、/nocpp</span><span class="sxs-lookup"><span data-stu-id="a9a5a-116">/no\_cpp, /nocpp</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




