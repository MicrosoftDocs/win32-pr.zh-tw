---
description: WorldToObject4x3-從世界空間轉換成物件空間的矩陣。
ms.assetid: ''
title: WorldToObject4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject4x3
api_type:
- NA
ms.openlocfilehash: 26775e10723a768aa5b526fadfae55414dafa2311b020b1683a99e2b2139dc30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565558"
---
# <a name="worldtoobject4x3"></a>WorldToObject4x3

從世界空間轉換成物件空間的矩陣。 物件空間是指目前最下層加速結構的空間。

## <a name="syntax"></a>語法

```
void WorldToObject4x3();

```




## <a name="remarks"></a>備註

矩陣是 **WorldToObject3x4** 矩陣的調換。

您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**任何命中著色器**](any-hit-shader.md)
* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**交集著色器**](intersection-shader.md)





## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




