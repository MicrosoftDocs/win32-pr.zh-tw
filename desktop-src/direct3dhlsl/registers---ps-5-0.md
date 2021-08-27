---
title: 註冊-ps_5_0
description: 下列輸入和輸出暫存器會實作為圖元著色器版本 5 \_ 0。
ms.assetid: F16E5CB8-E1DB-48CD-8C20-DBF1DF971110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d432e53626d547bcaf421a4b4ffd9c2aa0f5d0a78ecc3aff9f0b87059c40c0ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095338"
---
# <a name="registers---ps_5_0"></a>註冊-ps \_ 5 \_ 0

下列輸入和輸出暫存器會實作為圖元著色器版本 5 \_ 0。

## <a name="input-registers"></a>輸入暫存器



| 註冊類型                                     | 計數              | R/W | 尺寸 | R 可編制索引\# | Defaults | 需要 DCL |
|---------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| 32位 Temp (r \#)                                  | 4096 (r \# + x \# \[ n \])  | R/W | 4         | 否               | None     | Yes          |
| 32位可編制索引的暫存陣列 (x \# \[ n \])             | 4096 (r \# + x \# \[ n \])  | R/W | 4         | 是              | 無     | Yes          |
| 32位輸入屬性 (v \#)                       | 32                 | R   | 4         | 是              | 無     | Yes          |
| 輸入資源中的元素 (t \#)                 | 128                | R   | 1         | 否               | None     | Yes          |
| 取樣器 (s \#)                                      | 16                 | R   | 1         | 否               | None     | Yes          |
| ConstantBuffer 參考 (cb \# \[ 索引 \])           | 15                 | R   | 4         | 是 (內容)     | 無     | Yes          |
|  (icb \[ 索引) 的立即 ConstantBuffer 參考 \] | 1                  | R   | 4         | 是 (內容)     | 無     | Yes          |



 

## <a name="output-registers"></a>輸出暫存器



| 註冊類型                                                      | 計數                   | R/W | 尺寸                                | R 可編制索引\# | Defaults | 需要 DCL |
|--------------------------------------------------------------------|-------------------------|-----|------------------------------------------|------------------|----------|--------------|
| Null (捨棄結果，適用于具有多個結果的作業)  | N/A                     | W   | N/A                                      | N/A              | N/A      | 否           |
| 32位輸出元素 (o \#)                                         | 8                       | W   | 4                                        | N/A              | N/A      | 否           |
| 未排序的存取視圖 (u \#)                                         | 8 \# rendertargets | R/W | D3D11 \_ PS \_ CS \_ UAV \_ REGISTER \_ 元件 | 否               | 否       | 是          |
| 32-bit \[ 0.0 f。1.0 f \] 浮點數輸出深度 (oDepth)                   | 1                       | W   | 1                                        | N/A              | N/A      | 是          |
| 32位 UINT 輸出範例遮罩 (oMask)                              | 1                       | W   | 1                                        | N/A              | N/A      | 是          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




