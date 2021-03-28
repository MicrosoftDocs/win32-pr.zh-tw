---
title: ps
description: 此指示會指定著色器版本號碼，並可在所有著色器版本上運作。
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990819"
---
# <a name="ps"></a>ps

此指示會指定著色器版本號碼，並可在所有著色器版本上運作。

## <a name="syntax"></a>Syntax


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a>輸入引數

輸入引數包含單一的主要版本號碼，其具有單一的子版本號碼。 下表列出允許的組合。



| 主要版本 | 次要版本                   |
|---------------|--------------------------------|
| 1             | 1、2、3、4                     |
| 2             | 0、x (擴充) 、軟體 (軟體)  |
| 3             | 0、sw (軟體)                |



 

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| ps                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

此指令必須是圖元著色器中的第一個非批註指令。

硬體加速版本的軟體 (版本號碼) 的無軟體版本 \_ ，可以處理具有硬體 accelearation 或使用軟體頂點處理的頂點。 軟體版本 (版本 \_ 號碼中的 sw 版，) 只使用軟體處理頂點。

## <a name="examples"></a>範例

這個部分範例會宣告第1版的 \_ 圖元著色器。


```
ps_1_1
```



這個部分範例會宣告第1版的 \_ 圖元著色器。


```
ps_1_4
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




