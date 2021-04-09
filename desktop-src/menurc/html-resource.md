---
title: HTML 資源
description: 定義 HTML 檔案。
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- HTML 資源功能表與其他資源
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db6477aed5180ae18b99f53f4ebadf9d0ad0c91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841379"
---
# <a name="html-resource"></a><span data-ttu-id="852d8-104">HTML 資源</span><span class="sxs-lookup"><span data-stu-id="852d8-104">HTML resource</span></span>

<span data-ttu-id="852d8-105">定義 HTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="852d8-105">Defines an HTML file.</span></span>

``` syntax
nameID HTML filename
```

## <a name="parameters"></a><span data-ttu-id="852d8-106">參數</span><span class="sxs-lookup"><span data-stu-id="852d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="852d8-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="852d8-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="852d8-108">識別資源的唯一名稱或16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="852d8-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="852d8-109"><span id="filename"></span><span id="FILENAME"></span>*檔案名*</span><span class="sxs-lookup"><span data-stu-id="852d8-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="852d8-110">HTML 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="852d8-110">The name of the HTML file.</span></span> <span data-ttu-id="852d8-111">如果檔案不在目前的工作目錄中，則它必須是完整或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="852d8-111">It must be a full or relative path if the file is not in the current working directory.</span></span> <span data-ttu-id="852d8-112">路徑應該是加上引號的字串。</span><span class="sxs-lookup"><span data-stu-id="852d8-112">The path should be a quoted string.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="852d8-113">範例</span><span class="sxs-lookup"><span data-stu-id="852d8-113">Examples</span></span>

<span data-ttu-id="852d8-114">下列範例會定義 HTML 資源：</span><span class="sxs-lookup"><span data-stu-id="852d8-114">The following example defines an HTML resource:</span></span>

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




