---
description: IDirect3DDevice9 介面支援在軟體和硬體中處理頂點。
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: 處理 (Direct3D 9) 的頂點資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846591"
---
# <a name="processing-vertex-data-direct3d-9"></a>處理 (Direct3D 9) 的頂點資料

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面支援在軟體和硬體中處理頂點。 一般情況下，軟體和硬體頂點處理的裝置功能並不相同。 硬體功能是可變的，取決於顯示器介面卡和驅動程式，而軟體功能則是固定的。

下列旗標可控制硬體抽象層的頂點處理行為 (HAL) 和參考裝置。

-   D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING
-   D3DCREATE \_ 硬體 \_ VERTEXPROCESSING
-   D3DCREATE \_ 混合 \_ VERTEXPROCESSING

呼叫 [**IDirect3D9：： CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)時，請指定其中一個頂點處理行為旗標。 混合模式旗標可讓裝置執行軟體和硬體頂點處理。 裝置一次只能設定一個頂點處理旗標。 請注意， \_ \_ (D3DCREATE PUREDEVICE) 建立純裝置時，必須設定 D3DCREATE 硬體 VERTEXPROCESSING 旗標 \_ 。

為了避免單一裝置上的雙重頂點處理功能，在執行時間只會查詢硬體頂點處理功能。 軟體頂點處理功能是固定的，而且無法在執行時間查詢。

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)結構的 VertexProcessingCaps 成員會決定裝置的硬體頂點處理功能。

針對軟體頂點處理，支援下列功能。

-   D3DVTXPCAPS 的 D3DVTXPCAPS \_ DIRECTIONALLIGHTS 成員[](d3dvtxpcaps.md)
-   D3DVTXPCAPS 的 D3DVTXPCAPS \_ LOCALVIEWER 成員[](d3dvtxpcaps.md)
-   D3DVTXPCAPS 的 D3DVTXPCAPS \_ MATERIALSOURCE7 成員[](d3dvtxpcaps.md)
-   D3DVTXPCAPS 的 D3DVTXPCAPS \_ POSITIONALLIGHTS 成員[](d3dvtxpcaps.md)
-   D3DVTXPCAPS 的 D3DVTXPCAPS \_ TEXGEN 成員[](d3dvtxpcaps.md)
-   D3DVTXPCAPS 的 D3DVTXPCAPS \_ 補間成員[](d3dvtxpcaps.md)

此外，下表列出針對軟體頂點處理模式之裝置的 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構成員所設定的值。



| 成員                 | 軟體頂點處理功能 |
|------------------------|-----------------------------------------|
| MaxActiveLights        | 無限制                               |
| MaxUserClipPlanes      | 6                                       |
| MaxVertexBlendMatrices | 4                                       |
| MaxStreams             | 16                                      |
| MaxVertexIndex         | 0xFFFFFFFF                              |



 

一般而言，任何已系結至頂點的應用程式都應該使用 HAL 裝置。 軟體頂點處理提供一組保證的頂點處理功能，包括不限數目的燈光和可程式化頂點著色器的完整支援。 使用 HAL 裝置時，您隨時可以在軟體和硬體頂點處理之間切換 (這是唯一支援硬體和軟體頂點處理) 的裝置類型。 唯一的需求是必須在系統記憶體中配置用於軟體頂點處理的頂點緩衝區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 裝置](direct3d-devices.md)
</dt> </dl>

 

 
