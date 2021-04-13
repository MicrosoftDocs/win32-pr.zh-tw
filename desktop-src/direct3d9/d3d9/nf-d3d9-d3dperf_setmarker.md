---
title: D3DPERF_SetMarker 函式
description: 標示瞬間事件。 PIX 可以使用此事件來觸發動作。
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "104374706"
---
# <a name="d3dperf_setmarker-function"></a><span data-ttu-id="992e3-104">D3DPERF_SetMarker 函式</span><span class="sxs-lookup"><span data-stu-id="992e3-104">D3DPERF_SetMarker function</span></span>

<span data-ttu-id="992e3-105">標示瞬間事件。</span><span class="sxs-lookup"><span data-stu-id="992e3-105">Mark an instantaneous event.</span></span> <span data-ttu-id="992e3-106">PIX 可以使用此事件來觸發動作。</span><span class="sxs-lookup"><span data-stu-id="992e3-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="992e3-107">語法</span><span class="sxs-lookup"><span data-stu-id="992e3-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetMarker(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="992e3-108">參數</span><span class="sxs-lookup"><span data-stu-id="992e3-108">Parameters</span></span>

`col`

<span data-ttu-id="992e3-109">事件色彩。</span><span class="sxs-lookup"><span data-stu-id="992e3-109">Event color.</span></span> <span data-ttu-id="992e3-110">這是在事件檢視器中顯示事件的色彩。</span><span class="sxs-lookup"><span data-stu-id="992e3-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="992e3-111">事件名稱。</span><span class="sxs-lookup"><span data-stu-id="992e3-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="992e3-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="992e3-112">Return value</span></span>

<span data-ttu-id="992e3-113">此函數不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="992e3-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="992e3-114">備註</span><span class="sxs-lookup"><span data-stu-id="992e3-114">Remarks</span></span>

<span data-ttu-id="992e3-115">瞬間的使用者事件不會將其他事件括住或群組。</span><span class="sxs-lookup"><span data-stu-id="992e3-115">Instantaneous user events do not bracket or group other events.</span></span> <span data-ttu-id="992e3-116">例如，當使用者在遊戲中引發武器時， **D3DPERF_SetMarker** 的呼叫可能會建立 *引發引發* 的事件。</span><span class="sxs-lookup"><span data-stu-id="992e3-116">For example, when the user fires a weapon in a game, a *Shot Fired* event could be created by a **D3DPERF_SetMarker** call.</span></span> <span data-ttu-id="992e3-117">若要將多個事件以單一、使用者定義的名稱群組在一起，請使用 **D3DPERF_BeginEvent** 和 **D3DPERF_EndEvent** ，而不是 **D3DPERF_SetMarker**。</span><span class="sxs-lookup"><span data-stu-id="992e3-117">To group together multiple events under a single, user-defined name, use **D3DPERF_BeginEvent** and **D3DPERF_EndEvent** rather than **D3DPERF_SetMarker**.</span></span>

## <a name="requirements"></a><span data-ttu-id="992e3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="992e3-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="992e3-119">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="992e3-119">**Target Platform**</span></span> | <span data-ttu-id="992e3-120">Windows</span><span class="sxs-lookup"><span data-stu-id="992e3-120">Windows</span></span> |
| <span data-ttu-id="992e3-121">**標頭**</span><span class="sxs-lookup"><span data-stu-id="992e3-121">**Header**</span></span> | <span data-ttu-id="992e3-122">d3d9。h</span><span class="sxs-lookup"><span data-stu-id="992e3-122">d3d9.h</span></span> |
| <span data-ttu-id="992e3-123">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="992e3-123">**Library**</span></span> | <span data-ttu-id="992e3-124">d3d9 .lib</span><span class="sxs-lookup"><span data-stu-id="992e3-124">d3d9.lib</span></span> |
| <span data-ttu-id="992e3-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="992e3-125">**DLL**</span></span> | <span data-ttu-id="992e3-126">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="992e3-126">d3d9.dll</span></span> |