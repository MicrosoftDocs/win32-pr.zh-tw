---
description: 這些選項會識別查詢資源類型。
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eac450ed722da26fe4885d41707483adf401f89
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994105"
---
# <a name="d3dusage_query"></a>D3DUSAGE \_ 查詢

這些選項會識別查詢資源類型。



| \#定義                                   | Description                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DUSAGE \_ 查詢 \_ 篩選                    | 查詢資源格式，以查看它是否支援 D3DTEXF 點以外的材質篩選器類型， \_ (一律支援) 。                                                                                                                                                                                                                         |
| D3DUSAGE \_ 查詢 \_ LEGACYBUMPMAP             | 查詢有關舊版凹凸地圖的資源。                                                                                                                                                                                                                                                                                                         |
| D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ 混色 | 查詢資源以驗證支援的 post 圖元著色器混色支援。 如果 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 因為 D3DUSAGE \_ QUERY \_ POSTPIXELSHADER 混色而失敗 \_ ，則不支援 post 圖元混合作業。 這些包括 Alpha 測試、圖元霧化、轉譯目標混色、色彩寫入啟用和遞色。 |
| D3DUSAGE \_ 查詢 \_ SRGBREAD                  | 查詢資源，以確認材質在讀取作業期間是否支援 gamma 修正。                                                                                                                                                                                                                                                        |
| D3DUSAGE \_ 查詢 \_ SRGBWRITE                 | 查詢資源，以確認材質在寫入作業期間是否支援 gamma 修正。                                                                                                                                                                                                                                                       |
| D3DUSAGE \_ 查詢 \_ VERTEXTEXTURE             | 查詢資源以驗證端點著色器紋理取樣的支援。                                                                                                                                                                                                                                                                            |
| D3DUSAGE \_ 查詢 \_ WRAPANDMIP                | 查詢資源以確認紋理包裝和 mip 對應的支援。                                                                                                                                                                                                                                                                          |



 

使用 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 來查詢這些使用方式的硬體支援，以及 [D3DUSAGE](d3dusage.md)中列出的其他使用方式。

## <a name="constant-information"></a>常數資訊



|                          |             |
|--------------------------|-------------|
| 標頭                   | d3d9types。h |
| 最低作業系統 | Windows 98  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
