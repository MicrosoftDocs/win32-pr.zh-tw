---
title: vs
description: 此指示會指定著色器版本號碼。 此指示適用于所有著色器版本。
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373895"
---
# <a name="vs"></a>vs

此指示會指定著色器版本號碼。 此指示適用于所有著色器版本。

## <a name="syntax"></a>Syntax


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a>輸入引數

輸入引數包含單一的主要版本號碼，其具有單一的子版本號碼。 下表列出允許的組合。



| 主要版本 | 次要版本                   |
|---------------|--------------------------------|
| 1             | 1                              |
| 2             | 0、sw (software) 、x (擴充)  |
| 3             | 0、sw (軟體)                |



 

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| vs                     | x    | x    | x    | x     | x    | x     |



 

此指令必須是頂點著色器中的第一個非批註指令。

所有頂點著色器版本都支援此指令。

硬體加速版本的軟體 (版本號碼) 的無軟體版本 \_ ，可以處理具有硬體 accelearation 或使用軟體頂點處理的頂點。 軟體版本 (版本 \_ 號碼中的 sw 版，) 只使用軟體處理頂點。

## <a name="examples"></a>範例

這個部分範例會宣告第1版 \_ 頂點著色器。


```
vs_1_1
```



這個部分範例會宣告第2版軟體端點著色器。


```
vs_2_sw
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




