---
title: 使用 DXCore 來列舉介面卡
description: 查看 DXCore 的主要功能，並提供一些程式碼範例，以及最基本 DXCore 應用程式的完整源代碼清單。
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: f1c21971f2daea69de1f317d1db8eceb9ec00118
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968497"
---
# <a name="using-dxcore-to-enumerate-adapters"></a><span data-ttu-id="9dfd3-103">使用 DXCore 來列舉介面卡</span><span class="sxs-lookup"><span data-stu-id="9dfd3-103">Using DXCore to enumerate adapters</span></span>

<span data-ttu-id="9dfd3-104">DXCore 是適用于 DirectX 裝置的介面卡列舉 API，因此其某些設備會與 [DXGI](../direct3ddxgi/dx-graphics-dxgi.md)的部分重迭。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-104">DXCore is an adapter enumeration API for DirectX devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span>

<span data-ttu-id="9dfd3-105">DXCore 可讓您將新的裝置類型公開至使用者模式，例如 MCDM (Microsoft Compute Driver Model) ，以搭配 [Direct3D 12](../direct3d12/directx-12-programming-guide.md)、 [DirectML](../direct3d12/dml.md)和 [Windows Machine Learning](/windows/ai/windows-ml/)使用。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-105">DXCore enables the exposure of new device types to user mode, such as MCDM (Microsoft Compute Driver Model), for use with [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md), and [Windows Machine Learning](/windows/ai/windows-ml/).</span></span> <span data-ttu-id="9dfd3-106">與 DXGI 不同的是，DXCore 不會提供有關顯示相關技術或屬性的任何資訊</span><span class="sxs-lookup"><span data-stu-id="9dfd3-106">DXCore, unlike DXGI, does not provide any information about display-related technology or properties</span></span>

<span data-ttu-id="9dfd3-107">在接下來的幾節中，我們將探討 DXCore 的主要功能，其中包含一些程式碼範例， (以 [c + +/WinRT](/windows/uwp/cpp-and-winrt-apis)) 撰寫。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-107">In the next few sections, we'll take a look at the main features of DXCore with some code examples (written in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span></span> <span data-ttu-id="9dfd3-108">以下所示的程式碼範例會從完整的源代碼清單中解壓縮，您可以在 [最基本的 DXCore 應用程式](dxcore-source-code.md)中找到這些程式碼。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-108">The code examples shown below are extracted from the full source code listing that you can find in the topic [Minimal DXCore application](dxcore-source-code.md).</span></span>

## <a name="create-an-adapter-factory"></a><span data-ttu-id="9dfd3-109">建立介面卡 factory</span><span class="sxs-lookup"><span data-stu-id="9dfd3-109">Create an adapter factory</span></span>

<span data-ttu-id="9dfd3-110">您可以藉由建立 [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) 介面所表示的介面卡 factory 物件，開始 DXCore 介面卡列舉。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-110">You begin DXCore adapter enumeration by creating an adapter factory object, which is represented by the [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span> <span data-ttu-id="9dfd3-111">若要建立 factory，請包含 `dxcore.h` 標頭檔，然後呼叫 [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) free 函式。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-111">To create a factory, include the `dxcore.h` header file, and call the [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) free function.</span></span>

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a><span data-ttu-id="9dfd3-112">取得介面卡清單</span><span class="sxs-lookup"><span data-stu-id="9dfd3-112">Retrieve an adapter list</span></span>

