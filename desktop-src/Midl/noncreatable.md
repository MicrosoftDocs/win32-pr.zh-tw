---
title: noncreatable 屬性
description: '\ Noncreatable \ 屬性定義無法本身具現化的物件。'
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- noncreatable 屬性 MIDL
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2aa54be3416087c06651a4bb58902a0469e8f0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314809"
---
# <a name="noncreatable-attribute"></a><span data-ttu-id="75998-104">noncreatable 屬性</span><span class="sxs-lookup"><span data-stu-id="75998-104">noncreatable attribute</span></span>

<span data-ttu-id="75998-105">**\[ Noncreatable \]** 屬性會定義無法本身具現化的物件。</span><span class="sxs-lookup"><span data-stu-id="75998-105">The **\[noncreatable\]** attribute defines an object that cannot be instantiated by itself.</span></span>

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="75998-106">參數</span><span class="sxs-lookup"><span data-stu-id="75998-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75998-107">*coclass-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="75998-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="75998-108">適用于類別的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="75998-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="75998-109">*coclass-名稱*</span><span class="sxs-lookup"><span data-stu-id="75998-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="75998-110">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="75998-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="75998-111">*coclass-介面清單*</span><span class="sxs-lookup"><span data-stu-id="75998-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="75998-112">類別的介面清單。</span><span class="sxs-lookup"><span data-stu-id="75998-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75998-113">備註</span><span class="sxs-lookup"><span data-stu-id="75998-113">Remarks</span></span>

<span data-ttu-id="75998-114">使用 [**coclass**](coclass.md)語句上的 **\[ noncreatable \]** 屬性，向使用者指出他們無法在最上層建立這個類別的新物件，也就是呼叫 **CreateInstance** 或 **CoCreateInstance**。</span><span class="sxs-lookup"><span data-stu-id="75998-114">Use the **\[noncreatable\]** attribute on a [**coclass**](coclass.md) statement to indicate to users that they cannot create a new object of this class at the top level—that is, by calling **CreateInstance** or **CoCreateInstance**.</span></span> <span data-ttu-id="75998-115">此類別的物件具現化需要對另一個物件進行方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="75998-115">Instantiation of an object of this class requires a method call to another object.</span></span> <span data-ttu-id="75998-116">例如，在 Microsoft Excel 中，"Cell" 物件是 noncreatable 的，而且必須從 Microsoft Excel 工作表物件取得。</span><span class="sxs-lookup"><span data-stu-id="75998-116">For example, in Microsoft Excel, the "Cell" object is noncreatable and must be obtained from a Microsoft Excel Worksheet object.</span></span>

<span data-ttu-id="75998-117">傳回 noncreatable 類別之實例的方法應該傳回物件的確切型別，而不是 **VARIANT** 或 **IDispatch** \* 類型。</span><span class="sxs-lookup"><span data-stu-id="75998-117">Methods that return instances of noncreatable classes should return the exact type of the object, rather than **VARIANT** or **IDispatch**\* types.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="75998-118">Typeflag 標記法：</span><span class="sxs-lookup"><span data-stu-id="75998-118">Typeflag Representation:</span></span>

<span data-ttu-id="75998-119">缺少 TYPEFLAG \_ FCANCREATE。</span><span class="sxs-lookup"><span data-stu-id="75998-119">The absence of TYPEFLAG\_FCANCREATE.</span></span>

## <a name="examples"></a><span data-ttu-id="75998-120">範例</span><span class="sxs-lookup"><span data-stu-id="75998-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="75998-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75998-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75998-122">**coclass**</span><span class="sxs-lookup"><span data-stu-id="75998-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="75998-123">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="75998-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="75998-124">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="75998-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="75998-125">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="75998-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 