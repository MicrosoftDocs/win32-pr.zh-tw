---
title: represent_as 屬性
description: '\ 代表 \_ as \ ACF 屬性會將目的語言 repr 類型中的命名區欄位型別與在用戶端和伺服器之間傳送的傳輸類型命名為-type 產生關聯。'
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as 屬性 MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022208"
---
# <a name="represent_as-attribute"></a><span data-ttu-id="79189-104">表示 \_ 為屬性</span><span class="sxs-lookup"><span data-stu-id="79189-104">represent\_as attribute</span></span>

<span data-ttu-id="79189-105">**\[ 代表 \_ as \]** ACF 屬性會將目的語言 *repr 類型* 中的命名區欄位型別與在用戶端和伺服器之間傳輸的傳輸類型 *命名為類型*。</span><span class="sxs-lookup"><span data-stu-id="79189-105">The **\[represent\_as\]** ACF attribute associates a named local type in the target language *repr-type* with a transfer type *named-type* that is transferred between client and server.</span></span>

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a><span data-ttu-id="79189-106">參數</span><span class="sxs-lookup"><span data-stu-id="79189-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79189-107">*命名類型*</span><span class="sxs-lookup"><span data-stu-id="79189-107">*named-type*</span></span> 
</dt> <dd>

<span data-ttu-id="79189-108">指定在用戶端與伺服器之間傳送的命名傳輸資料類型。</span><span class="sxs-lookup"><span data-stu-id="79189-108">Specifies the named transfer data type that is transferred between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="79189-109">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="79189-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="79189-110">指定套用至類型的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="79189-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="79189-111">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="79189-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="79189-112">*repr-類型*</span><span class="sxs-lookup"><span data-stu-id="79189-112">*repr-type*</span></span> 
</dt> <dd>

<span data-ttu-id="79189-113">以呈現給用戶端和伺服器應用程式的目的語言指定表示的區欄位型別。</span><span class="sxs-lookup"><span data-stu-id="79189-113">Specifies the represented local type in the target language that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79189-114">備註</span><span class="sxs-lookup"><span data-stu-id="79189-114">Remarks</span></span>

