---
title: dllname (str) 屬性
description: '\ Dllname \ 屬性會定義包含模組進入點的 DLL 名稱。'
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- dllname (str) 屬性 MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023461"
---
# <a name="dllnamestr-attribute"></a><span data-ttu-id="76700-104">dllname (str) 屬性</span><span class="sxs-lookup"><span data-stu-id="76700-104">dllname(str) attribute</span></span>

<span data-ttu-id="76700-105">**\[ Dllname \]** 屬性會定義包含模組進入點的 DLL 名稱。</span><span class="sxs-lookup"><span data-stu-id="76700-105">The **\[dllname\]** attribute defines the name of the DLL that contains the entry points for a module.</span></span>

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="76700-106">參數</span><span class="sxs-lookup"><span data-stu-id="76700-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76700-107">*uuid-數位*</span><span class="sxs-lookup"><span data-stu-id="76700-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="76700-108">指定 [**模組**](module.md)的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="76700-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="76700-109">*filename*</span><span class="sxs-lookup"><span data-stu-id="76700-109">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="76700-110">指定以 Null 終止的字串，其中包含 Dll 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="76700-110">Specifies a NULL-terminated string which contains the full path to the Dll file.</span></span>

</dd> <dt>

<span data-ttu-id="76700-111">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="76700-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="76700-112">指定零個或更多 MIDL 介面屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="76700-112">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="76700-113">*modulename*</span><span class="sxs-lookup"><span data-stu-id="76700-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="76700-114">指定其他軟體元件可以用來參考模組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76700-114">Specifies the name which other software components can use to refer to the module.</span></span>

</dd> <dt>

<span data-ttu-id="76700-115">*elementlist*</span><span class="sxs-lookup"><span data-stu-id="76700-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="76700-116">指定一或多個模組元素定義語句。</span><span class="sxs-lookup"><span data-stu-id="76700-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76700-117">備註</span><span class="sxs-lookup"><span data-stu-id="76700-117">Remarks</span></span>

<span data-ttu-id="76700-118">模組上需要 **\[ dllname \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="76700-118">The **\[dllname\]** attribute is required on a module.</span></span>

## <a name="examples"></a><span data-ttu-id="76700-119">範例</span><span class="sxs-lookup"><span data-stu-id="76700-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a><span data-ttu-id="76700-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76700-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76700-121">**模組**</span><span class="sxs-lookup"><span data-stu-id="76700-121">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="76700-122">**進入**</span><span class="sxs-lookup"><span data-stu-id="76700-122">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="76700-123">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="76700-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="76700-124">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="76700-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="76700-125">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="76700-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 