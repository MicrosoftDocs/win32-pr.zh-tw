---
title: DXCoreAdapterMemoryBudget
description: 描述介面卡的記憶體預算。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463621"
---
# <a name="dxcoreadaptermemorybudget-structure"></a><span data-ttu-id="c39fe-103">DXCoreAdapterMemoryBudget 結構</span><span class="sxs-lookup"><span data-stu-id="c39fe-103">DXCoreAdapterMemoryBudget structure</span></span>

<span data-ttu-id="c39fe-104">指定可在介面卡上抓取或要求介面卡記憶體預算的 <em>AdapterMemoryBudget</em> 介面卡狀態。</span><span class="sxs-lookup"><span data-stu-id="c39fe-104">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span> <span data-ttu-id="c39fe-105">設定要求) 預算的 (代表要在介面卡上保留的最小實體記憶體（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c39fe-105">Setting (requesting) a budget represents the minimum required physical memory to reserve, in bytes, on the adapter.</span></span> <span data-ttu-id="c39fe-106">建議您設定介面卡保留區，以代表您的應用程式在沒有的情況下無法移出的實體記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="c39fe-106">We recommend that you set an adapter reservation in order to denote the amount of physical memory that your application can't go without.</span></span> <span data-ttu-id="c39fe-107">此值可協助作業系統 (作業系統) ，快速將大型記憶體壓力情況的影響降到最低。</span><span class="sxs-lookup"><span data-stu-id="c39fe-107">This value helps the operating system (OS) to quickly minimize the impact of large memory-pressure situations.</span></span>

<span data-ttu-id="c39fe-108">呼叫 [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)時， <em>AdapterMemoryBudget</em>介面卡狀態具有 *inputStateDetails* 的類型 <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> ，以及 *DXCoreAdapterMemoryBudget* 的類型 **outputBuffer** 。</span><span class="sxs-lookup"><span data-stu-id="c39fe-108">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **DXCoreAdapterMemoryBudget** for *outputBuffer*.</span></span>

<span data-ttu-id="c39fe-109">呼叫 [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)時， <em>AdapterMemoryBudget</em>介面卡狀態具有 *inputStateDetails* 的類型 <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> ，以及 *inputData* 的類型 **uint64_t** 。</span><span class="sxs-lookup"><span data-stu-id="c39fe-109">When calling [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **uint64_t** for *inputData*.</span></span>

## <a name="syntax"></a><span data-ttu-id="c39fe-110">語法</span><span class="sxs-lookup"><span data-stu-id="c39fe-110">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a><span data-ttu-id="c39fe-111">成員</span><span class="sxs-lookup"><span data-stu-id="c39fe-111">Members</span></span>

### <a name="budget"></a><span data-ttu-id="c39fe-112">預算</span><span class="sxs-lookup"><span data-stu-id="c39fe-112">budget</span></span>

<span data-ttu-id="c39fe-113">類型： **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="c39fe-113">Type: **uint64_t**</span></span>

<span data-ttu-id="c39fe-114">以位元組為單位，指定您的應用程式應鎖定的 OS 提供的介面卡記憶體預算（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c39fe-114">Specifies the OS-provided adapter memory budget, in bytes, that your application should target.</span></span> <span data-ttu-id="c39fe-115">如果 *currentUsage* 大於 *預算*，則您的應用程式可能會因為 OS 的背景活動而產生間斷情形或效能上的負面影響，這是為了讓其他應用程式能夠公平使用介面卡記憶體。</span><span class="sxs-lookup"><span data-stu-id="c39fe-115">If *currentUsage* is greater than *budget*, then your application may incur stuttering or performance penalties due to background activity by the OS, which is intended to provide other applications with a fair usage of adapter memory.</span></span>

### <a name="currentusage"></a><span data-ttu-id="c39fe-116">currentUsage</span><span class="sxs-lookup"><span data-stu-id="c39fe-116">currentUsage</span></span>

<span data-ttu-id="c39fe-117">類型： **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="c39fe-117">Type: **uint64_t**</span></span>

<span data-ttu-id="c39fe-118">指定應用程式目前的介面卡記憶體使用量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c39fe-118">Specifies your applicaton's current adapter memory usage, in bytes.</span></span>

### <a name="availableforreservation"></a><span data-ttu-id="c39fe-119">availableForReservation</span><span class="sxs-lookup"><span data-stu-id="c39fe-119">availableForReservation</span></span>

<span data-ttu-id="c39fe-120">類型： **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="c39fe-120">Type: **uint64_t**</span></span>

<span data-ttu-id="c39fe-121">指定您的應用程式可用於保留的介面卡記憶體量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c39fe-121">Specifies the amount of adapter memory, in bytes, that your application has available for reservation.</span></span> <span data-ttu-id="c39fe-122">若要保留此介面卡記憶體，您的應用程式應該呼叫 [IDXCoreAdapter：： SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) ，並將 *狀態* 設定為 [DXCoreAdapterState：： AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)。</span><span class="sxs-lookup"><span data-stu-id="c39fe-122">To reserve this adapter memory, your application should call [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) with *state* set to [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).</span></span>

### <a name="currentreservation"></a><span data-ttu-id="c39fe-123">currentReservation</span><span class="sxs-lookup"><span data-stu-id="c39fe-123">currentReservation</span></span>

<span data-ttu-id="c39fe-124">類型： **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="c39fe-124">Type: **uint64_t**</span></span>

<span data-ttu-id="c39fe-125">指定應用程式所保留的介面卡記憶體量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c39fe-125">Specifies the amount of adapter memory, in bytes, that is reserved by your application.</span></span> <span data-ttu-id="c39fe-126">OS 會使用保留做為提示，判斷應用程式的最小工作集。</span><span class="sxs-lookup"><span data-stu-id="c39fe-126">The OS uses the reservation as a hint to determine your application's minimum working set.</span></span> <span data-ttu-id="c39fe-127">您的應用程式應嘗試確定其介面卡的記憶體使用量可進行修剪，以符合此需求。</span><span class="sxs-lookup"><span data-stu-id="c39fe-127">Your application should attempt to ensure that its adapter memory usage can be trimmed to meet this requirement.</span></span>

## <a name="see-also"></a><span data-ttu-id="c39fe-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c39fe-128">See also</span></span>

<span data-ttu-id="c39fe-129">[DXCore 參考](../dxcore-reference.md)， [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="c39fe-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>