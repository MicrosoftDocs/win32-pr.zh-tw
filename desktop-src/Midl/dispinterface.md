---
title: dispinterface 屬性
description: 介面介面語句會定義一組屬性和方法，您可以在其上呼叫 IDispatch 調用。
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- 分派介面屬性 MIDL
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842267"
---
# <a name="dispinterface-attribute"></a><span data-ttu-id="9725b-104">dispinterface 屬性</span><span class="sxs-lookup"><span data-stu-id="9725b-104">dispinterface attribute</span></span>

<span data-ttu-id="9725b-105">**介面介面** 語句會定義一組屬性和方法，您可以在其上呼叫 **IDispatch：： Invoke**。</span><span class="sxs-lookup"><span data-stu-id="9725b-105">The **dispinterface** statement defines a set of properties and methods on which you can call **IDispatch::Invoke**.</span></span> <span data-ttu-id="9725b-106">您可以藉由明確地列出一組支援的方法和屬性 (語法 1) ，或 (語法 2) 列出單一介面，來定義一個介面。</span><span class="sxs-lookup"><span data-stu-id="9725b-106">A dispinterface may be defined by explicitly listing the set of supported methods and properties (Syntax 1), or by listing a single interface (Syntax 2).</span></span>

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a><span data-ttu-id="9725b-107">參數</span><span class="sxs-lookup"><span data-stu-id="9725b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9725b-108">*attributes*</span><span class="sxs-lookup"><span data-stu-id="9725b-108">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="9725b-109">指定適用于整個 **介面介面** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="9725b-109">Specifies attributes that apply to the entire **dispinterface**.</span></span> <span data-ttu-id="9725b-110">接受下列屬性： **\[** [**helpstring**](helpstring.md) **\]** 、 **\[** [**helpcoNtext**](helpcontext.md) **\]** 、的內容： **\[** [](helpfile.md) **\]** 、 **\[** [**hidden**](hidden.md) **\]** 、 **\[** [**nonextensible**](nonextensible.md) **\]** 、 **\[** [**oleautomation**](oleautomation.md) **\]** 、 **\[** [**受限**](restricted.md) **\]** 、 **\[** [**uuid**](uuid.md) **\]** 和 **\[** [**version**](version.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="9725b-110">The following attributes are accepted: **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**nonextensible**](nonextensible.md)**\]**, **\[**[**oleautomation**](oleautomation.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="9725b-111">*介面介面名稱*</span><span class="sxs-lookup"><span data-stu-id="9725b-111">*dispinterface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9725b-112">類型程式庫中已知的分配 **介面** 名稱。</span><span class="sxs-lookup"><span data-stu-id="9725b-112">The name by which the **dispinterface** is known in the type library.</span></span> <span data-ttu-id="9725b-113">這個名稱在類型程式庫中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="9725b-113">This name must be unique within the type library.</span></span>

</dd> <dt>

<span data-ttu-id="9725b-114">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="9725b-114">*property-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9725b-115"> (語法 1) 物件所支援的選擇性屬性清單，以變數的形式宣告。</span><span class="sxs-lookup"><span data-stu-id="9725b-115">(Syntax 1) An optional list of properties supported by the object, declared in the form of variables.</span></span> <span data-ttu-id="9725b-116">這是在方法清單中宣告屬性函式的簡短形式。</span><span class="sxs-lookup"><span data-stu-id="9725b-116">This is the short form for declaring the property functions in the methods list.</span></span> <span data-ttu-id="9725b-117">如需詳細資訊，請參閱「批註」一節。</span><span class="sxs-lookup"><span data-stu-id="9725b-117">See the comments section for details.</span></span>

</dd> <dt>

<span data-ttu-id="9725b-118">*方法-清單*</span><span class="sxs-lookup"><span data-stu-id="9725b-118">*method-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9725b-119"> (語法 1) 清單，其中包含在 **介面介面** 中每個方法和屬性的函式原型。</span><span class="sxs-lookup"><span data-stu-id="9725b-119">(Syntax 1) A list comprising a function prototype for each method and property in the **dispinterface**.</span></span> <span data-ttu-id="9725b-120">任何數目的函式定義都可以出現在 *methlist* 中。</span><span class="sxs-lookup"><span data-stu-id="9725b-120">Any number of function definitions can appear in *methlist*.</span></span> <span data-ttu-id="9725b-121">*Methlist* 中的函式具有下列形式：</span><span class="sxs-lookup"><span data-stu-id="9725b-121">A function in *methlist* has the following form:</span></span>

<span data-ttu-id="9725b-122">**\[ 屬性 \]** *returntype methname 類型 paramname ***(*** 參數 \* \* \* ) ;*\*</span><span class="sxs-lookup"><span data-stu-id="9725b-122">**\[***attributes***\]** *returntype methname type paramname ***(*** params\*\*\*);*\*</span></span>

<span data-ttu-id="9725b-123">在 **介面介面** 中的方法上接受下列屬性： **\[ helpstring \]**、 **\[ helpcoNtext \]**、 **\[** [**propget**](propget.md) **\]** 、 **\[** [**propput**](propput.md) **\]** 、 **\[** [**propputref**](propputref.md) **\]** 、 **\[** [**string**](string.md) **\]** 和 **\[** [**vararg**](vararg.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="9725b-123">The following attributes are accepted on a method in a **dispinterface**: **\[helpstring\]**, **\[helpcontext\]**, **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]**, **\[**[**propputref**](propputref.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**vararg**](vararg.md)**\]**.</span></span> <span data-ttu-id="9725b-124">如果指定了 **\[ \] vararg** ，則最後一個參數必須是 **VARIANT** 類型的安全陣列。</span><span class="sxs-lookup"><span data-stu-id="9725b-124">If **\[vararg\]** is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="9725b-125">參數清單是以逗號分隔的清單，其中的每個元素都具有下列格式：</span><span class="sxs-lookup"><span data-stu-id="9725b-125">The parameter list is a comma-delimited list, each element of which has the following form:</span></span>

<span data-ttu-id="9725b-126">**\[***屬性***\]**</span><span class="sxs-lookup"><span data-stu-id="9725b-126">**\[***attributes***\]**</span></span>

<span data-ttu-id="9725b-127">*類型* 可以是任何宣告的或內建類型，或任何類型的指標。</span><span class="sxs-lookup"><span data-stu-id="9725b-127">The *type* can be any declared or built-in type, or a pointer to any type.</span></span> <span data-ttu-id="9725b-128">參數上的屬性為：</span><span class="sxs-lookup"><span data-stu-id="9725b-128">Attributes on parameters are:</span></span>

<span data-ttu-id="9725b-129">**\[**[**in**](in.md) **\]** 、 **\[** [**out**](out-idl.md) **\]** 、 **\[** [**optional**](optional.md) **\]** 、 **\[ string \]**</span><span class="sxs-lookup"><span data-stu-id="9725b-129">**\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]**, **\[**[**optional**](optional.md)**\]**, **\[string\]**</span></span>

</dd> <dt>

<span data-ttu-id="9725b-130">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="9725b-130">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9725b-131"> (語法 2) 要宣告為 IDispatch 介面的介面名稱。</span><span class="sxs-lookup"><span data-stu-id="9725b-131">(Syntax 2) The name of the interface to declare as an IDispatch interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9725b-132">備註</span><span class="sxs-lookup"><span data-stu-id="9725b-132">Remarks</span></span>

<span data-ttu-id="9725b-133">MIDL 編譯器接受下列參數排序 (從左至右) ：</span><span class="sxs-lookup"><span data-stu-id="9725b-133">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="9725b-134">必要參數 (沒有 \[ defaultvalue \] 或 \[ 選擇性屬性的參數 \]) ，</span><span class="sxs-lookup"><span data-stu-id="9725b-134">Required parameters (parameters that do not have the \[defaultvalue\] or \[optional\] attributes),</span></span>
2.  <span data-ttu-id="9725b-135">具有或不具有 defaultvalue 屬性的選擇性參數 \[ \] ，</span><span class="sxs-lookup"><span data-stu-id="9725b-135">optional parameters with or without the \[defaultvalue\] attribute,</span></span>
3.  <span data-ttu-id="9725b-136">具有 \[ 選擇性 \] 屬性且不含 \[ defaultvalue \] 屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="9725b-136">parameters with the \[optional\] attribute and without the \[defaultvalue\] attribute,</span></span>
4.  <span data-ttu-id="9725b-137">\[[**lcid**](lcid.md) \] 參數（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="9725b-137">\[ [**lcid**](lcid.md)\] parameter, if any,</span></span>
5.  <span data-ttu-id="9725b-138">\[[**retval**](retval.md) \]參數</span><span class="sxs-lookup"><span data-stu-id="9725b-138">\[ [**retval**](retval.md)\] parameter</span></span>

<span data-ttu-id="9725b-139">方法函數的指定方式與 [**模組**](module.md)的參考頁面中所述完全相同，但 \[ [](entry.md) \] 不允許專案屬性。</span><span class="sxs-lookup"><span data-stu-id="9725b-139">Method functions are specified exactly as described in the reference page for [**module**](module.md) except that the \[ [**entry**](entry.md)\] attribute is not allowed.</span></span> <span data-ttu-id="9725b-140">請注意，STDOLE32。TLB (STDOLE。您必須匯入16位系統上的 TLB) ，因為分配 **介面** 繼承自 IDispatch。</span><span class="sxs-lookup"><span data-stu-id="9725b-140">Note that STDOLE32.TLB (STDOLE.TLB on 16-bit systems) must be imported, because a **dispinterface** inherits from IDispatch.</span></span>

<span data-ttu-id="9725b-141">您可以在屬性或方法清單中宣告屬性。</span><span class="sxs-lookup"><span data-stu-id="9725b-141">You can declare properties in either the properties or methods lists.</span></span> <span data-ttu-id="9725b-142">宣告屬性清單中的屬性並不表示屬性支援的存取類型 (也就是 get、put 或 putref) 。</span><span class="sxs-lookup"><span data-stu-id="9725b-142">Declaring properties in the properties list does not indicate the type of access the property supports (that is, get, put, or putref).</span></span> <span data-ttu-id="9725b-143">\[ [](readonly.md) \] 針對不支援 put 或 putref 的屬性指定 readonly 屬性。</span><span class="sxs-lookup"><span data-stu-id="9725b-143">Specify the \[ [**readonly**](readonly.md)\] attribute for properties that don't support put or putref.</span></span> <span data-ttu-id="9725b-144">如果您在方法清單中宣告屬性函式，則一個屬性的函式都有相同的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9725b-144">If you declare the property functions in the methods list, functions for one property all have the same identifier.</span></span>

<span data-ttu-id="9725b-145">使用第一個語法時，需要屬性：和方法：標記是必要的。</span><span class="sxs-lookup"><span data-stu-id="9725b-145">Using the first syntax, the properties: and methods: tags are required.</span></span> <span data-ttu-id="9725b-146">\[ [](id.md) \] 每個成員也都需要 id 屬性。</span><span class="sxs-lookup"><span data-stu-id="9725b-146">The \[ [**id**](id.md)\] attribute is also required on each member.</span></span> <span data-ttu-id="9725b-147">例如：</span><span class="sxs-lookup"><span data-stu-id="9725b-147">For example:</span></span>

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

<span data-ttu-id="9725b-148">與介面成員不同的是，因為在 HRESULT 錯誤碼之外，無法使用 [**retval**](retval.md) 屬性來傳回值。</span><span class="sxs-lookup"><span data-stu-id="9725b-148">Unlike interface members, dispinterface members cannot use the [**retval**](retval.md) attribute to return a value in addition to an HRESULT error code.</span></span> <span data-ttu-id="9725b-149">\[ [](lcid.md) \] 因為 IDispatch：： Invoke 傳遞 lcid，所以 lcid 屬性同樣對分配介面無效。</span><span class="sxs-lookup"><span data-stu-id="9725b-149">The \[ [**lcid**](lcid.md)\] attribute is likewise invalid for dispinterfaces, because IDispatch::Invoke passes an LCID.</span></span> <span data-ttu-id="9725b-150">不過，您可以重新宣告使用這些屬性的介面。</span><span class="sxs-lookup"><span data-stu-id="9725b-150">However, it is possible to redeclare an interface that uses these attributes.</span></span>

<span data-ttu-id="9725b-151">使用第二個語法，可將支援 IDispatch 的介面和先前在 ODL 腳本中宣告的介面重新宣告為 IDispatch 介面，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9725b-151">Using the second syntax, interfaces that support IDispatch and are declared earlier in an ODL script can be redeclared as IDispatch interfaces as follows:</span></span>

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

<span data-ttu-id="9725b-152">上述範例會宣告 hello 的所有成員，以及 hello 繼承為支援 IDispatch 的所有成員。</span><span class="sxs-lookup"><span data-stu-id="9725b-152">The preceding example declares all the members of hello and all the members that hello inherits as supporting IDispatch.</span></span> <span data-ttu-id="9725b-153">在此情況下，如果 hello 先前是使用 \[ \] 傳回 hresult 的 lcid 和 \[ retval 成員宣告，則 \] mktyplib.exe 會移除每個 \[ lcid \] 參數和 HRESULT 傳回型別，而會將傳回型別標記為 \[ retval \] 參數的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="9725b-153">In this case, if hello were declared earlier with \[lcid\] and \[retval\] members that returned HRESULTs, MkTypLib would remove each \[lcid\] parameter and HRESULT return type, and instead mark the return type as that of the \[retval\] parameter.</span></span>

> [!Note]  
> <span data-ttu-id="9725b-154">Mktyplib.exe 工具已淘汰。</span><span class="sxs-lookup"><span data-stu-id="9725b-154">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="9725b-155">請改用 MIDL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="9725b-155">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="9725b-156">分派介面的屬性和方法不是介面介面之 VTBL 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9725b-156">The properties and methods of a dispinterface are not part of the VTBL of the dispinterface.</span></span> <span data-ttu-id="9725b-157">因此， [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) 和 [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) 不能用來執行 IDispatch：： Invoke。</span><span class="sxs-lookup"><span data-stu-id="9725b-157">Consequently, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) and [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) cannot be used to implement IDispatch::Invoke.</span></span> <span data-ttu-id="9725b-158">當應用程式需要透過 Automation 公開現有的非 VTBL 函式時，就會使用此介面。</span><span class="sxs-lookup"><span data-stu-id="9725b-158">The dispinterface is used when an application needs to expose existing non-VTBL functions through Automation.</span></span> <span data-ttu-id="9725b-159">這些應用程式可以藉由檢查 dispidMember 參數並直接呼叫對應的函式，來執行 IDispatch：： Invoke。</span><span class="sxs-lookup"><span data-stu-id="9725b-159">These applications can implement IDispatch::Invoke by examining the dispidMember parameter and directly calling the corresponding function.</span></span>

## <a name="examples"></a><span data-ttu-id="9725b-160">範例</span><span class="sxs-lookup"><span data-stu-id="9725b-160">Examples</span></span>

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="9725b-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9725b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9725b-162">**bindable**</span><span class="sxs-lookup"><span data-stu-id="9725b-162">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="9725b-163">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="9725b-163">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="9725b-164">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="9725b-164">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="9725b-165">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="9725b-165">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="9725b-166">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="9725b-166">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="9725b-167">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="9725b-167">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="9725b-168">**隱藏**</span><span class="sxs-lookup"><span data-stu-id="9725b-168">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="9725b-169">**在**</span><span class="sxs-lookup"><span data-stu-id="9725b-169">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="9725b-170">**介面**</span><span class="sxs-lookup"><span data-stu-id="9725b-170">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="9725b-171">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="9725b-171">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="9725b-172">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="9725b-172">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="9725b-173">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="9725b-173">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="9725b-174">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9725b-174">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="9725b-175">**選**</span><span class="sxs-lookup"><span data-stu-id="9725b-175">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="9725b-176">**擴展**</span><span class="sxs-lookup"><span data-stu-id="9725b-176">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="9725b-177">**nonextensible**</span><span class="sxs-lookup"><span data-stu-id="9725b-177">**nonextensible**</span></span>](nonextensible.md)
</dt> <dt>

[<span data-ttu-id="9725b-178">**propget**</span><span class="sxs-lookup"><span data-stu-id="9725b-178">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="9725b-179">**propput**</span><span class="sxs-lookup"><span data-stu-id="9725b-179">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="9725b-180">**propputref**</span><span class="sxs-lookup"><span data-stu-id="9725b-180">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="9725b-181">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="9725b-181">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="9725b-182">**限制**</span><span class="sxs-lookup"><span data-stu-id="9725b-182">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="9725b-183">**字串**</span><span class="sxs-lookup"><span data-stu-id="9725b-183">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="9725b-184">**uuid**</span><span class="sxs-lookup"><span data-stu-id="9725b-184">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="9725b-185">**vararg**</span><span class="sxs-lookup"><span data-stu-id="9725b-185">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="9725b-186">**版本**</span><span class="sxs-lookup"><span data-stu-id="9725b-186">**version**</span></span>](version.md)
</dt> </dl>

 

 