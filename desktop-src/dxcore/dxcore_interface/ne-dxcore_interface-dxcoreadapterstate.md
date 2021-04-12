---
title: DXCoreAdapterState
description: 定義常數，指定 DXCore 介面卡狀態的種類。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: e588b75360c141b52989aa14e88c886092af2647
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315559"
---
# <a name="dxcoreadapterstate-enum"></a><span data-ttu-id="43188-103">DXCoreAdapterState 列舉</span><span class="sxs-lookup"><span data-stu-id="43188-103">DXCoreAdapterState enum</span></span>

<span data-ttu-id="43188-104">定義常數，指定 DXCore 介面卡狀態的種類。</span><span class="sxs-lookup"><span data-stu-id="43188-104">Defines constants that specify kinds of DXCore adapter states.</span></span> <span data-ttu-id="43188-105">將下列其中一個常數傳遞給 [IDXCoreAdapter：： QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) 方法，以取得狀態種類的介面卡狀態專案。將常數傳遞給 [IDXCoreAdapter：： SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) 方法，以設定狀態專案的介面卡資訊。</span><span class="sxs-lookup"><span data-stu-id="43188-105">Pass one of these constants to the [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) method to retrieve the adapter state item for a state kind; pass a constant to the [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) method to set an adapter's info for a state item.</span></span>

## <a name="syntax"></a><span data-ttu-id="43188-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="43188-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a><span data-ttu-id="43188-107">常數</span><span class="sxs-lookup"><span data-stu-id="43188-107">Constants</span></span>

### <a name="isdriverupdateinprogress"></a><span data-ttu-id="43188-108">IsDriverUpdateInProgress</span><span class="sxs-lookup"><span data-stu-id="43188-108">IsDriverUpdateInProgress</span></span>

<span data-ttu-id="43188-109">指定 <em>IsDriverUpdateInProgress</em> 介面卡狀態，表示已在 `true` 介面卡上起始驅動程式更新，但尚未完成。</span><span class="sxs-lookup"><span data-stu-id="43188-109">Specifies the <em>IsDriverUpdateInProgress</em> adapter state, which when `true` indicates that a driver update has been initiated on the adapter but it has not yet completed.</span></span> <span data-ttu-id="43188-110">如果驅動程式更新已完成，則介面卡將會失效，而您的[QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)呼叫會傳回<b>DXGI_ERROR_DEVICE_REMOVED</b>的<b>HRESULT</b> 。</span><span class="sxs-lookup"><span data-stu-id="43188-110">If the driver update has already completed, then the adapter will have been invalidated, and your [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) call will return a <b>HRESULT</b> of <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span></span>

<span data-ttu-id="43188-111">呼叫 [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)時， <em>IsDriverUpdateInProgress</em> 狀態專案的類型 <b>uint8_t</b>，代表布林值。</span><span class="sxs-lookup"><span data-stu-id="43188-111">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>IsDriverUpdateInProgress</em> state item has type <b>uint8_t</b>, representing a Boolean value.</span></span>

<span data-ttu-id="43188-112"><b>重要</b>：</span><span class="sxs-lookup"><span data-stu-id="43188-112"><b>Important</b>.</span></span> <span data-ttu-id="43188-113">此狀態專案不支援 [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)。</span><span class="sxs-lookup"><span data-stu-id="43188-113">This state item is not supported for [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span></span>

### <a name="adaptermemorybudget"></a><span data-ttu-id="43188-114">AdapterMemoryBudget</span><span class="sxs-lookup"><span data-stu-id="43188-114">AdapterMemoryBudget</span></span>

<span data-ttu-id="43188-115">指定可在介面卡上抓取或要求介面卡記憶體預算的 <em>AdapterMemoryBudget</em> 介面卡狀態。</span><span class="sxs-lookup"><span data-stu-id="43188-115">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span>

<span data-ttu-id="43188-116">呼叫 [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)時， <em>AdapterMemoryBudget</em>介面卡狀態具有 *inputStateDetails* 的類型 <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> ，以及 *DXCoreAdapterMemoryBudget* 的類型 <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">outputBuffer</a> 。</span><span class="sxs-lookup"><span data-stu-id="43188-116">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> for *outputBuffer*.</span></span>

## <a name="see-also"></a><span data-ttu-id="43188-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43188-117">See also</span></span>

<span data-ttu-id="43188-118">[IDXCoreAdapter：： QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)、 [IDXCoreAdapter：： SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="43188-118">[IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>