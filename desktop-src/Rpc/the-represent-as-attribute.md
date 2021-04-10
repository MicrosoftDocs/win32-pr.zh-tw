---
title: Represent_as 屬性
description: '\ 代表 \_ as \ 屬性可讓您指定特定可資料類型如何呈現給應用程式。'
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- 遠端程序呼叫 RPC、屬性、represent_as
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093183"
---
# <a name="the-represent_as-attribute"></a><span data-ttu-id="3c6c2-105">表示 \_ 為屬性</span><span class="sxs-lookup"><span data-stu-id="3c6c2-105">The represent\_as Attribute</span></span>

<span data-ttu-id="3c6c2-106">[ \[ [表示 \_ 為](/windows/desktop/Midl/represent-as)] \] 屬性可讓您指定特定的可資料類型如何呈現給應用程式。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-106">The \[ [represent\_as](/windows/desktop/Midl/represent-as)\] attribute lets you specify how a particular transmittable data type is represented to the application.</span></span> <span data-ttu-id="3c6c2-107">這是藉由針對已知的可類型指定表示類型的名稱，並提供轉換常式來完成。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-107">This is done by specifying the name of the represented type for a known transmittable type and supplying the conversion routines.</span></span> <span data-ttu-id="3c6c2-108">您也必須提供常式，才能釋放資料類型物件所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-108">You must also supply the routines to free the memory used by the data type objects.</span></span>

<span data-ttu-id="3c6c2-109">使用 **\[ 代表 \_ as \]** 屬性來呈現具有不同可能 untransmittable 資料類型的應用程式，而不是實際在用戶端與伺服器之間傳輸的類型。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-109">Use the **\[represent\_as\]** attribute to present an application with a different, possibly untransmittable, data type rather than the type that is actually transmitted between the client and server.</span></span> <span data-ttu-id="3c6c2-110">在 MIDL 編譯時，應用程式所操作的類型也可能是未知的。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-110">It is also possible that the type the application manipulates can be unknown at the time of MIDL compilation.</span></span> <span data-ttu-id="3c6c2-111">當您選擇定義完善的可類型時，您不需要擔心在異類環境中的資料標記法。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-111">When you choose a well-defined transmittable type, you need not be concerned about data representation in the heterogeneous environment.</span></span> <span data-ttu-id="3c6c2-112">**\[ 代表 \_ as \]** 屬性可以藉由減少透過網路傳輸的資料量，讓您的應用程式更有效率。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-112">The **\[represent\_as\]** attribute can make your application more efficient by reducing the amount of data transmitted over the network.</span></span>

<span data-ttu-id="3c6c2-113">**\[ 代表 \_ as \]** 屬性類似于 \[ [傳輸 \_ 為](/windows/desktop/Midl/transmit-as) \] 屬性。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-113">The **\[represent\_as\]** attribute is similar to the \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\] attribute.</span></span> <span data-ttu-id="3c6c2-114">不過，當 **\[ 傳輸 \_ 為 \]** 可讓您指定將用於傳輸的資料類型時， **\[ 表示 \_ 為 \]** 可讓您指定如何為應用程式表示資料類型。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-114">However, while **\[transmit\_as\]** lets you specify a data type that will be used for transmission, **\[represent\_as\]** lets you specify how a data type is represented for the application.</span></span> <span data-ttu-id="3c6c2-115">不需要在 MIDL 處理的檔案中定義表示的類型;您可以在使用 C 編譯器編譯存根的時候定義它。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-115">The represented type need not be defined in the MIDL processed files; it can be defined at the time the stubs are compiled with the C compiler.</span></span> <span data-ttu-id="3c6c2-116">若要這樣做，請使用 [應用程式佈建檔 ](the-application-configuration-file-acf-.md) 中的 include 指示詞 (ACF) 編譯適當的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-116">To do this, use the include directive in the [application configuration file (ACF)](the-application-configuration-file-acf-.md) to compile the appropriate header file.</span></span> <span data-ttu-id="3c6c2-117">例如，下列 ACF 會針對 **名為 \_ type** 的可類型，定義應用程式的本機類型， **repr \_ 類型**：</span><span class="sxs-lookup"><span data-stu-id="3c6c2-117">For example, the following ACF defines a type local to the application, **repr\_type**, for the transmittable type **named\_type:**</span></span>

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

<span data-ttu-id="3c6c2-118">下表描述四個程式設計人員提供的常式。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-118">The following table describes the four programmer-supplied routines.</span></span>



