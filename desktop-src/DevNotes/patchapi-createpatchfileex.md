---
description: 在指定的來源檔案和指定的目標檔案之間建立差異。
title: CreatePatchFileExA/W 函數
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: c84be2d859a780e46e7e940aa4a7e7da5296f0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977393"
---
# <a name="createpatchfileexaw-function"></a><span data-ttu-id="f8869-103">CreatePatchFileExA/W 函數</span><span class="sxs-lookup"><span data-stu-id="f8869-103">CreatePatchFileExA/W function</span></span>

<span data-ttu-id="f8869-104">**CreatePatchFileExA** 和 **CreatePatchFileExW** 函數會在指定的來源檔案和指定的目標檔案之間建立差異。</span><span class="sxs-lookup"><span data-stu-id="f8869-104">The **CreatePatchFileExA** and **CreatePatchFileExW** functions create a delta between the specified source file and the specified target file.</span></span> <span data-ttu-id="f8869-105">來源和目標檔案都會以路徑形式提供。</span><span class="sxs-lookup"><span data-stu-id="f8869-105">Both the source and the target files are provided as paths.</span></span> <span data-ttu-id="f8869-106">輸出差異也會寫入至提供的路徑。</span><span class="sxs-lookup"><span data-stu-id="f8869-106">The output delta is also written to a provided path.</span></span> <span data-ttu-id="f8869-107">這些函數會在建立程式期間提供進度報告。</span><span class="sxs-lookup"><span data-stu-id="f8869-107">These functions provide progress reporting during the create process.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8869-108">語法</span><span class="sxs-lookup"><span data-stu-id="f8869-108">Syntax</span></span>

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a><span data-ttu-id="f8869-109">參數</span><span class="sxs-lookup"><span data-stu-id="f8869-109">Parameters</span></span>

<span data-ttu-id="f8869-110">*OldFileCount*</span><span class="sxs-lookup"><span data-stu-id="f8869-110">*OldFileCount*</span></span>

<span data-ttu-id="f8869-111">原始程式檔總數。</span><span class="sxs-lookup"><span data-stu-id="f8869-111">The total number of source files.</span></span> <span data-ttu-id="f8869-112">用來針對多個來源檔案建立差異， (最大的 255) 。</span><span class="sxs-lookup"><span data-stu-id="f8869-112">Used to create deltas against multiple source files (maximum 255).</span></span>

<span data-ttu-id="f8869-113">*OldFileInfoArray*</span><span class="sxs-lookup"><span data-stu-id="f8869-113">*OldFileInfoArray*</span></span>

<span data-ttu-id="f8869-114">來源檔案資訊陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="f8869-114">Pointer to source file information array.</span></span>

<span data-ttu-id="f8869-115">*NewFileName*</span><span class="sxs-lookup"><span data-stu-id="f8869-115">*NewFileName*</span></span>

<span data-ttu-id="f8869-116">目標檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8869-116">The name of the target file.</span></span>

<span data-ttu-id="f8869-117">*PatchFileName*</span><span class="sxs-lookup"><span data-stu-id="f8869-117">*PatchFileName*</span></span>

<span data-ttu-id="f8869-118">所建立之差異的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8869-118">The name of the delta that is created.</span></span>

<span data-ttu-id="f8869-119">*OptionFlags*</span><span class="sxs-lookup"><span data-stu-id="f8869-119">*OptionFlags*</span></span>

<span data-ttu-id="f8869-120">建立旗標。</span><span class="sxs-lookup"><span data-stu-id="f8869-120">Creation flags.</span></span>

<span data-ttu-id="f8869-121">*ProgressCallback*</span><span class="sxs-lookup"><span data-stu-id="f8869-121">*ProgressCallback*</span></span>

<span data-ttu-id="f8869-122">應用程式定義的進度回呼的指標。</span><span class="sxs-lookup"><span data-stu-id="f8869-122">Pointer to application-defined progress callback.</span></span>

<span data-ttu-id="f8869-123">*CallbackCoNtext*</span><span class="sxs-lookup"><span data-stu-id="f8869-123">*CallbackContext*</span></span>

<span data-ttu-id="f8869-124">應用程式定義內容的指標。</span><span class="sxs-lookup"><span data-stu-id="f8869-124">Pointer to application-defined context.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8869-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8869-125">Return value</span></span>

<span data-ttu-id="f8869-126">如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f8869-126">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8869-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8869-127">Requirements</span></span>

| <span data-ttu-id="f8869-128">需求</span><span class="sxs-lookup"><span data-stu-id="f8869-128">Requirement</span></span> | <span data-ttu-id="f8869-129">值</span><span class="sxs-lookup"><span data-stu-id="f8869-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8869-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f8869-130">Header</span></span> | <span data-ttu-id="f8869-131">patchapi。h</span><span class="sxs-lookup"><span data-stu-id="f8869-131">patchapi.h</span></span> |
| <span data-ttu-id="f8869-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f8869-132">DLL</span></span> | <span data-ttu-id="f8869-133">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="f8869-133">mspatchc.dll</span></span> |
| <span data-ttu-id="f8869-134">Unicode</span><span class="sxs-lookup"><span data-stu-id="f8869-134">Unicode</span></span> | <span data-ttu-id="f8869-135">實作為 CreatePatchFileExW (Unicode) 和 CreatePatchFileExA (ANSI) </span><span class="sxs-lookup"><span data-stu-id="f8869-135">Implemented as CreatePatchFileExW (Unicode) and CreatePatchFileExA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="f8869-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8869-136">See also</span></span>

[<span data-ttu-id="f8869-137">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="f8869-137">PatchAPI</span></span>](patchapi.md)