<span data-ttu-id="79189-115">當使用 **\[ 表示 \_ 為 \]** 時，您必須提供在本機與傳輸類型之間轉換的常式，以及用來保存轉換資料的可用記憶體。</span><span class="sxs-lookup"><span data-stu-id="79189-115">When using **\[represent\_as\]**, you must supply routines that convert between the local and the transfer types and that free memory used to hold the converted data.</span></span> <span data-ttu-id="79189-116">**\[ 代表 \_ as \]** 屬性會指示存根呼叫使用者提供的轉換常式。</span><span class="sxs-lookup"><span data-stu-id="79189-116">The **\[represent\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="79189-117">*已* 傳送的型別必須解析為 MIDL 基底類型、預先定義的類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="79189-117">The transferred type *named-type* must resolve to a MIDL base type, predefined type, or to a type identifier.</span></span> <span data-ttu-id="79189-118">如需詳細資訊，請參閱 [MIDL 基底類型](midl-base-types.md)。</span><span class="sxs-lookup"><span data-stu-id="79189-118">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="79189-119">您必須提供下列常式：</span><span class="sxs-lookup"><span data-stu-id="79189-119">You must supply the following routines:</span></span>



| <span data-ttu-id="79189-120">常式名稱</span><span class="sxs-lookup"><span data-stu-id="79189-120">Routine name</span></span>                   | <span data-ttu-id="79189-121">Description</span><span class="sxs-lookup"><span data-stu-id="79189-121">Description</span></span>                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79189-122">*\_ \_ 來自本機的命名類型 \* \* \* \_*\*</span><span class="sxs-lookup"><span data-stu-id="79189-122">*named\_type\*\*\*\_from\_local*\*</span></span> | <span data-ttu-id="79189-123">將資料從本機類型轉換為網路類型。</span><span class="sxs-lookup"><span data-stu-id="79189-123">Converts data from the local type to the network type.</span></span> <span data-ttu-id="79189-124">常式會配置網路資料類型的記憶體，包括網路資料類型中指標所參考之任何資料的記憶體。</span><span class="sxs-lookup"><span data-stu-id="79189-124">The routine allocates memory for the network data type, including memory for any data referenced by pointers in the network data type.</span></span>              |
| <span data-ttu-id="79189-125">*命名 \_ 類型 \* \* \* \_ 至 \_ 本機*\*</span><span class="sxs-lookup"><span data-stu-id="79189-125">*named\_type\*\*\*\_to\_local*\*</span></span>   | <span data-ttu-id="79189-126">將資料從網路類型轉換成區欄位型別。</span><span class="sxs-lookup"><span data-stu-id="79189-126">Converts data from the network type to the local type.</span></span> <span data-ttu-id="79189-127">常式負責為本機類型中的指標所參考的資料配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="79189-127">The routine is responsible for allocating memory for data referenced by pointers in the local type.</span></span> <span data-ttu-id="79189-128">RPC 會為本機類型本身配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="79189-128">RPC allocates memory for the local type itself.</span></span> |
| <span data-ttu-id="79189-129">*命名 \_ 類型 \* \* \* \_ 可用 \_ 本機*\*</span><span class="sxs-lookup"><span data-stu-id="79189-129">*named\_type\*\*\*\_free\_local*\*</span></span> | <span data-ttu-id="79189-130">釋出配置給本機類型之指標所參考之資料的記憶體。</span><span class="sxs-lookup"><span data-stu-id="79189-130">Frees memory allocated for data referenced by pointers in the local type.</span></span> <span data-ttu-id="79189-131">RPC 釋出類型本身的記憶體</span><span class="sxs-lookup"><span data-stu-id="79189-131">RPC frees memory for the type itself</span></span>                                                                                             |
| <span data-ttu-id="79189-132">*命名 \_ 類型 \* \* \* \_ 免費 \_ inst*\*</span><span class="sxs-lookup"><span data-stu-id="79189-132">*named\_type\*\*\*\_free\_inst*\*</span></span>  | <span data-ttu-id="79189-133">釋出為網路類型和網路類型本身的指標所參考的資料所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="79189-133">Frees memory allocated for the data referenced by pointers in the network type and for the network type itself.</span></span>                                                                                            |



 

<span data-ttu-id="79189-134">用戶端 stub 會 \*\_ 從 \_ 本機 \* 呼叫名為 type \* \*\*\*，以配置已傳送類型的空間，以及將資料從本機類型轉譯為網路類型。</span><span class="sxs-lookup"><span data-stu-id="79189-134">The client stub calls *named-type\*\*\*\_from\_local*\* to allocate space for the transmitted type and to translate the data from the local type to the network type.</span></span> <span data-ttu-id="79189-135">伺服器 stub 會配置原始資料類型的空間，並呼叫 \*名稱為 \* \* \* 的 \_ \_ 本機\*\*，將資料從網路類型轉譯為本機類型。</span><span class="sxs-lookup"><span data-stu-id="79189-135">The server stub allocates space for the original data type and calls *named-type\*\*\*\_to\_local*\* to translate the data from the network type to the local type.</span></span>

<span data-ttu-id="79189-136">從應用程式程式碼傳回時，用戶端和伺服器 stub 會呼叫 *指名型別 \* \* \* \_ free \_ inst*\* 來解除配置網路類型的儲存體。</span><span class="sxs-lookup"><span data-stu-id="79189-136">Upon return from the application code, the client and server stubs call *named-type\*\*\*\_free\_inst*\* to deallocate the storage for network type.</span></span> <span data-ttu-id="79189-137">用戶端 stub 會呼叫 *名為 type \* \* \* \_ free \_ local*\* 來解除配置常式所傳回的儲存區。</span><span class="sxs-lookup"><span data-stu-id="79189-137">The client stub calls *named-type\*\*\*\_free\_local*\* to deallocate storage returned by the routine.</span></span>

<span data-ttu-id="79189-138">下列類型不能有 **\[ 代表 \_ 做為 \]** 屬性：</span><span class="sxs-lookup"><span data-stu-id="79189-138">The following types cannot have a **\[represent\_as\]** attribute:</span></span>

-   <span data-ttu-id="79189-139">一致、變化或一致的陣列</span><span class="sxs-lookup"><span data-stu-id="79189-139">Conformant, varying, or conformant-varying arrays</span></span>
-   <span data-ttu-id="79189-140">結構，其中最後一個成員是一致的陣列 (一致的結構) </span><span class="sxs-lookup"><span data-stu-id="79189-140">Structures in which the last member is a conformant array (a conformant structure)</span></span>
-   <span data-ttu-id="79189-141">包含指標的指標或類型</span><span class="sxs-lookup"><span data-stu-id="79189-141">Pointers or types that contain a pointer</span></span>
-   <span data-ttu-id="79189-142">包含管道的管道或類型</span><span class="sxs-lookup"><span data-stu-id="79189-142">Pipes or types that contain pipes</span></span>
-   <span data-ttu-id="79189-143">用來作為管道基底類型的類型</span><span class="sxs-lookup"><span data-stu-id="79189-143">Types that are used as the base type for a pipe</span></span>
-   <span data-ttu-id="79189-144">預先定義的類型會 [**處理 \_ t**](handle-t.md)、 [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="79189-144">Predefined types [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>
-   <span data-ttu-id="79189-145">具有 [**\[ handle \]**](handle.md)屬性的類型</span><span class="sxs-lookup"><span data-stu-id="79189-145">Types that have the [**\[handle\]**](handle.md) attribute</span></span>

## <a name="examples"></a><span data-ttu-id="79189-146">範例</span><span class="sxs-lookup"><span data-stu-id="79189-146">Examples</span></span>

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a><span data-ttu-id="79189-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79189-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79189-148">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="79189-148">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="79189-149">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="79189-149">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="79189-150">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="79189-150">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="79189-151">**處理 \_ t**</span><span class="sxs-lookup"><span data-stu-id="79189-151">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="79189-152">**著**</span><span class="sxs-lookup"><span data-stu-id="79189-152">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="79189-153">**void**</span><span class="sxs-lookup"><span data-stu-id="79189-153">**void**</span></span>](void.md)
</dt> </dl>

 

 