| <span data-ttu-id="3c6c2-119">常式傳回的值</span><span class="sxs-lookup"><span data-stu-id="3c6c2-119">Routine</span></span>                      | <span data-ttu-id="3c6c2-120">Description</span><span class="sxs-lookup"><span data-stu-id="3c6c2-120">Description</span></span>                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c6c2-121">**\_ \_ 來自本機的命名類型 \_**</span><span class="sxs-lookup"><span data-stu-id="3c6c2-121">**named\_type\_from\_local**</span></span> | <span data-ttu-id="3c6c2-122">配置網路類型的實例，並從本機類型轉換為網路類型。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-122">Allocates an instance of the network type and converts from the local type to the network type.</span></span>      |
| <span data-ttu-id="3c6c2-123">**命名 \_ 為 \_ local 的型別 \_**</span><span class="sxs-lookup"><span data-stu-id="3c6c2-123">**named\_type\_to\_local**</span></span>   | <span data-ttu-id="3c6c2-124">從網路類型轉換成區欄位型別。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-124">Converts from the network type to the local type.</span></span>                                                    |
| <span data-ttu-id="3c6c2-125">**命名 \_ 類型 \_ 可用 \_ 本機**</span><span class="sxs-lookup"><span data-stu-id="3c6c2-125">**named\_type\_free\_local**</span></span> | <span data-ttu-id="3c6c2-126">釋出呼叫所配置的記憶體 **\_ \_ 給 \_ 本機** 常式，但無法釋放類型本身。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-126">Frees memory allocated by a call to the **named\_type\_to\_local** routine, but not the type itself.</span></span> |
| <span data-ttu-id="3c6c2-127">**命名 \_ 類型 \_ free \_ inst**</span><span class="sxs-lookup"><span data-stu-id="3c6c2-127">**named\_type\_free\_inst**</span></span>  | <span data-ttu-id="3c6c2-128">釋出網路類型 (兩端) 的儲存體。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-128">Frees storage for the network type (both sides).</span></span>                                                     |



 

<span data-ttu-id="3c6c2-129">除了這四個由程式設計人員提供的常式之外，應用程式也不會操作命名的型別。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-129">Other than by these four programmer-supplied routines, the named type is not manipulated by the application.</span></span> <span data-ttu-id="3c6c2-130">應用程式可見的唯一類型是表示的類型。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-130">The only type visible to the application is the represented type.</span></span> <span data-ttu-id="3c6c2-131">應用程式會使用所表示的型別名稱，而不是編譯器所產生之原型和存根中的傳送型別名稱。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-131">The application uses the represented type name instead of the transmitted type name in the prototypes and stubs generated by the compiler.</span></span> <span data-ttu-id="3c6c2-132">您必須為雙方提供一組常式。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-132">You must supply the set of routines for both sides.</span></span>

<span data-ttu-id="3c6c2-133">針對暫時 **命名的 \_ 型** 別物件，存根會呼叫 **名為 \_ type \_ free \_ inst** ，以釋放 **\_ \_ 從 \_ 本機呼叫命名類型** 所配置的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-133">For temporary **named\_type** objects, the stub will call **named\_type\_free\_inst** to free any memory allocated by a call to **named\_type\_from\_local**.</span></span>

