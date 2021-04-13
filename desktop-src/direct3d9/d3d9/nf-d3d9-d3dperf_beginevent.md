---
title: D3DPERF_BeginEvent 函式
description: 標記使用者定義事件的開頭。 PIX 可以使用此事件來觸發動作。
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "104374703"
---
# <a name="d3dperf_beginevent-function"></a><span data-ttu-id="46339-104">D3DPERF_BeginEvent 函式</span><span class="sxs-lookup"><span data-stu-id="46339-104">D3DPERF_BeginEvent function</span></span>

<span data-ttu-id="46339-105">標記使用者定義事件的開頭。</span><span class="sxs-lookup"><span data-stu-id="46339-105">Marks the beginning of a user-defined event.</span></span> <span data-ttu-id="46339-106">PIX 可以使用此事件來觸發動作。</span><span class="sxs-lookup"><span data-stu-id="46339-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="46339-107">語法</span><span class="sxs-lookup"><span data-stu-id="46339-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_BeginEvent(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="46339-108">參數</span><span class="sxs-lookup"><span data-stu-id="46339-108">Parameters</span></span>

`col`

<span data-ttu-id="46339-109">事件色彩。</span><span class="sxs-lookup"><span data-stu-id="46339-109">Event color.</span></span> <span data-ttu-id="46339-110">這是在事件檢視器中顯示事件的色彩。</span><span class="sxs-lookup"><span data-stu-id="46339-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="46339-111">事件名稱。</span><span class="sxs-lookup"><span data-stu-id="46339-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="46339-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="46339-112">Return value</span></span>

<span data-ttu-id="46339-113">此事件開始的階層之以零為基底的層級。</span><span class="sxs-lookup"><span data-stu-id="46339-113">The zero-based level of the hierarchy that this event is starting in.</span></span> <span data-ttu-id="46339-114">如果發生錯誤，傳回值將會是負數。</span><span class="sxs-lookup"><span data-stu-id="46339-114">If an error occurs, the return value will be negative.</span></span>

## <a name="remarks"></a><span data-ttu-id="46339-115">備註</span><span class="sxs-lookup"><span data-stu-id="46339-115">Remarks</span></span>

<span data-ttu-id="46339-116">使用者自訂事件會以對目的程式有意義的方式，將其他事件群組在一起，使其在效能分析工具中更能呈現。</span><span class="sxs-lookup"><span data-stu-id="46339-116">User-defined events group together other events in a way that is meaningful to the target program so that they can be better represented in performance profiling tools.</span></span> <span data-ttu-id="46339-117">例如， *Draw 太空船* 事件可能會括住一些處理遊戲中繪製太空船的 Direct3D 呼叫。</span><span class="sxs-lookup"><span data-stu-id="46339-117">For example, a *Draw Spaceship* event might bracket a number of Direct3D calls that handle drawing a spaceship in a game.</span></span> <span data-ttu-id="46339-118">事件可以進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="46339-118">Events can be nested.</span></span>

<span data-ttu-id="46339-119">每個 **D3DPERF_BeginEvent** 呼叫都應該有相符的 **D3DPERF_EndEvent** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="46339-119">Each **D3DPERF_BeginEvent** call should have a matching **D3DPERF_EndEvent** call.</span></span> <span data-ttu-id="46339-120"> (不會將其他事件放在) 的即時事件，應該使用 **D3DPERF_SetMarker** 來標記，而不是 **D3DPERF_BeginEvent** 和 **D3DPERF_EndEvent**。</span><span class="sxs-lookup"><span data-stu-id="46339-120">Instantaneous events (which do not bracket other events) should be labeled by using **D3DPERF_SetMarker** rather than by **D3DPERF_BeginEvent** and **D3DPERF_EndEvent**.</span></span>

## <a name="requirements"></a><span data-ttu-id="46339-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="46339-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="46339-122">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="46339-122">**Target Platform**</span></span> | <span data-ttu-id="46339-123">Windows</span><span class="sxs-lookup"><span data-stu-id="46339-123">Windows</span></span> |
| <span data-ttu-id="46339-124">**標頭**</span><span class="sxs-lookup"><span data-stu-id="46339-124">**Header**</span></span> | <span data-ttu-id="46339-125">d3d9。h</span><span class="sxs-lookup"><span data-stu-id="46339-125">d3d9.h</span></span> |
| <span data-ttu-id="46339-126">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="46339-126">**Library**</span></span> | <span data-ttu-id="46339-127">d3d9 .lib</span><span class="sxs-lookup"><span data-stu-id="46339-127">d3d9.lib</span></span> |
| <span data-ttu-id="46339-128">**DLL**</span><span class="sxs-lookup"><span data-stu-id="46339-128">**DLL**</span></span> | <span data-ttu-id="46339-129">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="46339-129">d3d9.dll</span></span> |