<span data-ttu-id="9dfd3-113">與 DXGI 不同的是，新建立的 DXCore 介面卡 factory 不會自動建立系統的介面卡狀態的快照集。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-113">Unlike with DXGI, a newly-created DXCore adapter factory doesn't automatically create a snapshot of the adapter state of the system.</span></span> <span data-ttu-id="9dfd3-114">相反地，當您明確抓取以 [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) 介面表示的介面卡清單物件時，DXCore 會建立該快照集。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-114">Instead, DXCore creates that snapshot when you explicitly retrieve an adapter list object, which is represented by the [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface.</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a><span data-ttu-id="9dfd3-115">從清單中選取適當的介面卡</span><span class="sxs-lookup"><span data-stu-id="9dfd3-115">Select an appropriate adapter from the list</span></span>

<span data-ttu-id="9dfd3-116">本節將示範如何在指定介面卡清單物件的情況下，找到清單中的第一個硬體配接器。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-116">This section demonstrates how, given an adapter list object, you could find the first hardware adapter in the list.</span></span>

<span data-ttu-id="9dfd3-117">[**IDXCoreAdapterList：： GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md)方法會告訴您清單中的元素數目，而 [**IDXCoreAdapterList：： GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md)會依索引抓取特定的介面卡。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-117">The [**IDXCoreAdapterList::GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) method tells you the number of elements in the list, and [**IDXCoreAdapterList::GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) retrieves a specific adapter by index.</span></span>

<span data-ttu-id="9dfd3-118">然後，您可以依照下列步驟來查詢該介面卡的屬性。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-118">You can then query the properties of that adapter, by following these steps.</span></span>

- <span data-ttu-id="9dfd3-119">首先，若要確認它是有效的，可在此作業系統版本上取得此介面卡的指定屬性值，您可以呼叫 [**IDXCoreAdapter：： IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md)。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-119">First, to confirm that it's valid to retrieve the value of a given property for this adapter on this operating system version, you call [**IDXCoreAdapter::IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span></span> <span data-ttu-id="9dfd3-120">傳遞 [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) 列舉的值，以識別您要查詢的屬性。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-120">Pass a value of the [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) enumeration to identify which property you're querying about.</span></span>
- <span data-ttu-id="9dfd3-121">您可以選擇性地使用 [**IDXCoreAdapter：： GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md)的呼叫來確認屬性值的大小。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-121">Optionally confirm the size of the property value with a call to [**IDXCoreAdapter::GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span></span> <span data-ttu-id="9dfd3-122">對於 **DXCoreAdapterProperty：： IsHardware** 之類的屬性（這是簡單的布林值），則不需要此步驟。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-122">For a property such as **DXCoreAdapterProperty::IsHardware**, which is a simple Boolean, this step isn't necessary.</span></span>
- <span data-ttu-id="9dfd3-123">最後，藉由呼叫 [**IDXCoreAdapter：： GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md)來取得屬性的值。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-123">And, finally, retrieve the property's value by calling [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

const uint32_t count{ d3D12CoreComputeAdapters->GetAdapterCount() };

for (uint32_t i = 0; i < count; ++i)
{
    winrt::com_ptr<IDXCoreAdapter> candidateAdapter;
    winrt::check_hresult(
        d3D12CoreComputeAdapters->GetAdapter(i, candidateAdapter.put()));

    bool isHardware{ false };
    winrt::check_hresult(candidateAdapter->GetProperty(
        DXCoreAdapterProperty::IsHardware,
        &isHardware));

    if (isHardware)
    {
        // Choose the first hardware adapter, and stop looping.
        preferredAdapter = candidateAdapter;
        break;
    }

    // Otherwise, ensure that (as long as there are *any* adapters) we'll
    // at least choose one.
    if (!preferredAdapter)
    {
        preferredAdapter = candidateAdapter;
    }
}
```

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a><span data-ttu-id="9dfd3-124">藉由排序介面卡清單來選取慣用的介面卡</span><span class="sxs-lookup"><span data-stu-id="9dfd3-124">Select the preferred adapter by sorting an adapter list</span></span>

<span data-ttu-id="9dfd3-125">您可以藉由呼叫 [IDXCoreAdapterList：： sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) 方法來排序 DXCore 介面卡清單。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-125">You can sort a DXCore adapter list by calling the [IDXCoreAdapterList::Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) method.</span></span>

<span data-ttu-id="9dfd3-126">[DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md)列舉會定義代表排序準則的值。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-126">The [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) enumeration defines values that representing sort criteria.</span></span> <span data-ttu-id="9dfd3-127">傳遞這些值的陣列以 **進行排序**，然後讀取產生的排序清單中的第一個介面卡。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-127">Pass an array of those values to **Sort**, and then read off the first adapter in the resulting sorted list.</span></span>

<span data-ttu-id="9dfd3-128">若要判斷排序類型是否要依 **排序** 來理解，請先呼叫 [IDXCoreAdapterList：： IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md)。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-128">To determine whether a sort type is going to be understood by **Sort**, first call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> TryFindHardwareHighPerformanceGraphicsAdapter()
{
    // You begin DXCore adapter enumeration by creating an adapter factory.
    winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
    winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));

    // From the factory, retrieve a list of all the Direct3D 12 Graphics adapters.
    winrt::com_ptr<IDXCoreAdapterList> d3D12GraphicsAdapters;
    GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS };
    winrt::check_hresult(
        adapterFactory->CreateAdapterList(_countof(attributes),
            attributes,
            d3D12GraphicsAdapters.put()));

    DXCoreAdapterPreference sortPreferences[]{
        DXCoreAdapterPreference::Hardware, DXCoreAdapterPreference::HighPerformance };

    // Ask the OS to sort for the highest performance hardware adapter.
    winrt::check_hresult(d3D12GraphicsAdapters->Sort(_countof(sortPreferences), sortPreferences));

    winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

    if (d3D12GraphicsAdapters->GetAdapterCount() > 0)
    {
        winrt::check_hresult(d3D12GraphicsAdapters->GetAdapter(0, preferredAdapter.put()));
    }

    return preferredAdapter;
}
```

## <a name="query-and-set-adapter-state-properties"></a><span data-ttu-id="9dfd3-129">查詢和設定介面卡狀態 (屬性) </span><span class="sxs-lookup"><span data-stu-id="9dfd3-129">Query and set adapter state (properties)</span></span>

<span data-ttu-id="9dfd3-130">您可以藉由呼叫 [**IDXCoreAdapter：： QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) 和 [**IDXCoreAdapter：： SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) 方法，來取得和設定介面卡之指定狀態專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-130">You can retrieve and set the state of a specified state item of an adapter by calling the [**IDXCoreAdapter::QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) and [**IDXCoreAdapter::SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) methods.</span></span>

```cppwinrt
void SetDesiredMemoryReservation(winrt::com_ptr<IDXCoreAdapter> const& adapter, uint64_t reservation)
{
    DXCoreAdapterMemoryBudgetNodeSegmentGroup nodeSegmentGroup{};
    nodeSegmentGroup.nodeIndex = 0;
    nodeSegmentGroup.segmentGroup = DXCoreSegmentGroup::Local;

    DXCoreAdapterMemoryBudget memoryBudget{};
    winrt::check_hresult(adapter->QueryState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &memoryBudget));

    // Clamp the reservation to what's available.
    reservation = std::min<uint64_t>(reservation, memoryBudget.availableForReservation);

    winrt::check_hresult(adapter->SetState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &reservation));
}
```

<span data-ttu-id="9dfd3-131">在實務上，呼叫 **QueryState** 和 **SetState** 之前，您應該先呼叫 [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) 來確認查詢狀態種類是否適用于此介面卡和作業系統 (作業系統) 。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-131">In practice, before calling **QueryState** and **SetState**, you should call [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="adapter-list-freshness"></a><span data-ttu-id="9dfd3-132">介面卡清單時效性</span><span class="sxs-lookup"><span data-stu-id="9dfd3-132">Adapter list freshness</span></span>

<span data-ttu-id="9dfd3-133">如果介面卡清單因為系統狀況變更而變得過時，則會標示為如此。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-133">Should an adapter list become stale due to changing system conditions, it will be marked as such.</span></span> <span data-ttu-id="9dfd3-134">您可以藉由輪詢 [**IDXCoreAdapterList：： IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) 方法來判斷介面卡清單的有效期限。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-134">You can determine an adapter list's freshness by polling its [**IDXCoreAdapterList::IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) method.</span></span>

<span data-ttu-id="9dfd3-135">不過，更方便的方式是，您可以訂閱過期等狀況的通知。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-135">More conveniently, though, you can subscribe to notifications for conditions such as staleness.</span></span> <span data-ttu-id="9dfd3-136">若要這樣做，請將 [**DXCoreNotificationType：： AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) 傳遞至 [**IDXCoreAdapterFactory：： RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)，並安全地儲存傳回的 cookie 以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-136">To do that, pass [**DXCoreNotificationType::AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) to [**IDXCoreAdapterFactory::RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), and safely store the returned cookie for use later.</span></span>

```cppwinrt
uint32_t m_eventCookie = 0;
...
winrt::check_hresult(factory->RegisterEventNotification(
    m_adapters.get(),
    DXCoreNotificationType::AdapterListStale,
    OnAdapterListStale,
    this,
    &m_eventCookie));
...
static void WINAPI OnAdapterListStale(
    DXCoreNotificationType notificationType,
    IUnknown* staleObject,
    void* context)
{
    ...
}
```

<span data-ttu-id="9dfd3-137">然後，您可以從已有的 factory 物件產生新的、目前的介面卡清單物件。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-137">You can then generate a new, current, adapter list object from the factory object that you already have.</span></span> <span data-ttu-id="9dfd3-138">處理這些條件對於您能夠順暢地回應事件（例如介面卡抵達和移除）、 (是否為 GPU、特製化的計算介面卡) ，以及適當地轉移工作負載的回應，都很重要。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-138">Handling these conditions is critical to your ability to seamlessly respond to events such as adapter arrival and removal (whether that be a GPU, or a specialized compute adapter), and to appropriately shift workloads in response.</span></span>

<span data-ttu-id="9dfd3-139">在您終結介面卡清單物件之前，您必須使用 cookie 值，藉由呼叫 [IDXCoreAdapterFactory：： UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)，從通知取消註冊該物件。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-139">Before you destroy the adapter list object, you must use the cookie value to unregister that object from notifications by calling [IDXCoreAdapterFactory::UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span></span> <span data-ttu-id="9dfd3-140">如果您沒有取消註冊，則在偵測到情況時，就會引發嚴重的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-140">If you don't unregister, then a fatal exception is raised when the situation is detected.</span></span>

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a><span data-ttu-id="9dfd3-141">顯示資訊</span><span class="sxs-lookup"><span data-stu-id="9dfd3-141">Display information</span></span>

> [!NOTE]
> <span data-ttu-id="9dfd3-142">DXCore 本身不會提供任何顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-142">DXCore doesn't itself provide any display information.</span></span> <span data-ttu-id="9dfd3-143">必要時，您應該使用 Windows 執行階段 [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) 類別來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-143">Where necessary, you should use the Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) class to retrieve this information.</span></span> <span data-ttu-id="9dfd3-144">介面卡的 [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) 提供通用識別碼，可讓您用來將 DXCore 介面卡對應至 [**DisplayMonitor DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) 資訊。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-144">An adapter's [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) provides a common identifier that you can use to map a DXCore adapter to [**DisplayMonitor.DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) information.</span></span> <span data-ttu-id="9dfd3-145">若要取得介面卡的 LUID，請將 [**DXCoreAdapterProperty：： InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) 傳遞給 [**IDXCoreAdapter：： GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9dfd3-145">To obtain an adapter's LUID, pass [**DXCoreAdapterProperty::InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) to the [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="9dfd3-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9dfd3-146">See also</span></span>

* [<span data-ttu-id="9dfd3-147">最低 DXCore 應用程式</span><span class="sxs-lookup"><span data-stu-id="9dfd3-147">Minimal DXCore application</span></span>](dxcore-source-code.md)
* [<span data-ttu-id="9dfd3-148">DXCore 參考</span><span class="sxs-lookup"><span data-stu-id="9dfd3-148">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="9dfd3-149">Direct3D 12 圖形</span><span class="sxs-lookup"><span data-stu-id="9dfd3-149">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)