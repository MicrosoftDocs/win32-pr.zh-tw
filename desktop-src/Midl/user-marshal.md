---
title: user_marshal 屬性
description: 使用者 \_ 封送處理 ACF 屬性會將目標 (語言中的命名區欄位型別，與在用戶端和伺服器之間傳輸 () 類型) 的傳輸類型產生關聯。
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal 屬性 MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314797"
---
# <a name="user_marshal-attribute"></a><span data-ttu-id="2fa06-104">使用者 \_ 封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="2fa06-104">user\_marshal attribute</span></span>

<span data-ttu-id="2fa06-105">**使用者 \_ 封送** 處理 ACF 屬性會將目標 (語言中的命名區欄位型別，與在用戶端和伺服器之間 *傳輸 ()* *類型*) 的傳輸類型產生關聯。</span><span class="sxs-lookup"><span data-stu-id="2fa06-105">The **user\_marshal** ACF attribute associates a named local type in the target language (*userm-type*) with a transfer type (*wire-type*) that is transferred between client and server.</span></span>

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="2fa06-106">參數</span><span class="sxs-lookup"><span data-stu-id="2fa06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fa06-107">*userm-類型*</span><span class="sxs-lookup"><span data-stu-id="2fa06-107">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="2fa06-108">指定要封送處理之使用者資料類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2fa06-108">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="2fa06-109">*Userm 型* 別不需要可，也不需要是 MIDL 編譯器已知的型別。</span><span class="sxs-lookup"><span data-stu-id="2fa06-109">The *userm-type* need not be transmittable and need not be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="2fa06-110">*線路類型*</span><span class="sxs-lookup"><span data-stu-id="2fa06-110">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="2fa06-111">指定實際在用戶端與伺服器之間傳輸的命名傳輸資料類型。</span><span class="sxs-lookup"><span data-stu-id="2fa06-111">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="2fa06-112">網路類型必須是 MIDL 基底類型、預先定義的類型，或是可透過網路傳輸之類型的類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="2fa06-112">The wire type must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="2fa06-113">*pFlags*</span><span class="sxs-lookup"><span data-stu-id="2fa06-113">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="2fa06-114">指定旗標欄位的指標 ( 不 [**帶正負**](unsigned.md)號的 [**長**](long.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2fa06-114">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="2fa06-115">高序位單字會指定以 DCE 為浮點數、最大或最小的位元組和字元標記法所定義的 NDR 資料表示旗標。</span><span class="sxs-lookup"><span data-stu-id="2fa06-115">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="2fa06-116">低序位字組會指定封送處理內容旗標。</span><span class="sxs-lookup"><span data-stu-id="2fa06-116">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="2fa06-117">旗標的確切版面配置描述于 [type \_ UserSize](/windows/desktop/Rpc/the-type-usersize-function)函式中。</span><span class="sxs-lookup"><span data-stu-id="2fa06-117">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="2fa06-118">*StartingSize*</span><span class="sxs-lookup"><span data-stu-id="2fa06-118">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2fa06-119">在調整物件大小之前，指定目前的緩衝區大小 (位移) 。</span><span class="sxs-lookup"><span data-stu-id="2fa06-119">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="2fa06-120">*pUser \_ typeObject*</span><span class="sxs-lookup"><span data-stu-id="2fa06-120">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="2fa06-121">指定 *userm \_ 類型* 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="2fa06-121">Specifies a pointer to an object of *userm\_type*.</span></span>

</dd> <dt>

<span data-ttu-id="2fa06-122">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="2fa06-122">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="2fa06-123">指定目前的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="2fa06-123">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fa06-124">備註</span><span class="sxs-lookup"><span data-stu-id="2fa06-124">Remarks</span></span>

<span data-ttu-id="2fa06-125">每個命名區欄位型別（ *userm*）都有一對一的對應，其 *網路類型* 會定義類型的線路標記法。</span><span class="sxs-lookup"><span data-stu-id="2fa06-125">Each named local type, *userm-type*, has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="2fa06-126">您必須提供常式來調整資料的大小以進行封送處理、封送處理和 unmarshal 資料，以及釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="2fa06-126">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="2fa06-127">如需這些常式的詳細資訊，請參閱 [使用者 \_ 封送處理屬性](/windows/desktop/Rpc/the-user-marshal-attribute)。</span><span class="sxs-lookup"><span data-stu-id="2fa06-127">For more information on these routines, see [The user\_marshal Attribute](/windows/desktop/Rpc/the-user-marshal-attribute).</span></span> <span data-ttu-id="2fa06-128">請注意，如果您的資料中也有使用 **使用者 \_ 封送** 處理或網路封送 \[ [**\[ \_ \]**](wire-marshal.md)處理來定義的內嵌類型，您也需要管理這些內嵌類型的服務。</span><span class="sxs-lookup"><span data-stu-id="2fa06-128">Note that if there are embedded types in your data that are also defined with **user\_marshal** or \[ [**\[wire\_marshal\]**](wire-marshal.md), you need to manage the servicing of those embedded types also.</span></span>

<span data-ttu-id="2fa06-129">*網路類型* 不能是介面指標或完整指標。</span><span class="sxs-lookup"><span data-stu-id="2fa06-129">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="2fa06-130">*網路類型* 必須有妥善定義的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="2fa06-130">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="2fa06-131">如需有關如何封送處理指定 *網路類型* 的詳細資訊，請參閱 [使用者 \_ 封送處理和網路 \_ 封送處理的封送處理規則](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal)。</span><span class="sxs-lookup"><span data-stu-id="2fa06-131">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="2fa06-132">*Userm 類型* 不應該是介面指標，因為它們可以直接封送處理。</span><span class="sxs-lookup"><span data-stu-id="2fa06-132">The *userm-type* should not be an interface pointer as these can be marshaled directly.</span></span> <span data-ttu-id="2fa06-133">如果使用者類型是完整的指標，您必須自行管理別名。</span><span class="sxs-lookup"><span data-stu-id="2fa06-133">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

## <a name="examples"></a><span data-ttu-id="2fa06-134">範例</span><span class="sxs-lookup"><span data-stu-id="2fa06-134">Examples</span></span>

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a><span data-ttu-id="2fa06-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fa06-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa06-136">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="2fa06-136">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="2fa06-137">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="2fa06-137">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="2fa06-138">**long**</span><span class="sxs-lookup"><span data-stu-id="2fa06-138">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="2fa06-139">**表示 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="2fa06-139">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="2fa06-140">**符號**</span><span class="sxs-lookup"><span data-stu-id="2fa06-140">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="2fa06-141">使用者 \_ 封送處理屬性</span><span class="sxs-lookup"><span data-stu-id="2fa06-141">The user\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="2fa06-142">**網路 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="2fa06-142">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="2fa06-143">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="2fa06-143">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 