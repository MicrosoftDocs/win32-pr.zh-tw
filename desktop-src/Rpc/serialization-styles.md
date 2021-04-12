---
title: 序列化樣式
description: 您可以使用三種樣式來操作序列化控制碼。
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372397"
---
# <a name="serialization-styles"></a><span data-ttu-id="8a0b2-103">序列化樣式</span><span class="sxs-lookup"><span data-stu-id="8a0b2-103">Serialization Styles</span></span>

<span data-ttu-id="8a0b2-104">您可以使用三種樣式來操作序列化控制碼。</span><span class="sxs-lookup"><span data-stu-id="8a0b2-104">There are three styles you can use to manipulate serialization handles.</span></span> <span data-ttu-id="8a0b2-105">這些警告是：</span><span class="sxs-lookup"><span data-stu-id="8a0b2-105">These are:</span></span>

-   [<span data-ttu-id="8a0b2-106">固定緩衝區序列化</span><span class="sxs-lookup"><span data-stu-id="8a0b2-106">Fixed Buffer Serialization</span></span>](fixed-buffer-serialization.md)
-   [<span data-ttu-id="8a0b2-107">動態緩衝區序列化</span><span class="sxs-lookup"><span data-stu-id="8a0b2-107">Dynamic Buffer Serialization</span></span>](dynamic-buffer-serialization.md)
-   [<span data-ttu-id="8a0b2-108">累加式序列化</span><span class="sxs-lookup"><span data-stu-id="8a0b2-108">Incremental Serialization</span></span>](incremental-serialization.md)

<span data-ttu-id="8a0b2-109">無論您使用何種樣式，都必須建立序列化控制碼、序列化資料，然後釋放控制碼。</span><span class="sxs-lookup"><span data-stu-id="8a0b2-109">Regardless of the style you use, you must create a serialization handle, serialize the data, and then free the handle.</span></span> <span data-ttu-id="8a0b2-110">當程式建立控制碼並定義緩衝區操作的方式時，就會設定樣式。</span><span class="sxs-lookup"><span data-stu-id="8a0b2-110">The style is set when your program creates the handle and defines the way a buffer is manipulated.</span></span> <span data-ttu-id="8a0b2-111">控制碼會維護與三個序列化樣式相關聯的適當內容。</span><span class="sxs-lookup"><span data-stu-id="8a0b2-111">The handle maintains the appropriate context associated with each of the three serialization styles.</span></span>

 

 




