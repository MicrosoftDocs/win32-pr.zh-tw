---
title: transmit_as 屬性
description: '\ 傳輸 \_ as \ 屬性會指示編譯器將型別識別碼（用戶端和伺服器應用程式操作的呈現型別）與傳送的型別 xmit 類型產生關聯。'
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as 屬性 MIDL
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec0cba27e994f7d77d441aef7bb783cad71cbad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969699"
---
# <a name="transmit_as-attribute"></a><span data-ttu-id="5ea32-104">傳輸 \_ 為屬性</span><span class="sxs-lookup"><span data-stu-id="5ea32-104">transmit\_as attribute</span></span>

<span data-ttu-id="5ea32-105">[ **\[ 傳輸 \_ 為 \]** ] 屬性會指示編譯器建立 \*\*type-id \* \* \*\* 的關聯，這是用戶端和伺服器應用程式操作的呈現型別，且具有傳輸類型 **xmit 類型。**</span><span class="sxs-lookup"><span data-stu-id="5ea32-105">The **\[transmit\_as\]** attribute instructs the compiler to associate \**type-id\*\*\*,* which is a presented type that client and server applications manipulate, with a transmitted type **xmit-type.**</span></span>

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a><span data-ttu-id="5ea32-106">參數</span><span class="sxs-lookup"><span data-stu-id="5ea32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea32-107">*xmit-類型*</span><span class="sxs-lookup"><span data-stu-id="5ea32-107">*xmit-type*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea32-108">指定在用戶端與伺服器之間傳輸的資料類型。</span><span class="sxs-lookup"><span data-stu-id="5ea32-108">Specifies the data type that is transmitted between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="5ea32-109">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="5ea32-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea32-110">指定套用至類型的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="5ea32-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="5ea32-111">有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**字串**](string.md) **\]** 並 **\[** [**忽略**](ignore.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="5ea32-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="5ea32-112">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="5ea32-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="5ea32-113">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="5ea32-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea32-114">指定 [基底類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ea32-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="5ea32-115">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="5ea32-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="5ea32-116">*宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="5ea32-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea32-117">指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="5ea32-117">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="5ea32-118">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="5ea32-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="5ea32-119">宣告子 *清單* 包含一或多個以逗號分隔的宣告子。</span><span class="sxs-lookup"><span data-stu-id="5ea32-119">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="5ea32-120">函式宣告子中的參數宣告子（例如參數名稱）是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="5ea32-120">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> <dt>

<span data-ttu-id="5ea32-121">*類型識別碼*</span><span class="sxs-lookup"><span data-stu-id="5ea32-121">*type-id*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea32-122">指定呈現給用戶端和伺服器應用程式的資料類型名稱。</span><span class="sxs-lookup"><span data-stu-id="5ea32-122">Specifies the name of the data type that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ea32-123">備註</span><span class="sxs-lookup"><span data-stu-id="5ea32-123">Remarks</span></span>

<span data-ttu-id="5ea32-124">若要使用 **\[ 傳輸 \_ 為 \]** 屬性，使用者必須提供在所呈現的和傳輸的類型之間轉換資料的常式; 這些常式也必須釋放用來保存轉換資料的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5ea32-124">To use the **\[transmit\_as\]** attribute, the user must supply routines that convert data between the presented and the transmitted types; these routines must also free memory used to hold the converted data.</span></span> <span data-ttu-id="5ea32-125">[ **\[ 傳輸 \_ 為 \]** ] 屬性會指示存根呼叫使用者提供的轉換常式。</span><span class="sxs-lookup"><span data-stu-id="5ea32-125">The **\[transmit\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="5ea32-126">傳送的型別 *xmit 類型* 必須解析為 MIDL 基底類型、預先定義的類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ea32-126">The transmitted type *xmit-type* must resolve to a MIDL base type, predefined type, or a type identifier.</span></span> <span data-ttu-id="5ea32-127">如需詳細資訊，請參閱 [MIDL 基底類型](midl-base-types.md)。</span><span class="sxs-lookup"><span data-stu-id="5ea32-127">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="5ea32-128">使用者必須提供下列常式。</span><span class="sxs-lookup"><span data-stu-id="5ea32-128">The user must supply the following routines.</span></span>



| <span data-ttu-id="5ea32-129">常式名稱</span><span class="sxs-lookup"><span data-stu-id="5ea32-129">Routine name</span></span>              | <span data-ttu-id="5ea32-130">Description</span><span class="sxs-lookup"><span data-stu-id="5ea32-130">Description</span></span>                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea32-131">*類型識別碼 \* \* \* \_ 至 \_ xmit*\*</span><span class="sxs-lookup"><span data-stu-id="5ea32-131">*type-id\*\*\*\_to\_xmit*\*</span></span>   | <span data-ttu-id="5ea32-132">將資料從呈現的型別轉換成傳送的型別。</span><span class="sxs-lookup"><span data-stu-id="5ea32-132">Converts data from the presented type to the transmitted type.</span></span> <span data-ttu-id="5ea32-133">這個常式會為傳送的型別和傳送的型別中的指標所參考的任何資料，配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="5ea32-133">This routine allocates memory for the transmitted type and for any data referenced by pointers in the transmitted type.</span></span>                            |
| <span data-ttu-id="5ea32-134">*\_xmit 中的類型識別碼 \* \* \_*\*</span><span class="sxs-lookup"><span data-stu-id="5ea32-134">*type-id\*\*\*\_from\_xmit*\*</span></span> | <span data-ttu-id="5ea32-135">將資料從傳送的型別轉換成呈現的型別。</span><span class="sxs-lookup"><span data-stu-id="5ea32-135">Converts data from the transmitted type to the presented type.</span></span> <span data-ttu-id="5ea32-136">此常式負責針對呈現類型中的指標所參考的資料，配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="5ea32-136">This routine is responsible for allocating memory for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="5ea32-137">RPC 會為類型本身配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="5ea32-137">RPC allocates memory for the type itself.</span></span> |
| <span data-ttu-id="5ea32-138">*類型識別碼 \* \* \* \_ 免費 \_ inst*\*</span><span class="sxs-lookup"><span data-stu-id="5ea32-138">*type-id\*\*\*\_free\_inst*\*</span></span> | <span data-ttu-id="5ea32-139">釋出配置給所呈現型別中指標所參考之資料的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5ea32-139">Frees memory allocated for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="5ea32-140">RPC 會釋出類型本身的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5ea32-140">RPC frees memory for the type itself.</span></span>                                                                                               |
| <span data-ttu-id="5ea32-141">*類型識別碼 \* \* \* \_ 免費 \_ xmit*\*</span><span class="sxs-lookup"><span data-stu-id="5ea32-141">*type-id\*\*\*\_free\_xmit*\*</span></span> | <span data-ttu-id="5ea32-142">釋放呼叫端用來傳送的儲存體，以及傳送型別中指標所參考的資料。</span><span class="sxs-lookup"><span data-stu-id="5ea32-142">Frees storage used by the caller for the transmitted type and for data referenced by pointers in the transmitted type.</span></span>                                                                                            |



 

 

<span data-ttu-id="5ea32-143">用戶端 stub 會呼叫 \*\_ \_ xmit \* 的型別 id \* \*\*\* 來為傳輸的型別配置空間，以及將資料轉譯成 xmit 類型的物件 *。*</span><span class="sxs-lookup"><span data-stu-id="5ea32-143">The client stub calls *type-id\*\*\*\_to\_xmit*\* to allocate space for the transmitted type and to translate the data into objects of type *xmit-type.*</span></span> <span data-ttu-id="5ea32-144">伺服器 stub 會為原始資料類型配置空間，並 \*\_ 從 \_ xmit \* 呼叫類型識別碼 \* \* \*\*，以將資料從其傳送的類型轉譯為呈現的型別。</span><span class="sxs-lookup"><span data-stu-id="5ea32-144">The server stub allocates space for the original data type and calls *type-id\*\*\*\_from\_xmit*\* to translate the data from its transmitted type to the presented type.</span></span>

<span data-ttu-id="5ea32-145">從應用程式程式碼傳回時，伺服器 stub 會呼叫 \*類型識別碼 \* \* \* \_ free \_ inst\*\*，以在伺服器端解除配置 *型別識別碼* 的儲存體。</span><span class="sxs-lookup"><span data-stu-id="5ea32-145">Upon return from the application code, the server stub calls *type-id\*\*\*\_free\_inst*\* to deallocate the storage for *type-id* on the server side.</span></span> <span data-ttu-id="5ea32-146">用戶端 stub 會呼叫 \*類型 id \* \* \* \_ free \_ xmit\*\*，以在用戶端上解除配置 *xmit 類型* 的儲存體。</span><span class="sxs-lookup"><span data-stu-id="5ea32-146">The client stub calls *type-id\*\*\*\_free\_xmit*\* to deallocate the *xmit-type* storage on the client side.</span></span>

<span data-ttu-id="5ea32-147">下列類型不能有 **\[ 傳輸 \_ 為 \]** 屬性：</span><span class="sxs-lookup"><span data-stu-id="5ea32-147">The following types cannot have a **\[transmit\_as\]** attribute:</span></span>

-   <span data-ttu-id="5ea32-148">內容會以 **\[** [**內容 \_ 處理**](context-handle.md)程式類型屬性和型別來處理 (型別 **\]** ，而這些型別是用來當做具有 **\[ 內容 \_ 控制碼 \]** 屬性的參數) </span><span class="sxs-lookup"><span data-stu-id="5ea32-148">Context handles (types with the **\[**[**context\_handle**](context-handle.md)**\]** type attribute and types that are used as parameters with the **\[context\_handle\]** attribute)</span></span>
-   <span data-ttu-id="5ea32-149">管道或衍生自管道的類型</span><span class="sxs-lookup"><span data-stu-id="5ea32-149">Types that are pipes or derived from pipes</span></span>
-   <span data-ttu-id="5ea32-150">當做管道定義之基底類型使用的資料類型</span><span class="sxs-lookup"><span data-stu-id="5ea32-150">Data types that are used as the base type of a pipe definition</span></span>
-   <span data-ttu-id="5ea32-151">指標或解析為指標的參數</span><span class="sxs-lookup"><span data-stu-id="5ea32-151">Parameters that are pointers or resolve to pointers</span></span>
-   <span data-ttu-id="5ea32-152">符合一致性、變化或開放陣列的參數</span><span class="sxs-lookup"><span data-stu-id="5ea32-152">Parameters that are conformant, varying, or open arrays</span></span>
-   <span data-ttu-id="5ea32-153">包含符合標準陣列的結構</span><span class="sxs-lookup"><span data-stu-id="5ea32-153">Structures that contain conformant arrays</span></span>
-   <span data-ttu-id="5ea32-154">預先定義的類型 [**控制碼 \_ t**](handle-t.md)、 [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="5ea32-154">The predefined type [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>

<span data-ttu-id="5ea32-155">傳送的類型必須符合下列限制：</span><span class="sxs-lookup"><span data-stu-id="5ea32-155">Types that are transmitted must conform to the following restrictions:</span></span>

-   <span data-ttu-id="5ea32-156">它們不得為指標或包含指標。</span><span class="sxs-lookup"><span data-stu-id="5ea32-156">They must not be pointers or contain pointers.</span></span>
-   <span data-ttu-id="5ea32-157">它們不得為管道或包含管道。</span><span class="sxs-lookup"><span data-stu-id="5ea32-157">They must not be pipes or contain pipes.</span></span>

## <a name="examples"></a><span data-ttu-id="5ea32-158">範例</span><span class="sxs-lookup"><span data-stu-id="5ea32-158">Examples</span></span>

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a><span data-ttu-id="5ea32-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ea32-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea32-160">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="5ea32-160">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="5ea32-161">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="5ea32-161">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="5ea32-162">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="5ea32-162">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="5ea32-163">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="5ea32-163">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="5ea32-164">**處理**</span><span class="sxs-lookup"><span data-stu-id="5ea32-164">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="5ea32-165">**處理 \_ t**</span><span class="sxs-lookup"><span data-stu-id="5ea32-165">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="5ea32-166"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="5ea32-166">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="5ea32-167">**忽略**</span><span class="sxs-lookup"><span data-stu-id="5ea32-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="5ea32-168">**ptr**</span><span class="sxs-lookup"><span data-stu-id="5ea32-168">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="5ea32-169">**ref**</span><span class="sxs-lookup"><span data-stu-id="5ea32-169">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="5ea32-170">**字串**</span><span class="sxs-lookup"><span data-stu-id="5ea32-170">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="5ea32-171">**結構**</span><span class="sxs-lookup"><span data-stu-id="5ea32-171">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="5ea32-172">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="5ea32-172">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="5ea32-173">**著**</span><span class="sxs-lookup"><span data-stu-id="5ea32-173">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="5ea32-174">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="5ea32-174">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="5ea32-175">**獨特**</span><span class="sxs-lookup"><span data-stu-id="5ea32-175">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="5ea32-176">**void**</span><span class="sxs-lookup"><span data-stu-id="5ea32-176">**void**</span></span>](void.md)
</dt> </dl>

 

 