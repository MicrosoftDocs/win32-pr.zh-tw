---
description: GetFrameDstAddressOffset 函式會傳回指定框架之目的地位址的位移。
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: 'GetFrameDstAddressOffset 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973810"
---
# <a name="getframedstaddressoffset-function"></a><span data-ttu-id="4bf31-103">GetFrameDstAddressOffset 函式</span><span class="sxs-lookup"><span data-stu-id="4bf31-103">GetFrameDstAddressOffset function</span></span>

<span data-ttu-id="4bf31-104">**GetFrameDstAddressOffset** 函式會傳回指定框架之目的地位址的位移。</span><span class="sxs-lookup"><span data-stu-id="4bf31-104">The **GetFrameDstAddressOffset** function returns the offset to the destination address of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf31-105">語法</span><span class="sxs-lookup"><span data-stu-id="4bf31-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="4bf31-106">參數</span><span class="sxs-lookup"><span data-stu-id="4bf31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf31-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bf31-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf31-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4bf31-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="4bf31-109">*AddressType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bf31-109">*AddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf31-110">目的地位址的類型。</span><span class="sxs-lookup"><span data-stu-id="4bf31-110">Type of the destination address.</span></span> <span data-ttu-id="4bf31-111">指定下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="4bf31-111">Specify one of the following values:</span></span>

<span data-ttu-id="4bf31-112">位址 \_ 類型的 \_ 乙太網路位址類型 \_ IP 位址類型 TOKENRING 網址類別型的 IP 位址類型 \_ \_ \_ \_ \_ \_ \_ \_ \_ XNS 位址 \_ 類型 \_ VINES \_ IP 位址類型的 IP 位址類型 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="4bf31-112">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_IP ADDRESS\_TYPE\_IPX ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI ADDRESS\_TYPE\_XNS ADDRESS\_TYPE\_VINES\_IP ADDRESS\_TYPE\_ATM.</span></span>

</dd> <dt>

<span data-ttu-id="4bf31-113">*AddressLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bf31-113">*AddressLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf31-114">目的地位址的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4bf31-114">Length of the destination address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf31-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bf31-115">Return value</span></span>

<span data-ttu-id="4bf31-116">如果函式成功，則傳回值是以) 位元組為單位的位移 (測量到要求的網址類別型。</span><span class="sxs-lookup"><span data-stu-id="4bf31-116">If the function is successful, the return value is the offset (measured in bytes) to the requested address type.</span></span>

<span data-ttu-id="4bf31-117">如果函式不成功，則傳回值為減去 1 (-1) 。</span><span class="sxs-lookup"><span data-stu-id="4bf31-117">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="4bf31-118">備註</span><span class="sxs-lookup"><span data-stu-id="4bf31-118">Remarks</span></span>

<span data-ttu-id="4bf31-119">如果 *AddressType* 參數設定為 ADDRESS \_ 類型 \_ ETHERNET， **GetFrameDstAddressOffset** 函式的傳回值一律為零。</span><span class="sxs-lookup"><span data-stu-id="4bf31-119">If the *AddressType* parameter is set to ADDRESS\_TYPE\_ETHERNET, the return value of the **GetFrameDstAddressOffset** function is always zero.</span></span> <span data-ttu-id="4bf31-120">乙太網路位址的位移一律為零。</span><span class="sxs-lookup"><span data-stu-id="4bf31-120">The offset of an Ethernet address is always zero.</span></span>

<span data-ttu-id="4bf31-121">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameDstAddressOffset** 函數。</span><span class="sxs-lookup"><span data-stu-id="4bf31-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameDstAddressOffset** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf31-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bf31-122">Requirements</span></span>



| <span data-ttu-id="4bf31-123">需求</span><span class="sxs-lookup"><span data-stu-id="4bf31-123">Requirement</span></span> | <span data-ttu-id="4bf31-124">值</span><span class="sxs-lookup"><span data-stu-id="4bf31-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf31-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bf31-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4bf31-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bf31-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4bf31-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bf31-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4bf31-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bf31-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4bf31-129">標頭</span><span class="sxs-lookup"><span data-stu-id="4bf31-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bf31-130"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="4bf31-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4bf31-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="4bf31-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="4bf31-132"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bf31-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="4bf31-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4bf31-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bf31-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bf31-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




