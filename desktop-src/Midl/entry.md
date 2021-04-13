---
title: entry 屬性
description: '\ Entry \ 屬性會藉由識別 DLL 中的進入點，來指定模組中匯出的函式或常數。'
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- 專案屬性 MIDL
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314743"
---
# <a name="entry-attribute"></a><span data-ttu-id="d76ea-104">entry 屬性</span><span class="sxs-lookup"><span data-stu-id="d76ea-104">entry attribute</span></span>

<span data-ttu-id="d76ea-105">**\[ 專案 \]** 屬性會藉由識別 DLL 中的進入點，指定匯出的函式或模組中的常數。</span><span class="sxs-lookup"><span data-stu-id="d76ea-105">The **\[entry\]** attribute specifies an exported function or constant in a module by identifying the entry point in the DLL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
  [, optional-attribute-list]
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="d76ea-106">參數</span><span class="sxs-lookup"><span data-stu-id="d76ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76ea-107">*uuid-數位*</span><span class="sxs-lookup"><span data-stu-id="d76ea-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="d76ea-108">指定 [**模組**](module.md)的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d76ea-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="d76ea-109">*專案識別碼*</span><span class="sxs-lookup"><span data-stu-id="d76ea-109">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="d76ea-110">指定模組進入點函數名稱或整數識別碼。</span><span class="sxs-lookup"><span data-stu-id="d76ea-110">Specifies the module entry point function name or integer identification number.</span></span>

</dd> <dt>

<span data-ttu-id="d76ea-111">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="d76ea-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d76ea-112">指定要套用至 [**模組**](module.md)的 MIDL 編譯器的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="d76ea-112">Specifies zero or more attributes for the MIDL compiler to apply to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="d76ea-113">*modulename*</span><span class="sxs-lookup"><span data-stu-id="d76ea-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="d76ea-114">指定其他軟體元件用來表示 [**模組**](module.md)的名稱。</span><span class="sxs-lookup"><span data-stu-id="d76ea-114">Specifies the name other software components use to denote the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="d76ea-115">*elementlist*</span><span class="sxs-lookup"><span data-stu-id="d76ea-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="d76ea-116">指定一或多個模組元素定義語句。</span><span class="sxs-lookup"><span data-stu-id="d76ea-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d76ea-117">備註</span><span class="sxs-lookup"><span data-stu-id="d76ea-117">Remarks</span></span>

<span data-ttu-id="d76ea-118">如果 **\[ 專案 \]** 屬性的 *entryid* 變數是字串，這就是命名的進入點。</span><span class="sxs-lookup"><span data-stu-id="d76ea-118">If the *entryid* variable of the **\[entry\]** attribute is a string, this is a named entry point.</span></span> <span data-ttu-id="d76ea-119">如果 *entryid* 是數位，則進入點是由序數所定義。</span><span class="sxs-lookup"><span data-stu-id="d76ea-119">If *entryid* is a number, the entry point is defined by an ordinal.</span></span> <span data-ttu-id="d76ea-120">這個屬性會提供方法來取得模組中的函式位址。</span><span class="sxs-lookup"><span data-stu-id="d76ea-120">This attribute provides a way to obtain the address of a function in a module.</span></span>

## <a name="examples"></a><span data-ttu-id="d76ea-121">範例</span><span class="sxs-lookup"><span data-stu-id="d76ea-121">Examples</span></span>

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a><span data-ttu-id="d76ea-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d76ea-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d76ea-123">**dllname**</span><span class="sxs-lookup"><span data-stu-id="d76ea-123">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="d76ea-124">**模組**</span><span class="sxs-lookup"><span data-stu-id="d76ea-124">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="d76ea-125">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="d76ea-125">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="d76ea-126">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="d76ea-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="d76ea-127">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d76ea-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 