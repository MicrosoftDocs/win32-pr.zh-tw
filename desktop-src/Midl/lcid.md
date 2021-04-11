---
title: lcid 屬性
description: '\ Lcid \ 屬性指定地區設定識別碼，並啟用地區設定特定的 MIDL 編譯器支援。'
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- lcid 屬性 MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681806"
---
# <a name="lcid-attribute"></a><span data-ttu-id="223d9-104">lcid 屬性</span><span class="sxs-lookup"><span data-stu-id="223d9-104">lcid attribute</span></span>

<span data-ttu-id="223d9-105">**\[ Lcid \]** 屬性指定地區設定識別碼，並啟用地區設定特定的 MIDL 編譯器支援。</span><span class="sxs-lookup"><span data-stu-id="223d9-105">The **\[lcid\]** attribute specifies a locale identifier and enables locale-specific MIDL compiler support.</span></span>

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="223d9-106">參數</span><span class="sxs-lookup"><span data-stu-id="223d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="223d9-107">*uuid-數位*</span><span class="sxs-lookup"><span data-stu-id="223d9-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="223d9-108">指定 [**媒體**](library.md)櫃的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="223d9-108">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="223d9-109">*localeID*</span><span class="sxs-lookup"><span data-stu-id="223d9-109">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="223d9-110">指定 Windows 國家語言支援中使用的32位地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="223d9-110">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="223d9-111">一般而言，地區設定識別碼會以十六進位提供。</span><span class="sxs-lookup"><span data-stu-id="223d9-111">Typically the locale identifier is given in hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="223d9-112">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="223d9-112">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="223d9-113">要套用至連結 [**庫**](library.md)的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="223d9-113">Zero or more attributes to apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="223d9-114">*程式庫名稱*</span><span class="sxs-lookup"><span data-stu-id="223d9-114">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="223d9-115">軟體元件參考連結 [**庫**](library.md)的名稱。</span><span class="sxs-lookup"><span data-stu-id="223d9-115">The name by which software components refer to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="223d9-116">*程式庫定義語句*</span><span class="sxs-lookup"><span data-stu-id="223d9-116">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="223d9-117">定義連結 [**庫**](library.md)內容的一或多個 MIDL 語句。</span><span class="sxs-lookup"><span data-stu-id="223d9-117">One or more MIDL statements which define the contents of the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="223d9-118">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="223d9-118">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="223d9-119">在 IDL 檔案中指定函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="223d9-119">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="223d9-120">*參數屬性清單*</span><span class="sxs-lookup"><span data-stu-id="223d9-120">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="223d9-121">將套用至函數參數的零或多個 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="223d9-121">Zero or more MIDL attributes that will be applied to the function parameter.</span></span>

</dd> <dt>

<span data-ttu-id="223d9-122">*參數-名稱*</span><span class="sxs-lookup"><span data-stu-id="223d9-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="223d9-123">指定 IDL 檔案中的參數名稱。</span><span class="sxs-lookup"><span data-stu-id="223d9-123">Specifies the name of the parameter in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="223d9-124">備註</span><span class="sxs-lookup"><span data-stu-id="223d9-124">Remarks</span></span>

<span data-ttu-id="223d9-125">**\[ Lcid \]** 語法有兩種不同的形式; 屬性的影響取決於您所使用的語法，例如連結 [**庫**](library.md)語句語法或參數語法。</span><span class="sxs-lookup"><span data-stu-id="223d9-125">The **\[lcid\]** syntax has two different forms; the effect of the attribute depends on which syntax you use — either the [**library**](library.md) statement syntax or the parameter syntax.</span></span>

<span data-ttu-id="223d9-126">當套用至連結 [**庫**](library.md)語句，以及 localeID 引數（如第一個範例所示）時， **\[ lcid \]** 屬性會識別類型程式庫或函式引數的地區設定，並可讓您在程式庫區塊內使用國際字元。</span><span class="sxs-lookup"><span data-stu-id="223d9-126">When applied to the [**library**](library.md) statement, along with a localeID argument, as shown in the first example, the **\[lcid\]** attribute identifies the locale for a type library or for a function argument and lets you use international characters inside the library block.</span></span>

