---
description: 抓取離線檔案快取所使用之空間的相關資訊。
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: CSCGetSpaceUsageW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 608fd7736093ae1f8d131ede777a691e467de9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994817"
---
# <a name="cscgetspaceusagew-function"></a><span data-ttu-id="c2102-103">CSCGetSpaceUsageW 函式</span><span class="sxs-lookup"><span data-stu-id="c2102-103">CSCGetSpaceUsageW function</span></span>

<span data-ttu-id="c2102-104">\[這項功能不受支援，因此不應該使用。\]</span><span class="sxs-lookup"><span data-stu-id="c2102-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="c2102-105">抓取離線檔案快取所使用之空間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c2102-105">Retrieves information about the space used by the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2102-106">語法</span><span class="sxs-lookup"><span data-stu-id="c2102-106">Syntax</span></span>


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a><span data-ttu-id="c2102-107">參數</span><span class="sxs-lookup"><span data-stu-id="c2102-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2102-108">*lptzLocation* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c2102-108">*lptzLocation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2102-109">快取的目錄位置。</span><span class="sxs-lookup"><span data-stu-id="c2102-109">The directory location of the cache.</span></span>

</dd> <dt>

<span data-ttu-id="c2102-110">*dwSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2102-110">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2102-111">*LptzLocation* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c2102-111">The size of the *lptzLocation* buffer, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="c2102-112">*lpdwMaxSpaceHigh* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c2102-112">*lpdwMaxSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2102-113">快取中可用的最大位元組數目的高序位 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="c2102-113">The high-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="c2102-114">*lpdwMaxSpaceLow* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c2102-114">*lpdwMaxSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2102-115">快取中可用的最大位元組數目的低序位 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="c2102-115">The low-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="c2102-116">*lpdwCurrentSpaceHigh* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c2102-116">*lpdwCurrentSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2102-117">快取中目前可用位元組數目的高序位 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="c2102-117">The high-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="c2102-118">*lpdwCurrentSpaceLow* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c2102-118">*lpdwCurrentSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2102-119">快取中目前可用位元組數目的低序位 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="c2102-119">The low-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="c2102-120">*lpcntTotalFiles* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c2102-120">*lpcntTotalFiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2102-121">快取中的檔案總數。</span><span class="sxs-lookup"><span data-stu-id="c2102-121">The total number of files in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="c2102-122">*lpcntTotalDirs* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c2102-122">*lpcntTotalDirs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2102-123">快取中的目錄總數。</span><span class="sxs-lookup"><span data-stu-id="c2102-123">The total number of directories in the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2102-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2102-124">Return value</span></span>

<span data-ttu-id="c2102-125">如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c2102-125">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2102-126">備註</span><span class="sxs-lookup"><span data-stu-id="c2102-126">Remarks</span></span>

<span data-ttu-id="c2102-127">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="c2102-127">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2102-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2102-128">Requirements</span></span>



| <span data-ttu-id="c2102-129">需求</span><span class="sxs-lookup"><span data-stu-id="c2102-129">Requirement</span></span> | <span data-ttu-id="c2102-130">值</span><span class="sxs-lookup"><span data-stu-id="c2102-130">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2102-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c2102-131">DLL</span></span><br/> | <dl> <span data-ttu-id="c2102-132"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2102-132"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
