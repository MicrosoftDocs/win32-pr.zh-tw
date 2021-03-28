---
title: 建立磚資源
description: '\_ \_ 建立資源時，藉由指定 D3D11 資源的「其他並排顯示」旗標來建立並排顯示的資源 \_ 。'
ms.assetid: DED2B70C-1E95-4A85-A818-FD32165FBF6C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e2c0e457bfd8534d3a42c6f658095b3349572
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/13/2019
ms.locfileid: "104373678"
---
# <a name="creating-tiled-resources"></a>建立磚資源

建立資源時，藉由指定 [**D3D11 \_ 資源的「 \_ 其他 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 並排顯示」旗標來建立並排顯示的資源。

當您可以使用 [**D3D11 資源的 \_ \_ 其他 \_ 磚**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 來建立資源時，會在 [磚資源建立參數](tiled-resource-creation-parameters.md)中描述。

建立資源時，系統會在圖形系統中配置非磚資源的儲存體。 例如，當您呼叫 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) 來建立2d 材質的陣列時，圖形系統會為這些2d 材質配置儲存區。 當建立磚的資源時，圖形系統不會配置資源內容的儲存體。 相反地，當應用程式建立並排顯示的資源時，圖形系統只會為並排顯示的區域提供位址空間保留，然後再允許應用程式控制磚的對應。 磚的「對應」僅為資源中的邏輯磚在記憶體中所指向的實體位置 (若是對應磚則為 **NULL**)。 請勿將此概念與為 CPU 存取對應 Direct3D 資源的概念混淆，其名稱雖相同但卻是完全獨立的概念。 您將可視需要個別為每個磚定義並變更對應，並知悉無須一次為一個表面對應所有磚，因此可有效率地使用可用的記憶體量。

本節提供有關如何建立磚資源的詳細資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                             | 描述                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [對應在磚集區中](mappings-are-into-a-tile-pool.md)<br/>                                     | 使用 [**D3D11 資源的「 \_ \_ 其他 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 並排顯示」旗標來建立資源時，構成資源的磚會指向磚集區中的位置。 磚集區是記憶體的集區 (由一或多個配置於幕後備份 - 應用程式中看不見)。 <br/> |
| [磚資源建立參數](tiled-resource-creation-parameters.md)<br/>                           | 您可以使用 [**D3D11 \_ 資源 \_ 其他 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 並排顯示旗標建立的 Direct3D 資源類型有一些限制。 本節提供用來建立磚資源的有效參數。<br/>                                                |
| [磚資源可用的位址空間](address-space-available-for-tiled-resources.md)<br/>         | 此區段會指定可用於並排顯示資源的虛擬位址空間。 <br/>                                                                                                                                                                                                                           |
| [磚集區建立參數](tile-pool-creation-parameters.md)<br/>                                     | 使用本節中的參數透過 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API 定義磚集區。 <br/>                                                                                                                                                                              |
| [磚資源跨進程和裝置共用](tiled-resource-cross-process-and-device-sharing.md)<br/> | 磚集區可以與其他處理序共用，就像傳統資源一樣。 參考磚集區的並排資源無法跨裝置和進程共用。 但是，個別的進程可以建立自己的磚資源，對應至這些已並排資源之間共用的磚集區。 <br/>          |
| [磚資源上可用的作業](operations-available-on-tiled-resources.md)<br/>                 | 此區段會列出您可以在並排顯示的資源上執行的作業。<br/>                                                                                                                                                                                                                                             |
| [磚集區可用的作業](operations-available-on-tile-pools.md)<br/>                           | 此區段會列出您可以在磚集區上執行的作業。<br/>                                                                                                                                                                                                                                                  |
| [磚式資源的區域如何並排顯示](how-a-tiled-resource-s-area-is-tiled.md)<br/>                       | 當您建立並排顯示的資源時，維度、格式元素大小，以及 mipmap 和（或）陣列配量的數目 (（如果適用的話）) 決定要備份整個介面區所需的磚數目。 <br/>                                                                                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源](tiled-resources.md)
</dt> </dl>

 

 





