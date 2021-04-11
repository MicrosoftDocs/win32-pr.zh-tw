---
title: pointer_default 屬性
description: '\ 指標 \_ default \ 屬性會指定除了出現在參數清單中最上層指標以外的所有指標的預設指標屬性。'
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default 屬性 MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023330"
---
# <a name="pointer_default-attribute"></a><span data-ttu-id="d5038-104">指標 \_ 預設屬性</span><span class="sxs-lookup"><span data-stu-id="d5038-104">pointer\_default attribute</span></span>

<span data-ttu-id="d5038-105">**\[ 指標 \_ default \]** 屬性會指定除了出現在參數清單中最上層指標以外的所有指標的預設指標屬性。</span><span class="sxs-lookup"><span data-stu-id="d5038-105">The **\[pointer\_default\]** attribute specifies the default pointer attribute for all pointers except top-level pointers that appear in parameter lists.</span></span>

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a><span data-ttu-id="d5038-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5038-106">Parameters</span></span>

<span data-ttu-id="d5038-107">這個屬性沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d5038-107">This attribute has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="d5038-108">範例</span><span class="sxs-lookup"><span data-stu-id="d5038-108">Examples</span></span>

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="d5038-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5038-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5038-110">**介面**</span><span class="sxs-lookup"><span data-stu-id="d5038-110">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="d5038-111">陣列和 Sized-Pointer 屬性</span><span class="sxs-lookup"><span data-stu-id="d5038-111">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="d5038-112">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="d5038-112">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="d5038-113">陣列和指標</span><span class="sxs-lookup"><span data-stu-id="d5038-113">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="d5038-114">**ptr**</span><span class="sxs-lookup"><span data-stu-id="d5038-114">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="d5038-115">**ref**</span><span class="sxs-lookup"><span data-stu-id="d5038-115">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="d5038-116">**獨特**</span><span class="sxs-lookup"><span data-stu-id="d5038-116">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="d5038-117">預設指標類型</span><span class="sxs-lookup"><span data-stu-id="d5038-117">Default Pointer Types</span></span>](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 