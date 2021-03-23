---
title: 描述項總覽
description: 描述元是由 API 呼叫所建立，並識別資源。
ms.assetid: 64721226-5533-4816-865E-9429032FCC86
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d83b2fbfd5c5df2738c61aea4f1d1115d6c874
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548412"
---
# <a name="descriptors-overview"></a>描述項總覽

描述元是由 API 呼叫所建立，並識別資源。

-   [描述中繼資料](#descriptor-data)
-   [描述項控制碼](#descriptor-handles)
-   [Null 描述項](#null-descriptors)
-   [預設描述項](#default-descriptors)
-   [相關主題](#related-topics)

## <a name="descriptor-data"></a>描述中繼資料

描述項是相當小的資料區塊，可完整地以 GPU 特定的不透明格式來描述 GPU 的物件。 有幾種不同類型的描述項會 &mdash; 呈現目標視圖 (RTVs) 、深度樣板視圖 (dsv) 、著色器資源檢視 (SRVs) 、未排序的存取視圖 (UAVs) 、常數緩衝區視圖 (CBVs) 和取樣器。

描述項的大小視 GPU 硬體而異。 您可以藉由呼叫 [**ID3D12Device：： GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)，查詢 SRV、UAV 或 CBV 的大小。 此檔中顯示的描述項為不可分割單位;以下是範例。

![srv、cbv、uav 和取樣器](images/single-descriptor.png)

描述項是由 API 呼叫所建立，而且會包含您希望描述項包含的資源和 mip 對應等資訊。

驅動程式不會追蹤或保存描述項的參考，而是由應用程式確保正確的描述項類型正在使用中，而且資訊是最新的。 有一個小例外狀況;驅動程式會檢查轉譯目標系結，以確保交換鏈能正常運作。

物件描述項不需要釋出或釋放。 驅動程式不會將任何配置附加至描述項的建立。 不過，描述項可能會編碼應用程式擁有存留期之其他配置的參考。 比方說，SRV 的描述項必須包含 D3D 資源的虛擬位址 (例如 SRV 所參考的材質) 。 應用程式必須負責確保它在其相依的基礎 D3D 資源已損毀或遭到修改時，不會使用 SRV 描述項， (例如宣告為 nonresident) 。

使用描述項的主要方式是將它們放在描述元堆積中，而這些專案是描述項的記憶體。

## <a name="descriptor-handles"></a>描述項控制碼

描述項控制碼是描述項的唯一位址。 它類似于指標，但不是不透明的，因為其實作為硬體特有。 控制碼在描述元堆積之間是唯一的，因此，例如，控制碼陣列可以參考多個堆積中的描述項。

CPU 控制碼可供立即使用，例如複製來源和目的地都需要識別。 在使用 (（例如，呼叫 [**ID3D12GraphicsCommandList：： OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)) 、可以重複使用，或可處置其基礎堆積）之後立即使用。

GPU 控制碼無法立即使用 &mdash; ，它們會從命令清單識別位置，以在 gpu 執行時間使用。 您必須保留它們，直到任何參考它們的命令清單完全執行為止。

若要建立堆積開頭的描述項控制碼，建立描述元堆積本身之後，請呼叫下列其中一種方法：

-   [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)
-   [**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)

這些方法會傳回下列結構：

-   [**D3D12 \_ CPU \_ 描述項 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)
-   [**D3D12 \_ GPU \_ 描述項 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

由於描述項的大小會因硬體而異，因此可取得堆積中每個描述元之間的增量：

-   [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)

您可以使用數個增量、複製控制碼，以及將控制碼傳遞至 API 呼叫，以安全的方式來位移開始位置。 將控制碼取值為有效的 CPU 指標，也不能分析控制碼內的位，是不安全的。

已加入一些協助程式結構與初始化成員，以簡化管理處理程式的工作。

-   [**CD3DX12 \_ CPU \_ 描述項 \_ 控制碼**](cd3dx12-cpu-descriptor-handle.md)
-   [**CD3DX12 \_ GPU \_ 描述項 \_ 控制碼**](cd3dx12-gpu-descriptor-handle.md)

## <a name="null-descriptors"></a>Null 描述項

使用 API 呼叫建立描述項時，應用程式會針對描述項定義中的資源指標傳遞 Null，以達到著色器存取時沒有任何限制的效果。

其餘的描述項必須盡可能填入。 例如，在著色器資源檢視 (SRVs) 的情況下，可以使用描述元來區分它 (的檢視類型 Texture1D、Texture2D 等，) 。 視圖描述項中的數值參數（例如 mipmap 數目）必須全部設定為對資源有效的值。

在許多情況下，有一個已定義的行為可存取未系結的資源，例如傳回預設值的 SRVs。 只要著色器存取的類型與描述元類型相容，就會在存取 Null 描述元時接受這些值。 例如，如果著色器預期 Texture2D SRV 並存取定義為 Texture1D 的 Null SRV，則行為會是未定義的，而且可能會導致裝置重設。

總而言之，若要建立 null 描述項，請在 `null` 使用 [**CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)等方法建立視圖時傳遞 *pResource* 參數。 針對 [view description] 參數 *pDesc*，設定當資源不是 null 時可運作的設定 (否則某些硬體) 可能會發生損毀。

不過，根描述項不應設為 null。

在第1層硬體 (請參閱 [**硬體層**](./hardware-support.md)，透過描述項資料表系結 (的所有描述元) 都必須初始化為真實描述元或 null 描述項（即使硬體未存取），否則行為未定義。

在第2層硬體上，這適用于系結 CBV 和 UAV 描述項，但不適用於 SRV 描述項。

在 Tier3 硬體上，不會有任何限制，但前提是不會存取未初始化的描述項。

## <a name="default-descriptors"></a>預設描述項

若要建立特定視圖的預設描述項，請將有效的 *pResource* 參數傳遞至 create view 方法 (例如 [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)) ，但是針對 *pDesc* 參數傳遞 **Null** 。 例如，如果資源包含14個 mips，則此視圖會包含14個 mips。 預設的案例涵蓋資源與觀點的最明顯對應。 這需要配置具有完整格式名稱的資源 (例如 **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB** ，而非 **DXGI_FORMAT_R8G8B8A8_TYPELESS**) 。

因為提供的 *pResource* 參數必須是 **Null**，且必須透過 [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**]/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv) 傳遞位置，所以無法搭配使用預設描述項與 raytracing 加速結構視圖。

## <a name="related-topics"></a>相關主題

[描述項](descriptors.md)