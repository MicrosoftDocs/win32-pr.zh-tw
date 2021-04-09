---
title: CSCHOBJ.Cpp
description: 在範例提供者元件中，管理架構物件存留期的程式碼範例是在 cschobj .cpp 中。 下表列出支援的方法。
ms.assetid: ed8cc113-2ada-4522-87b9-32c922e89819
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0159d2101a3d7728c090aa8e7d110df792c04331
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671164"
---
# <a name="cschobjcpp"></a><span data-ttu-id="e3453-104">CSCHOBJ.Cpp</span><span class="sxs-lookup"><span data-stu-id="e3453-104">CSCHOBJ.CPP</span></span>

<span data-ttu-id="e3453-105">在範例提供者元件中，管理架構物件存留期的程式碼範例是在 cschobj .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="e3453-105">In the example provider component, a code example, that manages the lifetime of the schema objects, is in cschobj.cpp.</span></span> <span data-ttu-id="e3453-106">下表列出支援的方法。</span><span class="sxs-lookup"><span data-stu-id="e3453-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="e3453-107">方法</span><span class="sxs-lookup"><span data-stu-id="e3453-107">Method</span></span>                                                   | <span data-ttu-id="e3453-108">描述</span><span class="sxs-lookup"><span data-stu-id="e3453-108">Description</span></span>                                    |
|----------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="e3453-109">**CSampleDSSchema：： CreateSchema**</span><span class="sxs-lookup"><span data-stu-id="e3453-109">**CSampleDSSchema::CreateSchema**</span></span>                        | <span data-ttu-id="e3453-110">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="e3453-110">Standard constructor.</span></span>                          |
| <span data-ttu-id="e3453-111">**CSampleDSSchema：： ~ CSampleDSSchema**</span><span class="sxs-lookup"><span data-stu-id="e3453-111">**CSampleDSSchema::~CSampleDSSchema**</span></span>                    | <span data-ttu-id="e3453-112">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="e3453-112">Standard destructor.</span></span>                           |
| <span data-ttu-id="e3453-113">標準 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 方法。</span><span class="sxs-lookup"><span data-stu-id="e3453-113">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                   |                                                |
| <span data-ttu-id="e3453-114">標準 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 方法。</span><span class="sxs-lookup"><span data-stu-id="e3453-114">Standard [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) methods.</span></span> |                                                |
| <span data-ttu-id="e3453-115">**CSampleDSSchema：： QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="e3453-115">**CSampleDSSchema::QueryInterface**</span></span>                      | <span data-ttu-id="e3453-116">請確認此物件上的指定介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3453-116">Verify the given interface ID on this object.</span></span>  |
| <span data-ttu-id="e3453-117">**CSampleDSSchema::AllocateSchema**</span><span class="sxs-lookup"><span data-stu-id="e3453-117">**CSampleDSSchema::AllocateSchema**</span></span>                      | <span data-ttu-id="e3453-118">建立架構物件並載入其類型資料。</span><span class="sxs-lookup"><span data-stu-id="e3453-118">Create a schema object and load its type data.</span></span> |



 

 

 




