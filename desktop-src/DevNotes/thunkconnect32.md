---
description: ThunkConnect32 函式是由16位設備磁碟機所使用 (用於呼叫32位核心的 MS-DOS) 。
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: ThunkConnect32 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989276"
---
# <a name="thunkconnect32-function"></a><span data-ttu-id="2ad70-103">ThunkConnect32 函式</span><span class="sxs-lookup"><span data-stu-id="2ad70-103">ThunkConnect32 function</span></span>

<span data-ttu-id="2ad70-104">\[這個函式支援回溯相容性，但不存在於目前的 Windows 版本中。</span><span class="sxs-lookup"><span data-stu-id="2ad70-104">\[This function was supported for backward compatibility, but is not present in current versions of Windows.</span></span> <span data-ttu-id="2ad70-105">新的設備磁碟機應該是32或64位，而且不需要此功能。\]</span><span class="sxs-lookup"><span data-stu-id="2ad70-105">New device drivers should be 32- or 64-bit and do not need this function.\]</span></span>

<span data-ttu-id="2ad70-106">**ThunkConnect32** 函式是由16位設備磁碟機所使用 (用於呼叫32位核心的 MS-DOS) 。</span><span class="sxs-lookup"><span data-stu-id="2ad70-106">The **ThunkConnect32** function is used by 16-bit device drivers (for MS-DOS) that call into the 32-bit kernel.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ad70-107">語法</span><span class="sxs-lookup"><span data-stu-id="2ad70-107">Syntax</span></span>


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a><span data-ttu-id="2ad70-108">參數</span><span class="sxs-lookup"><span data-stu-id="2ad70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ad70-109">*lpThunkData32*</span><span class="sxs-lookup"><span data-stu-id="2ad70-109">*lpThunkData32*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad70-110">忽略。</span><span class="sxs-lookup"><span data-stu-id="2ad70-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2ad70-111">*pszThunkData16Name*</span><span class="sxs-lookup"><span data-stu-id="2ad70-111">*pszThunkData16Name*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad70-112">忽略。</span><span class="sxs-lookup"><span data-stu-id="2ad70-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2ad70-113">*pszDll16*</span><span class="sxs-lookup"><span data-stu-id="2ad70-113">*pszDll16*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad70-114">忽略。</span><span class="sxs-lookup"><span data-stu-id="2ad70-114">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2ad70-115">*pszDll32*</span><span class="sxs-lookup"><span data-stu-id="2ad70-115">*pszDll32*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad70-116">忽略。</span><span class="sxs-lookup"><span data-stu-id="2ad70-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2ad70-117">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="2ad70-117">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad70-118">忽略。</span><span class="sxs-lookup"><span data-stu-id="2ad70-118">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2ad70-119">*dwReason*</span><span class="sxs-lookup"><span data-stu-id="2ad70-119">*dwReason*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad70-120">忽略。</span><span class="sxs-lookup"><span data-stu-id="2ad70-120">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ad70-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ad70-121">Return value</span></span>

<span data-ttu-id="2ad70-122">一律傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2ad70-122">Always returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ad70-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ad70-123">Requirements</span></span>



| <span data-ttu-id="2ad70-124">需求</span><span class="sxs-lookup"><span data-stu-id="2ad70-124">Requirement</span></span> | <span data-ttu-id="2ad70-125">值</span><span class="sxs-lookup"><span data-stu-id="2ad70-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad70-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2ad70-126">DLL</span></span><br/> | <dl> <span data-ttu-id="2ad70-127"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ad70-127"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




