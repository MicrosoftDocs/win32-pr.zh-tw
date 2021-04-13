---
title: Transmit_as 屬性
description: '\ 傳輸 \_ as \ 屬性提供一種方式來控制資料封送處理，而不需要擔心在低層級 \ 郵件上封送處理資料，也就是不需要擔心資料大小或在異類環境中交換的位元組。'
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- 遠端程序呼叫 RPC、屬性、transmit_as
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376108"
---
# <a name="the-transmit_as-attribute"></a><span data-ttu-id="003e8-105">傳輸 \_ 為屬性</span><span class="sxs-lookup"><span data-stu-id="003e8-105">The transmit\_as Attribute</span></span>

<span data-ttu-id="003e8-106">[ **\[** [**傳輸 \_ 為**](/windows/desktop/Midl/transmit-as)] **\]** 屬性可讓您控制資料封送處理，而不需要擔心較低層級的封送處理資料，也就是不需要擔心資料大小或在異類環境中交換的位元組。</span><span class="sxs-lookup"><span data-stu-id="003e8-106">The **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute offers a way to control data marshaling without worrying about marshaling data at a low level—that is, without worrying about data sizes or byte swapping in a heterogeneous environment.</span></span> <span data-ttu-id="003e8-107">藉由讓您減少透過網路傳輸的資料量，[ **\[ 傳輸 \_ 為 \]** ] 屬性可以讓您的應用程式更有效率。</span><span class="sxs-lookup"><span data-stu-id="003e8-107">By letting you reduce the amount of data transmitted over the network, the **\[transmit\_as\]** attribute can make your application more efficient.</span></span>

<span data-ttu-id="003e8-108">您可以使用 [ **\[ 傳輸 \_ 為 \]** ] 屬性來指定 RPC 存根將透過網路傳輸的資料類型，而不是使用應用程式所提供的資料類型。</span><span class="sxs-lookup"><span data-stu-id="003e8-108">You use the **\[transmit\_as\]** attribute to specify a data type that the RPC stubs will transmit over the network instead of using the data type provided by the application.</span></span> <span data-ttu-id="003e8-109">您提供的常式會將資料類型轉換為用於傳輸的型別和型別。</span><span class="sxs-lookup"><span data-stu-id="003e8-109">You supply routines that convert the data type to and from the type that is used for transmission.</span></span> <span data-ttu-id="003e8-110">您也必須提供常式來釋出用於資料類型和傳輸類型的記憶體。</span><span class="sxs-lookup"><span data-stu-id="003e8-110">You must also supply routines to free the memory used for the data type and the transmitted type.</span></span> <span data-ttu-id="003e8-111">例如，下列會將 **xmit \_ 型** 別定義為針對指定為屬於類型 **type \_ 規格** 的所有應用程式資料所傳送的資料類型：</span><span class="sxs-lookup"><span data-stu-id="003e8-111">For example, the following defines **xmit\_type** as the data type transmitted for all application data specified as being of type **type\_spec**:</span></span>

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

<span data-ttu-id="003e8-112">下表描述四個程式設計人員提供的常式名稱。</span><span class="sxs-lookup"><span data-stu-id="003e8-112">The following table describes the four programmer-supplied routine names.</span></span> <span data-ttu-id="003e8-113">**Type** 是應用程式已知的資料類型，而 **xmit \_ 類型** 是用於傳輸的資料類型。</span><span class="sxs-lookup"><span data-stu-id="003e8-113">**Type** is the data type known to the application, and **xmit\_type** is the data type used for transmission.</span></span>



| <span data-ttu-id="003e8-114">常式傳回的值</span><span class="sxs-lookup"><span data-stu-id="003e8-114">Routine</span></span>                                                 | <span data-ttu-id="003e8-115">Description</span><span class="sxs-lookup"><span data-stu-id="003e8-115">Description</span></span>                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="003e8-116">**輸入 \_ 至 \_ xmit**</span><span class="sxs-lookup"><span data-stu-id="003e8-116">**type\_to\_xmit**</span></span>](the-type-to-xmit-function.md)     | <span data-ttu-id="003e8-117">配置傳送型別的物件，並從應用程式類型轉換成透過網路傳送的型別， (呼叫端和稱為) 的物件。</span><span class="sxs-lookup"><span data-stu-id="003e8-117">Allocates an object of the transmitted type and converts from application type to type transmitted over the network (caller and object called).</span></span> |
| [<span data-ttu-id="003e8-118">**\_從 \_ xmit 輸入**</span><span class="sxs-lookup"><span data-stu-id="003e8-118">**Type\_from\_xmit**</span></span>](the-type-from-xmit-function.md) | <span data-ttu-id="003e8-119">從傳輸型別轉換為應用程式類型 (呼叫端和稱為) 的物件。</span><span class="sxs-lookup"><span data-stu-id="003e8-119">Converts from transmitted type to application type (caller and object called).</span></span>                                                                  |
| [<span data-ttu-id="003e8-120">**輸入 \_ 免費 \_ inst**</span><span class="sxs-lookup"><span data-stu-id="003e8-120">**Type\_free\_inst**</span></span>](the-type-free-inst-function.md) | <span data-ttu-id="003e8-121">釋出應用程式類型所使用的資源 (只呼叫) 的物件。</span><span class="sxs-lookup"><span data-stu-id="003e8-121">Frees resources used by the application type (object called only).</span></span>                                                                              |
| [<span data-ttu-id="003e8-122">**輸入 \_ 免費 \_ xmit**</span><span class="sxs-lookup"><span data-stu-id="003e8-122">**Type\_free\_xmit**</span></span>](the-type-free-xmit-function.md) | <span data-ttu-id="003e8-123">釋出型別傳回的儲存空間， \*\*\*\*\*\_\*\*\* 以 \_ xmit\*\* 常式 (呼叫端和稱為) 的物件。</span><span class="sxs-lookup"><span data-stu-id="003e8-123">Frees storage returned by the **type ***\_*** to\_xmit** routine (caller and object called).</span></span>                                                      |



 

