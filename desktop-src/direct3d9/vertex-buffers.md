---
description: IDirect3DVertexBuffer9 介面所代表的頂點緩衝區是包含頂點資料的記憶體緩衝區。
ms.assetid: vs|directx_sdk|~\vertex_buffers.htm
title: " (Direct3D 9) 的頂點緩衝區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ceec0f5aee30597b20142945a4ffd3cbcd29500db4113ac2c8dcdd27d045d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043996"
---
# <a name="vertex-buffers-direct3d-9"></a> (Direct3D 9) 的頂點緩衝區

[**IDirect3DVertexBuffer9**](/windows/desktop/api)介面所代表的頂點緩衝區是包含頂點資料的記憶體緩衝區。 頂點緩衝區可以包含任何頂點型別轉換或未轉換、發亮或 unlit，可以透過在 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面中使用轉譯方法來呈現。 您可以在頂點緩衝區中處理頂點，執行例如轉換、光源，或產生裁剪旗標等作業。 轉換永遠會執行。

頂點緩衝區的彈性使其成為重複使用轉換幾何的理想預備環境點。 您可以建立單一頂點緩衝區，然後將其中的頂點轉換、照亮及裁剪，並視需要多次轉譯場景中的模型，而不重新轉換，即使有交錯的轉譯狀態變更。 轉譯使用多個紋理的模式時，這非常有用：幾何只轉換一次，然後視需要轉譯其中的一部分，以所需的紋理變更交錯。 處理頂點之後所做的轉譯狀態變更，在下一次處理頂點時才會生效。

-   [說明](#description)
-   [記憶體集區和使用量](#memory-pool-and-usage)

## <a name="description"></a>描述

頂點緩衝區的功能描述如下：如果它只能存在於系統記憶體中，則為，如果只用于寫入作業，以及它可以包含的頂點類型和數目。 所有這些特性都會保留在 [**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md) 結構中。

格式成員會設定為 D3DFMT \_ VERTEXDATA，表示這是頂點緩衝區。 此類型會識別頂點緩衝區的資源類型。 使用結構成員包含一般功能旗標。 D3DUSAGE \_ SOFTWAREPROCESSING 旗標表示頂點緩衝區要與軟體頂點處理搭配使用。 使用中的 D3DUSAGE WRITEONLY 旗標是否存在， \_ 表示頂點緩衝區記憶體僅用於寫入作業。 這樣就可以釋出驅動程式，將頂點資料放在最佳的記憶體位置，以啟用快速處理和轉譯。 如果 \_ 未使用 D3DUSAGE WRITEONLY 旗標，驅動程式較不可能將資料放在讀取作業效率不佳的位置。 這犧牲了一些處理和轉譯速度。 如果未指定此旗標，則會假設應用程式在頂點緩衝區內的資料上執行讀取和寫入作業。

集區會指定配置給頂點緩衝區的記憶體類別。 D3DPOOL \_ SYSTEMMEM 旗標表示系統在系統記憶體中建立了頂點緩衝區。

大小成員會儲存頂點緩衝區資料的大小（以位元組為單位）。 FVF 成員包含 [D3DFVF](d3dfvf.md) 的組合，可識別緩衝區所包含的頂點型別。

## <a name="memory-pool-and-usage"></a>記憶體集區和使用量

您可以使用 [**IDirect3DDevice9：： CreateVertexBuffer**](/windows/desktop/api) 方法建立頂點緩衝區，這會將集區 (memory 類別) 和使用方式參數。 您也可以使用指定的 FVF 碼來建立 **IDirect3DDevice9：： CreateVertexBuffer** ，以用於固定函式頂點處理，或做為處理常式頂點的輸出。 如需詳細資訊，請參閱 [FVF Direct3D 9 (的頂點緩衝區) ](fvf-vertex-buffers.md)。

當您 \_ 針對該裝置啟用混合模式或軟體頂點處理 (D3DCREATE \_ mixed \_ VERTEXPROCESSING/D3DCREATE \_ software \_ VERTEXPROCESSING) 時，可以設定 D3DUSAGE SOFTWAREPROCESSING 旗標。 您 \_ 必須針對要在混合模式中使用軟體頂點處理的緩衝區設定 D3DUSAGE SOFTWAREPROCESSING，但在混合模式中使用硬體頂點處理時，不應將其設定為最佳效能。 (D3DCREATE \_ 硬體 \_ VERTEXPROCESSING) 。 不過， \_ 當單一緩衝區同時用於硬體和軟體頂點處理時，設定 D3DUSAGE SOFTWAREPROCESSING 是唯一的選項。 \_混合以及軟體裝置也允許 D3DUSAGE SOFTWAREPROCESSING。

您可以指定 D3DPOOL SYSTEMMEM，將頂點和索引緩衝區強制到系統記憶體中 \_ ，即使在硬體中完成頂點處理也是一樣。 這是一種方法，可在驅動程式將這些緩衝區放入 AGP 記憶體時避免過度大量的頁面鎖定記憶體。

本節介紹在 Direct3D 應用程式中瞭解和使用頂點緩衝區所需的概念。 資訊分成下列各節。

-   [ (Direct3D 9) 建立頂點緩衝區 ](creating-a-vertex-buffer.md)
-   [存取頂點緩衝區的內容 (Direct3D 9) ](accessing-the-contents-of-a-vertex-buffer.md)
-   [從頂點緩衝區轉譯 (Direct3D 9) ](rendering-from-a-vertex-buffer.md)
-   [FVF (Direct3D 9) 的頂點緩衝區 ](fvf-vertex-buffers.md)
-   [修正 (Direct3D 9) 的函式頂點處理 ](fixed-function-vertex-processing.md)
-   [ (Direct3D 9) 的可程式化頂點處理 ](programmable-vertex-processing.md)
-   [ (Direct3D 9) 的裝置類型和頂點處理需求 ](device-types-and-vertex-processing-requirements.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 資源](direct3d-resources.md)
</dt> <dt>

[從頂點和索引緩衝區轉譯 (Direct3D 9) ](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[ (Direct3D 9) 的索引緩衝區 ](index-buffers.md)
</dt> </dl>

 

 