<span data-ttu-id="3c6c2-134">如果表示的類型是指標或包含指標，則在本機常式的 **命名 \_ 型 \_ \_** 別必須配置記憶體給指標指向 (表示型別物件本身的資料，而存根會以) 的一般方式操作。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-134">If the represented type is a pointer or contains a pointer, the **named\_type\_to\_local** routine must allocate memory for the data to which the pointers point (the represented type object itself is manipulated by the stub in the usual way).</span></span> <span data-ttu-id="3c6c2-135">若為 \[ [out](/windows/desktop/Midl/out-idl) \] 和 \[ [in](/windows/desktop/Midl/in)、out 的型別（ \] 包含 **\[ 代表 \_** 或其中一個元件的型別），就會針對包含屬性的資料物件，自動呼叫 **指名的型別 \_ \_ free \_ local** 常式。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-135">For \[ [out](/windows/desktop/Midl/out-idl)\] and \[ [in](/windows/desktop/Midl/in), out\] parameters of a type that contain **\[represent\_as** or one of its components, the **named\_type\_free\_local** routine is automatically called for the data objects that contain the attribute.</span></span> <span data-ttu-id="3c6c2-136">針對 **\[ in \]** 參數，只有當 **\[ 表示 \_ as \]** 屬性已套用至參數時，才會呼叫 **指名 \_ 型別 \_ free \_ local** 常式。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-136">For **\[in\]** parameters, the **named\_type\_free\_local** routine is called only if the **\[represent\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="3c6c2-137">如果屬性已套用至參數的元件，則不會呼叫 *\* \*\*\* \_ 免費的 \_ 本機*\* 常式。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-137">If the attribute has been applied to the components of the parameter, the *\*\*\*\*\_free\_local*\* routine is not called.</span></span> <span data-ttu-id="3c6c2-138">針對內嵌資料和最多一次的呼叫，不會呼叫釋出的常式， (與最上層屬性) **\[ \] （僅限** 參數）相關。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-138">Freeing routines are not called for the embedded data and at-most-once call (related to the top-level attribute) for an **\[in\]** only parameter.</span></span>

> [!Note]  
> <span data-ttu-id="3c6c2-139">您可以將 **\[ 傳輸 \_ as \]** 和 **\[ 表示為屬性（attribute \_ ） \]** 套用至相同的型別。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-139">It is possible to apply both the **\[transmit\_as\]** and **\[represent\_as\]** attributes to the same type.</span></span> <span data-ttu-id="3c6c2-140">封送處理資料時，會先套用 **\[ 表示 \_ 為 \]** 類型轉換，然後套用 **\[ 傳輸 \_ 作為 \]** 轉換。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-140">When marshaling data, the **\[represent\_as\]** type conversion is applied first and then the **\[transmit\_as\]** conversion is applied.</span></span> <span data-ttu-id="3c6c2-141">封送資料時，會反轉順序。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-141">The order is reversed when unmarshaling data.</span></span> <span data-ttu-id="3c6c2-142">因此，當封送處理時， \* **\_ 從 \_ local** 會配置命名型別的實例，並將它從區欄位型別物件轉譯為暫時命名的型別物件。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-142">Thus, when marshaling, \***\_from\_local** allocates an instance of a named type and translates it from a local type object to the temporary named type object.</span></span> <span data-ttu-id="3c6c2-143">此物件是用於 \* **\_ \_ xmit** 常式的呈現型別物件。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-143">This object is the presented type object used for the \***\_to\_xmit** routine.</span></span> <span data-ttu-id="3c6c2-144">然後， \* **\_ \_ xmit** 常式會配置傳送的型別物件，並將其從名為) 物件的呈現 (轉譯為傳輸的物件。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-144">The \***\_to\_xmit** routine then allocates a transmitted type object and translates it from the presented (named) object to the transmitted object.</span></span>

 

<span data-ttu-id="3c6c2-145">長整數陣列可以用來表示連結的清單。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-145">An array of long integers can be used to represent a linked list.</span></span> <span data-ttu-id="3c6c2-146">如此一來，應用程式就會操作此清單，而當傳輸此類型的清單時，傳輸會使用長整數陣列。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-146">In this way, the application manipulates the list, and the transmission uses an array of long integers when a list of this type is transmitted.</span></span> <span data-ttu-id="3c6c2-147">您可以從陣列開始，但使用具有 long 整數的開放式陣列的結構比較方便。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-147">You can begin with an array, but using a construct with an open array of long integers is more convenient.</span></span> <span data-ttu-id="3c6c2-148">下列範例示範如何執行。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-148">The following example shows how to do this.</span></span>

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

<span data-ttu-id="3c6c2-149">請注意，使用 **LONGARR** 類型的常式原型實際上會以 qps-ploc 方塊的形式顯示在存根檔案中， **以 \_** 取代 **LONGARR** 類型。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-149">Note that the prototypes of the routines that use the **LONGARR** type are actually displayed in the Stub.h files as **PLOC\_BOX** in place of the **LONGARR** type.</span></span> <span data-ttu-id="3c6c2-150">存根 c 檔案中的適當存根也是如此 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-150">The same is true of the appropriate stubs in the Stub\_c.c file.</span></span>

<span data-ttu-id="3c6c2-151">您必須提供下列四個功能：</span><span class="sxs-lookup"><span data-stu-id="3c6c2-151">You must supply the following four functions:</span></span>

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

<span data-ttu-id="3c6c2-152">以上所示的常式會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="3c6c2-152">The routines shown above do the following:</span></span>

-   <span data-ttu-id="3c6c2-153">**\_ \_ 本機** 常式的 LONGARR 會計算清單的節點、配置具有 **Sizeof** (**LONGARR**) + Count \* **Sizeof** (**long**) 、將 **Size** 欄位設定為 Count 的 LONGARR 物件，以及將資料複製到 **DataArr** 欄位。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-153">The **LONGARR\_from\_local** routine counts the nodes of the list, allocates a LONGARR object with the size **sizeof**(**LONGARR**) + Count\***sizeof**(**long**), sets the **Size** field to Count, and copies the data to the **DataArr** field.</span></span>
-   <span data-ttu-id="3c6c2-154">**LONGARR \_ 至 \_ local** 常式會建立具有大小節點的清單，並將陣列傳送至適當的節點。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-154">The **LONGARR\_to\_local** routine creates a list with Size nodes and transfers the array to the appropriate nodes.</span></span>
-   <span data-ttu-id="3c6c2-155">**LONGARR \_ free \_ inst** 常式在這種情況下不會釋出任何東西。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-155">The **LONGARR\_free\_inst** routine frees nothing in this case.</span></span>
-   <span data-ttu-id="3c6c2-156">**LONGARR \_ free \_ local** 常式會釋出列表中的所有節點。</span><span class="sxs-lookup"><span data-stu-id="3c6c2-156">The **LONGARR\_free\_local** routine frees all the nodes of the list.</span></span>

 

 