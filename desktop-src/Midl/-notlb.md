---
title: /notlb 參數
description: /Notlb 參數會防止 MIDL 編譯器產生類型程式庫 (TLB) 檔。
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- /notlb 參數 MIDL
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462569"
---
# <a name="notlb-switch"></a><span data-ttu-id="9d30d-104">/notlb 參數</span><span class="sxs-lookup"><span data-stu-id="9d30d-104">/notlb switch</span></span>

<span data-ttu-id="9d30d-105">**/Notlb** 參數會防止 MIDL 編譯器產生類型程式庫 (TLB) 檔。</span><span class="sxs-lookup"><span data-stu-id="9d30d-105">The **/notlb** switch prevents the MIDL compiler from generating a type library (TLB) file.</span></span>

``` syntax
midl /notlb
```

## <a name="switch-options"></a><span data-ttu-id="9d30d-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="9d30d-106">Switch Options</span></span>

<span data-ttu-id="9d30d-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9d30d-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d30d-108">備註</span><span class="sxs-lookup"><span data-stu-id="9d30d-108">Remarks</span></span>

<span data-ttu-id="9d30d-109">根據預設，MIDL 編譯器會在遇到連結 [**庫**](library.md) 語句時產生 TLB 檔案。</span><span class="sxs-lookup"><span data-stu-id="9d30d-109">By default, the MIDL compiler will generate a TLB file whenever it encounters a [**LIBRARY**](library.md) statement.</span></span> <span data-ttu-id="9d30d-110">此參數會覆寫預設行為。</span><span class="sxs-lookup"><span data-stu-id="9d30d-110">This switch overrides the default behavior.</span></span>

<span data-ttu-id="9d30d-111">當指定 **/notlb** 選項時，會如往常般產生所有其他的存根、標頭等等。</span><span class="sxs-lookup"><span data-stu-id="9d30d-111">When the **/notlb** option is specified, all other stubs, headers, etc. are generated as usual.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d30d-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d30d-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d30d-113">**/tlb**</span><span class="sxs-lookup"><span data-stu-id="9d30d-113">**/tlb**</span></span>](-tlb.md)
</dt> </dl>

 

 




