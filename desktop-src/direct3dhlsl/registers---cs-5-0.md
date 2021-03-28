---
title: 註冊-cs_5_0
description: 下列輸入和輸出暫存器會在計算著色器版本 5 0 中執行 \_ 。
ms.assetid: A602BA9F-0934-472F-BB07-5E7A97763CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9a1164a1b3b4d623ced8453bbee50f561d4666
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372552"
---
# <a name="registers---cs_5_0"></a>註冊-cs \_ 5 \_ 0

下列輸入和輸出暫存器會在計算著色器版本 5 0 中執行 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊類型                                        | Count                                                  | R/W | 維度                        | R 可編制索引\# | Defaults | 需要 DCL |
|------------------------------------------------------|--------------------------------------------------------|-----|----------------------------------|------------------|----------|--------------|
| 32位 Temp (r \#)                                     | 4096 (r \# + x \# \[ n \])                                      | R/W | 4                                | 否               | None     | Yes          |
| 32位可編制索引的暫存陣列 (x \# \[ n \])                | 4096 (r \# + x \# \[ n \])                                      | R/W | 4                                | 是              | 無     | Yes          |
| 32位執行緒群組共用記憶體 (g \# \[ n \])          | 8192 (執行緒群組) 的所有共用記憶體 decls 總和 | R/W | 1 (可以宣告各種不同的方式)  | Yes              | 無     | Yes          |
| 輸入資源中的元素 (t \#)                    | 128                                                    | R   | 1                                | 否               | None     | Yes          |
| 取樣器 (s \#)                                         | 16                                                     | R   | 1                                | 否               | None     | Yes          |
| ConstantBuffer 參考 (cb \# \[ 索引 \])              | 15                                                     | R   | 4                                | 是 (內容)    | 無     | Yes          |
|  (icb \[ 索引) 的立即 ConstantBuffer 參考 \]    | 1                                                      | R   | 4                                | 是 (內容)     | 無     | Yes          |
| ThreadID (vThreadID.xyz)                              | 1                                                      | R   | 3                                | 否               | N/A      | 是          |
| ThreadGroupID (vThreadGroupID.xyz)                    | 1                                                      | R   | 3                                | 否               | N/A      | 是          |
| ThreadIDInGroup (vThreadIDInGroup.xyz)                | 1                                                      | R   | 3                                | 否               | N/A      | 是          |
| ThreadIDInGroupFlattened (vThreadIDInGroupFlattened)  | 1                                                      | R   | 1                                | 否               | N/A      | 是          |



 

## <a name="output-registers"></a>輸出暫存器



| 註冊類型                                               | Count | R/W | 維度 | R 可編制索引\# | Defaults | 需要 DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Null (捨棄結果，適用于具有多個結果的 ops)  | N/A   | W   | N/A       | N/A              | N/A      | 否           |
| 未排序的存取視圖 (u \#)                                  | 8     | R/W | 1         | 否               | 否       | 是          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




