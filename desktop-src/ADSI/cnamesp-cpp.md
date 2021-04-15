---
title: CNAMESP.Cpp
description: 在範例提供者元件中，管理範例提供者元件命名空間物件之存留期的程式碼位於 cnamesp .cpp 中。 下表列出支援的方法。
ms.assetid: 2f570f87-d8c3-42b1-b8b9-758905bf4b86
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8204c953218692d91c52fb77d757b5e917264a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507036"
---
# <a name="cnamespcpp"></a><span data-ttu-id="a38e5-104">CNAMESP.Cpp</span><span class="sxs-lookup"><span data-stu-id="a38e5-104">CNAMESP.CPP</span></span>

<span data-ttu-id="a38e5-105">在範例提供者元件中，管理範例提供者元件命名空間物件之存留期的程式碼位於 cnamesp .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="a38e5-105">In the example provider component, code that manages the lifetime of the example provider component namespace object is in cnamesp.cpp.</span></span> <span data-ttu-id="a38e5-106">下表列出支援的方法。</span><span class="sxs-lookup"><span data-stu-id="a38e5-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="a38e5-107">方法</span><span class="sxs-lookup"><span data-stu-id="a38e5-107">Method</span></span>                                                   | <span data-ttu-id="a38e5-108">描述</span><span class="sxs-lookup"><span data-stu-id="a38e5-108">Description</span></span>                                            |
|----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="a38e5-109">**CSampleDSNamespace::CSampleDSNamespace**</span><span class="sxs-lookup"><span data-stu-id="a38e5-109">**CSampleDSNamespace::CSampleDSNamespace**</span></span>               | <span data-ttu-id="a38e5-110">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="a38e5-110">Standard constructor.</span></span>                                  |
| <span data-ttu-id="a38e5-111">**CSampleDSNamespace：： ~ CSampleDSNamespace**</span><span class="sxs-lookup"><span data-stu-id="a38e5-111">**CSampleDSNamespace::~CSampleDSNamespace**</span></span>              | <span data-ttu-id="a38e5-112">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="a38e5-112">Standard destructor.</span></span>                                   |
| <span data-ttu-id="a38e5-113">標準 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 方法。</span><span class="sxs-lookup"><span data-stu-id="a38e5-113">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                   |                                                        |
| <span data-ttu-id="a38e5-114">標準 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 方法。</span><span class="sxs-lookup"><span data-stu-id="a38e5-114">Standard [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) methods.</span></span> |                                                        |
| <span data-ttu-id="a38e5-115">**CSampleDSNamespace::AllocateNamespaceObject**</span><span class="sxs-lookup"><span data-stu-id="a38e5-115">**CSampleDSNamespace::AllocateNamespaceObject**</span></span>          | <span data-ttu-id="a38e5-116">建立命名空間物件，並載入其類型資料。</span><span class="sxs-lookup"><span data-stu-id="a38e5-116">Create a namespace object and load its type data.</span></span>      |
| <span data-ttu-id="a38e5-117">**CSampleDSNamespace::CreateNamespace**</span><span class="sxs-lookup"><span data-stu-id="a38e5-117">**CSampleDSNamespace::CreateNamespace**</span></span>                  | <span data-ttu-id="a38e5-118">配置、初始化和驗證命名空間物件。</span><span class="sxs-lookup"><span data-stu-id="a38e5-118">Allocate, initialize, and validate a namespace object.</span></span> |
| <span data-ttu-id="a38e5-119">**CSampleDSNamespace：： QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="a38e5-119">**CSampleDSNamespace::QueryInterface**</span></span>                   | <span data-ttu-id="a38e5-120">確認此物件上的指定 IID。</span><span class="sxs-lookup"><span data-stu-id="a38e5-120">Verify the given IID on this object.</span></span>                   |



 

 

 




