---
title: D3DPERF_SetRegion 函式
description: 在 PIXRun 檔案中，以指定的色彩和名稱來標記一系列的框架。 PIX 目前不支援此函式。
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "106966443"
---
# <a name="d3dperf_setregion-function"></a><span data-ttu-id="d6552-104">D3DPERF_SetRegion 函式</span><span class="sxs-lookup"><span data-stu-id="d6552-104">D3DPERF_SetRegion function</span></span>

<span data-ttu-id="d6552-105">在 PIXRun 檔案中，以指定的色彩和名稱來標記一系列的框架。</span><span class="sxs-lookup"><span data-stu-id="d6552-105">Mark a series of frames with the specified color and name in the PIXRun file.</span></span> <span data-ttu-id="d6552-106">PIX 目前不支援此函式。</span><span class="sxs-lookup"><span data-stu-id="d6552-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6552-107">語法</span><span class="sxs-lookup"><span data-stu-id="d6552-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="d6552-108">參數</span><span class="sxs-lookup"><span data-stu-id="d6552-108">Parameters</span></span>

`col`

<span data-ttu-id="d6552-109">事件色彩。</span><span class="sxs-lookup"><span data-stu-id="d6552-109">Event color.</span></span> <span data-ttu-id="d6552-110">這是在事件檢視器中顯示事件的色彩。</span><span class="sxs-lookup"><span data-stu-id="d6552-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="d6552-111">事件名稱。</span><span class="sxs-lookup"><span data-stu-id="d6552-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6552-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6552-112">Return value</span></span>

<span data-ttu-id="d6552-113">此函數不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d6552-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6552-114">備註</span><span class="sxs-lookup"><span data-stu-id="d6552-114">Remarks</span></span>

<span data-ttu-id="d6552-115">為了讓分析變得更容易，目的程式可以使用色彩來標記目的程式的每個層級。</span><span class="sxs-lookup"><span data-stu-id="d6552-115">To make analysis easier, the target program can use color to mark each level of a target program.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6552-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6552-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d6552-117">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="d6552-117">**Target Platform**</span></span> | <span data-ttu-id="d6552-118">Windows</span><span class="sxs-lookup"><span data-stu-id="d6552-118">Windows</span></span> |
| <span data-ttu-id="d6552-119">**標頭**</span><span class="sxs-lookup"><span data-stu-id="d6552-119">**Header**</span></span> | <span data-ttu-id="d6552-120">d3d9。h</span><span class="sxs-lookup"><span data-stu-id="d6552-120">d3d9.h</span></span> |
| <span data-ttu-id="d6552-121">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="d6552-121">**Library**</span></span> | <span data-ttu-id="d6552-122">d3d9 .lib</span><span class="sxs-lookup"><span data-stu-id="d6552-122">d3d9.lib</span></span> |
| <span data-ttu-id="d6552-123">**DLL**</span><span class="sxs-lookup"><span data-stu-id="d6552-123">**DLL**</span></span> | <span data-ttu-id="d6552-124">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="d6552-124">d3d9.dll</span></span> |