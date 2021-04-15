---
title: importlib 屬性
description: '\ Importlib \ 指示詞會讓已編譯成另一個類型程式庫的類型可用於建立的類型程式庫。'
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- importlib 屬性 MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462969"
---
# <a name="importlib-attribute"></a><span data-ttu-id="fa9c0-104">importlib 屬性</span><span class="sxs-lookup"><span data-stu-id="fa9c0-104">importlib attribute</span></span>

<span data-ttu-id="fa9c0-105">**\[ Importlib \]** 指示詞會讓已編譯成另一個類型程式庫的類型，可供建立的類型程式庫使用。</span><span class="sxs-lookup"><span data-stu-id="fa9c0-105">The **\[importlib\]** directive makes types that have already been compiled into another type library available to the type library being created.</span></span>

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a><span data-ttu-id="fa9c0-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa9c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa9c0-107">*程式庫-屬性*</span><span class="sxs-lookup"><span data-stu-id="fa9c0-107">*library-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9c0-108">將套用至程式庫的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="fa9c0-108">Zero or more attributes that will be applied to the library.</span></span>

</dd> <dt>

<span data-ttu-id="fa9c0-109">*程式庫名稱*</span><span class="sxs-lookup"><span data-stu-id="fa9c0-109">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9c0-110">軟體元件將用來表示此連結 [**庫**](library.md)的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fa9c0-110">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa9c0-111">*匯入檔案*</span><span class="sxs-lookup"><span data-stu-id="fa9c0-111">*file-to-import*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9c0-112">在 MIDL 編譯時期匯入之檔案的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="fa9c0-112">The name and location of the imported file at MIDL compile-time.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa9c0-113">備註</span><span class="sxs-lookup"><span data-stu-id="fa9c0-113">Remarks</span></span>

<span data-ttu-id="fa9c0-114">所有的 **\[ importlib \]** 指示詞都必須在程式庫中的其他類型描述之前。</span><span class="sxs-lookup"><span data-stu-id="fa9c0-114">All **\[importlib\]** directives must precede the other type descriptions in the library.</span></span> <span data-ttu-id="fa9c0-115">請注意，匯入的程式庫以及產生的程式庫都必須與應用程式一起散發，才能在執行時間使用。</span><span class="sxs-lookup"><span data-stu-id="fa9c0-115">Note that the imported library, as well as the generated library, must be distributed with the application so that it is available at run time.</span></span>

<span data-ttu-id="fa9c0-116">在大部分情況下，您應該使用 MIDL 匯入指示詞 **\[** [](import.md) **\]** 來參考另一個的定義。中的 IDL 檔。IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="fa9c0-116">In most cases you should use the MIDL **\[**[**import**](import.md)**\]** directive to reference definitions from another .IDL file in your .IDL file.</span></span> <span data-ttu-id="fa9c0-117">這個方法會提供您的型別程式庫與原始檔案中的所有資訊，而 **\[ importlib \]** 只會帶入類型程式庫的內容。</span><span class="sxs-lookup"><span data-stu-id="fa9c0-117">This method provides your type library with all the information from the original file, whereas **\[importlib\]** only brings in the contents of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="fa9c0-118">**\[ Importlib \]** 指示詞會讓所匯入的程式庫中定義的任何類型都可從正在編譯的程式庫中存取。</span><span class="sxs-lookup"><span data-stu-id="fa9c0-118">The **\[importlib\]** directive makes any type defined in the imported library accessible from within the library being compiled.</span></span> <span data-ttu-id="fa9c0-119">為了避免在有重複的參考時不清楚，我們建議您使用適當的程式庫名稱來限定每個這類參考，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fa9c0-119">To avoid ambiguity when there are duplicate references, we recommend that you qualify each such reference with the appropriate library name, as follows:</span></span>

 

``` syntax
library_name.type
```

<span data-ttu-id="fa9c0-120">在沒有這類限定性的情況下，MIDL 會解析重複的參考，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fa9c0-120">In the absence of such qualification, MIDL resolves duplicate reference ambiguity as follows:</span></span>

-   <span data-ttu-id="fa9c0-121">自3.1 版起，MIDL 會使用它所找到的第一個參考。</span><span class="sxs-lookup"><span data-stu-id="fa9c0-121">Effective with version 3.1, MIDL uses the first reference it finds.</span></span>
-   <span data-ttu-id="fa9c0-122">MIDL 的3.0 版（midl 的第一個版本，可以產生類型程式庫）會使用所找到的最後一個參考。</span><span class="sxs-lookup"><span data-stu-id="fa9c0-122">Version 3.0 of MIDL, the first version of MIDL that could generate type libraries, uses the last reference it found.</span></span>

## <a name="examples"></a><span data-ttu-id="fa9c0-123">範例</span><span class="sxs-lookup"><span data-stu-id="fa9c0-123">Examples</span></span>

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a><span data-ttu-id="fa9c0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa9c0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa9c0-125">**圖書館**</span><span class="sxs-lookup"><span data-stu-id="fa9c0-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="fa9c0-126">**進口**</span><span class="sxs-lookup"><span data-stu-id="fa9c0-126">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="fa9c0-127">匯入系統標頭檔</span><span class="sxs-lookup"><span data-stu-id="fa9c0-127">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="fa9c0-128">匯入檔案和型別程式庫</span><span class="sxs-lookup"><span data-stu-id="fa9c0-128">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="fa9c0-129">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="fa9c0-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="fa9c0-130">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="fa9c0-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="fa9c0-131">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="fa9c0-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 