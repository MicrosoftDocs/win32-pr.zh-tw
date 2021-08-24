---
title: 建立變形和參考裝置的限制
description: 在 Direct3D 10.1 和 Direct3D 11.0 中建立變形和參考裝置有一些限制。 本主題討論這些限制。
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0483ed6d5fd7348df39a4f3064f377845d6bfae1fe46abc47be5acd99e191c29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608608"
---
# <a name="limitations-creating-warp-and-reference-devices"></a>建立變形和參考裝置的限制

在 Direct3D 10.1 和 Direct3D 11.0 中建立變形和參考裝置有一些限制。 本主題討論這些限制。

D3D10 \_ 驅動程式 \_ 類型的 \_ 變形和 D3D10 驅動程式類型參考驅動程式類型在 \_ \_ \_ \_ Direct3D 10.1 的 D3D10 功能等級 \_ \_ 9 \_ 1 到 D3D10 \_ 功能等級 \_ \_ 9 \_ 3 功能層級上不受支援。 此外， \_ \_ \_ \_ DIRECT3D 11.0 中的 d3d 功能 \_ 等級 \_ 11 0 不支援 d3d 驅動程式類型變形驅動程式類型 \_ 。 也就是說，當您呼叫 [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) 來建立 direct3d 10.1 裝置，或當您呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 來建立 direct3d 11.0 裝置時，如果您在呼叫中指定這些驅動程式類型的其中一個，且其中一個功能等級的組合是不正確，則呼叫無效。 只有下列功能層級、執行時間和驅動程式類型組合適用于變形和參考裝置：

-   \_ \_ \_ Direct3D 11.1 中所有功能層級的 D3D 驅動程式類型變形，Windows 8 包含

    \_ \_ \_ Direct3D 11.1 中所有功能層級的 D3D 驅動程式類型參考

    當您呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 來建立 Direct3D 11.1 裝置時，如果您將其中一個驅動程式類型的組合指定為其中一個功能層級，則呼叫會是有效的。

-   D3d \_ 驅動程式 \_ 類型 \_ 在 d3d \_ 功能 \_ 層級 9 1 到 d3d 功能層級上的變形（ \_ \_ \_ \_ \_ \_ Direct3D 11 的功能等級為 10 1）

    \_ \_ \_ Direct3D 11 中的 d3d 驅動程式類型參考在 d3d 功能層 \_ \_ 級 \_ 9 \_ 1 到 d3d 功能 \_ \_ 等級 \_ 11 \_ 0 功能等級

    當您呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 來建立 Direct3D 11 裝置時，如果您將其中一個驅動程式類型的組合指定為其中一個功能層級，則呼叫會是有效的。

-   \_ \_ \_ \_ \_ \_ 在 \_ \_ \_ \_ \_ \_ \_ Direct3D 10.1 中透過 D3D10 功能等級 10 \_ 1 的功能層級 10 0 上的 D3D10 功能層級 10 0 D3D10 驅動程式類型的變形與 D3D10 驅動程式類型參考

    當您呼叫 [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) 來建立 Direct3D 10.1 裝置時，如果您將其中一個驅動程式類型的組合指定為其中一個功能層級，則呼叫會是有效的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置](overviews-direct3d-11-devices.md)
</dt> <dt>

[舊版硬體上的 Direct3D 11 簡介](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[如何：建立變形裝置](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[如何：建立參考裝置](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[**D3D10 \_ 驅動程式 \_ 類型**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[**D3D10 功能 1-1 \_ \_**](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[**D3D \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[**D3D \_ 功能 \_ 等級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 