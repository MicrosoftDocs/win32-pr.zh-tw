---
title: licensed 屬性
description: '\ 授權 \ 屬性工作表示其所套用的 coclass 已獲授權，必須使用 IClassFactory2 來具現化。'
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- 授權屬性 MIDL
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023345"
---
# <a name="licensed-attribute"></a><span data-ttu-id="f3cb6-104">licensed 屬性</span><span class="sxs-lookup"><span data-stu-id="f3cb6-104">licensed attribute</span></span>

<span data-ttu-id="f3cb6-105">**\[ 授權 \]** 屬性工作表示其所套用的 [**coclass**](coclass.md)已獲得授權，而且必須使用 [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)具現化。</span><span class="sxs-lookup"><span data-stu-id="f3cb6-105">The **\[licensed\]** attribute indicates that the [**coclass**](coclass.md) to which it applies is licensed, and must be instantiated using [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span></span>

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a><span data-ttu-id="f3cb6-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3cb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3cb6-107">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="f3cb6-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f3cb6-108">指定套用至 [**coclass**](coclass.md) 語句的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="f3cb6-108">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="f3cb6-109">允許的 **coclass** 屬性為 **\[** [**helpstring**](helpstring.md) **\]** 、 **\[** [**helpcoNtext**](helpcontext.md) **\]** 、 **\[ 授權 \]**、 **\[** [**版本**](version.md) **\]** 、 **\[** [**控制項**](control.md) **\]** 和 **\[** [**隱藏**](hidden.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="f3cb6-109">Allowable **coclass** attributes are **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[licensed\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, and **\[**[**hidden**](hidden.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="f3cb6-110">*classname*</span><span class="sxs-lookup"><span data-stu-id="f3cb6-110">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="f3cb6-111">指定在類型程式庫中已知元件物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3cb6-111">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="f3cb6-112">*coclass 定義*</span><span class="sxs-lookup"><span data-stu-id="f3cb6-112">*coclass-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="f3cb6-113">指定組成 [**coclass**](coclass.md) 定義的語句。</span><span class="sxs-lookup"><span data-stu-id="f3cb6-113">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3cb6-114">備註</span><span class="sxs-lookup"><span data-stu-id="f3cb6-114">Remarks</span></span>

<span data-ttu-id="f3cb6-115">授權是 COM 的功能，可控制物件的建立。</span><span class="sxs-lookup"><span data-stu-id="f3cb6-115">Licensing is a feature of COM that provides control over object creation.</span></span> <span data-ttu-id="f3cb6-116">授權物件只能由獲得授權使用的用戶端建立。</span><span class="sxs-lookup"><span data-stu-id="f3cb6-116">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="f3cb6-117">授權是透過 [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) 介面在 COM 中執行，並支援可在執行時間傳遞的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="f3cb6-117">Licensing is implemented in COM through the [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

### <a name="flags"></a><span data-ttu-id="f3cb6-118">Flags</span><span class="sxs-lookup"><span data-stu-id="f3cb6-118">Flags</span></span>

<span data-ttu-id="f3cb6-119">TYPEFLAG \_ FLICENSED</span><span class="sxs-lookup"><span data-stu-id="f3cb6-119">TYPEFLAG\_FLICENSED</span></span>

## <a name="examples"></a><span data-ttu-id="f3cb6-120">範例</span><span class="sxs-lookup"><span data-stu-id="f3cb6-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a><span data-ttu-id="f3cb6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3cb6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3cb6-122">**coclass**</span><span class="sxs-lookup"><span data-stu-id="f3cb6-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="f3cb6-123">型別程式庫的內容</span><span class="sxs-lookup"><span data-stu-id="f3cb6-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="f3cb6-124">**控制**</span><span class="sxs-lookup"><span data-stu-id="f3cb6-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="f3cb6-125">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f3cb6-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f3cb6-126">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="f3cb6-126">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="f3cb6-127">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="f3cb6-127">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="f3cb6-128">**隱藏**</span><span class="sxs-lookup"><span data-stu-id="f3cb6-128">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="f3cb6-129">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="f3cb6-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f3cb6-130">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="f3cb6-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="f3cb6-131">**版本**</span><span class="sxs-lookup"><span data-stu-id="f3cb6-131">**version**</span></span>](version.md)
</dt> </dl>

 

 