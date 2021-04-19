---
description: 從世界空間轉換成物件空間的矩陣。
ms.assetid: ''
title: WorldToObject3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject3x4
api_type:
- NA
ms.openlocfilehash: 6274b1d4d18aff0464d933c20f7b8052f3389e5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971977"
---
# <a name="worldtoobject3x4"></a>WorldToObject3x4

從世界空間轉換成物件空間的矩陣。 物件空間是指目前最下層加速結構的空間。

## <a name="syntax"></a>語法

```
void WorldToObject3x4();

```




## <a name="remarks"></a>備註

矩陣是 **WorldToObject4x3** 矩陣的調換。

您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**任何命中著色器**](any-hit-shader.md)
* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**交集著色器**](intersection-shader.md)





## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