<span data-ttu-id="223d9-127">自 MIDL 編譯器的版本3.01.75 起，此屬性所提供的地區設定識別碼不只會裝飾產生的類型程式庫，而是實際變更編譯器的行為。</span><span class="sxs-lookup"><span data-stu-id="223d9-127">Effective with version 3.01.75 of the MIDL compiler, the locale identifier supplied by this attribute not only decorates the resulting type library, but actually changes the behavior of the compiler.</span></span> <span data-ttu-id="223d9-128">在連結 [**庫**](library.md)語句中， **\[ \]** MIDL 會根據所指定的地區設定，接受當地語系化的輸入。</span><span class="sxs-lookup"><span data-stu-id="223d9-128">Within a [**library**](library.md) statement, from the point where the **\[lcid\]** attribute is used, MIDL will accept input localized according to the specified locale.</span></span> <span data-ttu-id="223d9-129">特別是，日文、中文和韓文等亞洲語言的完整支援 (提供完整的 DBCS 支援) 。</span><span class="sxs-lookup"><span data-stu-id="223d9-129">In particular, full support for Asian languages such as Japanese, Chinese and Korean (full DBCS support) is available.</span></span> <span data-ttu-id="223d9-130">當地語系化所支援的功能包括：批註、字串、helpstrings 和識別碼。</span><span class="sxs-lookup"><span data-stu-id="223d9-130">Features supported by the localization are: comments, strings, helpstrings and identifiers.</span></span>

<span data-ttu-id="223d9-131">使用 [**/lcid**](-lcid.md) 編譯器參數，讓整個輸入檔案都能使用此當地語系化支援，包括檔案名和目錄路徑，而不是只在程式庫區塊內。</span><span class="sxs-lookup"><span data-stu-id="223d9-131">Use the [**/lcid**](-lcid.md) compiler switch to have this localization support available to the entire input file, including file name and directory path, rather than just inside the library block.</span></span>

<span data-ttu-id="223d9-132">當套用至參數時， **\[ lcid \]** 屬性可讓您將地區設定識別碼傳遞至函式，如第二個範例所示。</span><span class="sxs-lookup"><span data-stu-id="223d9-132">When applied to a parameter, the **\[lcid\]** attribute lets you pass a locale identifier to a function, as shown in the second example.</span></span> <span data-ttu-id="223d9-133">下列限制適用于 **\[ lcid \]** 參數：</span><span class="sxs-lookup"><span data-stu-id="223d9-133">The following restrictions apply to **\[lcid\]** parameters:</span></span>

-   <span data-ttu-id="223d9-134">函數最多可以有一個 **\[ lcid \]** 參數。</span><span class="sxs-lookup"><span data-stu-id="223d9-134">A function can have at most one **\[lcid\]** parameter.</span></span>
-   <span data-ttu-id="223d9-135">參數的資料類型必須為 [**long**](long.md)。</span><span class="sxs-lookup"><span data-stu-id="223d9-135">The data type of the parameter must be [**long**](long.md).</span></span>
-   <span data-ttu-id="223d9-136">參數的方向必須是 **\[** [](in.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="223d9-136">The direction of the parameter must be **\[**[**in**](in.md)**\]** only.</span></span>
-   <span data-ttu-id="223d9-137">**\[ Lcid \]** 參數必須遵照任何其他參數，但 **\[** [**retval**](retval.md) **\]** 參數除外。</span><span class="sxs-lookup"><span data-stu-id="223d9-137">The **\[lcid\]** parameter must follow any other parameters, except a **\[**[**retval**](retval.md)**\]** parameter.</span></span>
-   <span data-ttu-id="223d9-138">您無法將 **\[ lcid \]** 屬性套用至 [**介面介面**](dispinterface.md)或 [**coclass**](coclass.md)參數。</span><span class="sxs-lookup"><span data-stu-id="223d9-138">You cannot apply the **\[lcid\]** attribute to a [**dispinterface**](dispinterface.md) or [**coclass**](coclass.md) parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="223d9-139">範例</span><span class="sxs-lookup"><span data-stu-id="223d9-139">Examples</span></span>

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a><span data-ttu-id="223d9-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="223d9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223d9-141">**coclass**</span><span class="sxs-lookup"><span data-stu-id="223d9-141">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="223d9-142">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="223d9-142">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="223d9-143">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="223d9-143">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="223d9-144">**/lcid**</span><span class="sxs-lookup"><span data-stu-id="223d9-144">**/lcid**</span></span>](-lcid.md)
</dt> <dt>

[<span data-ttu-id="223d9-145">**圖書館**</span><span class="sxs-lookup"><span data-stu-id="223d9-145">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="223d9-146">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="223d9-146">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="223d9-147">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="223d9-147">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="223d9-148">**retval**</span><span class="sxs-lookup"><span data-stu-id="223d9-148">**retval**</span></span>](retval.md)
</dt> </dl>

 

 