---
description: 浮點數，代表光線目前的參數結束點。
ms.assetid: ''
title: RayTCurrent
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 5db5e01fc4af6c3d9304f7f8cf72893029ea34a54cf815310fd1fb3b4c13cbe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028148"
---
# <a name="raytcurrent"></a>RayTCurrent

浮點數，代表光線目前的參數結束點。  

## <a name="syntax"></a>語法

```
float RayTCurrent();

```


## <a name="remarks"></a>備註

**RayTCurrent** 會根據下列公式來定義光線的目前結束點：原點 + (方向 * RayTCurrent) 。  *原點* 和 *方向* 可能位於世界或物件空間中，這會導致世界或物件空間結束點。

**RayTCurrent** 會在具有 [**RayDesc：： TMax**](raydesc.md)值的呼叫 [**TraceRay**](traceray-function.md)呼叫中初始化，然後在追蹤查詢期間更新，以在任何點擊) 中回報交集 (，並接受。

在 [交集著色器](intersection-shader.md)中，它代表到目前為止最接近交集的距離。  如果已接受叫用，則會在 () 至所提供的賦值值之後更新此值。

在 [任何點擊著色器](any-hit-shader.md)中，它代表目前所報告交集的距離。

在 [最接近的點擊著色器](closest-hit-shader.md)中，它代表已接受的最接近交集距離。

在 [遺漏著色器](miss-shader.md)中，它等於傳遞給 **TraceRay** 呼叫的 *TMax* 。


您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**任何命中著色器**](any-hit-shader.md)
* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**交集著色器**](intersection-shader.md)
* [**遺漏著色器**](miss-shader.md)





## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




