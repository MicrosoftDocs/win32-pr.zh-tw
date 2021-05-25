---
description: 驅動程式範本功能旗標。
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8999d73044a061cb8eea8f5829351c1d04079462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343053"
---
# <a name="d3dstencilcaps"></a>D3DSTENCILCAPS

驅動程式範本功能旗標。



| \#定義                 | 值       | 描述                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| D3DSTENCILCAPS \_ 保留     | 0x00000001L | 請勿更新樣板緩衝區中的專案。 這是預設值。                             |
| D3DSTENCILCAPS \_ 零     | 0x00000002L | 將樣板緩衝區專案設定為0。                                                                    |
| D3DSTENCILCAPS \_ REPLACE  | 0x00000004L | 將樣板緩衝區專案取代為參考值。                                                |
| D3DSTENCILCAPS \_ INCRSAT  | 0x00000008L | 將樣板緩衝區專案遞增，固定為最大值。                                    |
| D3DSTENCILCAPS \_ DECRSAT  | 0x00000010L | 遞減樣板緩衝區專案，固定為零。                                                 |
| D3DSTENCILCAPS \_ 反轉   | 0x00000020L | 反轉樣板緩衝區專案中的位。                                                          |
| D3DSTENCILCAPS \_ 增量     | 0x00000040L | 如果新值超過最大值，則將樣板緩衝區專案遞增，並將其換成零。      |
| D3DSTENCILCAPS \_ operators.decr     | 0x00000080L | 遞減樣板緩衝區專案，如果新值小於零，則會換行到最大值。 |
| D3DSTENCILCAPS \_ TWOSIDED | 0x00000100L | 裝置支援雙面樣板。                                                                |



 

樣板-緩衝區專案是整數值，範圍從0到2ⁿ-1，其中 n 是樣板緩衝區的位深度。

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 StencilCaps 成員會使用這些常數。

## <a name="constant-information"></a>常數資訊



| 需求                         | 值           |
|--------------------------|------------|
| 標頭                   | d3d9caps。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



