---
title: uidefault 屬性
description: '\ Uidefault \ 屬性工作表示類型資訊成員是要在使用者介面中顯示的預設成員。'
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- uidefault 屬性 MIDL
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375024"
---
# <a name="uidefault-attribute"></a><span data-ttu-id="0590d-104">uidefault 屬性</span><span class="sxs-lookup"><span data-stu-id="0590d-104">uidefault attribute</span></span>

<span data-ttu-id="0590d-105">**\[ Uidefault \]** 屬性指出型別資訊成員是在使用者介面中顯示的預設成員。</span><span class="sxs-lookup"><span data-stu-id="0590d-105">The **\[uidefault\]** attribute indicates that the type information member is the default member for display in the user interface.</span></span>

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="0590d-106">參數</span><span class="sxs-lookup"><span data-stu-id="0590d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0590d-107">*方法-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="0590d-107">*method-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0590d-108">適用于方法的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="0590d-108">Other attributes that apply to the method.</span></span>

</dd> <dt>

<span data-ttu-id="0590d-109">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="0590d-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="0590d-110">方法在完成執行時將會傳回的資料類型。</span><span class="sxs-lookup"><span data-stu-id="0590d-110">The type of the data that the method will return when it finishes execution.</span></span>

</dd> <dt>

<span data-ttu-id="0590d-111">*方法名稱*</span><span class="sxs-lookup"><span data-stu-id="0590d-111">*method-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0590d-112">方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="0590d-112">The name of the method.</span></span>

</dd> <dt>

<span data-ttu-id="0590d-113">*方法-參數-清單*</span><span class="sxs-lookup"><span data-stu-id="0590d-113">*method-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0590d-114">方法的零或多個參數。</span><span class="sxs-lookup"><span data-stu-id="0590d-114">Zero or more parameters for the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0590d-115">備註</span><span class="sxs-lookup"><span data-stu-id="0590d-115">Remarks</span></span>

<span data-ttu-id="0590d-116">將 **\[ uidefault \]** 屬性套用至介面的成員或介面介面，會在設計階段告知 Visual Basic，以自動將此事件或屬性顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="0590d-116">Applying the **\[uidefault\]** attribute to a member of an interface or a dispinterface tells Visual Basic, at design-time, to automatically display this event or property to the user.</span></span> <span data-ttu-id="0590d-117">這表示當使用者按兩下物件時，Visual Basic 會跳至具有 **\[ uidefault \]** 屬性之預設來源介面中的事件。</span><span class="sxs-lookup"><span data-stu-id="0590d-117">This means that when the user double-clicks an object, Visual Basic jumps to the event in the default source interface that has the **\[uidefault\]** attribute.</span></span> <span data-ttu-id="0590d-118">當使用者選取物件時，Visual Basic 的屬性瀏覽器會在具有這個屬性的預設來源介面中顯示內容。</span><span class="sxs-lookup"><span data-stu-id="0590d-118">When the user selects an object, Visual Basic's Properties browser displays the property in the default source interface that has this attribute.</span></span> <span data-ttu-id="0590d-119">如果沒有任何事件或屬性具有 **\[ uidefault \]** 屬性，Visual Basic 會顯示預設介面中列出的第一個事件或屬性。</span><span class="sxs-lookup"><span data-stu-id="0590d-119">If no event or property has the **\[uidefault\]** attribute, Visual Basic displays the first event or property listed in the default interface.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="0590d-120">Typeflag 標記法</span><span class="sxs-lookup"><span data-stu-id="0590d-120">Typeflag Representation</span></span>

<span data-ttu-id="0590d-121">FUNCFLAG \_ FUIDEFAULT 或 VARFLAG FUIDEFAULT 的存在 \_</span><span class="sxs-lookup"><span data-stu-id="0590d-121">The presence of FUNCFLAG\_FUIDEFAULT or VARFLAG\_FUIDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="0590d-122">範例</span><span class="sxs-lookup"><span data-stu-id="0590d-122">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="0590d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0590d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0590d-124">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0590d-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="0590d-125">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="0590d-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="0590d-126">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="0590d-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 