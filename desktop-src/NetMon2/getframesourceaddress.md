---
description: 抓取框架的來源位址。
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: 'GetFrameSourceAddress 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6939e5875c4d2f6f41ae33574c7a7240697042ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001326"
---
# <a name="getframesourceaddress-function"></a><span data-ttu-id="59231-103">GetFrameSourceAddress 函式</span><span class="sxs-lookup"><span data-stu-id="59231-103">GetFrameSourceAddress function</span></span>

<span data-ttu-id="59231-104">**GetFrameSourceAddress** 函式會捕獲框架的來源位址。</span><span class="sxs-lookup"><span data-stu-id="59231-104">The **GetFrameSourceAddress** function retrieves the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="59231-105">語法</span><span class="sxs-lookup"><span data-stu-id="59231-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSourceAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="59231-106">參數</span><span class="sxs-lookup"><span data-stu-id="59231-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59231-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="59231-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="59231-108">要取得其指標之框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="59231-108">A handle to the frame for which to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="59231-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="59231-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="59231-110">儲存畫面格來源位址的傳回緩衝區。</span><span class="sxs-lookup"><span data-stu-id="59231-110">A return buffer that stores the frame source address.</span></span>

</dd> <dt>

<span data-ttu-id="59231-111">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="59231-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="59231-112">搜尋的網址類別型，例如位址 \_ 類型 \_ ETHERNET 或位址 \_ 類型 \_ IP。</span><span class="sxs-lookup"><span data-stu-id="59231-112">The type of address searched for, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="59231-113">*旗標*</span><span class="sxs-lookup"><span data-stu-id="59231-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="59231-114">用來修改傳回之來源位址資料的旗標。</span><span class="sxs-lookup"><span data-stu-id="59231-114">The flags used to modify returned source address data.</span></span>



| <span data-ttu-id="59231-115">值</span><span class="sxs-lookup"><span data-stu-id="59231-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="59231-116">意義</span><span class="sxs-lookup"><span data-stu-id="59231-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="59231-117"><dt>**ADDRESSTYPE \_ 旗標正規化 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59231-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="59231-118">取消路由和群組位。</span><span class="sxs-lookup"><span data-stu-id="59231-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="59231-119"><dt>**ADDRESSTYPE \_ 旗標 \_ 位 \_ 反轉**</dt></span><span class="sxs-lookup"><span data-stu-id="59231-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="59231-120">將權杖通道的網路位址轉譯回一般。</span><span class="sxs-lookup"><span data-stu-id="59231-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59231-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="59231-121">Return value</span></span>

<span data-ttu-id="59231-122">如果函式成功，則 *lpAddress* 值有效，且傳回值為 BHERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="59231-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="59231-123">如果函式不成功，則傳回值為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="59231-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="59231-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="59231-124">Return code</span></span>                                                                                                | <span data-ttu-id="59231-125">Description</span><span class="sxs-lookup"><span data-stu-id="59231-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59231-126"><dt>**\_ \_ 找不到 BHERR 通訊協定 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59231-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="59231-127">*AddressType* 參數所指定的通訊協定對框架而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="59231-127">The protocol specified by the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="59231-128"><dt>**BHERR \_ 不正確 \_ HFRAME**</dt></span><span class="sxs-lookup"><span data-stu-id="59231-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="59231-129">*HFrame* 參數值無效。</span><span class="sxs-lookup"><span data-stu-id="59231-129">The *hFrame* parameter value is invalid.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="59231-130">備註</span><span class="sxs-lookup"><span data-stu-id="59231-130">Remarks</span></span>

<span data-ttu-id="59231-131">允許 [ **\_ \_ 尋找 \_ 最高] 網址類別型** 的網址類別型。</span><span class="sxs-lookup"><span data-stu-id="59231-131">An address type of **ADDRESS\_TYPE\_FIND\_HIGHEST** is allowed.</span></span> <span data-ttu-id="59231-132">使用此網址類別型時，此函式會先搜尋 IPX、XNS、IP 或 VINES IP 位址，再傳回 ETHERNET、TOKENRING 或 FDDI 位址。</span><span class="sxs-lookup"><span data-stu-id="59231-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="59231-133">這種方法適用于可在單一伺服器位址下多工處理兩個 Nic 的通訊協定和環境。</span><span class="sxs-lookup"><span data-stu-id="59231-133">This approach is useful for protocols and environments in which two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="59231-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="59231-134">Requirements</span></span>



| <span data-ttu-id="59231-135">需求</span><span class="sxs-lookup"><span data-stu-id="59231-135">Requirement</span></span> | <span data-ttu-id="59231-136">值</span><span class="sxs-lookup"><span data-stu-id="59231-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="59231-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59231-137">Minimum supported client</span></span><br/> | <span data-ttu-id="59231-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59231-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="59231-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59231-139">Minimum supported server</span></span><br/> | <span data-ttu-id="59231-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59231-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="59231-141">標頭</span><span class="sxs-lookup"><span data-stu-id="59231-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="59231-142"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="59231-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="59231-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="59231-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="59231-144"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="59231-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="59231-145">DLL</span><span class="sxs-lookup"><span data-stu-id="59231-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59231-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59231-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




