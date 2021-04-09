---
title: uuid 屬性
description: '\ Uuid \ 介面屬性會指定 (UUID) 的通用唯一識別碼，該識別碼會指派給介面，並將它與其他介面區別。'
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- uuid 屬性 MIDL
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678556"
---
# <a name="uuid-attribute"></a><span data-ttu-id="e9ece-104">uuid 屬性</span><span class="sxs-lookup"><span data-stu-id="e9ece-104">uuid attribute</span></span>

<span data-ttu-id="e9ece-105">**\[ Uuid \]** 介面屬性會指定 (uuid) 的通用唯一識別碼，該識別碼會指派給介面，並將它與其他介面區別。</span><span class="sxs-lookup"><span data-stu-id="e9ece-105">The **\[uuid\]** interface attribute designates a universally unique identifier (UUID) that is assigned to the interface and that distinguishes it from other interfaces.</span></span>

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a><span data-ttu-id="e9ece-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9ece-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ece-107">*字串-uuid*</span><span class="sxs-lookup"><span data-stu-id="e9ece-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ece-108">指定一個字串，其中包含8個十六進位數位，後面接著連字號，再接著三個4個十六進位數位的群組，後面接著連字號，再接著12個十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="e9ece-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="e9ece-109">您可以用引號括住 UUID 字串，但使用 MIDL 編譯器參數 [**/osf**](-osf.md)時除外。</span><span class="sxs-lookup"><span data-stu-id="e9ece-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9ece-110">備註</span><span class="sxs-lookup"><span data-stu-id="e9ece-110">Remarks</span></span>

<span data-ttu-id="e9ece-111">執行時間程式庫會使用 **\[ uuid \]** 屬性指定的介面 UUID，以協助建立用戶端和伺服器應用程式之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="e9ece-111">The run-time library uses the interface UUID that the **\[uuid\]** attribute designates to help establish communication between the client and server applications.</span></span> <span data-ttu-id="e9ece-112">**\[ Uuid \]** 屬性可以出現在 RPC 介面或 COM 介面的介面屬性清單中。</span><span class="sxs-lookup"><span data-stu-id="e9ece-112">The **\[uuid\]** attribute can appear in the interface attribute list for either an RPC interface or a COM interface.</span></span>

<span data-ttu-id="e9ece-113">若為 RPC 介面，介面屬性清單必須包含 **\[ uuid \]** 屬性或 **\[** [**區域**](local.md) **\]** 屬性，而您所選擇的屬性必須正好發生一次。</span><span class="sxs-lookup"><span data-stu-id="e9ece-113">For an RPC interface, the interface attribute list must include either the **\[uuid\]** attribute or the **\[**[**local**](local.md)**\]** attribute, and the one you choose must occur exactly once.</span></span> <span data-ttu-id="e9ece-114">如果清單包含 **\[ uuid \]** 屬性，它也可以包含 **\[** [**version**](version.md) **\]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e9ece-114">If the list includes the **\[uuid\]** attribute, it can also include the **\[**[**version**](version.md)**\]** attribute.</span></span>

<span data-ttu-id="e9ece-115">針對 (物件介面屬性識別的 COM 介面 **\[** [](object.md) **\]**) ，介面屬性清單必須包含 **\[ uuid \]** 屬性，但不能包含 **\[ version \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e9ece-115">For a COM interface (identified by the **\[**[**object**](object.md)**\]** interface attribute), the interface attribute list must include the **\[uuid\]** attribute, but it cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="e9ece-116">COM 介面的清單可以包含 **\[ 本機 \]** 屬性，即使 **\[ uuid \]** 屬性存在也一樣。</span><span class="sxs-lookup"><span data-stu-id="e9ece-116">The list for a COM interface can include the **\[local\]** attribute even though the **\[uuid\]** attribute is present.</span></span>

<span data-ttu-id="e9ece-117">Microsoft RPC 支援 DCE IDL 的延伸模組，可讓 UUID 以雙引號括住 ( "" "" ) 。</span><span class="sxs-lookup"><span data-stu-id="e9ece-117">Microsoft RPC supports an extension to DCE IDL that allows the UUID to be enclosed in double quotation marks ("" "").</span></span> <span data-ttu-id="e9ece-118">以引號括住的表單對於將 UUID 數位解讀為浮點數的 C 編譯器預處理器是必要的。</span><span class="sxs-lookup"><span data-stu-id="e9ece-118">The quoted form is needed for C-compiler preprocessors that interpret UUID numbers as floating-point numbers.</span></span>

<span data-ttu-id="e9ece-119">所有 UUID 值都應該是電腦產生的，以確保唯一性。</span><span class="sxs-lookup"><span data-stu-id="e9ece-119">All UUID values should be computer-generated to guarantee uniqueness.</span></span> <span data-ttu-id="e9ece-120">使用 Uuidgen.exe 公用程式來產生唯一的 UUID 值。</span><span class="sxs-lookup"><span data-stu-id="e9ece-120">Use the Uuidgen utility to generate unique UUID values.</span></span>

<span data-ttu-id="e9ece-121">介面的 UUID 和版本號碼會用來判斷用戶端是否可以系結至伺服器。</span><span class="sxs-lookup"><span data-stu-id="e9ece-121">The UUID and version numbers of the interface are used to determine whether the client can bind to the server.</span></span> <span data-ttu-id="e9ece-122">若要讓用戶端系結至伺服器，在用戶端和伺服器介面中指定的 UUID 必須相同。</span><span class="sxs-lookup"><span data-stu-id="e9ece-122">For the client to bind to the server, the UUID specified in the client and server interfaces must be the same.</span></span>

<span data-ttu-id="e9ece-123">請注意，沒有屬性的介面可以匯入基底 IDL 檔案中。</span><span class="sxs-lookup"><span data-stu-id="e9ece-123">Note that an interface without attributes can be imported into a base IDL file.</span></span> <span data-ttu-id="e9ece-124">不過，介面必須只包含沒有任何程式的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e9ece-124">However, the interface must contain only datatypes with no procedures.</span></span> <span data-ttu-id="e9ece-125">如果介面中包含一個程式，則必須指定 local 或 UUID 屬性。</span><span class="sxs-lookup"><span data-stu-id="e9ece-125">If even one procedure is contained in the interface, a local or UUID attribute must be specified.</span></span>

## <a name="examples"></a><span data-ttu-id="e9ece-126">範例</span><span class="sxs-lookup"><span data-stu-id="e9ece-126">Examples</span></span>

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a><span data-ttu-id="e9ece-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9ece-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ece-128"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="e9ece-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e9ece-129">**介面**</span><span class="sxs-lookup"><span data-stu-id="e9ece-129">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="e9ece-130">**當地**</span><span class="sxs-lookup"><span data-stu-id="e9ece-130">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="e9ece-131">**物件**</span><span class="sxs-lookup"><span data-stu-id="e9ece-131">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="e9ece-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="e9ece-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="e9ece-133">**版本**</span><span class="sxs-lookup"><span data-stu-id="e9ece-133">**version**</span></span>](version.md)
</dt> </dl>

 

 




