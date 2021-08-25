---
title: 磚資源功能層級
description: Direct3D 11.2 會以 D3D11 並排顯示的 \_ \_ 資源 \_ 層級值，來公開兩個層級的並排資源支援。
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1b76c1d90cc48210f02983817b317eb830224b8f87bb8b4904ee3e11d6cdd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894378"
---
# <a name="tiled-resources-features-tiers"></a>磚資源功能層級

Direct3D 11.2 會以 D3D11 並排顯示的 [**\_ \_ 資源 \_ 層級**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) 值，來公開兩個層級的並排資源支援。

若要查詢硬體和驅動程式是否支援並排顯示的資源和階層層級，請將 [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)值傳遞給 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)的 *feature* 參數。 此外，將 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) 結構的指標傳遞至 *pFeatureSupportData* 參數，並將 **D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ OPTIONS1** 結構的大小傳遞給 *FeatureSupportDataSize* 參數。 **CheckFeatureSupport** 會在 **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1** 的 **TiledResourcesTier** 成員中，以 D3D11 並排顯示的 [**\_ \_ 資源 \_ 層**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier)級值傳回階層層級。

本節說明這兩個層級。

## <a name="in-this-section"></a>本節內容



| 主題                           | 描述                                       |
|---------------------------------|---------------------------------------------------|
| [第 1 層](tier-1.md)<br/> | 本節描述第 1 層支援。<br/> |
| [第 2 層](tier-2.md)<br/> | 本節說明第2層支援。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源](tiled-resources.md)
</dt> </dl>

 

 