<span data-ttu-id="003e8-124">除了這四個程式設計人員提供的函式以外，應用程式不會操作傳輸的型別。</span><span class="sxs-lookup"><span data-stu-id="003e8-124">Other than by these four programmer-supplied functions, the transmitted type is not manipulated by the application.</span></span> <span data-ttu-id="003e8-125">傳送的類型只定義為透過網路移動資料。</span><span class="sxs-lookup"><span data-stu-id="003e8-125">The transmitted type is defined only to move data over the network.</span></span> <span data-ttu-id="003e8-126">將資料轉換為應用程式所使用的型別之後，會釋出傳輸類型所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="003e8-126">After the data is converted to the type used by the application, the memory used by the transmitted type is freed.</span></span>

<span data-ttu-id="003e8-127">這些程式設計人員提供的常式是由用戶端或伺服器應用程式根據方向屬性提供。</span><span class="sxs-lookup"><span data-stu-id="003e8-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span> <span data-ttu-id="003e8-128">如果參數為 **\[** [](/windows/desktop/Midl/in) **\]** ，則用戶端會傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="003e8-128">If the parameter is **\[**[**in**](/windows/desktop/Midl/in)**\]** only, the client transmits to the server.</span></span> <span data-ttu-id="003e8-129">用戶端必須 **要有型別 \_ 才能 \_ xmit** 和 **輸入 \_ free \_ xmit** 函數。</span><span class="sxs-lookup"><span data-stu-id="003e8-129">The client needs the **type\_to\_xmit** and **type\_free\_xmit** functions.</span></span> <span data-ttu-id="003e8-130">伺服器需要 **\_ 來自 \_ xmit 的類型** ，並 **輸入 \_ free \_ inst** 函數。</span><span class="sxs-lookup"><span data-stu-id="003e8-130">The server needs the **type\_from\_xmit** and **type\_free\_inst** functions.</span></span> <span data-ttu-id="003e8-131">針對 **\[** [**out**](/windows/desktop/Midl/out-idl) **\]** 參數，伺服器會傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="003e8-131">For an **\[**[**out**](/windows/desktop/Midl/out-idl)**\]**-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="003e8-132">當用戶端程式必須 **\_ 從 \_ xmit** 函式提供型別時，伺服器應用程式必須將型別實 **\_ \_ xmit** 和 **輸入 \_ free \_ xmit** 函數。</span><span class="sxs-lookup"><span data-stu-id="003e8-132">The server application must implement the **type\_to\_xmit** and **type\_free\_xmit** functions, while the client program must supply the **type\_from\_xmit** function.</span></span> <span data-ttu-id="003e8-133">針對暫存 **xmit \_ 型** 別物件，存根會呼叫 **類型 ***\_*** free \_ xmit** ，以釋出對 **\_ \_ xmit** 的呼叫所配置的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="003e8-133">For the temporary **xmit\_type** objects, the stub will call **type ***\_*** free\_xmit** to free any memory allocated by a call to **type\_to\_xmit**.</span></span>

<span data-ttu-id="003e8-134">某些指導方針適用于應用程式類型實例。</span><span class="sxs-lookup"><span data-stu-id="003e8-134">Certain guidelines apply to the application type instance.</span></span> <span data-ttu-id="003e8-135">如果應用程式類型是指標或包含指標，則 \_ **\_ xmit** 常式的型別必須配置記憶體給指標指向 (應用程式類型物件本身是由存根) 的一般方式來操作。</span><span class="sxs-lookup"><span data-stu-id="003e8-135">If the application type is a pointer or contains a pointer, then the **type**\_**from\_xmit** routine must allocate memory for the data that the pointers point to (the application type object itself is manipulated by the stub in the usual way).</span></span>

