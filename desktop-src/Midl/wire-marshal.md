---
title: wire_marshal 屬性
description: '\\ 電傳 \_ 封送處理 \ 屬性（attribute）會指定將用於傳輸 (類型) 的資料類型，而不是 (userm 類型) 的應用程式特定資料類型。'
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- wire_marshal 屬性 MIDL
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383117"
---
# <a name="wire_marshal-attribute"></a><span data-ttu-id="4a58e-104">有線 \_ 封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="4a58e-104">wire\_marshal attribute</span></span>

<span data-ttu-id="4a58e-105">[ **\[ 有線 \_ 封 \] 送** 處理] 屬性指定的資料類型將用於傳輸 (類型 *) ，* 而不是 (*userm 類型*) 的應用程式特定資料類型。</span><span class="sxs-lookup"><span data-stu-id="4a58e-105">The **\[wire\_marshal\]** attribute specifies a data type that will be used for transmission (the *wire-type*) instead of an application-specific data type (the *userm-type*).</span></span>

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="4a58e-106">參數</span><span class="sxs-lookup"><span data-stu-id="4a58e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a58e-107">*線路類型*</span><span class="sxs-lookup"><span data-stu-id="4a58e-107">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4a58e-108">指定實際在用戶端與伺服器之間傳輸的命名傳輸資料類型。</span><span class="sxs-lookup"><span data-stu-id="4a58e-108">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="4a58e-109">連線 *類型* 必須是 MIDL 基底類型、預先定義的類型，或是可透過網路傳輸之類型的類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a58e-109">The *wire-type* must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="4a58e-110">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="4a58e-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="4a58e-111">*Userm* 類型將會成為別名的型別。</span><span class="sxs-lookup"><span data-stu-id="4a58e-111">The type for which *userm-type* will become an alias.</span></span>

</dd> <dt>

<span data-ttu-id="4a58e-112">*userm-類型*</span><span class="sxs-lookup"><span data-stu-id="4a58e-112">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4a58e-113">指定要封送處理之使用者資料類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a58e-113">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="4a58e-114">它可以是 *類型規範* 所提供的任何類型，只要它具有妥善定義的大小即可。</span><span class="sxs-lookup"><span data-stu-id="4a58e-114">It can be any type, as given by the *type-specifier*, as long as it has a well-defined size.</span></span> <span data-ttu-id="4a58e-115">*Userm 型* 別不需要可，但必須是 MIDL 編譯器的已知型別。</span><span class="sxs-lookup"><span data-stu-id="4a58e-115">The *userm-type* need not be transmittable but must be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="4a58e-116">*pFlags*</span><span class="sxs-lookup"><span data-stu-id="4a58e-116">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="4a58e-117">指定旗標欄位的指標 ( 不 [**帶正負**](unsigned.md)號的 [**長**](long.md)) 。</span><span class="sxs-lookup"><span data-stu-id="4a58e-117">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="4a58e-118">高序位單字會指定以 DCE 為浮點數、最大或最小的位元組和字元標記法所定義的 NDR 資料表示旗標。</span><span class="sxs-lookup"><span data-stu-id="4a58e-118">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="4a58e-119">低序位字組會指定封送處理內容旗標。</span><span class="sxs-lookup"><span data-stu-id="4a58e-119">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="4a58e-120">旗標的確切版面配置描述于 [type \_ UserSize](/windows/desktop/Rpc/the-type-usersize-function)函式中。</span><span class="sxs-lookup"><span data-stu-id="4a58e-120">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="4a58e-121">*StartingSize*</span><span class="sxs-lookup"><span data-stu-id="4a58e-121">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="4a58e-122">在調整物件大小之前，指定目前的緩衝區大小 (位移) 。</span><span class="sxs-lookup"><span data-stu-id="4a58e-122">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="4a58e-123">*pUser \_ typeObject*</span><span class="sxs-lookup"><span data-stu-id="4a58e-123">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="4a58e-124">指定 *userm \_ 類型* 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="4a58e-124">Specifies a pointer to an object of *userm\_type.*</span></span>

</dd> <dt>

<span data-ttu-id="4a58e-125">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="4a58e-125">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="4a58e-126">指定目前的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="4a58e-126">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a58e-127">備註</span><span class="sxs-lookup"><span data-stu-id="4a58e-127">Remarks</span></span>

