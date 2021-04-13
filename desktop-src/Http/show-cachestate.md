---
title: show cachestate
description: 列出在 HTTP 回應快取中快取的所有資源及其相關聯的屬性，或顯示單一資源和其相關聯的屬性。
ms.assetid: 9daa445e-dd2f-4b73-8938-58df931c015b
keywords:
- 顯示 cachestate HTTP
topic_type:
- apiref
api_name:
- show cachestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088a59eaa92db8ed9e8cbe59075d540507e51535
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313316"
---
# <a name="show-cachestate"></a><span data-ttu-id="ca4f3-104">show cachestate</span><span class="sxs-lookup"><span data-stu-id="ca4f3-104">show cachestate</span></span>

<span data-ttu-id="ca4f3-105">列出在 HTTP 回應快取中快取的所有資源及其相關聯的屬性，或顯示單一資源和其相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="ca4f3-105">Lists all resources and their associated properties that are cached in the HTTP response cache or displays a single resource and its associated properties.</span></span>

``` syntax
show cachestate [[url=]string]
 
```

## <a name="parameters"></a><span data-ttu-id="ca4f3-106">參數</span><span class="sxs-lookup"><span data-stu-id="ca4f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca4f3-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[url = \] ***字串***\]**</span><span class="sxs-lookup"><span data-stu-id="ca4f3-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[url=\]***string***\]**</span></span>
</dt> <dd>

<span data-ttu-id="ca4f3-108">完整 URL。</span><span class="sxs-lookup"><span data-stu-id="ca4f3-108">Fully qualified URL.</span></span> <span data-ttu-id="ca4f3-109">如果未指定，即表示所有 Url。</span><span class="sxs-lookup"><span data-stu-id="ca4f3-109">If unspecified, implies all URLs.</span></span> <span data-ttu-id="ca4f3-110">URL 也可以是已註冊之 Url 的前置詞。</span><span class="sxs-lookup"><span data-stu-id="ca4f3-110">The URL can also be a prefix to registered URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ca4f3-111">範例</span><span class="sxs-lookup"><span data-stu-id="ca4f3-111">Examples</span></span>

<span data-ttu-id="ca4f3-112">**顯示 cachestate url =https://www.contoso.com:80/myresource**</span><span class="sxs-lookup"><span data-stu-id="ca4f3-112">**show cachestate url=https://www.contoso.com:80/myresource**</span></span>

 

 




