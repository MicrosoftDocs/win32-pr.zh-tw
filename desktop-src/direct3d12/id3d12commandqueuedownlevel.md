---
title: ID3D12CommandQueueDownlevel 介面
description: 提供 Windows 7 特定的現有機制。
keywords:
- ID3D12CommandQueueDownlevel 介面
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981076"
---
# <a name="id3d12commandqueuedownlevel-interface"></a><span data-ttu-id="7091c-104">ID3D12CommandQueueDownlevel 介面</span><span class="sxs-lookup"><span data-stu-id="7091c-104">ID3D12CommandQueueDownlevel interface</span></span>

<span data-ttu-id="7091c-105">在 [Windows 7 上使用 direct3d](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)12 時，可以從 [direct3d 12 命令佇列](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue)使用 **QueryInterface** 來存取這個介面。</span><span class="sxs-lookup"><span data-stu-id="7091c-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 command queue](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="7091c-106">它提供 Windows 7 特定的現有機制。</span><span class="sxs-lookup"><span data-stu-id="7091c-106">It provides a Windows-7-specific present mechanism.</span></span>

### <a name="methods"></a><span data-ttu-id="7091c-107">方法</span><span class="sxs-lookup"><span data-stu-id="7091c-107">Methods</span></span>

<span data-ttu-id="7091c-108">**ID3D12CommandQueueDownlevel** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7091c-108">The **ID3D12CommandQueueDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="7091c-109">方法</span><span class="sxs-lookup"><span data-stu-id="7091c-109">Method</span></span> | <span data-ttu-id="7091c-110">描述</span><span class="sxs-lookup"><span data-stu-id="7091c-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="7091c-111">**目前**</span><span class="sxs-lookup"><span data-stu-id="7091c-111">**Present**</span></span>](id3d12commandqueuedownlevel-present.md) | <span data-ttu-id="7091c-112">從 D3D12 Texture2D 資源將內容複寫到視窗。</span><span class="sxs-lookup"><span data-stu-id="7091c-112">Copies contents from a D3D12 Texture2D resource into a window.</span></span> |

## <a name="requirements"></a><span data-ttu-id="7091c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7091c-113">Requirements</span></span>

| <span data-ttu-id="7091c-114">需求</span><span class="sxs-lookup"><span data-stu-id="7091c-114">Requirement</span></span> | <span data-ttu-id="7091c-115">值</span><span class="sxs-lookup"><span data-stu-id="7091c-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="7091c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="7091c-116">Header</span></span> | <span data-ttu-id="7091c-117">d3d12downlevel。h</span><span class="sxs-lookup"><span data-stu-id="7091c-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="7091c-118">DLL</span><span class="sxs-lookup"><span data-stu-id="7091c-118">DLL</span></span>    | <span data-ttu-id="7091c-119">D3D12.dll 只 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="7091c-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="7091c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7091c-120">See also</span></span>
* [<span data-ttu-id="7091c-121">Windows 7 上的 Direct3D 12 介面</span><span class="sxs-lookup"><span data-stu-id="7091c-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="7091c-122">Windows 7 上的 Direct3D 12 參考 (d3d12downlevel .h) </span><span class="sxs-lookup"><span data-stu-id="7091c-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="7091c-123">Windows 7 上的 Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7091c-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
