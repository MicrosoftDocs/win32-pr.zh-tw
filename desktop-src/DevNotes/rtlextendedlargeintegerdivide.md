---
description: 分割擴充的整數。
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: RtlExtendedLargeIntegerDivide 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994997"
---
# <a name="rtlextendedlargeintegerdivide-function"></a><span data-ttu-id="50317-103">RtlExtendedLargeIntegerDivide 函式</span><span class="sxs-lookup"><span data-stu-id="50317-103">RtlExtendedLargeIntegerDivide function</span></span>

<span data-ttu-id="50317-104">\[**RtlExtendedLargeIntegerDivide** 函式會匯出以支援現有的驅動程式二進位檔，並已淘汰。</span><span class="sxs-lookup"><span data-stu-id="50317-104">\[The **RtlExtendedLargeIntegerDivide** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="50317-105">為了獲得更好的效能，請使用編譯器支援64位的整數作業。\]</span><span class="sxs-lookup"><span data-stu-id="50317-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="50317-106">分割擴充的整數。</span><span class="sxs-lookup"><span data-stu-id="50317-106">Divides extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="50317-107">語法</span><span class="sxs-lookup"><span data-stu-id="50317-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a><span data-ttu-id="50317-108">參數</span><span class="sxs-lookup"><span data-stu-id="50317-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50317-109">被 *除數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50317-109">*Dividend* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50317-110">股利。</span><span class="sxs-lookup"><span data-stu-id="50317-110">Dividend.</span></span>

</dd> <dt>

<span data-ttu-id="50317-111">*除數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50317-111">*Divisor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50317-112">因數。</span><span class="sxs-lookup"><span data-stu-id="50317-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="50317-113">*餘數* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="50317-113">*Remainder* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50317-114">除法餘數的指標。</span><span class="sxs-lookup"><span data-stu-id="50317-114">Pointer to division remainder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50317-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="50317-115">Return value</span></span>

<span data-ttu-id="50317-116">傳回除法運算的結果。</span><span class="sxs-lookup"><span data-stu-id="50317-116">Returns the result of the division operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="50317-117">備註</span><span class="sxs-lookup"><span data-stu-id="50317-117">Remarks</span></span>

<span data-ttu-id="50317-118">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="50317-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="50317-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="50317-119">Requirements</span></span>



| <span data-ttu-id="50317-120">需求</span><span class="sxs-lookup"><span data-stu-id="50317-120">Requirement</span></span> | <span data-ttu-id="50317-121">值</span><span class="sxs-lookup"><span data-stu-id="50317-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="50317-122">DLL</span><span class="sxs-lookup"><span data-stu-id="50317-122">DLL</span></span><br/> | <dl> <span data-ttu-id="50317-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50317-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
