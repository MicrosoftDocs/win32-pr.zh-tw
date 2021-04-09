---
title: 指標類型屬性
description: 下列屬性會指定指標的特性。
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- IDL MIDL、屬性、指標類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675771"
---
# <a name="pointer-type-attributes"></a><span data-ttu-id="96461-104">指標類型屬性</span><span class="sxs-lookup"><span data-stu-id="96461-104">Pointer Type Attributes</span></span>

<span data-ttu-id="96461-105">下列屬性會指定指標的特性。</span><span class="sxs-lookup"><span data-stu-id="96461-105">The following attributes specify the characteristics of pointers.</span></span>



| <span data-ttu-id="96461-106">屬性</span><span class="sxs-lookup"><span data-stu-id="96461-106">Attribute</span></span>                                   | <span data-ttu-id="96461-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="96461-107">Usage</span></span>                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96461-108">**ptr**</span><span class="sxs-lookup"><span data-stu-id="96461-108">**ptr**</span></span>](ptr.md)                          | <span data-ttu-id="96461-109">使用 C 語言指標的所有功能（包括別名）將指標指定為完整指標。</span><span class="sxs-lookup"><span data-stu-id="96461-109">Designates a pointer as a full pointer, with all the capabilities of a C-language pointer, including aliasing.</span></span>                                                                                       |
| [<span data-ttu-id="96461-110">**ref**</span><span class="sxs-lookup"><span data-stu-id="96461-110">**ref**</span></span>](ref.md)                          | <span data-ttu-id="96461-111">指定 MIDL 中最簡單的指標類型，一個只提供某些資料的位址。</span><span class="sxs-lookup"><span data-stu-id="96461-111">Designates the simplest type of pointer in MIDL—one that simply provides the address of some data.</span></span> <span data-ttu-id="96461-112">參考指標永遠不可以是 null。</span><span class="sxs-lookup"><span data-stu-id="96461-112">Reference pointers can never be null.</span></span>                                                             |
| [<span data-ttu-id="96461-113">**獨特**</span><span class="sxs-lookup"><span data-stu-id="96461-113">**unique**</span></span>](unique.md)                    | <span data-ttu-id="96461-114">讓指標為 null，但不支援別名。</span><span class="sxs-lookup"><span data-stu-id="96461-114">Lets a pointer be null, but does not support aliasing.</span></span>                                                                                                                                               |
| [<span data-ttu-id="96461-115">**指標 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="96461-115">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="96461-116">套用至介面，以指定該介面中所有指標的預設指標類型，但最上層參數指標除外，後者會自動預設為 [**ref**](ref.md) 指標。</span><span class="sxs-lookup"><span data-stu-id="96461-116">Applied to an interface to specify the default pointer type for all pointers in that interface, except for top-level parameter pointers, which automatically default to [**ref**](ref.md) pointers.</span></span> |
| [<span data-ttu-id="96461-117">**iid \_ 為**</span><span class="sxs-lookup"><span data-stu-id="96461-117">**iid\_is**</span></span>](iid-is.md)                   | <span data-ttu-id="96461-118">提供 COM 介面的介面識別碼，該介面是指標的物件。</span><span class="sxs-lookup"><span data-stu-id="96461-118">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                                                                                            |
| [<span data-ttu-id="96461-119">**字串**</span><span class="sxs-lookup"><span data-stu-id="96461-119">**string**</span></span>](string.md)                    | <span data-ttu-id="96461-120">指定指標指向字串。</span><span class="sxs-lookup"><span data-stu-id="96461-120">Specifies that the pointer points to a string.</span></span>                                                                                                                                                       |



 

 

 




