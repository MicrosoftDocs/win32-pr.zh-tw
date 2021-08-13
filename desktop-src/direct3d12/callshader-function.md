---
description: 從著色器中叫用另一個著色器。
ms.assetid: ''
title: CallShader 函式
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: e411ef61c34eafcef71f3e68f6700651e4b3073423afd40451f139f02826e504
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119280348"
---
# <a name="callshader-function"></a>CallShader 函式

從著色器中叫用另一個著色器。

## <a name="syntax"></a>Syntax
此內建函式定義相當於下列函式範本：

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a>參數

`ShaderIndex`

不帶正負號的整數，表示在 [**DispatchRays**] 的呼叫中指定之可呼叫 [著色器](callable-shader.md)資料表的索引， (/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays。

`Parameter`

要傳遞至可呼叫著色器的使用者定義參數。  這個參數結構必須符合著色器資料表中所指的可呼叫著色器所使用的參數結構。


## <a name="return-value"></a>傳回值

**void**

## <a name="remarks"></a>備註

您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**可呼叫著色器**](callable-shader.md)
* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**遺漏著色器**](miss-shader.md)
* [**光線產生著色器**](ray-generation-shader.md)



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




