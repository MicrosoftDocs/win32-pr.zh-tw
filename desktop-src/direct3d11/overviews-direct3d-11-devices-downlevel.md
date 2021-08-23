---
title: 舊版硬體上的 Direct3D 11
description: 本節討論如何設計 Direct3D 11，以支援新的和現有的硬體，從 DirectX 9 到 DirectX 11。
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb9dde5bfaa32808752206ebe96702aaaf10cc39c1e053675ddfced765331be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045506"
---
# <a name="direct3d-11-on-downlevel-hardware"></a>舊版硬體上的 Direct3D 11

本節討論如何設計 Direct3D 11，以支援新的和現有的硬體，從 DirectX 9 到 DirectX 11。

下圖顯示 Direct3D 11 如何支援新的和現有的硬體。

![direct3d 11 支援的硬體圖表](images/d3d11-on-downlevel-hardware.png)

使用 Direct3D 11 時，引進了新的典範，稱為功能層級。 功能層級是一組定義完善的 GPU 功能。 使用功能層級，您可以將 Direct3D 應用程式的目標設為在舊版 Direct3D 硬體上執行。

[ [10Level9 參考](d3d11-graphics-reference-10level9.md) ] 區段會列出各種 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 和 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法在各種10Level9 功能層級的行為方式之間的差異。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                  | 描述                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Direct3D 功能層級](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | 本主題討論 Direct3D 功能等級。<br/>                                                                                                                       |
| [例外狀況](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | 本主題說明在舊版硬體上使用 Direct3D 11 時的例外狀況。 <br/>                                                                                      |
| [下層硬體上的計算著色器](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | 本主題將討論如何在 Direct3D 10 硬體上的 Direct3D 11 應用程式中使用 [計算著色](direct3d-11-advanced-stages-compute-shader.md) 器。<br/>             |
| [防止不必要的 Null 圖元著色器 SRVs](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | 本主題討論如何解決接收 **null** 著色器資源檢視 (SRVs) 的驅動程式，即使非 **Null** SRVs 系結至圖元著色器階段也是如此。<br/> |



 

## <a name="how-to-topics-about-feature-levels"></a>功能層級的相關主題



| 主題                                                                                                                                                                                                                                                                   | 描述                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[如何：取得裝置功能等級](overviews-direct3d-11-devices-downlevel-get.md)<br/> | 如何取得功能等級。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





