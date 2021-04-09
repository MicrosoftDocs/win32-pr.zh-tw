---
title: defaultvtable 屬性
description: '\ Defaultvtable \ 屬性會將介面定義為預設 Vtable 介面。'
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- defaultvtable 屬性 MIDL
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8086d60d0936dcf56738afadea4244a5fff758b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842232"
---
# <a name="defaultvtable-attribute"></a><span data-ttu-id="33222-104">defaultvtable 屬性</span><span class="sxs-lookup"><span data-stu-id="33222-104">defaultvtable attribute</span></span>

<span data-ttu-id="33222-105">**\[ Defaultvtable \]** 屬性會將介面定義為預設 Vtable 介面。</span><span class="sxs-lookup"><span data-stu-id="33222-105">The **\[defaultvtable\]** attribute defines an interface as the default Vtable interface.</span></span>

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
]
coclass coclass-name
{
    coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="33222-106">參數</span><span class="sxs-lookup"><span data-stu-id="33222-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33222-107">*coclass-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="33222-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="33222-108">適用于類別的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="33222-108">Other attributes that apply to the class.</span></span> <span data-ttu-id="33222-109">需要 **\[** [**來源**](source.md) **\]** 和 **\[** [**uuid**](uuid.md) **\]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="33222-109">The **\[**[**source**](source.md)**\]** and **\[**[**uuid**](uuid.md)**\]** attributes are required.</span></span>

</dd> <dt>

<span data-ttu-id="33222-110">*coclass-名稱*</span><span class="sxs-lookup"><span data-stu-id="33222-110">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="33222-111">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="33222-111">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="33222-112">*coclass-介面清單*</span><span class="sxs-lookup"><span data-stu-id="33222-112">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="33222-113">類別的介面清單。</span><span class="sxs-lookup"><span data-stu-id="33222-113">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33222-114">備註</span><span class="sxs-lookup"><span data-stu-id="33222-114">Remarks</span></span>

<span data-ttu-id="33222-115">預設 Vtable 介面不可以是介面介面，它必須是雙重或 Vtable 或介面。</span><span class="sxs-lookup"><span data-stu-id="33222-115">A default Vtable interface cannot be a dispinterface—it must be a dual or Vtable or interface.</span></span> <span data-ttu-id="33222-116">如果介面是雙重介面，則接收會假設它們會透過 Vtable 接收事件。</span><span class="sxs-lookup"><span data-stu-id="33222-116">If the interface is a dual interface, then sinks can assume that they will receive events through Vtable.</span></span>

<span data-ttu-id="33222-117">類別可以是預設來源介面和預設 Vtable 來源介面（如範例所示）。</span><span class="sxs-lookup"><span data-stu-id="33222-117">A class can be both a default source interface and a default Vtable source interface as shown in the example.</span></span> <span data-ttu-id="33222-118">在此情況下，建議接收器應該使用 IID \_ IDISPATCH 來接收分派事件，並使用介面識別碼接收 Vtable 事件。</span><span class="sxs-lookup"><span data-stu-id="33222-118">In this case an advise sink should use IID\_IDISPATCH to receive dispatch events and use the interface identifier to receive Vtable events.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="33222-119">Typeflag 標記法</span><span class="sxs-lookup"><span data-stu-id="33222-119">Typeflag Representation</span></span>

<span data-ttu-id="33222-120">IMPLTYPEFLAG FDEFAULTVTABLE 的存在 \_ 。</span><span class="sxs-lookup"><span data-stu-id="33222-120">The presence of IMPLTYPEFLAG\_FDEFAULTVTABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="33222-121">範例</span><span class="sxs-lookup"><span data-stu-id="33222-121">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="33222-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33222-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33222-123">**coclass**</span><span class="sxs-lookup"><span data-stu-id="33222-123">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="33222-124">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="33222-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="33222-125">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="33222-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="33222-126">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="33222-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="33222-127">**源**</span><span class="sxs-lookup"><span data-stu-id="33222-127">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="33222-128">**uuid**</span><span class="sxs-lookup"><span data-stu-id="33222-128">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 