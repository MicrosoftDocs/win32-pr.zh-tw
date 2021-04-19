---
title: D3D12_DOWNLEVEL_PRESENT_FLAGS 列舉
description: 傳遞至 ID3D12CommandQueueDownlevel 的旗標：:P 重發的方法。
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993858"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a><span data-ttu-id="86cbb-103">D3D12 \_ 下層 \_ 目前的 \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="86cbb-103">D3D12\_DOWNLEVEL\_PRESENT\_FLAGS enumeration</span></span>

<span data-ttu-id="86cbb-104">傳遞至 ID3D12CommandQueueDownlevel 的旗標 [**：:P**](id3d12commandqueuedownlevel-present.md) 重新傳送的函式來修改行為。</span><span class="sxs-lookup"><span data-stu-id="86cbb-104">Flags passed to the [**ID3D12CommandQueueDownlevel::Present**](id3d12commandqueuedownlevel-present.md) function to modify behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="86cbb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="86cbb-105">Syntax</span></span>

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a><span data-ttu-id="86cbb-106">常數</span><span class="sxs-lookup"><span data-stu-id="86cbb-106">Constants</span></span>

<span data-ttu-id="86cbb-107">**D3D12 \_ 下層 \_ 目前 \_ 旗標 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="86cbb-107">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_NONE**</span></span>

<span data-ttu-id="86cbb-108">未選取任何選項。</span><span class="sxs-lookup"><span data-stu-id="86cbb-108">No options selected.</span></span>

<span data-ttu-id="86cbb-109">**D3D12 \_ 下層 \_ 目前 \_ 旗 \_ 標 \_ 等候 \_ VBLANK**</span><span class="sxs-lookup"><span data-stu-id="86cbb-109">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_WAIT\_FOR\_VBLANK**</span></span>

<span data-ttu-id="86cbb-110">**目前** 的作業將不會執行，直到您上次 **顯示** ed 之後發生 VSync 為止。</span><span class="sxs-lookup"><span data-stu-id="86cbb-110">The **Present** operation won't be done until a VSync has occurred since the last time you **Present** ed.</span></span>

## <a name="requirements"></a><span data-ttu-id="86cbb-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="86cbb-111">Requirements</span></span>

| <span data-ttu-id="86cbb-112">需求</span><span class="sxs-lookup"><span data-stu-id="86cbb-112">Requirement</span></span> | <span data-ttu-id="86cbb-113">值</span><span class="sxs-lookup"><span data-stu-id="86cbb-113">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="86cbb-114">標頭</span><span class="sxs-lookup"><span data-stu-id="86cbb-114">Header</span></span> | <span data-ttu-id="86cbb-115">d3d12downlevel。h</span><span class="sxs-lookup"><span data-stu-id="86cbb-115">d3d12downlevel.h</span></span> |
| <span data-ttu-id="86cbb-116">DLL</span><span class="sxs-lookup"><span data-stu-id="86cbb-116">DLL</span></span>    | <span data-ttu-id="86cbb-117">D3D12.dll 只 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="86cbb-117">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="86cbb-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86cbb-118">See also</span></span>
* [<span data-ttu-id="86cbb-119">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="86cbb-119">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="86cbb-120">Windows 7 上的 Direct3D 12 列舉</span><span class="sxs-lookup"><span data-stu-id="86cbb-120">Direct3D 12 On Windows 7 enumerations</span></span>](direct3d-12on7-enumerations.md)
* [<span data-ttu-id="86cbb-121">Windows 7 上的 Direct3D 12 參考 (d3d12downlevel .h) </span><span class="sxs-lookup"><span data-stu-id="86cbb-121">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="86cbb-122">Windows 7 上的 Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="86cbb-122">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
