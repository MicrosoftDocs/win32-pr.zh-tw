---
title: helpstringdll 屬性
description: '\ Helpstringdll \ 屬性會設定用來執行檔字串查閱之 DLL 的名稱。'
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- helpstringdll 屬性 MIDL
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933138"
---
# <a name="helpstringdll-attribute"></a><span data-ttu-id="e4772-104">helpstringdll 屬性</span><span class="sxs-lookup"><span data-stu-id="e4772-104">helpstringdll attribute</span></span>

<span data-ttu-id="e4772-105">**\[ Helpstringdll \]** 屬性會設定用來執行檔字串查閱之 DLL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4772-105">The **\[helpstringdll\]** attribute sets the name of the DLL to use to perform a document string lookup.</span></span>

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a><span data-ttu-id="e4772-106">參數</span><span class="sxs-lookup"><span data-stu-id="e4772-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4772-107">*說明-文字字串*</span><span class="sxs-lookup"><span data-stu-id="e4772-107">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="e4772-108">以零結束的字元字串，指定 DLL 的完整檔案名。</span><span class="sxs-lookup"><span data-stu-id="e4772-108">A zero-terminated string of characters specifying the fully qualified file name of a DLL.</span></span>

</dd> <dt>

<span data-ttu-id="e4772-109">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="e4772-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e4772-110">適用于整個程式庫語句的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="e4772-110">Other attributes that apply to the library statement as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="e4772-111">*程式庫名稱*</span><span class="sxs-lookup"><span data-stu-id="e4772-111">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e4772-112">軟體元件將用來表示此連結 [**庫**](library.md)的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4772-112">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4772-113">*程式庫定義語句*</span><span class="sxs-lookup"><span data-stu-id="e4772-113">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="e4772-114">定義連結 [**庫**](library.md)介面的一個或多個 MIDL 語句。</span><span class="sxs-lookup"><span data-stu-id="e4772-114">One or more MIDL statement which define the interface of the [**library**](library.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4772-115">備註</span><span class="sxs-lookup"><span data-stu-id="e4772-115">Remarks</span></span>

<span data-ttu-id="e4772-116">使用程式庫語句上的 **\[ helpstringdll \]** 屬性，將動態連結程式庫的完整檔案名指定為字元字串。</span><span class="sxs-lookup"><span data-stu-id="e4772-116">Use the **\[helpstringdll\]** attribute on a library statement to specify, as a character string, the fully qualified file name of a dynamic link library.</span></span> <span data-ttu-id="e4772-117">這可讓使用者使用物件檢視器來查看 DLL 的描述。</span><span class="sxs-lookup"><span data-stu-id="e4772-117">This allows a user to view a description of the DLL with the object viewer.</span></span>

<span data-ttu-id="e4772-118">使用 **ITypeLib2** 和 **ITypeInfo2** 介面中的 **GetDocumentation2** 函式來取出說明字串。</span><span class="sxs-lookup"><span data-stu-id="e4772-118">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4772-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4772-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4772-120">**圖書館**</span><span class="sxs-lookup"><span data-stu-id="e4772-120">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="e4772-121">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="e4772-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e4772-122">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="e4772-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="e4772-123">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e4772-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 