<span data-ttu-id="003e8-136">針對包含 **\[ 傳輸 \_ 為 \]** 屬性之類型的 **\[ out \]** 和 **\[ in、out \] out \]** 參數或其中一個元件，系統 \_ 會自動為具有屬性的資料物件呼叫 **free \_ inst** 常式類型。</span><span class="sxs-lookup"><span data-stu-id="003e8-136">For **\[out\]** and **\[in, out\] out\]** parameters, or one of their components, of a type that contains the **\[transmit\_as\]** attribute, the **type**\_**free\_inst** routine is automatically called for the data objects that have the attribute.</span></span> <span data-ttu-id="003e8-137">對於 **in** 參數，  \_ 只有在將 **\[ \_ \] as** 屬性套用至參數時，才會呼叫 type **free \_ inst** 常式。</span><span class="sxs-lookup"><span data-stu-id="003e8-137">For **in** parameters, the **type**\_**free\_inst** routine is called only if the **\[transmit\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="003e8-138">如果屬性已套用至參數的元件，則 \_ 不會呼叫類型 **free \_ inst** 常式。</span><span class="sxs-lookup"><span data-stu-id="003e8-138">If the attribute has been applied to the components of the parameter, the **type**\_**free\_inst** routine is not called.</span></span> <span data-ttu-id="003e8-139">對於內嵌資料和最多一次的呼叫，不會釋出呼叫 (與最上層屬性) （僅限 **in** 參數）相關。</span><span class="sxs-lookup"><span data-stu-id="003e8-139">There are no freeing calls for the embedded data and at-most-one call (related to the top-level attribute) for an **in** only parameter.</span></span>

<span data-ttu-id="003e8-140">用戶端和伺服器都必須提供這四個函式，才能有效使用 MIDL 2.0。</span><span class="sxs-lookup"><span data-stu-id="003e8-140">Effective with MIDL 2.0, both client and server must supply all four functions.</span></span> <span data-ttu-id="003e8-141">例如，連結清單可以傳輸為大小的陣列。</span><span class="sxs-lookup"><span data-stu-id="003e8-141">For example, a linked list can be transmitted as a sized array.</span></span> <span data-ttu-id="003e8-142">**\_ \_ Xmit** 常式的類型會引導連結清單，並將已排序的資料複製到陣列中。</span><span class="sxs-lookup"><span data-stu-id="003e8-142">The **type\_to\_xmit** routine walks the linked list and copies the ordered data into an array.</span></span> <span data-ttu-id="003e8-143">陣列元素已排序，因此不需要傳送與清單結構相關聯的許多指標。</span><span class="sxs-lookup"><span data-stu-id="003e8-143">The array elements are ordered so that the many pointers associated with the list structure do not have to be transmitted.</span></span> <span data-ttu-id="003e8-144">**\_ \_ Xmit** 常式的型別會讀取陣列，並將它的元素放入連結清單結構中。</span><span class="sxs-lookup"><span data-stu-id="003e8-144">The **type\_from\_xmit** routine reads the array and puts its elements into a linked-list structure.</span></span>

<span data-ttu-id="003e8-145">雙連結清單 (雙重 \_ 連結 \_ 清單) 包含前一個和下一個清單元素的資料和指標：</span><span class="sxs-lookup"><span data-stu-id="003e8-145">The double-linked list (DOUBLE\_LINK\_LIST) includes data and pointers to the previous and next list elements:</span></span>

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

<span data-ttu-id="003e8-146">**\[**[**傳輸 \_ as**](/windows/desktop/Midl/transmit-as) **\]** 屬性可以用來透過網路以陣列形式傳送，而不是傳送複雜結構。</span><span class="sxs-lookup"><span data-stu-id="003e8-146">Rather than shipping the complex structure, the **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute can be used to send it over the network as an array.</span></span> <span data-ttu-id="003e8-147">陣列中的專案順序會以較低的成本保留清單中元素的順序：</span><span class="sxs-lookup"><span data-stu-id="003e8-147">The sequence of items in the array retains the ordering of the elements in the list at a lower cost:</span></span>

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

<span data-ttu-id="003e8-148">[ **\[ 傳輸 \_ 為 \]** ] 屬性會出現在 IDL 檔案中：</span><span class="sxs-lookup"><span data-stu-id="003e8-148">The **\[transmit\_as\]** attribute appears in the IDL file:</span></span>

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

<span data-ttu-id="003e8-149">在下列範例中， **ModifyListProc** 會將類型為 DOUBLE 連結類型的參數定義 \_ \_ 為 **\[ in、 \] out** 參數：</span><span class="sxs-lookup"><span data-stu-id="003e8-149">In the following example, **ModifyListProc** defines the parameter of type DOUBLE\_LINK\_TYPE as an **\[in, out\]** parameter:</span></span>

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

<span data-ttu-id="003e8-150">四個程式設計人員定義的函式會在函式名稱中使用類型的名稱，並視需要使用所呈現和傳輸的類型作為參數類型：</span><span class="sxs-lookup"><span data-stu-id="003e8-150">The four programmer-defined functions use the name of the type in the function names, and use the presented and transmitted types as parameter types, as required:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 