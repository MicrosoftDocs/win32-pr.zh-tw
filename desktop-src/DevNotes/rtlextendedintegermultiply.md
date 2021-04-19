---
description: 將擴展的整數相乘。
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: RtlExtendedIntegerMultiply 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982991"
---
# <a name="rtlextendedintegermultiply-function"></a><span data-ttu-id="29c2a-103">RtlExtendedIntegerMultiply 函式</span><span class="sxs-lookup"><span data-stu-id="29c2a-103">RtlExtendedIntegerMultiply function</span></span>

<span data-ttu-id="29c2a-104">\[**RtlExtendedIntegerMultiply** 函式會匯出以支援現有的驅動程式二進位檔，並已淘汰。</span><span class="sxs-lookup"><span data-stu-id="29c2a-104">\[The **RtlExtendedIntegerMultiply** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="29c2a-105">為了獲得更好的效能，請使用編譯器支援64位的整數作業。\]</span><span class="sxs-lookup"><span data-stu-id="29c2a-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="29c2a-106">將擴展的整數相乘。</span><span class="sxs-lookup"><span data-stu-id="29c2a-106">Multiplies extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="29c2a-107">語法</span><span class="sxs-lookup"><span data-stu-id="29c2a-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a><span data-ttu-id="29c2a-108">參數</span><span class="sxs-lookup"><span data-stu-id="29c2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29c2a-109">*被乘數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29c2a-109">*Multiplicand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29c2a-110">被乘數.</span><span class="sxs-lookup"><span data-stu-id="29c2a-110">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="29c2a-111">*乘數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29c2a-111">*Multiplier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29c2a-112">乘數。</span><span class="sxs-lookup"><span data-stu-id="29c2a-112">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29c2a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="29c2a-113">Return value</span></span>

<span data-ttu-id="29c2a-114">傳回乘法結果。</span><span class="sxs-lookup"><span data-stu-id="29c2a-114">Returns multiplication result.</span></span>

## <a name="remarks"></a><span data-ttu-id="29c2a-115">備註</span><span class="sxs-lookup"><span data-stu-id="29c2a-115">Remarks</span></span>

<span data-ttu-id="29c2a-116">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="29c2a-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="29c2a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="29c2a-117">Requirements</span></span>



| <span data-ttu-id="29c2a-118">需求</span><span class="sxs-lookup"><span data-stu-id="29c2a-118">Requirement</span></span> | <span data-ttu-id="29c2a-119">值</span><span class="sxs-lookup"><span data-stu-id="29c2a-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="29c2a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="29c2a-120">DLL</span></span><br/> | <dl> <span data-ttu-id="29c2a-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29c2a-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
