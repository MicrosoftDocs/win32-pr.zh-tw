---
title: 登錄-vs
description: 計算輸入的正負號。
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373806"
---
# <a name="sgn---vs"></a>登錄-vs

計算輸入的正負號。

## <a name="syntax"></a>Syntax



| 登錄 dst、src0、src1、src2 收取 |
|---------------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是來源註冊。
-   src1 是保存中繼結果的臨時暫存器。 執行之後，內容是未定義的。
-   src2 收取是保存中繼結果的臨時暫存器。 執行之後，內容是未定義的。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| 登錄                    |      | x    | x    | x     | x    | x     |



 

此指示的運作方式如下所示。


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



src1 和 src2 收取必須是不同的 [臨時](dx9-graphics-reference-asm-vs-registers-temporary.md)暫存器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




