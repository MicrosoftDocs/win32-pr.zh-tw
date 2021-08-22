---
description: 從具有 CallShader 內建的另一個著色器叫用的著色器。
ms.assetid: ''
title: 可呼叫著色器
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: b84ec6ea58fbc456db1747259f687a2fb6c8cb0fe3374b3d32396861dcd2f9b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461068"
---
# <a name="callable-shader"></a>可呼叫著色器

從具有 [**CallShader**](callshader-function.md) 內建的另一個著色器叫用的著色器。

**CallShader** 呼叫位置提供的參數結構必須符合要求索引所指向之可呼叫著色器中所使用的參數結構，以供透過 [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays)方法提供的可呼叫著色器資料表使用。  可呼叫的著色器必須將此參數宣告為 *inout*。  此外，可呼叫的著色器可能會讀取啟動索引和維度輸入。 如需詳細資訊，請參閱 [**系統值內建函式**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md)。 


## <a name="shader-type-attribute"></a>著色器類型屬性


```
[shader("callable")]
```



## <a name="example"></a>範例

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




