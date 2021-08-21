---
title: '執行時間 (Direct3D 12 圖形) '
description: 本節涵蓋查詢時間戳記，以及校準 GPU 和 CPU 時間戳計數器。
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84676d36523fe23d33946e164d245e1619eb41d0af11a898acc52194348e439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045366"
---
# <a name="timing-direct3d-12-graphics"></a>執行時間 (Direct3D 12 圖形) 

本節涵蓋查詢時間戳記，以及校準 GPU 和 CPU 時間戳計數器。

## <a name="timestamp-frequency"></a>時間戳記頻率

您的應用程式可以根據每個命令佇列來查詢 GPU 時間戳記頻率 (請參閱 [**ID3D12CommandQueue：： GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) 方法) 。

傳回的頻率是以 Hz (滴答/秒) 來測量。 如果指定的命令佇列不支援時間戳記 (請參閱 [ [查詢](queries.md) ] 區段中的表格) ，然後此 API 會失敗 (並傳回 **E_FAIL**) 。 [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) 和 [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) 一律支援時間戳記。 如果 [**D3D12_FEATURE_DATA_D3D12_OPTIONS3：： CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3)成員為 **TRUE**， [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)選擇性地支援時間戳記。

## <a name="timestamp-calibration"></a>時間戳記校正

D3D12 可讓應用程式將從 timestamp 查詢取得的結果與從呼叫取得的結果相互關聯 `QueryPerformanceCounter` 。 這是由呼叫 [**ID3D12CommandQueue：： GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)啟用。

[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) 會取樣指定命令佇列的 GPU timestamp 計數器，並透過 `QueryPerformanceCounter` 幾乎相同的時間取樣 CPU 計數器。 同樣地，這個 API 會失敗 (傳回 E \_ 失敗) 如果指定的命令佇列不支援時間戳記 (請參閱 [查詢](queries.md) 主題中的表格) 。

請注意，GPU 和 CPU 時間戳計數器不一定會與這些處理器的頻率速度直接相關，而是會從時間戳記的刻度進行工作。

## <a name="timestamp-queries"></a>時間戳記查詢

您可以取得時間戳記作為命令清單的一部分， (而不是透過時間戳記查詢) 命令佇列上的 CPU 端呼叫。  (如 [需查詢的](queries.md) 詳細資訊，請參閱一般) 。 

所有時間戳記查詢都使用實際查詢的類型 [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) 。 不過，由於硬體限制的緣故， [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)和 [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)使用 [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)所使用的 D3D12_QUERY_HEAP_TYPE 不同的 [](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) 。

直接和計算佇列會使用 [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type)。

複製佇列會使用 [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type)。

只有當 [**D3D12_FEATURE_DATA_D3D12_OPTIONS3：： CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) 成員為 **TRUE** 時，才支援複製佇列查詢。

時間戳記查詢是透過 [**ID3D12GraphicsCommandList：： ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)解析的 UINT64，是代表刻度的 **UINT64** ，如 [**ID3D12CommandQueue：： GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)所傳回，因此必須除以佇列頻率，以秒為單位來取得長度。

> [!IMPORTANT]
> 為了精確度，請在計算時間戳記的第二個或毫秒間隔時使用浮點算術。 例如，請使用 `queriedTicks / (double)Frequency`，而不要使用 `queriedTicks / Frequency`。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[計數器和查詢](counters-and-queries.md)
</dt> <dt>

[**ID3D12Device::SetStablePowerState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[**ID3D12Object：： SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[效能測量](performance-measurement.md)
</dt> </dl>
