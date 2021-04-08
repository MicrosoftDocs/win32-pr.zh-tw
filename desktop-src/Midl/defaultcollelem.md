---
title: defaultcollelem 屬性
description: '\ Defaultcollelem \ 屬性會將屬性標示為預設集合之元素的存取子函數。'
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- defaultcollelem 屬性 MIDL
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023422"
---
# <a name="defaultcollelem-attribute"></a><span data-ttu-id="990ce-104">defaultcollelem 屬性</span><span class="sxs-lookup"><span data-stu-id="990ce-104">defaultcollelem attribute</span></span>

<span data-ttu-id="990ce-105">**\[ Defaultcollelem \]** 屬性會將屬性標示為預設集合之元素的存取子函數。</span><span class="sxs-lookup"><span data-stu-id="990ce-105">The **\[defaultcollelem\]** attribute flags a property as an accessor function for an element of the default collection.</span></span>

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="990ce-106">參數</span><span class="sxs-lookup"><span data-stu-id="990ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="990ce-107">*屬性屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="990ce-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="990ce-108">適用于屬性的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="990ce-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="990ce-109">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="990ce-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="990ce-110">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="990ce-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="990ce-111">*屬性名稱*</span><span class="sxs-lookup"><span data-stu-id="990ce-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="990ce-112">屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="990ce-112">The name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="990ce-113">*元件-param 清單*</span><span class="sxs-lookup"><span data-stu-id="990ce-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="990ce-114">與屬性相關聯的零或多個參數清單。</span><span class="sxs-lookup"><span data-stu-id="990ce-114">A list of zero or more parameters associated with the property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="990ce-115">備註</span><span class="sxs-lookup"><span data-stu-id="990ce-115">Remarks</span></span>

<span data-ttu-id="990ce-116">**\[ Defaultcollelem \]** 屬性用於 Visual BasicÂ®程式碼優化。</span><span class="sxs-lookup"><span data-stu-id="990ce-116">The **\[defaultcollelem\]** attribute is used for Visual BasicÂ® code optimization.</span></span> <span data-ttu-id="990ce-117">如果介面或分配介面的成員標示為存取子函式，則呼叫會直接移至該成員。</span><span class="sxs-lookup"><span data-stu-id="990ce-117">If a member of an interface or dispinterface is flagged as an accessor function, then the call will go directly to that member.</span></span>

<span data-ttu-id="990ce-118">**\[ Defaultcollelem \]** 的使用必須與屬性一致。</span><span class="sxs-lookup"><span data-stu-id="990ce-118">Use of **\[defaultcollelem\]** must be consistent for a property.</span></span> <span data-ttu-id="990ce-119">例如，如果您在 *Get* 屬性上使用屬性，則它也必須出現在 *Let* 屬性上。</span><span class="sxs-lookup"><span data-stu-id="990ce-119">For example, if you use the attribute on a *Get* property, it must also be present on a *Let* property.</span></span>

### <a name="typeflags-representation"></a><span data-ttu-id="990ce-120">Typeflags 標記法</span><span class="sxs-lookup"><span data-stu-id="990ce-120">Typeflags Representation</span></span>

<span data-ttu-id="990ce-121">FUNCFLAG \_ FDEFAULTCOLLELEM 或 VARFLAG FDEFAULTCOLLELEM 的存在 \_ 。</span><span class="sxs-lookup"><span data-stu-id="990ce-121">The presence of FUNCFLAG\_FDEFAULTCOLLELEM or VARFLAG\_FDEFAULTCOLLELEM.</span></span>

## <a name="examples"></a><span data-ttu-id="990ce-122">範例</span><span class="sxs-lookup"><span data-stu-id="990ce-122">Examples</span></span>

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a><span data-ttu-id="990ce-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="990ce-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="990ce-124">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="990ce-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="990ce-125">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="990ce-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="990ce-126">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="990ce-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 