---
title: UAV 計數器
description: 您可以使用未排序的存取-view (UAV) 計數器，將32位不可部分完成的計數器與未排序的存取權 (UAV) 產生關聯。
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: c33321b02f22378f4d039137b8ff65559a25a32ed219c2bf336528913777791d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460788"
---
# <a name="uav-counters"></a>UAV 計數器
您可以使用未排序的存取-view (UAV) 計數器，將32位不可部分完成的計數器與未排序的存取權 (UAV) 產生關聯。

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a>從 Direct3D 11 UAV 至 Direct3D 12 的計數器差異
Direct3D 12 應用程式和 Direct3D 11 應用程式都使用相同的高階著色器語言 (HLSL) 著色器函數來存取 UAV 計數器。

-   **IncrementCounter**
-   **DecrementCounter**
-   **Append**
-   **取用**

### <a name="direct3d-12"></a>Direct3D 12
在 Direct3D 12 中，32位值是由應用程式佈建，因此，CPU 或 GPU 可以讀取和寫入32位值，就像任何其他 Direct3D 12 資源一樣。

### <a name="direct3d-11"></a>Direct3D 11
在著色器之外，使用 Direct3D 11 需要呼叫 API 方法才能存取計數器 (例如 [>id3d11devicecoNtext：： CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)) 。

## <a name="using-uav-counters"></a>使用 UAV 計數器
您的應用程式會負責為 UAV 計數器配置32位的儲存體。 此儲存體可以配置在不同的資源中，因為其中包含可透過 UAV 存取的資料。

請參閱 [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)、 [**D3D12 \_ Buffer \_ UAV \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) 和 [**D3D12 \_ BUFFER \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav)。

如果在 [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)的呼叫中指定 *pCounterResource* ，則會有與 UAV 相關聯的計數器。 在此案例中：

-   *StructureByteStride* 必須大於零
-   格式必須為未知的 DXGI \_ 格式 \_
-   不得設定原始旗標
-   這兩個資源都必須是緩衝區
-   *CounterOffsetInBytes* 必須是4個位元組的倍數
-   *CounterOffsetInBytes* 必須在計數器資源的範圍內
-   *pDesc* 不可為 Null
-   *pResource* 不可為 Null

並注意下列使用案例：

-   如果未指定 *pCounterResource* ，則 *CounterOffsetInBytes* 必須為0。
-   如果已設定原始旗標，則格式必須為 DXGI \_ 格式 \_ R32 無格式 \_ ，而且 UAV 資源必須是緩衝區。
-   如果未設定 *pCounterResource* ，則 *CounterOffsetInBytes* 必須為0。
-   如果未設定 RAW 旗標，且 *StructureByteStride* = 0，則格式必須是有效的 UAV 格式。

Direct3D 12 會移除附加和計數器 UAVs (之間的差異，不過 HLSL 位元組碼) 中仍然存在差異。

核心執行時間會在 [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)內驗證這些限制。

在繪製/分派期間，計數器資源必須處於狀態 [**D3D12 \_ 資源狀態的 \_ 未 \_ 排序 \_ 存取**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)。 此外，在單一繪製/分派呼叫中，應用程式會透過兩個不同的 UAV 計數器來存取相同的32位記憶體位置，這是不正確。 如果偵測到其中一個錯誤，debug 層將會發出錯誤。

沒有 "SetUnorderedAccessViewCounterValue" 或 "CopyStructureCount" 方法，因為應用程式可以直接將資料複製到計數器值或從中複製資料。

支援使用計數器的 UAVs 動態索引。

如果著色器嘗試存取沒有相關聯計數器之 UAV 的計數器，則調試層會發出警告，而且會發生 GPU 分頁錯誤，導致移除應用程式的裝置。

所有堆積類型都支援 UAV 計數器 (預設、上傳、readback) 。

## <a name="related-topics"></a>相關主題

* [計數器和查詢](counters-and-queries.md)