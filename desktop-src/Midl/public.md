---
title: public 屬性
description: '\ Public \ 屬性包含在類型程式庫中使用 typedef 關鍵字宣告的別名。'
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- public 屬性 MIDL
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967884"
---
# <a name="public-attribute"></a><span data-ttu-id="995ac-104">public 屬性</span><span class="sxs-lookup"><span data-stu-id="995ac-104">public attribute</span></span>

<span data-ttu-id="995ac-105">**\[ Public \]** 屬性包含在類型程式庫中使用 [**typedef**](typedef.md)關鍵字宣告的別名。</span><span class="sxs-lookup"><span data-stu-id="995ac-105">The **\[public\]** attribute includes an alias declared with the [**typedef**](typedef.md) keyword in the type library.</span></span>

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a><span data-ttu-id="995ac-106">參數</span><span class="sxs-lookup"><span data-stu-id="995ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="995ac-107">*資料類型*</span><span class="sxs-lookup"><span data-stu-id="995ac-107">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="995ac-108">識別碼將為其別名的資料類型。</span><span class="sxs-lookup"><span data-stu-id="995ac-108">The data type that the identifier will be an alias for.</span></span>

</dd> <dt>

<span data-ttu-id="995ac-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="995ac-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="995ac-110">軟體中將會知道 *資料類型* 的另一個名稱。</span><span class="sxs-lookup"><span data-stu-id="995ac-110">Another name by which *data-type* will be known in the software.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="995ac-111">備註</span><span class="sxs-lookup"><span data-stu-id="995ac-111">Remarks</span></span>

<span data-ttu-id="995ac-112">根據預設，以 [**typedef**](typedef.md)宣告且沒有其他屬性的別名會被視為 **\# 定義**，而且不會包含在類型程式庫中。</span><span class="sxs-lookup"><span data-stu-id="995ac-112">By default, an alias that is declared with [**typedef**](typedef.md) and has no other attributes is treated as a **\#define** and is not included in the type library.</span></span> <span data-ttu-id="995ac-113">使用 **\[ public \]** 屬性可確保別名會成為類型程式庫的一部分。</span><span class="sxs-lookup"><span data-stu-id="995ac-113">Using the **\[public\]** attribute ensures that the alias becomes part of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="995ac-114">MIDL 編譯器要求您明確地將 **\[ 公用 \]** 屬性套用至您想要公開的每一個 typedef。</span><span class="sxs-lookup"><span data-stu-id="995ac-114">The MIDL compiler requires that you explicitly apply the **\[public\]** attribute to each typedef that you want public.</span></span>

 

## <a name="examples"></a><span data-ttu-id="995ac-115">範例</span><span class="sxs-lookup"><span data-stu-id="995ac-115">Examples</span></span>

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a><span data-ttu-id="995ac-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="995ac-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="995ac-117">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="995ac-117">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="995ac-118">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="995ac-118">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="995ac-119">**介面**</span><span class="sxs-lookup"><span data-stu-id="995ac-119">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="995ac-120">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="995ac-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="995ac-121">**著**</span><span class="sxs-lookup"><span data-stu-id="995ac-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 