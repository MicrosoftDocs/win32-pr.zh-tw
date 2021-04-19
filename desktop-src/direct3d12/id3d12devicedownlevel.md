---
title: ID3D12DeviceDownlevel 介面
description: 提供 Windows 7 特定的記憶體統計資料查詢。
keywords:
- ID3D12DeviceDownlevel 介面
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998996"
---
# <a name="id3d12devicedownlevel-interface"></a><span data-ttu-id="70e15-104">ID3D12DeviceDownlevel 介面</span><span class="sxs-lookup"><span data-stu-id="70e15-104">ID3D12DeviceDownlevel interface</span></span>

<span data-ttu-id="70e15-105">在 [Windows 7 上使用 direct3d](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)12 裝置時，可以透過 **QueryInterface** 從 [direct3d 12 裝置](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)存取這個介面。</span><span class="sxs-lookup"><span data-stu-id="70e15-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 device](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="70e15-106">它會提供 Windows 7 特定的記憶體統計資料查詢。</span><span class="sxs-lookup"><span data-stu-id="70e15-106">It provides a Windows-7-specific memory statistics query.</span></span>

### <a name="methods"></a><span data-ttu-id="70e15-107">方法</span><span class="sxs-lookup"><span data-stu-id="70e15-107">Methods</span></span>

<span data-ttu-id="70e15-108">**ID3D12DeviceDownlevel** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="70e15-108">The **ID3D12DeviceDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="70e15-109">方法</span><span class="sxs-lookup"><span data-stu-id="70e15-109">Method</span></span> | <span data-ttu-id="70e15-110">描述</span><span class="sxs-lookup"><span data-stu-id="70e15-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="70e15-111">**QueryVideoMemoryInfo**</span><span class="sxs-lookup"><span data-stu-id="70e15-111">**QueryVideoMemoryInfo**</span></span>](id3d12devicedownlevel-queryvideomemoryinfo.md) | <span data-ttu-id="70e15-112">提供 Windows 7 的記憶體統計資料。</span><span class="sxs-lookup"><span data-stu-id="70e15-112">Provides memory statistics on Windows 7.</span></span> |

## <a name="requirements"></a><span data-ttu-id="70e15-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="70e15-113">Requirements</span></span>

| <span data-ttu-id="70e15-114">需求</span><span class="sxs-lookup"><span data-stu-id="70e15-114">Requirement</span></span> | <span data-ttu-id="70e15-115">值</span><span class="sxs-lookup"><span data-stu-id="70e15-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="70e15-116">標頭</span><span class="sxs-lookup"><span data-stu-id="70e15-116">Header</span></span> | <span data-ttu-id="70e15-117">d3d12downlevel。h</span><span class="sxs-lookup"><span data-stu-id="70e15-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="70e15-118">DLL</span><span class="sxs-lookup"><span data-stu-id="70e15-118">DLL</span></span>    | <span data-ttu-id="70e15-119">D3D12.dll 只 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="70e15-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="70e15-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70e15-120">See also</span></span>
* [<span data-ttu-id="70e15-121">Windows 7 上的 Direct3D 12 介面</span><span class="sxs-lookup"><span data-stu-id="70e15-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="70e15-122">Windows 7 上的 Direct3D 12 參考 (d3d12downlevel .h) </span><span class="sxs-lookup"><span data-stu-id="70e15-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="70e15-123">Windows 7 上的 Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="70e15-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
