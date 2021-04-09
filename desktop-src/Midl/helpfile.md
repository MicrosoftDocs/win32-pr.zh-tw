---
title: helpfile 屬性
description: '\ 保護 \ 屬性會設定類型程式庫的說明檔名稱。 程式庫中的所有類型都會共用相同的說明檔。'
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- 説明的屬性 MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681823"
---
# <a name="helpfile-attribute"></a><span data-ttu-id="c5d33-105">helpfile 屬性</span><span class="sxs-lookup"><span data-stu-id="c5d33-105">helpfile attribute</span></span>

<span data-ttu-id="c5d33-106">[輔助檔] 屬性會設定類型程式庫的說明檔名稱。 **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="c5d33-106">The **\[helpfile\]** attribute sets the name of the Help file for a type library.</span></span> <span data-ttu-id="c5d33-107">程式庫中的所有類型都會共用相同的說明檔。</span><span class="sxs-lookup"><span data-stu-id="c5d33-107">All types in a library share the same Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a><span data-ttu-id="c5d33-108">參數</span><span class="sxs-lookup"><span data-stu-id="c5d33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5d33-109">*uuid-數位*</span><span class="sxs-lookup"><span data-stu-id="c5d33-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="c5d33-110">指定 [**媒體**](library.md)櫃的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5d33-110">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5d33-111">*filename*</span><span class="sxs-lookup"><span data-stu-id="c5d33-111">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="c5d33-112">指定包含解說文字的檔案名。</span><span class="sxs-lookup"><span data-stu-id="c5d33-112">Specifies the name of the file containing the help text.</span></span>

</dd> <dt>

<span data-ttu-id="c5d33-113">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="c5d33-113">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c5d33-114">指定 MIDL 編譯器將套用至連結 [**庫**](library.md)的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="c5d33-114">Specifies zero or more attributes that the MIDL compiler will apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5d33-115">*程式庫語句*</span><span class="sxs-lookup"><span data-stu-id="c5d33-115">*library statements*</span></span> 
</dt> <dd>

<span data-ttu-id="c5d33-116">指定定義程式庫介面的一或多個 MIDL 語句。</span><span class="sxs-lookup"><span data-stu-id="c5d33-116">Specifies one or more MIDL statements that define the library interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5d33-117">備註</span><span class="sxs-lookup"><span data-stu-id="c5d33-117">Remarks</span></span>

<span data-ttu-id="c5d33-118">使用 **ITypeLib** 和 **ITypeInfo** 介面中的 **GetDocumentation** 函式來取出檔案名。</span><span class="sxs-lookup"><span data-stu-id="c5d33-118">Use the **GetDocumentation** functions in the **ITypeLib** and **ITypeInfo** interfaces to retrieve the file name.</span></span>

## <a name="examples"></a><span data-ttu-id="c5d33-119">範例</span><span class="sxs-lookup"><span data-stu-id="c5d33-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="c5d33-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5d33-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d33-121">**圖書館**</span><span class="sxs-lookup"><span data-stu-id="c5d33-121">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="c5d33-122">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="c5d33-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c5d33-123">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="c5d33-123">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c5d33-124">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c5d33-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 