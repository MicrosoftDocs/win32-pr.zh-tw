---
title: 字型資源
description: 定義包含字型的檔案。
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- 字型資源功能表與其他資源
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678692"
---
# <a name="font-resource"></a><span data-ttu-id="e2749-104">字型資源</span><span class="sxs-lookup"><span data-stu-id="e2749-104">FONT resource</span></span>

<span data-ttu-id="e2749-105">定義包含字型的檔案。</span><span class="sxs-lookup"><span data-stu-id="e2749-105">Defines a file that contains a font.</span></span>

``` syntax
nameID FONT filename
```

## <a name="parameters"></a><span data-ttu-id="e2749-106">參數</span><span class="sxs-lookup"><span data-stu-id="e2749-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2749-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="e2749-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="e2749-108">識別資源的唯一16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="e2749-108">Unique 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="e2749-109"><span id="filename"></span><span id="FILENAME"></span>*檔案名*</span><span class="sxs-lookup"><span data-stu-id="e2749-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="e2749-110">包含資源的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e2749-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="e2749-111">名稱必須是有效的檔案名;如果檔案不在目前的工作目錄中，它必須是完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e2749-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="e2749-112">路徑應該是加上引號的字串。</span><span class="sxs-lookup"><span data-stu-id="e2749-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="e2749-113">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="e2749-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="e2749-114">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="e2749-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e2749-115">範例</span><span class="sxs-lookup"><span data-stu-id="e2749-115">Examples</span></span>

<span data-ttu-id="e2749-116">下列範例會定義單一字型資源：</span><span class="sxs-lookup"><span data-stu-id="e2749-116">The following example defines a single font resource:</span></span>

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




