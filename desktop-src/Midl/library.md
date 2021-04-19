---
title: 程式庫屬性
description: Library 語句包含 MIDL 編譯器用來產生類型程式庫的所有資訊。
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- 程式庫屬性 MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969103"
---
# <a name="library-attribute"></a><span data-ttu-id="e9e68-104">程式庫屬性</span><span class="sxs-lookup"><span data-stu-id="e9e68-104">library attribute</span></span>

<span data-ttu-id="e9e68-105">**Library** 語句包含 MIDL 編譯器用來產生類型程式庫的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="e9e68-105">The **library** statement contains all the information that the MIDL compiler uses to generate a type library.</span></span>

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="e9e68-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9e68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9e68-107">*uuid-數位*</span><span class="sxs-lookup"><span data-stu-id="e9e68-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e68-108">指定媒體櫃的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9e68-108">Specifies a universally unique identification number for the library.</span></span>

</dd> <dt>

<span data-ttu-id="e9e68-109">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="e9e68-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e68-110">指定適用于整個連結 **庫** 語句的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="e9e68-110">Specifies additional attributes that apply to the entire **library** statement.</span></span> <span data-ttu-id="e9e68-111">允許的屬性包括 **\[** [**control**](control.md) **\]** 、 **\[** [**helpcoNtext**](helpcontext.md) **\]** 、 **\[** [**説明**](helpfile.md) **\]** 、 **\[** [**helpstring**](helpstring.md) **\]** 、 **\[** [**hidden**](hidden.md) **\]** 、 **\[** [**lcid**](lcid.md) **\]** 、 **\[** [**受限**](restricted.md) **\]** 及 **\[** [**版本**](version.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="e9e68-111">Allowable attributes include **\[**[**control**](control.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**lcid**](lcid.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="e9e68-112">*程式庫名稱*</span><span class="sxs-lookup"><span data-stu-id="e9e68-112">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e68-113">軟體元件參考連結 **庫** 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9e68-113">The name by which software components refer to the **library**.</span></span>

</dd> <dt>

<span data-ttu-id="e9e68-114">*程式庫定義語句*</span><span class="sxs-lookup"><span data-stu-id="e9e68-114">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e68-115">定義連結 **庫** 內容的一或多個 MIDL 語句。</span><span class="sxs-lookup"><span data-stu-id="e9e68-115">One or more MIDL statements which define the contents of the **library**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9e68-116">備註</span><span class="sxs-lookup"><span data-stu-id="e9e68-116">Remarks</span></span>

<span data-ttu-id="e9e68-117">程式庫區塊內的語句可以使用在程式庫區塊內部或外部宣告的元素。</span><span class="sxs-lookup"><span data-stu-id="e9e68-117">Statements inside the library block can use elements that are declared inside or outside of the library block.</span></span> <span data-ttu-id="e9e68-118">程式庫語句可以使用這些專案做為基底類型、繼承自這些元素，或直接在行上參考它們，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e9e68-118">Library statements can use those elements as base types, inheriting from those elements, or by simply referencing them on a line, as follows:</span></span>

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

<span data-ttu-id="e9e68-119">MIDL 編譯器會建立類型程式庫，其中包含程式庫區塊內每個元素的定義，以及程式庫區塊內所定義和參考之任何專案的定義。</span><span class="sxs-lookup"><span data-stu-id="e9e68-119">The MIDL compiler will create a type library that includes definitions for every element inside the library block, plus definitions for any elements defined outside and referenced from within the library block.</span></span>

<span data-ttu-id="e9e68-120">如需從單一 IDL 檔案產生類型程式庫和 proxy 存根和標頭的詳細資訊，請參閱 [從單一 idl 檔案產生 PROXY DLL 和型別程式庫](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md)。</span><span class="sxs-lookup"><span data-stu-id="e9e68-120">For information on generating both a type library and proxy stubs and headers from a single IDL file see [Generating a Proxy DLL and a Type Library From a Single IDL File](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e9e68-121">範例</span><span class="sxs-lookup"><span data-stu-id="e9e68-121">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a><span data-ttu-id="e9e68-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9e68-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e68-123">型別程式庫的內容</span><span class="sxs-lookup"><span data-stu-id="e9e68-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="e9e68-124">**控制**</span><span class="sxs-lookup"><span data-stu-id="e9e68-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="e9e68-125">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e9e68-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="e9e68-126">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="e9e68-126">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="e9e68-127">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="e9e68-127">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="e9e68-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="e9e68-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="e9e68-129">**隱藏**</span><span class="sxs-lookup"><span data-stu-id="e9e68-129">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="e9e68-130">**Lcid**</span><span class="sxs-lookup"><span data-stu-id="e9e68-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="e9e68-131">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="e9e68-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e9e68-132">**限制**</span><span class="sxs-lookup"><span data-stu-id="e9e68-132">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="e9e68-133">**版本**</span><span class="sxs-lookup"><span data-stu-id="e9e68-133">**version**</span></span>](version.md)
</dt> </dl>

 

 