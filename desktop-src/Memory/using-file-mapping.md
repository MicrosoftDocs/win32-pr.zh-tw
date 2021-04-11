---
description: 下列範例示範兩個處理常式如何以命名共用記憶體的形式存取現有的檔案。
ms.assetid: 4da527b7-7e40-43b7-b6f4-989b5a7aa096
title: 使用檔案對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a58bb5c9ec6efd856e5267830ab27011cf550b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849012"
---
# <a name="using-file-mapping"></a><span data-ttu-id="ae27a-103">使用檔案對應</span><span class="sxs-lookup"><span data-stu-id="ae27a-103">Using File Mapping</span></span>

<span data-ttu-id="ae27a-104">下列範例示範兩個處理常式如何存取現有的檔案作為命名的共用記憶體：</span><span class="sxs-lookup"><span data-stu-id="ae27a-104">The following examples demonstrate how two processes might access an existing file as named shared memory:</span></span>

-   [<span data-ttu-id="ae27a-105">在檔案中建立視圖</span><span class="sxs-lookup"><span data-stu-id="ae27a-105">Creating a View Within a File</span></span>](creating-a-view-within-a-file.md)
-   [<span data-ttu-id="ae27a-106">建立命名的共用記憶體</span><span class="sxs-lookup"><span data-stu-id="ae27a-106">Creating Named Shared Memory</span></span>](creating-named-shared-memory.md)
-   [<span data-ttu-id="ae27a-107">使用大型頁面建立檔案對應</span><span class="sxs-lookup"><span data-stu-id="ae27a-107">Creating a File Mapping Using Large Pages</span></span>](creating-a-file-mapping-using-large-pages.md)
-   [<span data-ttu-id="ae27a-108">從檔案控制代碼取得檔案名</span><span class="sxs-lookup"><span data-stu-id="ae27a-108">Obtaining a File Name From a File Handle</span></span>](obtaining-a-file-name-from-a-file-handle.md)

<span data-ttu-id="ae27a-109">處理常式必須同步處理其對記憶體的存取。</span><span class="sxs-lookup"><span data-stu-id="ae27a-109">The processes must synchronize their access to the memory.</span></span> <span data-ttu-id="ae27a-110">如需詳細資訊，請參閱 [同步](../sync/synchronization.md)處理。</span><span class="sxs-lookup"><span data-stu-id="ae27a-110">For more information, see [Synchronization](../sync/synchronization.md).</span></span>

 

 
