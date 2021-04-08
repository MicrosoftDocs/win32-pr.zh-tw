---
title: 效能屬性
description: 在 IDL 檔案中使用下列屬性，以減少存根程式碼的大小或改善效能。
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- IDL MIDL，屬性，效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022087"
---
# <a name="performance-attributes"></a><span data-ttu-id="46ea4-104">效能屬性</span><span class="sxs-lookup"><span data-stu-id="46ea4-104">Performance Attributes</span></span>

<span data-ttu-id="46ea4-105">在 IDL 檔案中使用下列屬性，以減少存根程式碼的大小或改善效能。</span><span class="sxs-lookup"><span data-stu-id="46ea4-105">Use the following attributes in an IDL file to reduce the size of the stub code or otherwise improve performance.</span></span>



| <span data-ttu-id="46ea4-106">屬性</span><span class="sxs-lookup"><span data-stu-id="46ea4-106">Attribute</span></span>                             | <span data-ttu-id="46ea4-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="46ea4-107">Usage</span></span>                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46ea4-108">**忽略**</span><span class="sxs-lookup"><span data-stu-id="46ea4-108">**ignore**</span></span>](ignore.md)              | <span data-ttu-id="46ea4-109">指定包含在結構或等位中的指標，以及指標所指出的物件不會傳送。</span><span class="sxs-lookup"><span data-stu-id="46ea4-109">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span>                        |
| [<span data-ttu-id="46ea4-110">**當地**</span><span class="sxs-lookup"><span data-stu-id="46ea4-110">**local**</span></span>](local.md)                | <span data-ttu-id="46ea4-111">指定應用程式的本機函式，MIDL 不需要產生 stub 程式碼。</span><span class="sxs-lookup"><span data-stu-id="46ea4-111">Designates a function that is local to the application for which MIDL does not need to generate stub code.</span></span>                                           |
| [<span data-ttu-id="46ea4-112">**網路 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="46ea4-112">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="46ea4-113">將資料類型定義為透過網路傳輸的較簡單類型，並可讓您針對該類型執行封送處理和封送處理常式。</span><span class="sxs-lookup"><span data-stu-id="46ea4-113">Defines a data type as a simpler type for transmission over a network and allows you to implement marshaling and unmarshaling routines for the type.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="46ea4-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="46ea4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46ea4-115">記憶體管理 ACF 屬性</span><span class="sxs-lookup"><span data-stu-id="46ea4-115">Memory Management ACF Attributes</span></span>](memory-management-acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="46ea4-116">存根優化 ACF 屬性</span><span class="sxs-lookup"><span data-stu-id="46ea4-116">Stub Optimization ACF Attributes</span></span>](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




