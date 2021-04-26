---
description: D3DDEVCAPS2 驅動程式功能旗標。
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ef30540f19add130aaca6eb48655a5ac47b2b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999465"
---
# <a name="d3ddevcaps2"></a>D3DDEVCAPS2

D3DDEVCAPS2 驅動程式功能旗標。



| \#定義                                        | Description                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH                | 裝置支援 RT-修補程式的自我調整鑲嵌                                                                                                                                                                       |
| D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH                 | 裝置支援自我調整的 N 個修補程式鑲嵌。                                                                                                                                                                       |
| D3DDEVCAPS2 \_ 可以 \_ \_ 從 \_ 紋理 STRETCHRECT   | 裝置支援使用材質作為來源的 [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) 。                                                                                                                       |
| D3DDEVCAPS2 \_ DMAPNPATCH                         | 裝置支援 N 個修補程式的置換對應。                                                                                                                                                                          |
| D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH               | 裝置支援 N 個修補程式的 presampled 置換對應。 如需置換對應的詳細資訊，請參閱 [ (Direct3D 9) 的置換對應 ](displacement-mapping.md)。                                           |
| D3DDEVCAPS2 \_ STREAMOFFSET                       | 裝置支援資料流程位移。                                                                                                                                                                                           |
| D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET | 如果 \_ 裝置已設定 D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET，且頂點宣告沒有具有 D3DDECLUSAGE POSITIONT0 的元素，則多個頂點元素可以在資料流程中共用相同的位移 \_ 。 |



 

## <a name="constant-information"></a>常數資訊



|                          |            |
|--------------------------|------------|
| 標頭                   | d3d9caps。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
