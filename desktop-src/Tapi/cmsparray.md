---
description: CMSPArray 範本會執行隨需成長的智慧陣列。
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: CMSPArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944345"
---
# <a name="cmsparray"></a><span data-ttu-id="27fdb-103">CMSPArray</span><span class="sxs-lookup"><span data-stu-id="27fdb-103">CMSPArray</span></span>

<span data-ttu-id="27fdb-104">CMSPArray 範本會執行隨需成長的智慧陣列。</span><span class="sxs-lookup"><span data-stu-id="27fdb-104">The CMSPArray template implements a smart array that will grow on demand.</span></span> <span data-ttu-id="27fdb-105">它是設計來保存具有單一資料型別的小型陣列。</span><span class="sxs-lookup"><span data-stu-id="27fdb-105">It is designed to hold small arrays with simple data types.</span></span> <span data-ttu-id="27fdb-106">它沒有重要的區段。</span><span class="sxs-lookup"><span data-stu-id="27fdb-106">It doesn't have a critical section.</span></span> <span data-ttu-id="27fdb-107">其唯一的相依性為 **realloc** 和 **memmove**。</span><span class="sxs-lookup"><span data-stu-id="27fdb-107">Its only dependencies are **realloc** and **memmove**.</span></span> <span data-ttu-id="27fdb-108">它是在內部用來保留物件指標的清單。</span><span class="sxs-lookup"><span data-stu-id="27fdb-108">It is used internally to keep lists of object pointers.</span></span> <span data-ttu-id="27fdb-109">它類似于 ATL 的 **CSimpleArray** 執行，但對於初始配置更有效率。</span><span class="sxs-lookup"><span data-stu-id="27fdb-109">It is similar to ATL's **CSimpleArray** implementation, but it is more efficient for initial allocations.</span></span>

<span data-ttu-id="27fdb-110">此範本定義于 MSPutils 中。</span><span class="sxs-lookup"><span data-stu-id="27fdb-110">This template is defined in MSPutils.h.</span></span>

 

 



