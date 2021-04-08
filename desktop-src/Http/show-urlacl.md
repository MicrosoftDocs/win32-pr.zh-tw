---
title: show urlacl
description: 列出指定之保留的 URL 或所有保留的 Url 的 Dacl。
ms.assetid: 8428583c-b420-408f-974f-670b6809fa3c
keywords:
- 顯示 urlacl HTTP
topic_type:
- apiref
api_name:
- show urlacl
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86f7856e70a1be327297bb3fd4b892b3bf39789
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "103932769"
---
# <a name="show-urlacl"></a><span data-ttu-id="936af-104">show urlacl</span><span class="sxs-lookup"><span data-stu-id="936af-104">show urlacl</span></span>

<span data-ttu-id="936af-105">列出指定之保留的 URL 或所有保留的 Url 的 Dacl。</span><span class="sxs-lookup"><span data-stu-id="936af-105">Lists DACLs for the specified reserved URL or all reserved URLs.</span></span>

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a><span data-ttu-id="936af-106">參數</span><span class="sxs-lookup"><span data-stu-id="936af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936af-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url = \] \* \* \* 字串*</span><span class="sxs-lookup"><span data-stu-id="936af-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="936af-108">指定完整的 URL。</span><span class="sxs-lookup"><span data-stu-id="936af-108">Specifies the fully qualified URL.</span></span> <span data-ttu-id="936af-109">如果未指定，即表示所有 Url。</span><span class="sxs-lookup"><span data-stu-id="936af-109">If unspecified, implies all URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="936af-110">範例</span><span class="sxs-lookup"><span data-stu-id="936af-110">Examples</span></span>

<span data-ttu-id="936af-111">**顯示 urlacl url =https://+:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="936af-111">**show urlacl url=https://+:80/MyUrl**</span></span>

<span data-ttu-id="936af-112">**顯示 urlacl url =https://www.contoso.com:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="936af-112">**show urlacl url=https://www.contoso.com:80/MyUrl**</span></span>

 

 




