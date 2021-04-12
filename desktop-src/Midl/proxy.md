---
title: proxy 屬性
description: '\ Proxy \ 屬性可防止 Automation 註冊為雙重介面的 proxy/stub 處理常式。'
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- proxy 屬性 MIDL
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa8c9d305b7f51a012ae26d7b1a76d2e3011fd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462965"
---
# <a name="proxy-attribute"></a><span data-ttu-id="1e287-104">proxy 屬性</span><span class="sxs-lookup"><span data-stu-id="1e287-104">proxy attribute</span></span>

<span data-ttu-id="1e287-105">**\[ Proxy \]** 屬性會防止 Automation 註冊為雙重介面的 proxy/stub 處理常式。</span><span class="sxs-lookup"><span data-stu-id="1e287-105">The **\[proxy\]** attribute prevents Automation from registering as a proxy/stub handler for a dual interface.</span></span>

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="1e287-106">參數</span><span class="sxs-lookup"><span data-stu-id="1e287-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e287-107">*字串-uuid*</span><span class="sxs-lookup"><span data-stu-id="1e287-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="1e287-108">指定一個字串，其中包含8個十六進位數位，後面接著連字號，再接著三個4個十六進位數位的群組，後面接著連字號，再接著12個十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="1e287-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="1e287-109">您可以用引號括住 UUID 字串，但使用 MIDL 編譯器參數 [**/osf**](-osf.md)時除外。</span><span class="sxs-lookup"><span data-stu-id="1e287-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e287-110">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="1e287-110">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1e287-111">指定套用至整個介面的零或多個 IDL 屬性清單。</span><span class="sxs-lookup"><span data-stu-id="1e287-111">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="1e287-112">當有兩個或多個介面屬性存在時，它們必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="1e287-112">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="1e287-113">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="1e287-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1e287-114">介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e287-114">Name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="1e287-115">*基底介面*</span><span class="sxs-lookup"><span data-stu-id="1e287-115">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="1e287-116">指定此衍生介面繼承成員函式、狀態碼和介面屬性之介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e287-116">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="1e287-117">衍生介面不會繼承型別定義。</span><span class="sxs-lookup"><span data-stu-id="1e287-117">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="1e287-118">若要這樣做，請使用 [**import**](import.md) 關鍵字匯入基底介面的 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="1e287-118">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e287-119">備註</span><span class="sxs-lookup"><span data-stu-id="1e287-119">Remarks</span></span>

<span data-ttu-id="1e287-120">使用 \[  \] 雙重介面的 PROXY 屬性可防止 TLB 接管產生的存根。</span><span class="sxs-lookup"><span data-stu-id="1e287-120">Using the \[ **proxy**\] attribute for a dual interface prevents the TLB from taking over generated stubs.</span></span> <span data-ttu-id="1e287-121">如果指定了這個屬性，當 typelib 未註冊時，就不應該取消註冊 typelib proxy。</span><span class="sxs-lookup"><span data-stu-id="1e287-121">If this attribute is specified, the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

### <a name="flags"></a><span data-ttu-id="1e287-122">Flags</span><span class="sxs-lookup"><span data-stu-id="1e287-122">Flags</span></span>

<dl> <dt>

<span data-ttu-id="1e287-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG \_ PROXY</span><span class="sxs-lookup"><span data-stu-id="1e287-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="1e287-124">介面可以用 TYPEFLAG proxy 旗標標示， \_ 表示它們將使用 PROXY/stub 動態連結程式庫。</span><span class="sxs-lookup"><span data-stu-id="1e287-124">Interfaces can be marked with the TYPEFLAG\_PROXY flag to indicate they will be using a proxy/stub dynamic link library.</span></span> <span data-ttu-id="1e287-125">此旗標指定當 typelib 未註冊時，不應該取消註冊 typelib proxy。</span><span class="sxs-lookup"><span data-stu-id="1e287-125">This flag specifies the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="1e287-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e287-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e287-127">**使用 MIDL 產生類型程式庫**</span><span class="sxs-lookup"><span data-stu-id="1e287-127">**Generating a Type Library with MIDL**</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="1e287-128">**雙**</span><span class="sxs-lookup"><span data-stu-id="1e287-128">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="1e287-129">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="1e287-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 