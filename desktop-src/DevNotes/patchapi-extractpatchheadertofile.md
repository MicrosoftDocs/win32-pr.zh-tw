---
description: 從差異解壓縮標頭資訊。
title: ExtractPatchHeaderToFileA/W 函數
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993341"
---
# <a name="extractpatchheadertofileaw-function"></a><span data-ttu-id="45fdd-103">ExtractPatchHeaderToFileA/W 函數</span><span class="sxs-lookup"><span data-stu-id="45fdd-103">ExtractPatchHeaderToFileA/W function</span></span>

<span data-ttu-id="45fdd-104">**ExtractPatchHeaderToFileA** 和 **ExtractPatchHeaderToFileW** 函式會從差異中解壓縮標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="45fdd-104">The **ExtractPatchHeaderToFileA** and **ExtractPatchHeaderToFileW** functions extract the header information from a delta.</span></span> <span data-ttu-id="45fdd-105">差異會以檔案路徑的形式提供。</span><span class="sxs-lookup"><span data-stu-id="45fdd-105">The delta is provided as a file path.</span></span> <span data-ttu-id="45fdd-106">輸出標頭也會寫入至提供的路徑。</span><span class="sxs-lookup"><span data-stu-id="45fdd-106">The output header is also written to a provided path.</span></span>

## <a name="syntax"></a><span data-ttu-id="45fdd-107">語法</span><span class="sxs-lookup"><span data-stu-id="45fdd-107">Syntax</span></span>

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a><span data-ttu-id="45fdd-108">參數</span><span class="sxs-lookup"><span data-stu-id="45fdd-108">Parameters</span></span>

<span data-ttu-id="45fdd-109">*PatchFileName*</span><span class="sxs-lookup"><span data-stu-id="45fdd-109">*PatchFileName*</span></span>

<span data-ttu-id="45fdd-110">包含標頭之差異的名稱。</span><span class="sxs-lookup"><span data-stu-id="45fdd-110">The name of the delta containing the header.</span></span>

<span data-ttu-id="45fdd-111">*PatchHeaderFileName*</span><span class="sxs-lookup"><span data-stu-id="45fdd-111">*PatchHeaderFileName*</span></span>

<span data-ttu-id="45fdd-112">要建立的標頭檔名稱。</span><span class="sxs-lookup"><span data-stu-id="45fdd-112">The name of the header file that is to be created.</span></span>

## <a name="return-value"></a><span data-ttu-id="45fdd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="45fdd-113">Return value</span></span>

<span data-ttu-id="45fdd-114">如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="45fdd-114">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="45fdd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="45fdd-115">Requirements</span></span>

| <span data-ttu-id="45fdd-116">需求</span><span class="sxs-lookup"><span data-stu-id="45fdd-116">Requirement</span></span> | <span data-ttu-id="45fdd-117">值</span><span class="sxs-lookup"><span data-stu-id="45fdd-117">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45fdd-118">標頭</span><span class="sxs-lookup"><span data-stu-id="45fdd-118">Header</span></span> | <span data-ttu-id="45fdd-119">patchapi。h</span><span class="sxs-lookup"><span data-stu-id="45fdd-119">patchapi.h</span></span> |
| <span data-ttu-id="45fdd-120">DLL</span><span class="sxs-lookup"><span data-stu-id="45fdd-120">DLL</span></span> | <span data-ttu-id="45fdd-121">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="45fdd-121">mspatchc.dll</span></span> |
| <span data-ttu-id="45fdd-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="45fdd-122">Unicode</span></span> | <span data-ttu-id="45fdd-123">實作為 ExtractPatchHeaderToFileW (Unicode) 和 ExtractPatchHeaderToFileA (ANSI) </span><span class="sxs-lookup"><span data-stu-id="45fdd-123">Implemented as ExtractPatchHeaderToFileW (Unicode) and ExtractPatchHeaderToFileA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="45fdd-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45fdd-124">See also</span></span>

[<span data-ttu-id="45fdd-125">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="45fdd-125">PatchAPI</span></span>](patchapi.md)
