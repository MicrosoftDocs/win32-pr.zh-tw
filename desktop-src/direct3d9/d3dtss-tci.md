---
description: 驅動程式材質座標功能旗標。
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da9ca23ebc4dd121527721a9d10a2db55a4d555
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995255"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

驅動程式材質座標功能旗標。



| \#定義                                 | 值       | 描述                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTSS \_ TCI \_ PASSTHRU                    | 0x00000000L | 使用包含在頂點格式內的指定材質座標。 此值會解析為零。                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | 使用轉換成相機空間的頂點，作為此階段之材質轉換的輸入材質座標。                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | 使用轉換成相機空間的頂點位置，作為此階段之材質轉換的輸入材質座標。                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | 使用轉換成相機空間的反映向量，作為此階段之材質轉換的輸入材質座標。 反映向量是從輸入頂點位置和一般向量計算而來。 |
| D3DTSS \_ TCI \_ SPHEREMAP                   | 0x00040000L | 使用指定的材質座標做為球體對應。                                                                                                                                                            |



 

這些常數會由 D3DTSS \_ TEXCOORDINDEX 使用。

## <a name="constant-information"></a>常數資訊



|                          |            |
|--------------------------|------------|
| 標頭                   | d3d9caps。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



