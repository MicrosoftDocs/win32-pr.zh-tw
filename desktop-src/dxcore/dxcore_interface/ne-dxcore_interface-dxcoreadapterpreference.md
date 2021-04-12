---
title: DXCoreAdapterPreference
description: 定義常數，指定要當做清單排序準則使用的 DXCore 介面卡喜好設定。
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376172"
---
# <a name="dxcoreadapterpreference-enum"></a><span data-ttu-id="4f0ae-103">DXCoreAdapterPreference 列舉</span><span class="sxs-lookup"><span data-stu-id="4f0ae-103">DXCoreAdapterPreference enum</span></span>

## <a name="description"></a><span data-ttu-id="4f0ae-104">Description</span><span class="sxs-lookup"><span data-stu-id="4f0ae-104">Description</span></span>

<span data-ttu-id="4f0ae-105">定義常數，指定要當做清單排序準則使用的 DXCore 介面卡喜好設定。</span><span class="sxs-lookup"><span data-stu-id="4f0ae-105">Defines constants that specify DXCore adapter preferences to be used as list-sorting criteria.</span></span> <span data-ttu-id="4f0ae-106">您可以藉由將 **DXCoreAdapterPreference** 陣列傳遞至 [IDXCoreAdapterList：： sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md)，來排序 DXCore 介面卡清單。</span><span class="sxs-lookup"><span data-stu-id="4f0ae-106">You can sort a DXCore adapter list by passing an array of **DXCoreAdapterPreference** to [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f0ae-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f0ae-107">Syntax</span></span>

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a><span data-ttu-id="4f0ae-108">列舉欄位</span><span class="sxs-lookup"><span data-stu-id="4f0ae-108">Enum fields</span></span>

### <a name="hardware"></a><span data-ttu-id="4f0ae-109">硬體</span><span class="sxs-lookup"><span data-stu-id="4f0ae-109">Hardware</span></span>

<span data-ttu-id="4f0ae-110">指定硬體配接器 (的喜好設定，而不是) 的軟體配接器。</span><span class="sxs-lookup"><span data-stu-id="4f0ae-110">Specifies a preference for hardware adapters (as opposed to software adapters).</span></span>

### <a name="minimumpower"></a><span data-ttu-id="4f0ae-111">MinimumPower</span><span class="sxs-lookup"><span data-stu-id="4f0ae-111">MinimumPower</span></span>

<span data-ttu-id="4f0ae-112">指定最小的 GPU (的喜好設定，例如整合式圖形處理器或 iGPU) 。</span><span class="sxs-lookup"><span data-stu-id="4f0ae-112">Specifies a preference for the minimum-powered GPU (such as an integrated graphics processor, or iGPU).</span></span>

### <a name="highperformance"></a><span data-ttu-id="4f0ae-113">高效能</span><span class="sxs-lookup"><span data-stu-id="4f0ae-113">HighPerformance</span></span>

<span data-ttu-id="4f0ae-114">指定最高效能 GPU 的喜好設定，例如外部圖形處理器 (xGPU) （如果有的話），或離散圖形處理器 (dGPU) （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="4f0ae-114">Specifies a preference for the highest-performance GPU, such as an external graphics processor (xGPU), if available, or discrete graphics processor (dGPU) if available.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f0ae-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f0ae-115">See also</span></span>

<span data-ttu-id="4f0ae-116">[IDXCoreAdapterList：： Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="4f0ae-116">[IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>