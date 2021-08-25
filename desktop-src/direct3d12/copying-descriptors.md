---
title: 複製描述項
description: 裝置介面上的 ID3D12Device CopyDescriptors 和 ID3D12Device CopyDescriptorsSimple 方法會使用 CPU 來立即複製描述項。
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02abfb433b36738de0fd62285e44b2f065ac017217a1e61f8c305e8ca76228
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069698"
---
# <a name="copying-descriptors"></a>複製描述項

裝置介面上的 [**ID3D12Device：： CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) 和 [**ID3D12Device：： CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) 方法會使用 CPU 來立即複製描述項。 只要 CPU 或 GPU 上的多個執行緒不會執行任何可能衝突的寫入，就可以將它們稱為「自由執行緒」。

## <a name="copying-descriptors-immediately-cpu-timeline"></a>立即複製描述項 (CPU 時間軸) 

 (從) 複製的來源描述項數目（指定為一組描述項範圍）必須等於要複製到) 的目的地 (描述項數目（指定為一組個別的描述項範圍）。 來源和目的範圍也不需要行出。 例如，您可以將一組稀疏的描述項複製到連續的目的地，反之亦然，或是某種組合。

複製作業可包含多個描述元堆積，兩者皆為來源和目的地。 使用描述項控制碼作為參數，表示複製方法不在意任何指定之描述項所在的堆積–它們都只是記憶體。

要從中複製或的描述元堆積類型必須相符，因此方法會採用單一描述元堆積類型做為輸入。 驅動程式必須知道指定複製作業中所有描述項的堆積類型，因此它知道複製作業中牽涉到的資料大小。 如果指定的描述項堆積類型需要，驅動程式也可能需要執行自訂複製工作，這是一個實作為的詳細資料。 請注意，描述項本身不會識別它們所指向的類型;因此，複製作業需要額外的參數。

針對將單一範圍的描述項從一個位置複製到另一個位置（ [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)）的簡單案例，提供 [**COPYDESCRIPTORS**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors)的替代 API。

針對這些以裝置為基礎的 (CPU 時間軸) 描述項複製方法，來源描述項必須來自非著色器可見的描述元堆積。 目的地描述項可以位於任何可顯示 CPU (著色器可見或未) 的描述元堆積中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[描述項](descriptors.md)
</dt> </dl>

 

 




