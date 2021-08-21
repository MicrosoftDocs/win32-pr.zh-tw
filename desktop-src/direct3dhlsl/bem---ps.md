---
title: bem-ps
description: 套用假的凹凸環境對應轉換。
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fdc28e6eaf71156504306b247a1a2a3797423f9a7e3bde6d4040ecb1297e09da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794819"
---
# <a name="bem---ps"></a>bem-ps

套用假的凹凸環境對應轉換。

## <a name="syntax"></a>Syntax



| bem src0、src1 的 dst |
|------------------------|



 

其中

-   dst. rg dst 是目的地註冊。 必須使用紅色和綠色的元件書寫遮罩。
-   src0 是來源註冊。
-   src1 是來源註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| bem                   |      |      |      | x    |      |      |       |      |       |



 

此指令會執行下列計算。


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



使用 bem 的規則：

1.  bem 必須出現在著色器的第一個階段， (也就是在階段標記) 之前。
2.  bem 會使用兩個算術指示位置。
3.  每個著色器只允許一個使用此指令。
4.  目的地 writemask 必須是. rg/.xy。
5.  無法共同發出此指令。
6.  除了目的地寫入遮罩的限制之外，來源 src0、src1 和指令修飾詞上的修飾詞不受限制。

## <a name="instruction-information"></a>指示資訊



| 需求                         | 值           |
|--------------------------|------------|
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




