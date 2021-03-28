---
title: dsy-ps
description: 計算轉譯目標的 y 方向變化率。
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373747"
---
# <a name="dsy---ps"></a>dsy-ps

計算轉譯目標的 y 方向變化率。

## <a name="syntax"></a>Syntax



| dsy dst、src |
|--------------|



 

其中：

-   dst 是目的地註冊。
-   src 是輸入來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dsy                   |      |      |      |      |      | x    | x     | x    | x     |



 

從來源暫存器計算的變更速率是相鄰圖元 (s 中相同暫存器內容的近似值，) 以目前的圖元來執行鎖定步驟中的圖元著色器。

[Dsx](dsx---ps.md)和 dsy 指示會藉由查看每個元件的來源暫存器 (的目前內容，) 在鎖定步驟中執行的區域區域內的各種圖元來計算結果。 用來計算漸層的確切公式會因硬體而異，但應該與硬體執行相同作業的方式，如同紋理取樣的詳細資料計算程式一部分。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[texldd-ps](texldd---ps.md)
</dt> </dl>

 

 




