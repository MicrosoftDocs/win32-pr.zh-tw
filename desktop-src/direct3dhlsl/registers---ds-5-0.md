---
title: 註冊-ds_5_0
description: 下列輸入和輸出暫存器會實作為網域著色器版本 5 \_ 0。
ms.assetid: 8AE00EC6-0BDC-4F63-B95C-FF434B98D7CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b787f4a1f7e647a49340d49796dc2986e442178f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301887"
---
# <a name="registers---ds_5_0"></a>註冊-ds \_ 5 \_ 0

下列輸入和輸出暫存器會實作為網域著色器版本 5 \_ 0。

## <a name="input-registers"></a>輸入暫存器



| 註冊類型                                              | Count                | R/W | 維度                           | R 可編制索引\# | Defaults | 需要 DCL |
|------------------------------------------------------------|----------------------|-----|-------------------------------------|------------------|----------|--------------|
| 32位 Temp (r \#)                                           | 4096 (r \# + x \# \[ n \])    | R/W | 4                                   | 否               | None     | Yes          |
| 32位可編制索引的暫存陣列 (x \# \[ n \])                      | 4096 (r \# + x \# \[ n \])    | R/W | 4                                   | 是              | 無     | Yes          |
| 32位輸入控制點 (vcp \[ 頂點 \] \[ 元素 \])      | 32請參閱下方的附注1。 | R   | 4 (元件) \* 32 (元素) \* 32 (垂直)  | Yes              | 無     | Yes          |
| 32位輸入修補程式常數 (vpc \[ 頂點 \])                | 32請參閱下方的附注2。 | R   | 4                                   | 是              | 無     | Yes          |
| 32位輸入位置在網域 (vDomain 中，vDomain.xyz) )  | 1                    | R   | 3                                   | 否               | N/A      | 是          |
| 32位 UINT 輸入 PrimitiveID (vPrim)                       | 1                    | R   | 1                                   | 否               | N/A      | 是          |
| 輸入資源中的元素 (t \#)                          | 128                  | R   | 128                                 | Yes              | 無     | Yes          |
| 取樣器 (s \#)                                               | 16                   | R   | 1                                   | 是              | 無     | Yes          |
| iConstantBuffer 參考 (cb \# \[ 索引 \])                   | 15                   | R   | 4                                   | 是              | 無     | Yes          |
| iImmediate ConstantBuffer 參考 (的 icb \[ 索引 \])          | 1                    | R   | 4                                   | 是 (內容)     | 無     | Yes          |



 

**附注1：** 網域著色器會在2組不同的暫存器中看到輪廓著色器輸出。 Vcp 暫存器可以查看所有的輪廓著色器輸出控制點。 Vpc 暫存器可以看到所有輪廓著色器的 Patch 常數輸出資料。

**附注2：** 由於輪廓著色器的程式碼會使用像是 SV TessFactor 的名稱來修補常數分叉或聯結階段輸出 TessFactors，因此， \_ 如果想要查看這些值，則網域著色器必須符合相等 vpc 輸入的這些宣告。

## <a name="output-registers"></a>輸出暫存器



| 註冊類型                           | Count | R/W | 維度 | R 可編制索引\# | Defaults | 需要 DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| 32位輸出頂點資料元素 (o \#)  | 32    | W   | 4         | 是              | 無     | Yes          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




