---
description: 瞭解一或多個旗標的組合，以控制裝置在 D3DVTXPCAPS 常數中的建立行為。
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b544f3e4a69de23607366832aca110e42c61d6d
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011081"
---
# <a name="d3dvtxpcaps"></a>D3DVTXPCAPS

一或多個旗標的組合，可控制裝置的建立行為。



| \#定義                                | Description                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVTXPCAPS \_ DIRECTIONALLIGHTS          | 裝置可以進行方向燈。                                                                                                                                                                  |
| D3DVTXPCAPS \_ LOCALVIEWER                | 裝置可以進行本機檢視器。                                                                                                                                                                        |
| D3DVTXPCAPS \_ MATERIALSOURCE7            | 設定此上限時，裝置會支援色彩材質狀態： D3DRS \_ AMBIENTMATERIALSOURCE、D3DRS \_ DIFFUSEMATERIALSOURCE、D3DRS \_ EMISSIVEMATERIALSOURCE 和 D3DRS \_ SPECULARMATERIALSOURCE。 |
| D3DVTXPCAPS \_ NO \_ TEXGEN \_ NONLOCALVIEWER | 裝置不支援在非本機檢視器模式中產生紋理。                                                                                                                               |
| D3DVTXPCAPS \_ POSITIONALLIGHTS           | 裝置可以進行位置燈光 (包括點和點) 。                                                                                                                                         |
| D3DVTXPCAPS \_ TEXGEN                     | 裝置可以進行 texgen。                                                                                                                                                                              |
| D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP          | 裝置支援 D3DTSS \_ TCI \_ SPHEREMAP。                                                                                                                                                            |
| D3DVTXPCAPS \_ 補間                   | 裝置可以進行頂點補間。                                                                                                                                                                     |



 

## <a name="constant-information"></a>常數資訊



| 需求                         | 值           |
|--------------------------|------------|
| 標頭                   | d3d9caps。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



