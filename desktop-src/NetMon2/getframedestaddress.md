---
description: 抓取框架的目的位址。
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: 'GetFrameDestAddress 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: afec32f0e0fc66ccd5a1d78cc9769b0e742f1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936629"
---
# <a name="getframedestaddress-function"></a><span data-ttu-id="bc97c-103">GetFrameDestAddress 函式</span><span class="sxs-lookup"><span data-stu-id="bc97c-103">GetFrameDestAddress function</span></span>

<span data-ttu-id="bc97c-104">**GetFrameDestAddress** 函式會捕獲框架的目的位址。</span><span class="sxs-lookup"><span data-stu-id="bc97c-104">The **GetFrameDestAddress** function retrieves the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc97c-105">語法</span><span class="sxs-lookup"><span data-stu-id="bc97c-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDestAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="bc97c-106">參數</span><span class="sxs-lookup"><span data-stu-id="bc97c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc97c-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="bc97c-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="bc97c-108">要取得指標之框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bc97c-108">A handle of the frame to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="bc97c-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="bc97c-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="bc97c-110">儲存框架目的地位址的傳回緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bc97c-110">A return buffer that stores the frame destination address.</span></span>

</dd> <dt>

<span data-ttu-id="bc97c-111">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="bc97c-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="bc97c-112">網址類別型，例如位址 \_ 類型 \_ ETHERNET 或位址 \_ 類型 \_ IP。</span><span class="sxs-lookup"><span data-stu-id="bc97c-112">A type of address, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="bc97c-113">*旗標*</span><span class="sxs-lookup"><span data-stu-id="bc97c-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="bc97c-114">用來修改傳回之目的地位址資料的旗標。</span><span class="sxs-lookup"><span data-stu-id="bc97c-114">The flags used to modify returned destination address data.</span></span>



| <span data-ttu-id="bc97c-115">值</span><span class="sxs-lookup"><span data-stu-id="bc97c-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="bc97c-116">意義</span><span class="sxs-lookup"><span data-stu-id="bc97c-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="bc97c-117"><dt>**ADDRESSTYPE \_ 旗標正規化 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc97c-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="bc97c-118">取消路由和群組位。</span><span class="sxs-lookup"><span data-stu-id="bc97c-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="bc97c-119"><dt>**ADDRESSTYPE \_ 旗標 \_ 位 \_ 反轉**</dt></span><span class="sxs-lookup"><span data-stu-id="bc97c-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="bc97c-120">將權杖通道的網路位址轉譯回一般。</span><span class="sxs-lookup"><span data-stu-id="bc97c-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc97c-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc97c-121">Return value</span></span>

<span data-ttu-id="bc97c-122">如果函式成功，則 *lpAddress* 值有效，且傳回值為 BHERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="bc97c-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="bc97c-123">如果函式不成功，則傳回值為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bc97c-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="bc97c-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bc97c-124">Return code</span></span>                                                                                                | <span data-ttu-id="bc97c-125">Description</span><span class="sxs-lookup"><span data-stu-id="bc97c-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bc97c-126"><dt>**\_ \_ 找不到 BHERR 通訊協定 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc97c-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="bc97c-127">*AddressType* 參數中指定的通訊協定對框架而言無效。</span><span class="sxs-lookup"><span data-stu-id="bc97c-127">The specified protocol in the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="bc97c-128"><dt>**BHERR \_ 不正確 \_ HFRAME**</dt></span><span class="sxs-lookup"><span data-stu-id="bc97c-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="bc97c-129">*HFrame* 值無效。</span><span class="sxs-lookup"><span data-stu-id="bc97c-129">The *hFrame* value is invalid.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="bc97c-130">備註</span><span class="sxs-lookup"><span data-stu-id="bc97c-130">Remarks</span></span>

<span data-ttu-id="bc97c-131">允許 **位址 \_ 類型 \_ 尋找 \_ 最高** 的網址類別型。</span><span class="sxs-lookup"><span data-stu-id="bc97c-131">The **ADDRESS\_TYPE\_FIND\_HIGHEST** address type is allowed.</span></span> <span data-ttu-id="bc97c-132">使用此網址類別型時，此函式會先搜尋 IPX、XNS、IP 或 VINES IP 位址，再傳回 ETHERNET、TOKENRING 或 FDDI 位址。</span><span class="sxs-lookup"><span data-stu-id="bc97c-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="bc97c-133">這種方法適用于通訊協定和環境，在此環境中，可在單一伺服器位址下多工處理兩個 Nic。</span><span class="sxs-lookup"><span data-stu-id="bc97c-133">This approach is useful for protocols and in environments where two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc97c-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc97c-134">Requirements</span></span>



| <span data-ttu-id="bc97c-135">需求</span><span class="sxs-lookup"><span data-stu-id="bc97c-135">Requirement</span></span> | <span data-ttu-id="bc97c-136">值</span><span class="sxs-lookup"><span data-stu-id="bc97c-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bc97c-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc97c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bc97c-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc97c-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bc97c-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc97c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bc97c-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc97c-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bc97c-141">標頭</span><span class="sxs-lookup"><span data-stu-id="bc97c-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc97c-142"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="bc97c-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="bc97c-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="bc97c-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc97c-144"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc97c-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bc97c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bc97c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc97c-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc97c-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




