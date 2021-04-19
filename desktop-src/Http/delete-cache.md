---
title: delete cache
description: 清除整個 URL 快取，或根據指定的 URL 刪除專案。
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- 刪除快取 HTTP
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "106967873"
---
# <a name="delete-cache"></a><span data-ttu-id="3742b-104">delete cache</span><span class="sxs-lookup"><span data-stu-id="3742b-104">delete cache</span></span>

<span data-ttu-id="3742b-105">清除整個 URL 快取，或根據指定的 URL 刪除專案。</span><span class="sxs-lookup"><span data-stu-id="3742b-105">Flushes the entire URL cache or deletes entries according to the specified URL.</span></span>

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="3742b-106">參數</span><span class="sxs-lookup"><span data-stu-id="3742b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3742b-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url = \] \* \* \* 字串*</span><span class="sxs-lookup"><span data-stu-id="3742b-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="3742b-108">必要。</span><span class="sxs-lookup"><span data-stu-id="3742b-108">Required.</span></span> <span data-ttu-id="3742b-109">指定完整的 URL。</span><span class="sxs-lookup"><span data-stu-id="3742b-109">Specifies the fully qualified URL.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3742b-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive = \] {yes \| 否}**</span><span class="sxs-lookup"><span data-stu-id="3742b-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive=\]{yes\|no}**</span></span>
</dt> <dd>

<span data-ttu-id="3742b-111">如果是，則會移除指定之 URL 下的所有專案。</span><span class="sxs-lookup"><span data-stu-id="3742b-111">If yes, removes all entries under the specified URL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3742b-112">範例</span><span class="sxs-lookup"><span data-stu-id="3742b-112">Examples</span></span>

<span data-ttu-id="3742b-113">**刪除快取 url = https://www.contoso.com:80/myresource/ 遞迴 = 是**</span><span class="sxs-lookup"><span data-stu-id="3742b-113">**delete cache url=https://www.contoso.com:80/myresource/ recursive=yes**</span></span>

 

 




