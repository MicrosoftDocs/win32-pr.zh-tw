---
title: 設定和填入描述元堆積
description: 可以在命令清單上設定的描述項堆積型別，也就是包含描述項資料表的描述項，其中每一次最多隻能使用 (的描述中繼資料表) 。
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/03/2019
ms.locfileid: "104548381"
---
# <a name="setting-and-populating-descriptor-heaps"></a>設定和填入描述元堆積

可以在命令清單上設定的描述項堆積型別，也就是包含描述項資料表的描述項，其中每一次最多隻能使用 (的描述中繼資料表) 。

-   [設定描述元堆積](#setting-and-populating-descriptor-heaps)
-   [填入描述元堆積](#populating-descriptor-heaps)
-   [相關主題](#related-topics)

## <a name="setting-descriptor-heaps"></a>設定描述元堆積

可以在命令清單上設定的描述元堆積類型為：

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

命令清單上所設定的堆積也必須已建立為著色器可見。 有三種類型的命令清單： DIRECT、配套和計算。

在命令清單上設定描述項堆積之後，定義描述中繼資料表的後續呼叫會參考目前的描述元堆積。 在命令清單的開頭，以及在命令清單上變更描述項堆積之後，會定義描述項資料表狀態。 重複設定相同的描述元堆積不會造成描述項資料表設定未定義。

相較之下，相較之下，只有在 (重複的呼叫設定相同堆積兩次不會產生錯誤) ;否則，行為會是未定義的。 當任何命令清單呼叫組合時，所設定的描述元堆積必須符合狀態;否則，行為會是未定義的。 這可讓配套來繼承和編輯命令清單的描述項資料表設定。 不會變更描述項資料表的配套 (只會繼承它們) 完全不需要設定描述元堆積，而只會繼承自呼叫命令清單。

當 (使用 [**ID3D12GraphicsCommandList：： SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)) 設定描述元堆積時，所使用的所有堆積都會設定在單一呼叫中 (而且所有先前設定的堆積都會由呼叫) 取消設定。 在此呼叫中，最多可以設定上面所列之每個類型的一個堆積。

## <a name="populating-descriptor-heaps"></a>填入描述元堆積

在應用程式建立描述元堆積之後，接著就可以在裝置上使用方法，將描述項直接產生到堆積，或從一個位置將描述項複製到另一個位置。

描述元堆積記憶體的初始內容尚未定義，因此，要求 GPU 或驅動程式參考未初始化的記憶體來進行轉譯，可能會導致未定義的結果，例如裝置重設。

如果應用程式將描述項堆積設定為可供 CPU 使用，則 CPU 可以呼叫方法來建立堆積中的描述元，並從就地複製以放置 (包括以立即、自由執行緒方式) 的堆積。 如果堆積已設定為 SHADER_VISIBLE，則不允許讀取 CPU。



## <a name="related-topics"></a>相關主題

<dl> <dt>

[描述元堆積](descriptor-heaps.md)
</dt> </dl>

 

 




