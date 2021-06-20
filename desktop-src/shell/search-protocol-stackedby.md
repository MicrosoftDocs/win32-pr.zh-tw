---
description: 瞭解如何在 Windows Shell UI 中使用 stackedby 引數。 這個引數會指定要用來堆疊結果的屬性資料行。
title: " (Windows Shell 的 STACKEDBY 引數) "
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 781ea9f7-3d82-401b-995f-89bad7d47b3f
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bc786e2ae95309b72f82dd3121692793ac2bd3ab
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403581"
---
# <a name="stackedby-argument-the-windows-shell"></a><span data-ttu-id="0e0db-104"> (Windows Shell 的 STACKEDBY 引數) </span><span class="sxs-lookup"><span data-stu-id="0e0db-104">STACKEDBY Argument (The Windows Shell)</span></span>

<span data-ttu-id="0e0db-105">`stackedby`引數會指定要用來堆疊結果的屬性資料行。</span><span class="sxs-lookup"><span data-stu-id="0e0db-105">The `stackedby` argument specifies the property column to stack results by.</span></span> <span data-ttu-id="0e0db-106">您可以從屬性系統將任何有效的屬性堆疊。</span><span class="sxs-lookup"><span data-stu-id="0e0db-106">You can stack by any valid property from the property system.</span></span>

## <a name="example"></a><span data-ttu-id="0e0db-107">範例</span><span class="sxs-lookup"><span data-stu-id="0e0db-107">Example</span></span>


```
search:query=vacation&stackedby=System.Author
```



### <a name="argument-information"></a><span data-ttu-id="0e0db-108">引數資訊</span><span class="sxs-lookup"><span data-stu-id="0e0db-108">Argument Information</span></span>



|                              | <span data-ttu-id="0e0db-109">值</span><span class="sxs-lookup"><span data-stu-id="0e0db-109">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="0e0db-110">**最低作業系統**</span><span class="sxs-lookup"><span data-stu-id="0e0db-110">**Minimum Operating System**</span></span> | <span data-ttu-id="0e0db-111">Windows Vista 包含 Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="0e0db-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



