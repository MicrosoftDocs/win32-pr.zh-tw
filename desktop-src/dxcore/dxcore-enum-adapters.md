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
# <a name="using-dxcore-to-enumerate-adapters"></a>使用 DXCore 來列舉介面卡

DXCore 是適用于 DirectX 裝置的介面卡列舉 API，因此其某些設備會與 [DXGI](../direct3ddxgi/dx-graphics-dxgi.md)的部分重迭。

DXCore 可讓您將新的裝置類型公開至使用者模式，例如 MCDM (Microsoft Compute Driver Model) ，以搭配 [Direct3D 12](../direct3d12/directx-12-programming-guide.md)、 [DirectML](../direct3d12/dml.md)和 [Windows Machine Learning](/windows/ai/windows-ml/)使用。 與 DXGI 不同的是，DXCore 不會提供有關顯示相關技術或屬性的任何資訊

在接下來的幾節中，我們將探討 DXCore 的主要功能，其中包含一些程式碼範例， (以 [c + +/WinRT](/windows/uwp/cpp-and-winrt-apis)) 撰寫。 以下所示的程式碼範例會從完整的源代碼清單中解壓縮，您可以在 [最基本的 DXCore 應用程式](dxcore-source-code.md)中找到這些程式碼。

## <a name="create-an-adapter-factory"></a>建立介面卡 factory

您可以藉由建立 [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) 介面所表示的介面卡 factory 物件，開始 DXCore 介面卡列舉。 若要建立 factory，請包含 `dxcore.h` 標頭檔，然後呼叫 [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) free 函式。

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a>取得介面卡清單

與 DXGI 不同的是，新建立的 DXCore 介面卡 factory 不會自動建立系統的介面卡狀態的快照集。 相反地，當您明確抓取以 [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) 介面表示的介面卡清單物件時，DXCore 會建立該快照集。

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a>從清單中選取適當的介面卡

本節將示範如何在指定介面卡清單物件的情況下，找到清單中的第一個硬體配接器。

[**IDXCoreAdapterList：： GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md)方法會告訴您清單中的元素數目，而 [**IDXCoreAdapterList：： GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md)會依索引抓取特定的介面卡。

然後，您可以依照下列步驟來查詢該介面卡的屬性。

- 首先，若要確認它是有效的，可在此作業系統版本上取得此介面卡的指定屬性值，您可以呼叫 [**IDXCoreAdapter：： IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md)。 傳遞 [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) 列舉的值，以識別您要查詢的屬性。
- 您可以選擇性地使用 [**IDXCoreAdapter：： GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md)的呼叫來確認屬性值的大小。 對於 **DXCoreAdapterProperty：： IsHardware** 之類的屬性（這是簡單的布林值），則不需要此步驟。
- 最後，藉由呼叫 [**IDXCoreAdapter：： GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md)來取得屬性的值。

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

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a>藉由排序介面卡清單來選取慣用的介面卡

您可以藉由呼叫 [IDXCoreAdapterList：： sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) 方法來排序 DXCore 介面卡清單。

[DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md)列舉會定義代表排序準則的值。 傳遞這些值的陣列以 **進行排序**，然後讀取產生的排序清單中的第一個介面卡。

若要判斷排序類型是否要依 **排序** 來理解，請先呼叫 [IDXCoreAdapterList：： IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md)。

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

## <a name="query-and-set-adapter-state-properties"></a>查詢和設定介面卡狀態 (屬性) 

您可以藉由呼叫 [**IDXCoreAdapter：： QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) 和 [**IDXCoreAdapter：： SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) 方法，來取得和設定介面卡之指定狀態專案的狀態。

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

在實務上，呼叫 **QueryState** 和 **SetState** 之前，您應該先呼叫 [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) 來確認查詢狀態種類是否適用于此介面卡和作業系統 (作業系統) 。

## <a name="adapter-list-freshness"></a>介面卡清單時效性

如果介面卡清單因為系統狀況變更而變得過時，則會標示為如此。 您可以藉由輪詢 [**IDXCoreAdapterList：： IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) 方法來判斷介面卡清單的有效期限。

不過，更方便的方式是，您可以訂閱過期等狀況的通知。 若要這樣做，請將 [**DXCoreNotificationType：： AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) 傳遞至 [**IDXCoreAdapterFactory：： RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)，並安全地儲存傳回的 cookie 以供稍後使用。

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

然後，您可以從已有的 factory 物件產生新的、目前的介面卡清單物件。 處理這些條件對於您能夠順暢地回應事件（例如介面卡抵達和移除）、 (是否為 GPU、特製化的計算介面卡) ，以及適當地轉移工作負載的回應，都很重要。

在您終結介面卡清單物件之前，您必須使用 cookie 值，藉由呼叫 [IDXCoreAdapterFactory：： UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)，從通知取消註冊該物件。 如果您沒有取消註冊，則在偵測到情況時，就會引發嚴重的例外狀況。

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a>顯示資訊

> [!NOTE]
> DXCore 本身不會提供任何顯示資訊。 必要時，您應該使用 Windows 執行階段 [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) 類別來取得此資訊。 介面卡的 [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) 提供通用識別碼，可讓您用來將 DXCore 介面卡對應至 [**DisplayMonitor DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) 資訊。 若要取得介面卡的 LUID，請將 [**DXCoreAdapterProperty：： InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) 傳遞給 [**IDXCoreAdapter：： GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) 方法。

## <a name="see-also"></a>另請參閱

* [最低 DXCore 應用程式](dxcore-source-code.md)
* [DXCore 參考](./dxcore-reference.md)
* [Direct3D 12 圖形](../direct3d12/direct3d-12-graphics.md)