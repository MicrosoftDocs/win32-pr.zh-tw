---
description: MacTypeToAddressType 函式會將指定的 MAC 型別轉換為網址類別型。
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: 'MacTypeToAddressType 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848161"
---
# <a name="mactypetoaddresstype-function"></a><span data-ttu-id="1ad76-103">MacTypeToAddressType 函式</span><span class="sxs-lookup"><span data-stu-id="1ad76-103">MacTypeToAddressType function</span></span>

<span data-ttu-id="1ad76-104">**MacTypeToAddressType** 函式會將指定的 MAC 型別轉換為網址類別型。</span><span class="sxs-lookup"><span data-stu-id="1ad76-104">The **MacTypeToAddressType** function converts a given MAC type to an address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad76-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ad76-105">Syntax</span></span>


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a><span data-ttu-id="1ad76-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ad76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ad76-107">*MacType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1ad76-107">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ad76-108">要轉換的 MAC 類型。</span><span class="sxs-lookup"><span data-stu-id="1ad76-108">MAC type to be converted.</span></span> <span data-ttu-id="1ad76-109">指定下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="1ad76-109">Specify one of the following values:</span></span>

<span data-ttu-id="1ad76-110">MAC \_ 類型 \_ ETHERNET MAC \_ 類型 \_ TOKENRING MAC \_ 類型的 \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="1ad76-110">MAC\_TYPE\_ETHERNET MAC\_TYPE\_TOKENRING MAC\_TYPE\_FDDI</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ad76-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ad76-111">Return value</span></span>

<span data-ttu-id="1ad76-112">如果函式成功，則傳回值是下列其中一種網址類別型。</span><span class="sxs-lookup"><span data-stu-id="1ad76-112">If the function is successful, the return value is one of the following address types.</span></span>

<span data-ttu-id="1ad76-113">位址 \_ 類型 \_ 乙太網路位址類型 \_ \_ TOKENRING 位址 \_ 類型 \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="1ad76-113">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI</span></span>

<span data-ttu-id="1ad76-114">如果函式不成功，則 MAC 類型未知，傳回值為-1。</span><span class="sxs-lookup"><span data-stu-id="1ad76-114">If the function is unsuccessful, the MAC type is unknown, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad76-115">備註</span><span class="sxs-lookup"><span data-stu-id="1ad76-115">Remarks</span></span>

<span data-ttu-id="1ad76-116">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **MacTypeToAddressType** 函數。</span><span class="sxs-lookup"><span data-stu-id="1ad76-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **MacTypeToAddressType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ad76-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ad76-117">Requirements</span></span>



| <span data-ttu-id="1ad76-118">需求</span><span class="sxs-lookup"><span data-stu-id="1ad76-118">Requirement</span></span> | <span data-ttu-id="1ad76-119">值</span><span class="sxs-lookup"><span data-stu-id="1ad76-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad76-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ad76-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad76-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ad76-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1ad76-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ad76-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad76-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ad76-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1ad76-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1ad76-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ad76-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1ad76-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1ad76-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ad76-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ad76-127"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ad76-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1ad76-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1ad76-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ad76-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ad76-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