<span data-ttu-id="4a58e-128">每個應用程式專屬的資料類型（ *userm 型別）* 都有 *一對一的對應，其會定義* 類型的線路標記法。</span><span class="sxs-lookup"><span data-stu-id="4a58e-128">Each application-specific data type, *userm-type,* has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="4a58e-129">您必須提供常式來調整資料的大小以進行封送處理、封送處理和 unmarshal 資料，以及釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="4a58e-129">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="4a58e-130">請注意，如果您的資料中有內嵌類型也使用了 **\[ 網路 \_ 封送 \]** 處理或 **\[** [**使用者 \_ 封送**](user-marshal.md)來定義 **\]** ，則您也需要管理這些內嵌類型的服務。</span><span class="sxs-lookup"><span data-stu-id="4a58e-130">Note that if there are embedded types in your data that are also defined with **\[wire\_marshal\]** or **\[**[**user\_marshal**](user-marshal.md)**\]**, you need to manage the servicing of those embedded types also.</span></span> <span data-ttu-id="4a58e-131">如需這些常式的詳細資訊，請參閱「 [有線 \_ 封送](/windows/desktop/Rpc/the-wire-marshal-attribute)處理」屬性。</span><span class="sxs-lookup"><span data-stu-id="4a58e-131">For more information on these routines, see [The wire\_marshal Attribute](/windows/desktop/Rpc/the-wire-marshal-attribute).</span></span>

<span data-ttu-id="4a58e-132">您的實作為依據憑證-DCE 規格，必須遵循封送處理規則。</span><span class="sxs-lookup"><span data-stu-id="4a58e-132">Your implementation must follow the marshalling rules according to the OSF-DCE specification.</span></span> <span data-ttu-id="4a58e-133">您可以在中找到有關 NDR 傳送語法的詳細資料 [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) 。</span><span class="sxs-lookup"><span data-stu-id="4a58e-133">Details about NDR transfer syntax can be found at [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).</span></span> <span data-ttu-id="4a58e-134">如果您不熟悉網路通訊協定，則不建議使用 **\[ 網路 \_ 封送 \]** 處理。</span><span class="sxs-lookup"><span data-stu-id="4a58e-134">It is not recommended to use **\[wire\_marshal\]** if you are not familiar with the wire protocol.</span></span>

<span data-ttu-id="4a58e-135">*網路類型* 不能是介面指標或完整指標。</span><span class="sxs-lookup"><span data-stu-id="4a58e-135">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="4a58e-136">*網路類型* 必須有妥善定義的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="4a58e-136">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="4a58e-137">如需有關如何封送處理指定 *網路類型* 的詳細資訊，請參閱 [使用者 \_ 封送處理和網路 \_ 封送處理的封送處理規則](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal)。</span><span class="sxs-lookup"><span data-stu-id="4a58e-137">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="4a58e-138">*Userm 類型* 不應該是介面指標，因為它們可以直接封送處理。</span><span class="sxs-lookup"><span data-stu-id="4a58e-138">The *userm-type* should not be an interface pointer because these can be marshaled directly.</span></span> <span data-ttu-id="4a58e-139">如果使用者類型是完整的指標，您必須自行管理別名。</span><span class="sxs-lookup"><span data-stu-id="4a58e-139">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

<span data-ttu-id="4a58e-140">您無法直接或間接使用 [ **\[ 電匯 \_ \]** ] 屬性與 [ **\[** [**配置**](allocate.md)] **\]** 屬性，因為 NDR 引擎不會控制傳輸類型的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="4a58e-140">You cannot use the **\[wire\_marshal\]** attribute with the **\[**[**allocate**](allocate.md)**\]** attribute, either directly or indirectly, because the NDR engine does not control memory allocation for the transmitted type.</span></span>

## <a name="examples"></a><span data-ttu-id="4a58e-141">範例</span><span class="sxs-lookup"><span data-stu-id="4a58e-141">Examples</span></span>

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a><span data-ttu-id="4a58e-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a58e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a58e-143">**分配**</span><span class="sxs-lookup"><span data-stu-id="4a58e-143">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="4a58e-144">資料表示</span><span class="sxs-lookup"><span data-stu-id="4a58e-144">Data Representation</span></span>](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[<span data-ttu-id="4a58e-145">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="4a58e-145">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="4a58e-146">**long**</span><span class="sxs-lookup"><span data-stu-id="4a58e-146">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="4a58e-147">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="4a58e-147">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[<span data-ttu-id="4a58e-148">有線 \_ 封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="4a58e-148">The wire\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="4a58e-149">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="4a58e-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="4a58e-150">**符號**</span><span class="sxs-lookup"><span data-stu-id="4a58e-150">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="4a58e-151">**使用者 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="4a58e-151">**user\_marshal**</span></span>](user-marshal.md)
</dt> </dl>

 

 